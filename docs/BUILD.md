# Build

Toolchain: Arm GNU Toolchain (arm-none-eabi-gcc), CMake + Ninja, CMSIS core and STM32H7 device headers (no HAL in phases 1-2), OpenOCD or STM32CubeProgrammer, GDB over SWD. Host unit tests use Unity.

    cmake -B build -G Ninja -DCMAKE_TOOLCHAIN_FILE=cmake/arm-none-eabi.cmake
    cmake --build build
