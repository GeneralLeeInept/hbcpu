# ALU Functions
* shl   a, b, c     // a = b << c
* shr   a, b, c     // a = b >> c
* shra  a, b, c     // a = b >> c (arithmetic)
* add   a, b, c     // a = b + c
* sub   a, b, c     // a = b - c
* addc  a, b, c     // a = b + c + carry
* subb  a, b, c     // a = b - c - carry
* not   a, b        // a = ~b
* or    a, b, c     // a = b | c
* and   a, b, c     // a = b & c
* xor   a, b, c     // a = b ^ c
* cmp   a, b        // N = a < b, Z = a == b

* mul   a, b, c, d  // a = lo(c * d), b = hi(c * d)
* div   a, b, c     // a = b / c
* mod   a, b, c     // a = b % c


# ALU opcode

## Units
00 - LeftShift
01 - RightShift
10 - Adder
11 - Logic

## Operations
000 - SLL / SRL / ADD / AND
001 - SLL / SRA / ADDC / OR
010 - SLL / SRL / SUB / XOR
011 - SLL / SRA / SUBB / NOT

## Adder
Operation   CIn   Sub
000 ADD       0     0
001 ADDC      1     0
010 SUB       0     1
011 SUBB      1     1

