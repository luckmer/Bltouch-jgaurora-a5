<h1 align="center">Hi👋, Z Axis Calibration</h1>
<h3 align="center">📦 Provides a simple guide for calibrating your 3D printer axis using G-code commands. This calibration process will ensure that your printer's axes are properly aligned. 📦</h3>
<h1 align="left">Calibration Steps</h1>
<h3 align="left">Please follow these steps carefully to calibrate your 3D printer's axis:</h3>

Home all axes using G28
```
G28
```
Set the Z-offset to zero using M851:
```
M851 Z0
```
Move the Z-axis to zero using G1:
```
G1 Z0
```
Disable the axis locks for all axes using M211:
```
M211 S0
```
This command disables the axis locks, allowing you to manually adjust the axis if needed.
Using your printer's control panel or Pronterface, manually level the Z-axis until you are satisfied with its alignment.
You can check the current position of each axis using the M114 command:
```
M114
```
Once you are satisfied with the Z-axis alignment, set the Z-offset accordingly using M851.
Replace <enter Z axis from m114> with the desired Z-offset value (e.g., -3.5 in this example):
```
M851 Z<enter Z axis from m114>
```
Re-enable the axis locks using M211:
```
M211 S1
```
This command locks the axes in their current positions.
Save the settings to EEPROM using M500:
```
M500
```
Reload the saved settings using M501:
```
M501
```
Display the current settings using M503:
```
M503
```
To ensure that the changes have taken effect, home all axes again using G28:
```
G28
```
<h1 align="center">AUTO BED LEVELING</h1>

```
G28
```
Use G29 to enable auto bed leveling using G29:
```
G29
```
Save the updated settings to EEPROM again using M500:
```
M500
```
Reload the settings using M501:
```
M501
```
Display the current settings using M503:
```
M503
```
Finally, move the Z-axis to zero to verify that it is still properly aligned:
```
G1 Z0
```
You're all set! Enjoy 3D printing with your calibrated axis.
Feel free to reach out if you have any questions or encounter any issues during the calibration process.
<h1 align="center">Happy printing!</h1>

