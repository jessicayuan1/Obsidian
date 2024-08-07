1) Unsigned Integers
	- positional number systems:
		- decimal base 10
		- binary base 2
		- octal base 8
		- hexadecimal base 16

	FE02 = (154096) + (14*  256 ) + ... = 65026


2) Signed 2s Complement
	- To convert to s2c, subtract full amount from the negative int. 2^n - X = Y
	- Negation methods:
		a) Take 1's complement then add 1 (flip all bits then add 1 to the right most)
		b) Start at rightmost one and flip all greater
	* To find the magnitude of a negative number:
		a) Take it's two's complement 
			e.g: -(-6) = -(1010) = (0110) 
		b) 
	* Range of n-bit numbers
		* unsigned = [0, 2^n - 1]
		* signed = [- 2^(n-1), +2^(n-1) ]
		* 