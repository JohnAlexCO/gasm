# gasm

### This repo is gonna be quiet for a while, but the basic gist is 

- [Garter's](https://github.com/johnalexco/garter) bootstrapper is compiled and 0.0.0 begins testing 
- Once a stable 0.1.0 is available, gasm is designed and compiled 
- Garter's 0.2.0 is then built ontop of gasm
- gasm is incorporated into Garter

### How will these two programs interact/be integrated?

- Garter 0.0.0 will be bootstrapped in and target x86 assembly using `nasm`
- Then, the `gasm` assembler will be built to produce `x86-32` and `arm32` ELF Binaries (Linux and Mac), and `x86-32` PE-EXE binaries (Windows)
- `gasm` is added as a secondary compilation target to Garter
- Finally, a version of Garter is built that has gasm fully contained within it

Once these steps are complete, Garter will not depend on any external binaries to compile itself or other programs,
and the only syscalls it will depend on are for reading and writing to the disk. 
