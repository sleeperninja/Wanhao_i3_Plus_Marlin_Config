# Wanhao i3 Plus / MMSP SKR 1.4 Turbo Marlin Config

This is a set of Marlin Bugfix configs for replacing the stock motherboard with the SKR 1.4 Turbo.

### Hardware Configuration

* Stock Monoprice Maker Select Plus hardware has gone through the [MK3x conversion](https://www.thingiverse.com/thing:2686588)
* Melzi motherboard and Keypin board (X-axis breakout board) replaced by [Bigtreetech SKR 1.4 Turbo w/TMC2209 stepper drivers](https://www.amazon.com/gp/product/B08F7XTR72)
* LCD replaced with TFT35 V3.0
* [Micro Swiss All Metal Hotend](https://www.amazon.com/Hotend-SLOTTED-Cooling-Wanhao-nozzle/dp/B01N3P08PA)
* [BLTouch](https://www.amazon.com/ANTCLABS-BLTouch-Leveling-Premium-Extension/dp/B07FR2LLZP)

### Features

* Sensorless homing
* BLTouch in Marlin mode
* Babystepping
* Near dead silence
* Hotend fan only comes on at {temp}>50°C
* Build using [PlatformIO](https://platformio.org/)
* Relative extrusion
* Almost compatible with MK3s slicer profiles*

*MK3s profile custom gcode should always be modified to remove Prusa-specific commands

### To Do

* Z-tramming (G34, in progress)
* Need to add SKR 1.4 Turbo wiring diagram (SKR 1.4 Turbo discontinued...)
* MK3s compatibility: MK3s extrusion rates are considerably higher as the layer hight increases. This was somewhat fixed when enabling relative extrusion, but may also be attributed to the custom start gcode changes in extruder current.
* Nozzle homing (consideration): I love the BLTouch, but the wires are pretty delicate. There might be value in enabling full sensorless homing for two reasons:
  * Fewer wires in X-axis bundle
  * True Z=0
