# DataTypes
ARM supports operations on different datatypes on which can be registered the data.


# Length
The extension specifies how every instruction changes based on which data type is used as parameter.

## Byte
#### Extension: -b, -sb
The byte data type is composed of 8 bits, from 0 to 7.
Ex: 
ldr*b* - unsigned
ldr*bs* - signed

## Halfword
#### Extension: h, sh
The byte data type is composed of 16 bits, from 0 to 15.
Ex: 
ldr*h* - unsigned
ldr*hs* - signed

## Word
#### Extension: no extension
The byte data type is composed of 32 bits, from 0 to 31.
The Least-Significant-Byte is stored at the 0 bit, while the Most-Significant-Byte is stored at the 31th bit.
Ex: 
ld

# Sign
Every data type can be signed or unsiged.

## Signed
Can hold both positive and negative values and are therefore lower in range

## Unsigned
Can hold large positive values, including 'Zero'. but cannot hold negative values.

<img width="462" alt="image" src="https://github.com/anauroranon/assembly-diary/assets/58305348/dab3881d-1dcc-48e5-838f-f1a4ca979463">


# Endianness
Two basic ways of viewing bytes in memory, and they differ in the byte-order in which each bute of an object is stored in memory.
The ARM architecture was little-endian before version 3. Now is bi-endian.

## Little-endian (LE)
Least-significant byte is stored at the lowest address (address closest to zero).


## Big-endian (BE)
Most-significant-byte is stored at the lowest address.

