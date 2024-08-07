[[Cache, Secondary Storage]]
Overview
	- a process is a running program
	- each process has its own virtual address space:
		addresses [0 - 2^n -1] where n= # address bits
	- the virutal address space is mapped onto physical memory (DRAM)
	- the mapping is done by page (usually 4KiB/page)
	- multiple processes share physical memory, which only holds the active subset pf pages (the rest are swapped to secondary storage)
	- advantages: 
		1) memory protection between processes
		2) increases effective memory size
		3) makes loading programs easier


#### Page Table
- the processor issues virtual addresses and the memory management unit (MMU) translates them to physical addresses
- the MMU is part of the processor 
	- uses page tables for these translations
- there is one page table per process
- page tables are managed by the OS (operating system) and reside in kernel memory space
	- OS is kernel plus utilities + kernel responsible for managing memory, processes, and threads
- ARMv8
	- registers are 64 bits, top 16 of addresses are ignored -> 48 bit virtual addresses
	- only have 40 physical address bits

#### Translation Lookaside Buffer
* a special cache for vpn-to-ppn  translations
* without a TLB, 



PS6 Q10:
- given: 48-bit virtual addresses, 4KiB, page table entries PTE are 8 bytes
a) support we have a "flat" page table (one big page table)
	numb.  PTE /process = 2^48   /    2 ^ 12    = 2 ^36
	page table size = 2^36  PTE * 8 B/PTE =   2 ^ 39 B   = 512GiB (too big)
b) instead we have a hierarchical page table
	ARMv8

|     | L0 Index | L1 Index | L2 Index | L4 Index | Page Offset |
| --- | -------- | -------- | -------- | -------- | ----------- |
|     | 9        | 9        | 9        | 9        | 12          |



