# Assembly Functions (x86 / x86-64)

# Data Movement

## lea

---

## push 

---

## pop

---

## mov 

---

## movsxd
**MOVSXD r64, r/m32**

Move with sign extension from 32-bit to 64-bit. This is the instruction in 64-bit code that takes a 32-bit register or an address to a 32-bit value and moves it sign extended into a 64-bit register. Sign extension is taking the value of the top most bit (sign bit) of the source and using it to fill in all the upper bits of the destination.

Sign extension preserves the sign bit across the upper bits of a wider register so that the signedness of the destination is preserved.

### Example

AT&T:
```asm
movsxd %edx, %rdx
```

Intel:
```asm
movsxd rdx, edx
```

---

## cdqe
**CDQE — Convert Doubleword to Quadword**

Sign-extends EAX into RAX. Double the size of the source operand. Sign extends the content of the source 32-bit register of the previous instruction to the 64-bit register in x64.

### Example

AT&T / Intel:
```asm
cdqe
```

# Arithmetic Instructions

## add
**ADD source, destination (AT&T)**  
**ADD destination, source (Intel)**  

Adds together its two operands and stores the result in the destination operand.  
If both operands are registers, at most one operand may be a memory location.

### Example

AT&T:
```asm
addl %ebx, %eax
```

Intel:
```asm
add eax, ebx
```

---

## sub / subq
**SUBQ data, destination (AT&T)**  

Subtracts the immediate data from the destination operand and stores the result in the destination location.  
The suffix `q` specifies a 64-bit (quadword) operation.
The size of the operation may be specified as byte, word, or long. Only word and long operations are allowed with address registers, and the condition codes are not affected. When subtracting from address registers, the entire destination address register is used, regardless of the operation size.

### Example

AT&T:
```asm
subq $8, %rsp
```

Intel:
```asm
sub rsp, 8
```

---

## imul

---

## idiv

---

## inc

---

## dec

---

# Logical / Bitwise Instructions

## test
**TEST r1, r2**

Performs a bitwise AND without storing the result. 
Used to update processor flags (content of the register and itself) for conditional jumps.

The "test" instruction affects the flags in the processor's status register (typically the EFLAGS register). Specifically, it sets the zero flag (ZF) based on the result of the bitwise AND operation. If the result is zero, indicating that all bits in EAX are cleared, the zero flag is set (ZF=1). If the result is non-zero, indicating that at least one bit in EAX is set, the zero flag is cleared (ZF=0).

By checking the state of the zero flag after the "test" instruction, you can determine whether the value in EAX is zero or non-zero, without altering the contents of EAX. This can be useful in conditional branching or decision-making within a program.

### Example

AT&T:
```asm
test %eax, %eax
```

Intel:
```asm
test eax, eax
```


---

## and

---

## or

---

## xor

---

## not

# Shift and Rotate Instructions

# Coomparison Instructions

# Control Flow (Conditional Jumps)

## jge
**JGE label**

Conditional jump that follows a test. It performs a signed comparison jump after a cmp if the destination is greater than or equal to the source operand.

### Example

AT&T:
```asm
cmp %ebx, %eax
jge label
```

Intel:
```asm
cmp eax, ebx
jge label
```

---

## shl
**SHL destination, count**

Shifts the bits of the operand destination to the left, by the number of bits specified in the count operand. Equivalent to multiplying by 2^n (shl eax, 2 ; equivalent to eax * 4 or eax * (2^2)) Zeros fill vacated positions during the shift operation.

### Example

AT&T:
```asm
shll $2, %eax (eax * (2^2)
```

Intel:
```asm
shl eax, 2
```

---

# Control Flow (Conditional Jumps)
