---
icon: material/folder-cog
---

# Project Template

Simple template for a project can be downloaded from a Git repository at <https://github.com/realcharmer/capyboard-starter>. It can be easily downloaded by using the following command: 

```
git clone https://github.com/realcharmer/capyboard-starter
```

[Download Zip :fontawesome-solid-file-zipper:](https://github.com/realcharmer/capyboard-starter/archive/refs/heads/master.zip){ .md-button }

## File structure

The starter template contains configuration files and a sample "Hello World" source code.

### platformio.ini

```ini
--8<-- "https://raw.githubusercontent.com/realcharmer/capyboard-starter/refs/heads/master/platformio.ini"
```

This is the configuration of the PlatformIO framework, such as the platform and board specification, as well as serial monitor speed.

### Makefile

```makefile
--8<-- "https://raw.githubusercontent.com/realcharmer/capyboard-starter/refs/heads/master/makefile"
```

The makefile is used to aid with PlatformIO commands. Instead of having to execute separate commands for building and uploading, the makefile provides a simple alternative. Refer to the [Usage](usage.md) section for more information on how to use Make.

## Source Code

All source code should be placed in the `src` directory, typically named `main.ino`. The starter template provides a very simple starting point. The program initializes serial communication and prints "Hello!" to the serial output. This can easily be expanded for further use.

```arduino
--8<-- "https://raw.githubusercontent.com/realcharmer/capyboard-starter/refs/heads/master/src/main.ino"
```
