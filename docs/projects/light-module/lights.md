---
icon: material/lightbulb
---

# Lights

The point of this exercise is to light up the entire display using loops.

!!! info

    Make sure to import the library into your `platformio.ini`:

    ```ini
    lib_deps =
      MD_MAX72XX
    ```

??? question "Useful links and resources"

    - [Light Module](../../modules/light-module.md)
    - [MD_MAX72xx library documentation](https://majicdesigns.github.io/MD_MAX72XX/class_m_d___m_a_x72_x_x.html)

## Challenges

??? tip "Challenge 1"

    Try animating the screen that it fills slowly one pixel after pixel.

??? tip "Challenge 2"

    Make it so that the animation flows like a snake, not only left-to-right or right-to-left.

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

void setup() {
	display.begin();
	display.clear();

	for (int row = 0; row < 8; row++) {
		for (int col = 0; col < 8; col++) {
			display.setPoint(col, row, 1);
		}
	}	
}

void loop() {
}
```
