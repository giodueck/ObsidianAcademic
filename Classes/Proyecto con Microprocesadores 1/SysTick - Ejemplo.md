18-10-2022
---
# SysTick - Ejemplo

```c
void espera10ms()
{
	SysTick->CTRL &= ~ 0x03;     // desactiva el systick y las interrupciones
	SysTick->LOAD &= ~ 0xFFFFFF; // borra reload
	SysTick->LOAD |= ~ 0x0270FF; // carga 160000 - 1 en reload
	SysTick->VAL = 0;            // borra el valor actual
	SysTick->CTRL |= 0x01;       // activa el systick
	while (!(SysTick->CTRL & (1 << 16))); // espera hasta que el systick cuente 10 ms
	SysTick->CTRL &= ~ 0x01;     // desactiva el systick
}
```