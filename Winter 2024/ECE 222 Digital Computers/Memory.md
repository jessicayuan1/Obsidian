[[ECE 222 Digital Computers]]

Flash
- Like EEPROM but is is erased in blocks (128-256)
- Written in pages of 2-4KiB
- Used in SSDs, BIOS, cellphones

Gate controls the transistor 

2) Volatile Memory
	loses data on power off
2.1) Static RAM (SRAM)
	Chart of bit cell: Stores one bit  
	![[Pasted image 20240318144720.png]]
- to read, assert word line, read b 
- to write, assert word line, and drive bit line, b, and it's complement, b'
- holds it's value as long as power  is supplied ("static")

2.2 ) Dynamic Ram
- C: charged = 1 , discharged = 0 
- To write: assert word line and drive Vdd or GND on b 
- To read: precharge b o Vdd/2; assert word line; capacitor C causes bit line voltage to increase or decrease slightly.
- 
  
  
Important: to understand when to use one or the other (DRAM a lot cheaper so used for main memory)

3) Memory Size Prefixes
SI = Systeme Internationale
IEC = International Electrotechnical Commission

| SI Prefix | (decimal) | mult. | IEC | (binary) | mult. |
| --------- | --------- | ----- | --- | -------- | ----- |
| k         | kilo      | 10^3  | Ki  | kibi     | 2^10  |
| M         | mega      | 10^6  | Mi  | mebi     | 2^20  |
| G         | giga      | 10^9  | Gi  | gibi     | 2^30  |
| T         | tera      | 10^12 | Ti  | tebi     | 2^40  |
| P         | peta      | 10^15 | Pi  | pebi     | 2^50  |
| E         | exa       | 10^18 | Ei  | exbi     | 2^60  |
- memory sizes should be reported with IEC prefixes


4) DRAM Chips
- 16*4 chip 
- (16 data words, 4 bits per word)

| a3a2a1a0 |     |
| -------- | --- |
| 0000     |     |
| 0001     |     |
| ...      |     |
|          |     |
