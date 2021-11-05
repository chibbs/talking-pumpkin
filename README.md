# Speaking Halloween Pumpkin With Arduino
This was a little fun project for Halloween. We used a real pumpkin, of course. But we added a small Arduino setup that enabled the pumpkin to talk and glow whenever somebody approached. Got hilarious reactions!

## Components
Here is what I used...
* Arduino Nano
* 12 NeoPixel Ring
* DFRobot DFPlayer Mini
* PIR sensor - I got some really tiny ones :-)
* 1kΩ Resistor
* speaker
* prototyping board, jumper wires, pin header, screw terminals, ... - whatever you like to use. I soldered my setup unto a pcb board (the black one in the picture) and built a casing out of a plastic box.
* a power source... I simply plugged a power bank into the mini usb port of the Nano.

![wiring](info/image1.jpg)
![wiring](info/image2.jpg)
![wiring](info/image4.jpg)

## Wiring
This is the same setup you can see in the photo above (the one with the red PCB board). My final design was slightly different (I moved the pin headers for the PIR and Neopixel to a more convenient place, was all.)

![wiring](info/pumpkin_assembly.jpg)

## TF card
The sounds are stored on a mini SD TF card. The DFPlayer Mini is rather fickle. If you get com errors it might be caused by the TF card (read the documentations!).

For this project the sound files must be placed in a folder named 'mp3' or 'MP3' (case does not matter). I would also name the files '0001.mp3', '0002.mp3' etc. Not sure if that matters, though. The sketch reads the number of files present in that folder and plays them in a random order.

You can copy the mp3 folder included in this repository and add custom sound files to it.

## Code
You can find the Arduino code in the folder 'code'. It consists of the sketch proper and two libraries I wrote. Be sure to download all three!

You also need to install two libraries in your Arduino IDE:
* Adafruit Neopixel (I use the current version 1.10.0)
* DFPlayer Mini Mp3 by Makuna (**must be version 1.0.5!**)

## Images
Here is our pumpkin (it looked more impressive in the dark, of course!). The white dot in the lower part is the PIR sensor.

![Our pumpkin](info/image3.jpg)
