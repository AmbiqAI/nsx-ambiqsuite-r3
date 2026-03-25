# nsx-ambiqsuite-r3

`nsx-ambiqsuite-r3` is the raw AmbiqSuite R3 SDK provider repo used by NSX.

This repo keeps the imported vendor SDK under `sdk/` and exposes a thin NSX
provider target through `CMakeLists.txt` and `nsx-module.yaml`.

The default branch corresponds to the R3.1.1 line used for Apollo3 and Apollo3P
targets in NSX.

Licensing for the imported SDK content follows the upstream AmbiqSuite terms.
The root-level [`AM-BSD-EULA.txt`](AM-BSD-EULA.txt) is copied from the imported
R3.1.1 SDK snapshot for visibility.
