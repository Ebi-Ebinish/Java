
Bytecode = platform-independent code for the JVM.  
Binary code = platform-dependent machine code for the CPU.  

1 byte means 8 bits, Bits is nothing but it’s called 0’s and 1’s  

| Data Type | Size |
|-----------|------|
| Char      | 16 bits |
| Float     | 32 bits |
| Boolean   | 1 bit |
| Byte      | 8 bits |
| Short     | 16 bits |
| Int       | 32 bits |
| Long      | 64 bits |

Most significant bit    Least significant bit  
== 1 byte  

Here a bit’s block means it’s a single binary digit which has two possibilities: 0’s and 1’s.  

The formula for calculating range is:  2^bits == 2^8 = 256

So the range is the combination of binary and the bits.  

Unsigned means the positive number is called unsigned.  
Like (ex. 1, 9)  

Signed number means the negative numbers because it has the signs (-).  

The final formula for calculating range is:  [-2^(bit-1) to 2^(bit-1) – 1]


Why the 2^(bit-1) we are taking the Most Significant Bit for predict the binary whether it’s signed or unsigned. If the Most Significant bit is 1 means the value of the bits will be in negative format (signed). If the Most significant Bit starts with 0 means all bits will be positive format (Unsigned).  

So the most significant bit will not be considered in the range because it is used to identify whether the range is positive or negative.  
That’s why 2^16 bits-1, that 2^(bit-1) is the Most Significant Bit Range Identifier.  

The unsigned means the 0. This also will come under the positive number (Unsigned). Then the range will be calculated from zero, so the formula is 2^(bits-1) - 1. That’s why the -1.  

| Name     | Equal To        | Size (In Bytes)   |
| -------- | --------------- | ----------------- |
| Kilobyte | 1,024 Bytes     | 1,024             |
| Megabyte | 1,024 Kilobytes | 1,048,576         |
| Gigabyte | 1,024 Megabytes | 1,073,741,824     |
| Terabyte | 1,024 Gigabytes | 1,099,511,627,776 |