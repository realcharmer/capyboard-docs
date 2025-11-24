---
icon: material/wrench
---

# Usage

## Makefile

The default makefile is relatively simple and it can be used by executing `make` in the terminal. It also accepts an optional argument, such as `make build`. If no argument is supplied, Make automatically runs `all`. It exposes several targets:

Command   | Description
--------- | -----------
`help`    | Show available Makefile targets
`all`     | Run `build` and `upload` (default)
`build`   | Build the firmware
`upload`  | Build and upload the firmware to the device
`clean`   | Remove temporary build files
`minitor` | Open the serial monitor

## Using PlatformIO Directly

You can, of course, use PlatformIO commands directly without having to use the Makefile. The core commands would be as follows:

Command              | Description
-------------------- | -----------
`pio -t build`       | Build the firmware
`pio -t upload`      | Build and upload the firmware to the device
`pio -t clean`       | Remove temporary build files
`pio device monitor` | Open the serial monitor
