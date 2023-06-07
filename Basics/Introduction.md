# Assembly basics
## Definition
Assembly is a low-level programming language that bridges the gap between high-level programming languages and the hardware of a 
computer system. It uses symbolic instructions and memory addresses to manipulate the underlying hardware directly. 
Assembly code is translated into machine code and provides precise control over the computer's operations, 
making it suitable for tasks that require performance optimization or low-level hardware interaction.

![From high level language, to assembly, to machine code](https://www.cs.mtsu.edu/~xyang/images/computer-languages.png)

### High level language
- High-level languages (e.g., Python, C++, Java) are designed to be more human-readable and programmer-friendly.
- They use English-like statements and abstract concepts to write programs.
- High-level languages are portable and platform-independent.

**Compilation:** High-level language programs are transformed into machine code through the compilation. The compilation process involves analyzing, parsing, optimizing, and transforming the source code into an executable format, typically resulting in an output file or binary that can be run on a specific platform or operating system.
The translation is provided by the compiler.

### Assembly language
- Assembly language is a low-level language that represents a symbolic form of machine code.
- It uses mnemonic codes and symbols to represent specific operations and memory addresses.
- Assembly language provides a more readable format for programmers compared to machine code.
- Each assembly instruction corresponds to a specific machine instruction.

**Assembler:** An assembler converts assembly language instructions into machine code instructions, using a one-to-one mapping between them.

### Machine code language
- Machine language is the lowest-level language that directly communicates with the computer hardware.
- It consists of binary code represented by sequences of 0s and 1s.
- Each binary instruction corresponds to a specific operation or data manipulation.
- Machine language is specific to the computer architecture and processor.

**Machine code execution:** The machine code is excuted directly by the computer's hardware.
