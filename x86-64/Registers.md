# x64 Registers cheat sheet
Registers are used for holding temporary data, passing function arguments, and returning values from functions. 

In x64 assembly, there are several registers available for use. 
It's important to note that the every 64-bit registers (RAX, RBX, RCX, etc.) 
can be accessed as lower 32-bit registers (EAX, EBX, ECX, etc.) or lower 16-bit registers (AX, BX, CX, etc.) 
or lower 8-bit registers (AH, AL, BH, BL, etc.). This provides backward compatibility with 32-bit and 16-bit software.
Here is a list of the general-purpose registers commonly used in x64 architecture:

| 64-bit | 32-bit | 16-bit | 8-bit  | Usage                               | Description                                              | Group          |
| ------ | ------ | ------ | ------ | ---------------------------------- | -------------------------------------------------------- | -------------- |
| RAX    | EAX    | AX     | AH, AL | Return value, arithmetic operations | Primary accumulator register, used for arithmetic and data movement (I/O). Stores a function's return value if exists and is no longer than 64 bits. | Data Registers. Caller-save register. |
| RBX    | EBX    | BX     | BH, BL | Base pointer for memory addressing  | Base register, used for addressing memory                 | Data Registers. Callee-save register. |
| RCX    | ECX    | CX     | CH, CL | Function argument, loop counters    | Counter register, used for looping and function arguments. **4th** integer or pointer parameter to called functions. | Data Registers. Caller-save register. |
| RDX    | EDX    | DX     | DH, DL | Function argument, arithmetic ops   | Data register, used for I/O and arithmetic operations. **3rd** integer or pointer parameter to called functions. Used with AX for multiply and divide operations involving large values     | Data Registers. Caller-save register. |
| RSI    | ESI    | SI     | -      | Source index for memory operations  | Source index register, used for string operations. **2nd** integer or pointer parameter to called functions.         | Index Registers. Caller-save register.|
| RDI    | EDI    | DI     | -      | Destination index for memory ops    | Destination index register, used for string operations. **1st** integer or pointer parameter to called functions.    | Index Registers. Caller-save register.|
| RBP    | EBP    | BP     | -      | Base pointer for stack frames       | Base pointer register, used for stack frame access. Helps referencing the parameter passed to a subroutine. NOT OFTEN TRUE ON 64 BIT. | Pointer Register. Callee-save register.|
| RSP    | ESP    | SP     | -      | Stack pointer                      | Stack pointer register, used for managing the stack. Points the topmost element in the stack. SS:SP refers to be current position of data or address within the program stack.       | Pointer Register. Caller-save register.|
| R8     | R8D    | R8W    | R8B    | Additional general-purpose register | General-purpose register. **5th** integer or pointer parameter to called functions.                                  | Data Registers. Caller-save register. |
| R9     | R9D    | R9W    | R9B    | Additional general-purpose register | General-purpose register **6th** integer or pointer parameter to called functions.                                 | Data Registers. Caller-save register.|
| R10    | R10D   | R10W   | R10B   | Additional general-purpose register | General-purpose register                                  | Data Registers. Caller-save register. |
| R11    | R11D   | R11W   | R11B   | Additional general-purpose register | General-purpose register                                  | Data Registers. Caller-save register. |
| R12    | R12D   | R12W   | R12B   | Additional general-purpose register | General-purpose register                                  | Data Registers. Callee-save register. |
| R13    | R13D   | R13W   | R13B   | Additional general-purpose register | General-purpose register                                  | Data Registers. Callee-save register. |
| R14    | R14D   | R14W   | R14B   | Additional general-purpose register | General-purpose register                                  | Data Registers. Callee-save register. |
| R15    | R15D   | R15W   | R15B   | Additional general-purpose register | General-purpose register                                  | Data Registers. Callee-save register. |
| RIP    | EIP    | IP     | -      | Instruction pointer                | Instruction pointer register, contains the offset address of the next instruction. CS:IP gives the complete address in the code segment | Pointer Register|
| -      | EFLAGS | FLAGS  | -      | Flags register                     | Flags register, holds various status flags                 | Pointer Register|
| XMM0   | -      | -      | -      | Floating-point/SIMD register       | Register for floating-point and SIMD operations           | Data Registers |



