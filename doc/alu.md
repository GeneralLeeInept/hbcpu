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
00 - SLL / SRL / ADD / AND
01 - SLL / SRA / ADDC / OR
10 - SLL / SRL / SUB / XOR
11 - SLL / SRA / SUBB / NOT

## Adder
Operation   CIn   Sub
00 ADD       0     0
01 SUB       1     1
10 ADDC      C     0
11 SUBB      C     1

## ALU Ops
0000 (0) - SLL
0100 (4) - SRL
0101 (5) - SRA
1000 (8) - ADD
1001 (9) - SUB
1010 (A) - ADDC
1011 (B) - SUBB
1100 (C) - AND
1101 (D) - OR
1110 (E) - XOR
1111 (F) - NOT

