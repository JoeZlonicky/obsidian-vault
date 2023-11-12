### Description
In JavaScript, there is only one primary number datatype: double precision (64-bit) floating point:
* Bits 0-51: the fraction
* Bits 52-62: the exponent
* Bit 63: sign

Note: There is also BigInt for very large numbers that can't be represent with a Number.

A string can be converted to a number using `Number(my_string)` or simply `+my_string`.