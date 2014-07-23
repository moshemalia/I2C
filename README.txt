I2C
===
I2Csend: 0xC2 0x02 0x3C
x:	0
CMD_ACK 2 3C
-->Not(0x3C+0x02+0xC2)+1 ==0x00

I2Csend: 0xCF 
x:	0
CMD_ACK 2

I2Csend: 0x71 0x01 0x8E
x:	0
3A 1 FFFFFF8E

I2Csend: 0x71 0x00 0x8F
x:	0
2 0 FFFFFF8F




Page  60  Model Number
Send: 0x67
x:	0
32 30 2D 36 38 39 35 30 2D 30 31  ===  20-68950-01

Page  60  Serial Number
Send: 0x65
x:	0
4D 31 4C 35 34 43 35 36 55 === M1L54C56U
