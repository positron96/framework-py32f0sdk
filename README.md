# framework-py32f0sdk

PlatformIO framework for PY32 microcontrollers.

It is based on https://github.com/IOsetting/py32f0-template repository.

The repo has both HAL and LL drivers.
LL driver is always available, but HAL driver will be compiled only if `USE_HAL_DRIVER` is defined in platformio.ini

Corresponding BSP package will be available if `USE_BSP` is defined.
