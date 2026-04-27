# nsx-ambiqsuite-r3

`nsx-ambiqsuite-r3` is the raw AmbiqSuite R3 SDK provider repo used by NSX.

This repo keeps the imported vendor SDK under `sdk/` and exposes a thin NSX
provider target through `CMakeLists.txt` and `nsx-module.yaml`.

The default branch corresponds to the R3.1.1 line used for Apollo3 and Apollo3P
targets in NSX.

## Toolchains

Prebuilt HAL/BSP libraries shipped under `sdk/lib/` are GCC builds; armclang
and ATfE consume the same prebuilts (Arm AAPCS-compatible). End-to-end builds
through this provider are validated under:

- `arm-none-eabi-gcc` (reference)
- `armclang` (Arm Compiler 6)
- `clang` / ATfE (Arm Toolchain for Embedded)

The vendored CMSIS-5 ARM core headers were removed from `sdk/CMSIS/ARM/Include/`;
CMSIS core headers are now provided exclusively by `nsx-cmsis-core` (CMSIS-6).

Licensing for the imported SDK content follows the upstream AmbiqSuite terms.
The root-level [`AM-BSD-EULA.txt`](AM-BSD-EULA.txt) is copied from the imported
R3.1.1 SDK snapshot for visibility.
