# Introduction-assembly-language
This is a quick introduction by writing a "Hello, World" program in Assembly language

We will need also to install the NASM assembler program which is the Netwide Assembler for the Intel X86 achritechture,

An assembler works as a compiler but for assembly, go ahead and install that :

sudo apt-get install nasm and I am running this on ubuntu, this will work on any debian based distro like Mint, Kali, Pureos

There are many assemblers like Microsoft Assembler (MASM) The GNU assembler (GAS)

An assembly program can be divided into three sections −

The text section. The data section, The bss section :

The text section is used for keeping the actual code. This section must begin with the declaration global _start, which tells the kernel where the program execution begins, and global keyword followed by _start is essential for the linker, later when we will run our program.

The data section is used for declaring data or constants. This data does not change at runtime. You can declare various constant values, file names, or buffer size, etc., in this section. You can think of this as the keyword const in javascript for constants declaration

The bss section is used for declaring variables You can think of this as the word let in javascript for variables declaration

time to assemble our code :

nasm -f elf64 (assembly program format for 64 bit virtual memory) -o (this is our output) hello.o (output file) hello.asm (input file)

and this will produce a file called hello.o which is an object file

There is a linker built in Linux called ld , we'll use it to link the hello.o file

ld hello.o -o hello
now hello is in green highliht with no extension, we have produced an executable file
to run it : ./hello

Hope you enjoyed this.
Until next time, stay safe
Bek
