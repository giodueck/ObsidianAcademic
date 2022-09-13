04-09-2022
---
# Project Euler on ARM Cortex-M4F
## 3. Largest prime factor
The prime factors of 13195 are 5, 7, 13 and 29.
What is the largest prime factor of the number 600851475143 ?

600851475143 is 0x8BE589EAC7, which is a 64-bit value, complicating divisions and floating-point operations.

$\frac{a + bc}{d} = \frac{a}{d} + \frac{bc}{d}$
$\frac{a}{d} + \frac{bc}{d} = \frac{a}{d} + \frac{b}{d}\frac{c}{d}$

%%```c
int low = 0xE589EAC7;
int high = 0x8B;
int il = 2;
int ih = 0;

while (il < low && ih < high)
{
	if (low % )

	if (++il == 0)
	{
		ih++;
	}
}
```%%