05-09-2023
---
# Introduccion a PGE

## Contenido
- Introducción a PGE
	- Hello World
	- Métodos para pintar pixeles
	- Métodos para captar entradas
	- Explicación de codigo: [[Curvas de Bezier]]

## Introducción: olc::PixelGameEngine
https://github.com/OneLoneCoder/olcPixelGameEngine

Motor de gráficos minimalista, rápido y cross-platform en un archivo: **olcPixelGameEngine.h**

Implementado en C++, puede usarse para:
- Desarrollo de juegos
- Visualización de algoritmos
- Prototipación y experimentación
- Educación

Provee métodos para:
- Manipular la pantalla a nivel de píxel
- Dibujar puntos, líneas, rectángulos, círculos, triángulos
- Dibujar *sprites*, que pueden ser imágenes PNG
- Dibujar *decals*, sprites dibujados por la GPU
- Dibujar texto
- Captar eventos del mouse y teclado

Existen varias extensiones:
- Transformaciones 2D (rotation, translation, scaling, shearing)
- 3D rendering
- Utilidades de cámara 2D
- Input de controles
- Sonido
- etc.

Plataformas:
- Windows
- Linux / Raspberry Pi / ChromeOS
- MacOS (coming soon to official, but already available in "Contributors")
- PSP & Switch (Not supported by OneLoneCoder)

## Hello World
Primero se incluye la librería:
```cpp
#define OLC_PGE_APPLICATION
#include "olcPixelGameEngine.h"
```

Se crea una clase que hereda de `olc::PixelGameEngine`, y se implementan los metodos `bool OnUserCreate()` y `bool OnUserUpdate(float fElapsedTime)`:
```cpp
class Example : public olc::PixelGameEngine
{
public:
	Example()
	{
		sAppName = "Example";
	}

public:
	bool OnUserCreate() override
	{
		// Called once at the start, so create things here
		return true;
	}

	bool OnUserUpdate(float fElapsedTime) override
	{
		// called once per frame
		for (int x = 0; x < ScreenWidth(); x++)
			for (int y = 0; y < ScreenHeight(); y++)
				Draw(x, y, olc::Pixel(rand() % 255, rand() % 255, rand() % 255));	
		return true;
	}
};
```

Desde `main()` se construye la ventana con el ancho y alto de la resolución, y el tamaño de cada pixel, ancho y alto:
```cpp
int main()
{
	Example demo;
	if (demo.Construct(256, 240, 4, 4))
		demo.Start();

	return 0;
}
```