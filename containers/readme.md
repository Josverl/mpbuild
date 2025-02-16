
## Simple Build Container for MicroPython using MinGW

This container is designed to build MicroPython using the MinGW toolchain. 
It uses the same build process as the official MicroPython Docker container, but with the MinGW toolchain instead of the ARM toolchain.

It provides a consistent and isolated environment to ensure that the build process is reproducible and free from conflicts with other software on your system.

### Usage

To build the container, navigate to the `containers` directory and run the following command:

```bash
cd containers

docker build -t micropython/build-micropython-win-mingw build-micropython-win-mingw
```