* Word size (default data size) is 32 bits
	* All registers are 32 bits
	* Most instructions are 32 bits
	* Other operand sizes: byte 8 bits, half word 16 bits
* 16 registers: R0-R15
	* R15 the program counter
* Load-store architecture
	* ALU operands can't come directly from memory 
	* ALU operands come from registers or immediate values
	* Load-store instructions move data between memory and registers

3) Load/Store Instructions 
	   LDR = load register, STR = store register
	   from memory             **to** memory
	* first operand is the data register
	* second operand is the address register, plus an offset
		e.g. LDR R3
	EX. Sum an array of 5 integers.
	