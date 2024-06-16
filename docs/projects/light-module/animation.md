---
icon: material/animation
---

# Animation

Create animated scrolling text using the Parola library.

## Resources

- [Light Module](../../modules/light-module.md)
- [MD_MAX72xx library documentation](https://majicdesigns.github.io/MD_MAX72XX/class_m_d___m_a_x72_x_x.html)
- [MD_Parola library documentation](https://majicdesigns.github.io/MD_Parola/class_m_d___parola.html)


### Example

```ini
lib_deps =
  MD_MAX72XX
  MD_Parola
```

`MD_Parola` builds upon the `MD_MAX72XX` library providing many interesting features, such as animations.

```arduino
#include <MD_Parola.h>
#include <MD_MAX72xx.h>

#define HARDWARE_TYPE 
#define CS_PIN 10
#define SEGMENTS 1

MD_Parola display = MD_Parola(MD_MAX72XX::FC16_HW, CS_PIN, SEGMENTS);

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
