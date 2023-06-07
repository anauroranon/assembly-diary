# Types of assemblies
There are various types of assembly language, associated with different computer architectures and processor families. There are many notable
types, but here will be reported only the most common ones related to college studies.

Each architecture has its own set of instructions, registers, and addressing modes. Assembly language programming in these architectures requires an understanding of their specific instruction sets and programming conventions. 

## x86 assembly:
x86 is a popular instruction set architecture (ISA) used by Intel and AMD processors for personal computers and servers.
It is commonly found in desktops, laptops, and servers running operating systems like Windows, macOS, and Linux.
x86 assembly language is used to write low-level programs that directly interact with the x86 processor.
It offers a wide range of instructions and features, including support for complex memory addressing modes and a rich set of arithmetic and logical operations.

### x86 32-bit variant:
The 32-bit x86 architecture, also known as x86-32 or IA-32, was the original version of the x86 architecture.
It uses 32-bit memory addressing, allowing access to up to 4 GB (2^32) of memory.
The general-purpose registers in the CPU are 32 bits wide, allowing them to store and operate on 32-bit data.
32-bit x86 CPUs support a specific set of instructions optimized for 32-bit operations.
Software compiled for 32-bit x86 architecture can run on both 32-bit and 64-bit operating systems.

### x86 64-bit variant:
The 64-bit x86 architecture, also known as x86-64 or AMD64, is an extension of the original 32-bit x86 architecture.
It introduces 64-bit memory addressing, which allows access to significantly larger amounts of memory, theoretically up to 18.4 million TB (2^64) of memory.
The general-purpose registers in the CPU are extended to 64 bits wide, providing increased computational capabilities for working with larger data sets.
The 64-bit version of x86 supports a backward-compatible set of instructions, allowing software designed for 32-bit x86 to run on 64-bit CPUs.
Additionally, the 64-bit version introduces new instructions and features specifically optimized for 64-bit operations, such as more efficient memory access and support for larger data types.

#### Advantages of 64-bit x86
- Expanded memory addressing capabilities, allowing systems to access and utilize larger amounts of RAM.
- Increased computational power, with larger registers enabling more efficient processing of 64-bit data.
- Improved performance for applications that require extensive memory usage or involve large datasets.
- Enhanced security features, including better address space layout randomization (ASLR) for improved protection against memory-based attacks.
- Support for more advanced operating systems and software that take advantage of 64-bit architecture.

#### How to understand difference between 64-bit and 32-bit
Typically, by observing 
- the size of the registers (eax vs. rax)
- the size of the allocated memory (dd vs. dq), 

we can distinguish between the 32-bit and 64-bit versions of assembly code.

**32-bit**
```
section .data
    value dd 42

section .text
    global _start

_start:
    mov eax, [value]   ; Load 32-bit value from memory into eax register
    add eax, 10        ; Add 10 to the value
    mov [value], eax   ; Store the result back in memory
```
   
   
   
**64-bit**
```
section .data
    value dq 42

section .text
    global _start

_start:
    mov rax, [value]   ; Load 64-bit value from memory into rax register
    add rax, 10        ; Add 10 to the value
    mov [value], rax   ; Store the result back in memory
    
```



## ARM assembly:
ARM (Advanced RISC Machines) is a widely used architecture known for its energy-efficient and low-power design.
ARM processors are commonly found in mobile devices, tablets, smartphones, and embedded systems.
ARM assembly language is used to write programs targeting ARM processors.
It offers a reduced instruction set (RISC) design, focusing on simplicity and efficiency.
ARM processors are known for their performance-per-watt efficiency, making them ideal for battery-powered devices.

## MIPS assembly:
MIPS (Microprocessor without Interlocked Pipelined Stages) is an architecture developed by MIPS Technologies.
MIPS processors have been widely used in various applications, including embedded systems, routers, gaming consoles, and some older workstations.
MIPS assembly language is used to write programs specifically for MIPS processors.
MIPS architecture follows a RISC design philosophy, emphasizing simplicity, reduced complexity, and a streamlined instruction set.
It is known for its ease of implementation and efficiency in handling pipelining and instruction-level parallelism.

### NOTE: Both ARM and MIPS have 64-bit and 32-bit variants, but will not be explained in these notes. All the notes are based on the x86 assembly language.
