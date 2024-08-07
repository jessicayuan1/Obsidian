
2.1) Hard Disk drive (HDD)
- data is stored on magnetized platters, spinning at 5400-7200 RPM 
- r/w head (transducer that floats on an air cushion created by the spinning platter)
- data is stored as transitions in polarity (no change = 0, change = 1)
- concentric rings composing of (100's thousands of ) tracks
	- sector of each arc used to be 512 B, now 4096B
- access = seek time (time to move r/w head)+ rotational latency (time for sector to rotate under the r/w head)

2.2) Solid State Drives (SSD) **(11)**
* mimics a HDD to the OS (uses logical sector numbers)
* data is stored in flash memory chips (circuit board )
* bits/data is stored in charge trap transistors
* flash is erased in blocks (128+ KiB) and programmed (written) in pages (4+ KiB)
* erasing degrades the insulating layer between the substrate and the charge trap layer -- so flash memories have limit program/erase (P/E) cycles


SLC - Single level cell
MLC - Multi level cell, Triple, quad, etc
threshold voltage levels -- 

| type of cell | bits/cell | threshold voltage levels | P/E cycles |                         |
| ------------ | --------- | ------------------------ | ---------- | ----------------------- |
| SLC          | 1         | 2                        | 100 000    | <- servers              |
| MLC          | 2         | 4                        | 10 000     | <- servers ( expensive) |
| TLC          | 3         | 8                        | 3000       | <-commodity             |
| QLC          | 4         | 16                       | 1000       | <-commodity             |
- wear-levelling spreads erase cycles over the blocks in a flash memory

To be continued on Friday -- 

- example: from Micron technical notes TN-29-42 (omg I kinda want to work at micron)
	- SSD with 4096 blocks
	- have 3 files of 50 blocks each, rewritten 2x/hr 
	- assuming that only 200 blocks are used 
	- time to failure
		- 100 PE cucles * 200 blocks 
		-divided by
			50 PE cyucles/file * 6 files/hr * 24 hr/day
			= 278 days !!
		