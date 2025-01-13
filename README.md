# framework-py32f0sdk

PlatformIO framework for PY32 microcontrollers.

It is based on https://github.com/IOsetting/py32f0-template repository.

The repo has both HAL and LL drivers.
LL driver is always available, but HAL driver will be compiled only if `USE_HAL_DRIVER`.
Some parts of LL driver are only enabled if `USE_FULL_LL_DRIVER` is defined.

Corresponding BSP package will be available if `USE_BSP` is defined.

To have respective headers available and sources compiled, use the following configurations in your `platformio.ini`:

```
build_flags =
 -DUSE_FULL_LL_DRIVER
 -DUSE_HAL_DRIVER
 -DUSE_BSP
```

If you use HAL with `py32f0xx_hal_conf.h` file, place it in your project's `include` directory.
The example of HAL project can be seen here: https://github.com/positron96/platform-py32f0/tree/master/examples/example-hal.