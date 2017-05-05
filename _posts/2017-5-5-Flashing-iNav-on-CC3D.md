---
layout: post
title: Flashing iNav on CC3D
published: true
---

So you want to know how to install iNav on your CC3D – We have you covered!

Since the OpenPilot Software is no longer in development and their site is now down, you can breath new life into your CC3D flight controller by flashing it with the latest release of CleanFlight, here’s how……

Software & Drivers Required:

iNav Configurator (For Chrome App Launcher) – Requires that you have the “Chrome Browser” Installed!
The correct FTDI drivers installed for your particular FTDI adapter (This guide assumes you already have the drivers installed and working!)
 

Hardware Required:

1: CC3D Flight Controller (Duh)

CC3D available from: Amazon | Banggood | eBay

## Installing cleanflight on cc3d

2: 4 Wire Molex Cable (It came with your CC3D)
cc3d 4 pin Serial Molex thrustworx

2:  “Mini” not “Micro” data capable USB Cable (Make sure its a USB data Cable and not USB power only!)
Mini USB Cable Thrustworx

3: FTDI Adapter
FTDI available from: Amazon | Banggood | eBay

4: Paperclip for shorting the pads on the CC3D

5: Optional USB battery charger (For powering the CC3D Board since we do not use the FTDI 5V power!)

### Step One:
Install iNav Configurator in Chrome.

### Step Two:
Install USB to UART Bridge VCP Drivers

### Step Three:
Connect your 4 pin Molex connector to the “Main Port” of your CC3D. (Its the one on the right! 😉

CC3D Main Port Cleanflight Pinouts

### Step Four:
#### 1: Connect the other end of your 4 pin Molex connector to your FTDI Adapter following the pinouts below.
NOTE: The  color of your cables might be different than outlined below. As long as you follow the actual orientation and pattern, the wire colors are irrelevant!

Ground to Ground (Far Left wire)
Power (Not Used)
TX to RX (Third in from the left)
RX to TX (Last wire on the far right)
FTDI to CC3D Cleanflight Pinouts

#### 2: Now plug your FTDI adapter into a working USB port on your computer.

### Step Five & Six:

This step can be a little tricky and take a couple of tries before you get it right if your CC3D board does not have pre-soldered pins (most do not!)

If your lucky enough to have the pins already soldered, then all you have to do at this point is install a jumper.

Tip: You can solder your own pins for future flashing. My suggestion is if you are proficient with a soldering iron, solder the pins on, and save yourself a whole lot of hassle!

 

If you are like the rest of us and only have the pads as shown below, then this is what you will need to do…

#### 1: While shorting the pins with a paperclip

CC3D Boot Pins

#### 2: Connect your USB cable to the USB port on your CC3D board to supply it with power.
TIP: The method I have used for ease of handling a finicky job like this, is to connect the USB cable to a USB Power charger that has an On/Off switch first.

Then, while shorting the pins with one hand, turn the power on the charger with the other.

CC3D USB Port Connection

#### 3: You know you got it right when the LED’s on your CC3D have gone solid orange.

### Step Seven:

You should now have solid (non flashing) LED’s on your CC3D. If not, go back to step Five/Six above!

#### 1: Open Cleanflight in Chrome.

#### 2: Select/Go to the “Firmware Flasher” tab at the top Left corner of the Cleanflight Configurator.

#### 3: Select your FTDI adapters “COM Port” from the top right hand side of Cleanflight Configurator.

#### 4: Select the latest “CC3D” firmware file from the “Choose a Firmware / Board” drop down menu in the top left area of Configurator.

#### 5: Make sure the following options are selected under the drop down menu:

- No reboot sequence (On/Selected)
- Flash on connect (Off/De-Selected)
- Full chip erase (On/Selected)
- Manual baud rate (On/Selected) – You should be OK with the default settings!

iNav Configurator Settings

#### 5: Select “Load Firmware [Online] and wait for it to load

#### 6: Select “Flash Firmware”

iNav Configurator Flash Firmware

You should now see the green bar across the bottom of configurator moving along its merry way. If not, go back and troubleshoot the steps above.

Once its done verifying, unplug the USB power from the CC3D (as well as your FTDI adapter) and restart Configurator.

You can now plug your USB adapter into the USB Port on your CC3D and your computer. Cleanflight Configurator should now pickup your CC3D board directly via the USB cable.

Congratulations, Your done!
