---
icon: material/animation
---

# Animation

This is a follow-up task to the previous [drawing of shapes](shapes/index.md). This time try creating a set of frames and animate them by displaying them one by one. You can try recreating a spinning shape, or even a complex moving object.

!!! tip

    You can try separating the frames into a second file, such as `frames.h`, and importing that file into your `main.ino`. This lets you create a complex set of frames without cluttering the entire source code.

## Challenges

??? tip "Channelnge 1"

    Create an animation with more than two frames, such as countdown.

??? tip "Channelnge 2"

    Create multiple animated scenes.

??? tip "Channelnge 3"

    Use hexadecimal format all of the frames, just like in the challenge from the [previous project](shapes/index.md).

## Example

```arduino title="main.ino"
--8<-- "https://raw.githubusercontent.com/realcharmer/capyboard-examples/refs/heads/master/light-module/animation/src/main.ino"
```
