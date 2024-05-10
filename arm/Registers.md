# Registers
There are 30 general-purpose 32-bit registers.
The first 16 are accessible in user-level mode;
The rest 16 are available in privileged software execution.

# Any privilege mode: R0-R15
Calling convention: first four arguments stored in r0-r3

| 64-bit | 32-bit | 16-bit | 8-bit | Usage                                  | Description | Group | x86 Register |
|--------|--------|--------|-------|----------------------------------------|-------------|-------|--------------|
| R0     |        |        |       | General Purpose                        | Accumulator, return value            | Store values      | EAX          |
| R1-R5  |        |        |       | General Purpose                        |             | Store values      | EBX, ECX, EDX, ESI, EDI |
| R6     |        |        |       | General Purpose                        |             | Store values      | -            |
| R7     |        |        |       | General Purpose                        | Syscall number            | Store values      | -            |
| R8-R10 |        |        |       | General Purpose                        |             | Store values      | -            |
| R11 (FP)|        |        |       | Frame Pointer                          |             |       | EBP          |
| R12    |        |        |       | Intra Procedural Call                  |             |       | -            |
| R13 (SP)|        |        |       | Stack Pointer                          | Points to the top of the stack. Used to allocate space on the stack with R13 - Value in bytes            |       | ESP          |
| R14 (LR)|        |        |       | Link Register                          | Memory address referenscing the next instruction where the function was initiated from. (Return address)            |       | -            |
| R15 (PC)|        |        |       | Program Counter                        | Incremented by the size of the instruction executed (4 butes). Execute branch instruction -> destination address. Normal execution -> current instruction + 8 (two ARM instructions).            |       | EIP. Remember: Here the PC always points to the next instruction to be executed.          |
| CPSR   |        |        |       | Current Program Status Register/Flags  |             |       | EFLAGS       |



