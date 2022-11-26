# Changes from Elegoo Stock firmware

## Borrowed from [mlee12382's fork](https://github.com/mlee12382/Neptune_3)

 - Linear Advance with K=0 so it won't affect anything unless you set it up.
 - Fade height set to a more reasonable 5.0mm instead of 50.0mm.
 - Power Loss Recovery disabled since it is buggy.
 - Host Action Commands enabled.
 - Advanced Pause Enabled with M600 support, though there seems to be an issue with resuming a print after filament change.
 - PID for the Bed instead of Bang-Bang.
 - S-Curve Acceleration enabled.
 - M48 Probe Repeatability Test enabled.
 - G26 Mesh Validation Enabled.
 - Faster BLTouch probing.

Dual Independent Z firmware requires a TMC2208 driver in the spare slot on the control board which will require manual vref setting.

Dual Extruder firmware also requires a TMC2208 driver.

Dual Independent Z and Dual Extruder are mutually exclusive and cannot be used together as there is only one available driver socket. You can however do split driver dual Z and Dual Extruders. Additional hardware will also be needed for both options. Both of these firmwares are untested so use at your own risk.