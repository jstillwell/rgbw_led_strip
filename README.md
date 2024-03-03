# RGBW LED Strip Driver
I made this because all I can find are RGB drivers. This might turn into an actual circuit board and library since nobody makes one, apparently. Its nothing fancy. I took an existing RGB driver board and added another MOSFET to handle the extra channel for the White LED's. 
I am using this on one of my 3d printers to provide overhead lighting. I am hoping to use the API to integrate it with octoprint, klipper and such.

## Libraries
### NodeMCU
The code uses NodeMCU library to create an API and web UI that allows users to change the colors and set an intensity level for the white LED's.
### FastLED
It uses the FastLED library to help with the RGB driver board.
### Secrets.h
This is a common way to hide secrets in your code when you want to share it. Basically, you need a folder called secrets with a file called secrets.h in the arduino libraries folder. In the file you declare constant strings, or whatever, that you need to use.

## Parts list
 - NodeMCU TODO: add link
 - LED strip driver TODO: add link
 - N-channel Mosfet
 - 1k resistor
 - 100uf electrolytic capacitor
 - 2 voltage regulators (This part may change based on your needs or the LED strip you are using. Mine are 12v. The nodeMCU needs 5v. The LED driver board needs 12v and 5v.)
   - 1 for 24v to 12v
   - 1 for 12v to 5v
