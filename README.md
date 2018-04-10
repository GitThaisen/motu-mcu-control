# Motu-MCU-control
Control your MOTU AVB soundcard with your MCU enabled controller

Based on documentation from MOTU:  http://cdn-data.motu.com/downloads/audio/AVB/avb_osc_api.pdf

Work in progress...

This program convert data from your Midi controller and send it to your MOTU sound interface.
It can be placed on your computer or on a RaspberryPi like computer board.


# Quick start 
- Connect your MCU (in my case a BCF2000) to the RaspberryPi with USB and connect the RaspberryPi to the network where the MOTU soundcard is.
- Run the main.py program (you can use *--ip* arguments to set the MOTU interface IP address)
- That's it!
- Faders should move to their corresponding positions and active outputs should be lighted.

## Features (available)
* Choose between output mode, or mixer mode by using buttons (encoder group buttons) (displays the mode on the assign 7segments screen)
* Control outputs (output mode): 
* * Headphones, with faders, select to enable
* * Main output, with faders, select to enable
* * Dim Main output by clicking on F8 button (apply -20dB on main)
* Control inputs from strip 1 to 8 (mixer mode):
* * Solo, mute, Pan and Faders
* Store settings in a database

## TODO
* Handle banks to use multiple layers of fader if more than 8 channels
* Handle the send mode:
* * Using already defined personal send vues
* * Selecting a send output, then selecting all desired strips to add to the vue
* Change dim value by keeping dim button down and use vpot to set it up
* Handle flip mode (invert fader and rotary vPot)
* Add a mute all / unmute all
* Add a clear solo button
* Handle MCU extension for larger setups

* Display track names and different values on scribbles 
* Create a virtual strip to control EQ, Comp, and Limiter (web vue?)

* Improve setup routine (via a remote web interface or directly ) to setup the MOTU IP address and other relevant settings directly from the controller, without using the computer/rapspi

