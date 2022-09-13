09-09-2022
---
# TP Final - Specifications

## Drawing library
### Constants
Not `const` constants, just global variables set using the settings menu
```c
// 2-color palette
pixel WHITE, BLACK;

// 4-color palette
pixel PRIMARY, SECONDARY;

// 8-color palette
pixel RED, GREEN, BLUE, TEAL, MAGENTA, YELLOW;

// 16-color palette
pixel GREY, DARK_GREY, DARK_GREEN, ORANGE, BROWN, PURPLE, LIGHT_BLUE, AQUA;
```

Colors from the global palette can be identified regardless of actual pixel values using this enum
```c
enum color { BLACK = 0, WHITE = 1, // 1 bits
             RED = 2, GREEN = 3,   // 2 bits, 2-bit palettes can set a primary and secondary color independently
             BLUE = 4, TEAL = 5, MAGENTA = 6, YELLOW = 7, // 3 bits
             GREY = 8, DARK_GREY = 9, DARK_GREEN = 10, ORANGE = 11, BROWN = 12, PURPLE = 13, LIGHT_BLUE = 14, AQUA = 15 // 4 bits
            };
```

### Types
```c
typedef struct pixel
{
	uint8_t a, r, g, b;
} pixel;
```

```c
typedef struct point
{
	int32_t x, y;
} point;
```

Sprites are an array of pixels arranged in a rectangle described by w and h (width and height). All arrays must be of size w * h, and if a palette is used, colors is an array of indices for the palette color. Any color index outside of the palette is considered black
```c
// Arrays of colors and 
typedef struct sprite
{
	int8_t w, h;
	point *points;
	pixel *pixels;
	uint8_t palette; // 1-4, otherwise none
	uint8_t *colors; // 1-(2^(palette) - 1)
	uint32_t len;
} sprite;
```

### Functions
#### General

All functions take into account the screen brightness, if it is not hardware controlled
```c
void draw(point v, pixel p);

void draw_line(point v1, point v2, pixel p);

void draw_rect(point v1, point v2, pixel p);

void draw_triangle(point v1, point v2, point v3, pixel p);

void draw_circle(point v, int32_t r, pixel p);
void draw_circle_f(point v, float r, pixel p);

void fill(pixel p);

void fill_rect(point v1, point v2, pixel p);

void fill_triangle(point v1, point v2, point v3, pixel p);

void fill_circle(point v, int32_t r, pixel p);
void fill_circle_f(point v, float r, pixel p);
```

#### setup
```c
// Controls whether alpha values are taken into account
// P: -1: No
//    0: Only background (useful for sprites)
//    1: Yes
void enable_transparent(uint8_t b);
```

#### Operations
```c
pixel pixel_negative(pixel p);

pixel pixel_add(pixel a, pixel b);

pixel pixel_sub(pixel a, pixel b);

// only useful for full transparency mode and pixels with alpha values other than 0 and 255
pixel pixel_layer(pixel fg, pixel bg);
```

#### Conversions
```c
uint32_t pixel_to_int(pixel p);
pixel int_to_pixel(uint32_t i);
```