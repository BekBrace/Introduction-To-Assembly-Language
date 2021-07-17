We will need also to install the NASM assembler program which is the
Netwide Assembler for the Intel X86 achritechture, 

An assembler works as a compiler but for assembly, 
go ahead and install that : 

sudo apt-get install nasm
and I am running this on ubuntu, this will work on any debian based distro like Mint, 
Kali, Pureos

There are many assemblers like 
Microsoft Assembler (MASM)
The GNU assembler (GAS)

An assembly program can be divided into three sections −

The text section.
The data section,
The bss section, and

1) The text section is used for keeping the actual code. 
This section must begin with the declaration global _start, which tells the kernel where the program execution begins, and global keyword followed by _start is essential for the linker, later when we will run our program.

2) The data section is used for declaring data or constants. 
This data does not change at runtime. 
You can declare various constant values, file names, or buffer size, etc., in this section.
You can think of this as the keyword const in javascript for constants declaration

3) The bss section is used for declaring variables
You can think of this as the word let in javascript for variables declaration


