# Assembly Functions

## add
**ADD source, destination**
Adds together its two operands, storing the result in its first operand. If both operands are registers, at most one operand may be a memory location.

## test
**TEST r1, r2**

### test eax, eax
The instruction "test eax, eax" in assembly language is used to perform a bitwise AND operation between the contents of the EAX register and itself. The purpose of this instruction is primarily to test the value of the EAX register without modifying its contents.

The "test" instruction affects the flags in the processor's status register (typically the EFLAGS register). Specifically, it sets the zero flag (ZF) based on the result of the bitwise AND operation. If the result is zero, indicating that all bits in EAX are cleared, the zero flag is set (ZF=1). If the result is non-zero, indicating that at least one bit in EAX is set, the zero flag is cleared (ZF=0).

By checking the state of the zero flag after the "test" instruction, you can determine whether the value in EAX is zero or non-zero, without altering the contents of EAX. This can be useful in conditional branching or decision-making within a program.

## cdqe
**CDQE**, Convert Doubleword to Quadword 
Double the size of the source operand. Sign extends the content of the source 32-bit register of the previous instruction to the 64-bit
register in x64.

## jge
**JGE destination, source**
Conditional jump that follows a test. It performs a signed comparison jump after a cmp if the destination is greater than or equal to the
source operand.

## shl
**SHL r64, count**, Shift Left operand
Shifts the bits of the operand destination to the left, by the number of bits specified in the count operand.
Equivalent to multiplying by 2^n (shl eax, 2  ; equivalent to eax * 4 or eax * (2^2))
Zeros fill vacated positions during the shift operation.

## movsdx
**MOVSDX r64, r/m32** , Move Signed Extended
Move doubleword to quadword with sign-extension.

This is the instruction in 64-bit code that takes a 32-bit register or an address to a 32-bit value and moves it sign extended 
into a 64-bit register. Sign extension is taking the value of the top most bit (sign bit) of the source and using it to fill in all 
the upper bits of the destination.

movsxd rdx,edx takes a look at bit 31 (top most bit) of EDX and sets the upper 32 bits of the destination to that value and copies the 
lower 32 bits as is. If the sign bit is set in EDX the upper 32 bits of the 64-bit register will be set to 1. If the sign bit is clear 
the upper 32 bits of RDX will be 0.

Sign extension preserves the sign bit across the upper bits of a wider register so that the signedness of the destination is preserved.
