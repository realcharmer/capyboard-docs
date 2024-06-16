---
icon: material/shape
---

# Shapes

Draw a custom shape, such as circle, qsuare, or a sprite. 

## Resources

- [Light Module](../../modules/light-module.md)
- [MD_MAX72xx library documentation](https://majicdesigns.github.io/MD_MAX72XX/class_m_d___m_a_x72_x_x.html)

## Example

```arduino
#include <MD_MAX72xx.h>

#define HARDWARE_TYPE MD_MAX72XX::FC16_HW
#define CS_PIN 10
#define SEGMENTS 1

MD_MAX72XX display = MD_MAX72XX(HARDWARE_TYPE, CS_PIN, SEGMENTS);

const int shape[8][8] = {
	{0, 0, 0, 0, 0, 0, 0, 0},
	{0, 1, 1, 0, 0, 1, 1, 0},
	{1, 1, 1, 1, 1, 1, 1, 1},
	{1, 1, 1, 1, 1, 1, 1, 1},
	{0, 1, 1, 1, 1, 1, 1, 0},
	{0, 0, 1, 1, 1, 1, 0, 0},
	{0, 0, 0, 1, 1, 0, 0, 0},
	{0, 0, 0, 0, 0, 0, 0, 0}
};

void displayShape(const int shape[8][8]) {
	for (int row = 0; row < 8; row++) {
		for (int col = 0; col < 8; col++) {
			display.setPoint(col, row, shape[row][col]);
		}
	}
}

void setup() {
	display.begin();
	display.clear();

	displayShape(shape);
}

void loop() {
}
```
