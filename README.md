README for Axis Calibration
This README provides a simple guide for calibrating your 3D printer axis using G-code commands. This calibration process will ensure that your printer's axes are properly aligned.

Calibration Steps
Please follow these steps carefully to calibrate your 3D printer's axis:

Home all axes using G28:

Copy code
G28
Set the Z-offset to zero using M851:

Copy code
M851 Z0
Move the Z-axis to zero using G1:

Copy code
G1 Z0
Disable the axis locks for all axes using M211:

Copy code
M211 S0
This command disables the axis locks, allowing you to manually adjust the axis if needed.

Using your printer's control panel or Pronterface, manually level the Z-axis until you are satisfied with its alignment. You can check the current position of each axis using the M114 command:

Copy code
M114
Once you are satisfied with the Z-axis alignment, set the Z-offset accordingly using M851. Replace <enter Z axis from m114> with the desired Z-offset value (e.g., -3.5 in this example):

php
Copy code
M851 Z<enter Z axis from m114>
Re-enable the axis locks using M211:

Copy code
M211 S1
This command locks the axes in their current positions.

Save the settings to EEPROM using M500:

Copy code
M500
Reload the saved settings using M501:

Copy code
M501
Display the current settings using M503:

Copy code
M503
To ensure that the changes have taken effect, home all axes again using G28:

Copy code
G28
Optionally, perform an auto-leveling process if your printer supports it:

scss
Copy code
AUTO LEVELING
G28
G29
Save the updated settings to EEPROM again using M500:

Copy code
M500
Reload the settings using M501:

Copy code
M501
Display the current settings using M503:

Copy code
M503
Finally, move the Z-axis to zero to verify that it is still properly aligned:

Copy code
G1 Z0
You're all set! Enjoy 3D printing with your calibrated axis.

Feel free to reach out if you have any questions or encounter any issues during the calibration process. Happy printing!
