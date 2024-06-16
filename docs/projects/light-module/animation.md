---
icon: material/animation
---

# Animation

This is a follow-up task to the previous [drawing of shapes](shapes.md). This time try creating a set of frames and animate them by displaying them one by one. You can try recreating a spinning shape, or even a complex moving object.

!!! tip

    You can try separating the frames into a second file, such as `frames.h`, and importing that file into your `main.ino`. This lets you create a complex set of frames without cluttering the entire source code.

??? question "Useful links and resources"

    - [Light Module](../../modules/light-module.md)
    - [MD_MAX72xx library documentation](https://majicdesigns.github.io/MD_MAX72XX/class_m_d___m_a_x72_x_x.html)

## Challenges

??? tip "Channelnge 1"

    Create an animation with more than two frames, such as countdown.

??? tip "Channelnge 2"

    Create multiple animated scenes.

## Example

```arduino
#include <MD_MAX72xx.h>

#define HARDWARE_TYPE MD_MAX72XX::FC16_HW
#define CS_PIN 10
#define SEGMENTS 1

MD_MAX72XX display = MD_MAX72XX(HARDWARE_TYPE, CS_PIN, SEGMENTS);

const int frames[2][8][8] = {
	{
		{0, 0, 0, 0, 0, 0, 0, 0},
		{0, 0, 1, 0, 0, 1, 0, 0},
		{0, 1, 1, 1, 1, 1, 1, 0},
		{0, 1, 1, 1, 1, 1, 1, 0},
		{0, 0, 1, 1, 1, 1, 0, 0},
		{0, 0, 0, 1, 1, 0, 0, 0},
		{0, 0, 0, 0, 0, 0, 0, 0},
		{0, 0, 0, 0, 0, 0, 0, 0}
	},
	{
		{0, 0, 0, 0, 0, 0, 0, 0},
		{0, 1, 1, 0, 0, 1, 1, 0},
		{1, 1, 1, 1, 1, 1, 1, 1},
		{1, 1, 1, 1, 1, 1, 1, 1},
		{0, 1, 1, 1, 1, 1, 1, 0},
		{0, 0, 1, 1, 1, 1, 0, 0},
		{0, 0, 0, 1, 1, 0, 0, 0},
		{0, 0, 0, 0, 0, 0, 0, 0}
	}
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
}

void loop() {
	for (int i = 0; i < 2; i++) {
		displayShape(frames[i]);
		delay(500);
	}
}
```
