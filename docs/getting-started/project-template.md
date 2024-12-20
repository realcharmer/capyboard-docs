---
icon: material/folder-cog
---

# Project Template

Simple template for a project can be downloaded from a Git repository at <https://github.com/realcharmer/capyboard-starter>. It can be easily downloaded by using the following command: 

```
git clone https://github.com/realcharmer/capyboard-starter
```

[Download Zip :fontawesome-solid-file-zipper:](https://github.com/realcharmer/capyboard-docs/archive/refs/heads/master.zip){ .md-button }

## File structure

The starter template contains few configuration files and a sample "Hello World" source code.

### platformio.ini

```ini
[env:esp32-s3-devkitc-1]
platform = espressif32
board = esp32-s3-devkitc-1
framework = arduino
monitor_speed = 115200
```

This is the configuration of the PlatformIO framework, such as the platform and board specification, as well as serial monitor speed.

### Makefile

```makefile
PROJECT_DIR = $(CURDIR)
PLATFORMIO_BIN = /bin/pio

all: build upload

build:
	$(PLATFORMIO_BIN) run -d $(PROJECT_DIR)

upload:
	$(PLATFORMIO_BIN) run -d $(PROJECT_DIR) -t upload

clean:
	$(PLATFORMIO_BIN) run -d $(PROJECT_DIR) -t clean

monitor:
	$(PLATFORMIO_BIN) device monitor

.PHONY: all build upload clean monitor
```

The makefile is used to aid with PlatformIO commands. Instead of having to execute separate commands for building and uploading, the makefile provides a simple alternative. Refer to the [Usage](usage.md) section for more information on how to use Make.

## Source Code

All source code should be placed in the `src` directory, typically named `main.ino`. The starter template provides a very simple starting point. The program initializes serial communication and prints "Hello!" to the serial output. This can easily be expanded for further use.

```arduino
void setup() {
	Serial.begin(115200);
}

void loop() {
	Serial.println("Hello!");
	delay(1000);
}
```
