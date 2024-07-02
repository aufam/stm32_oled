# STM32 OLED
OLED I2C interface for STM32. Cloned from https://github.com/greiman/SSD1306Ascii

## Requirements
* Arm GNU toolchain
* cmake minimum version 3.10
* STM32CubeMx generated code

## How to use
* Clone this repo to your STM32 project folder. For example:
```bash
git clone https://github.com/aufam/stm32_oled.git <your_project_path>/Middlewares/Third_Party/stm32_oled
```
* Or, if Git is configured, you can add this repo as a submodule:
```bash
git submodule add https://github.com/aufam/stm32_oled.git <your_project_path>/Middlewares/Third_Party/stm32_oled
git submodule update --init --recursive
```
* Add these line to your project CMakeLists.txt:
```cmake
add_subdirectory(Middlewares/Third_Party/stm32_oled)
target_link_libraries(${PROJECT_NAME}.elf oled)
```
