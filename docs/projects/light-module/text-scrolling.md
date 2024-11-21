---
icon: material/format-text-rotation-none
---

# Text Scrolling

Create animated scrolling text using the Parola library. This can, of course, be achieved with [frame animation](animation.md) as well, but by using libraries, we don't have to re-invent the wheel. The Parola library builds upon the MD_MAX72xx library end expands it by adding several features, such as alignment, scrolling, animations and much more.

!!! info

    Make sure to import the library into your `platformio.ini`:

    ```ini
    lib_deps =
      MD_MAX72XX
      MD_Parola
    ```

??? question "Useful links and resources"

    - [Light Module](../../modules/light-module.md)
    - [MD_MAX72xx library documentation](https://majicdesigns.github.io/MD_MAX72XX/class_m_d___m_a_x72_x_x.html)
    - [MD_Parola library documentation](https://majicdesigns.github.io/MD_Parola/class_m_d___parola.html)

## Challenges

??? tip "Challenge 1"

    Make it so that the text changes after it finishes the animation.


??? tip "Challenge 2"

    Change the direction and speed of scrolling with each new message.

## Example

```arduino
#include <MD_Parola.h>
#include <MD_MAX72xx.h>

#define HARDWARE_TYPE MD_MAX72XX::FC16_HW
#define CS_PIN 10
#define SEGMENTS 1

MD_Parola display = MD_Parola(HARDWARE_TYPE, CS_PIN, SEGMENTS);

void setup() {
    display.begin();
    display.displayClear();

    ledMatrix.displayScroll("Capyboard", PA_CENTER, PA_SCROLL_LEFT, 100);
}

void loop() {
    if (ledMatrix.displayAnimate()) {
        ledMatrix.displayReset();
    }
}
```
