CS204 Project Phase 2 : Pipelined Implementation of 32bit RISC-V instruction execution
Language used : C++

Team Member Details : Drishti Jain - 2020EEB1168 Muskan Singhvi - 2020EEB1295 Tejasvini Uppal - 2020EEB1032

HOW TO RUN -First download all the files. -Make sure all files are present in the in the same folder before running the code. -Open the command line. -Work in the directory path same as that of the folder in which all files are stored. -run Command:- g++ -o myprogram mainf.cpp ./myprogram fibonacci.mc -Here, the .mc file is the input file containing the desired instructions. After the code is compiled successfully, check the outputs in RegisterDump.mc and MemoryDump.mc files.

DESCRIPTION A 5 stage (Instruction Fetch, Decode, Execute, Memory Access, Write Back) pipelined instruction execution is implemented. The input is taken from .mc file in the given format:- <instruction address (PC)> <‘#’ beginning comments> The program terminates with "0x11" code.

26 Instructions are supported in the simulator:- 
R format - add, and, or, sll, slt, sra, srl, sub, xor 
I format - addi, andi, ori, lb, lh, lw, jalr 
S format - sb, sw, sh B format - beq, bne, bge, blt 
U format - auipc, lui 
J format - jal

The program fetches the instruction, decodes it, fetches the operands, generates control signals and ALU signals, performs the ALU operations, reads and writes back from the memory file.

The simulator is tested on the given instructions(test files) i.e. bubblesort.mc, ArraySum.mc and fibonacci.mc files.