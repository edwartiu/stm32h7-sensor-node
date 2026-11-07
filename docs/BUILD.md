# Build

| Purpose | Tool |
|---|---|
| Compiler | Arm GNU Toolchain (`arm-none-eabi-gcc`), C11 |
| Build system | CMake + Ninja |
| Device support | CMSIS core + STM32H7 device headers (no vendor HAL in phases 1-2) |
| Flash and debug | OpenOCD / STM32CubeProgrammer, GDB over SWD |
| RTOS | FreeRTOS |
| Unit tests | Unity (host-side) |
| Static analysis and style | cppcheck (MISRA C addon), clang-format, clang-tidy |
| Bus analysis | Logic analyzer with PulseView (sigrok) |
| CI | GitHub Actions |

```sh
cmake -B build -G Ninja -DCMAKE_TOOLCHAIN_FILE=cmake/arm-none-eabi.cmake
cmake --build build

# Host unit tests
cmake -B build-test -DBUILD_TESTS=ON
cmake --build build-test
ctest --test-dir build-test

# Static analysis
cppcheck --enable=warning,style --addon=misra src drivers
```
