---
icon: material/shape
---

# Shapes

![Shape](shape.png){ align=right width=150 }

Draw a custom shape, such as circle, square, or a more complicated sprite. Do this by creating a two-dimensional array of bytes with a simple logic of `1` for light on and `0` for light off.

## Challenges

??? tip "Challenge 1"

    Invert your shape **without modifying the array itself**. Pixels which are now on should be off and vice-versa.

    ![Inverted Shape](shape-inverted.png){ width=150 }

??? tip "Challenge 2"

    Define your shape in base16 (Hexadecimal) instead of base2 (Binary).
    For example:

    ```
    0  0  0  0  0  0  0  0
	0  1  1  0  0  1  1  0
	1  1  1  1  1  1  1  1
	1  1  1  1  1  1  1  1
	0  1  1  1  1  1  1  0
	0  0  1  1  1  1  0  0
	0  0  0  1  1  0  0  0
	0  0  0  0  0  0  0  0   <-- base2

    30 78 7C 7E 7E 7C 78 30  <-- Base16
    ```

## Example

```arduino title="main.ino"
--8<-- "https://raw.githubusercontent.com/realcharmer/capyboard-examples/refs/heads/master/light-module/shapes/src/main.ino"
```
