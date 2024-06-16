---
icon: material/wrench
---

# Usage

## Makefile

The default makefile is relatively simple and it can be used by executing `make` in the terminal. It also accepts an optional argument, such as `make build`. If no argument is supplied, Make automatically runs `all`. It exposes several commands:

Command   | Description
--------- | -----------
`all`     | Run `build` and `upload` (default)
`build`   | Build the firmware
`upload`  | Upload built firmware to the development board
`clean`   | Remove all temporary files created during firmware build
`minitor` | Open a serial monitor

## Using PlatformIO Directly

You can, of course, use PlatformIO commands directly without having to use the Makefile. The core commands would be as follows:

Command              | Description
-------------------- | -----------
`pio -t build`       | Build the firmware
`pio -t upload`      | Upload built firmware to the development board
`pio -t clean`       | Remove all temporary files created during firmware build
`pio device monitor` | Open a serial monitor
