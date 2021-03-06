# CherryPi Tablet 

A RaspberryPi powered Tablet

![CherryPi running RetroPi](Pictures/CherryPiRunningRetroPi.jpg "Photo of Tablet")

## About

This was my final project for the high school's piloting "STEAM" course, offered in the senior year of high school. Here are a few of the projects that was the inspiration for this one:

  * [PIPAD by Michael K Castor](https://www.mkcastor.com/pipad-build/)

  * [PIPAD 2.0 by Michael K Castor](https://www.mkcastor.com/raspberry-pi-7-touchscreen-setup-review-and-case-design/) (This came out as I was designing mine and it's CAD files were amazingly helpful!)
  * [7" Portable Multitouch Raspberry Pi Tablet by Ruiz Brothers](https://learn.adafruit.com/7-portable-raspberry-pi-multitouch-tablet?view=all)

I was luckly enough to have access to some amazing tools (like a 3D printer and CNC Mill). This project gave me the opprotunity to tackle a project that I had wanted to complete in a structured setting. Where I had to write up a proposal and define the scope of the project, set milestones, and research other people's approaches and solutions to very similar projects. 

This project also gave me an opprotunity to get my hand's dirty, giving me a reason to learn basic CAD and CAM skills in Fusion 360, and operating (and assembling) a CNC Mill. The biggest problem I had to deal with was the translation from digital to physical, forcing me to find ways to calibrate the tools with few accurate tools.

## Design
### CherryPi's Bill of Materials (BOM): 
* Raspberry Pi Foundation's 7-inch Touchscreen Kit
* Raspberry Pi 2 (modified to have an "internal" USB port)
* 1x8" Cherry wood plank from Home Depot
* Adafruit's PowerBoost & 500mA Lipo
* Powered USB hub from Amazon

### Screen & Logic Board
While I could have gone with a larger Touch-Screen and one built for more general use, RPiF's kit removed the variable of having to deal with a potential, headache-inducing, issue with screen drivers and other issues.
The RPi 3 would have been a better choice than a RPi 2 considering that I wanted the Tablet to have WiFi, at the time of building this project (2015-2016) the RPi 3 hadn't/was about to be annouced. If I was to redo this project today I would definitely have used a RPi 3. 
### Chassis
I wanted something a bit nicer than just 3d-printed ABS. So I decided that a nice wooden body was the way to go. Cherry was a choice for a couple of reasons, mainly because it's a cheaper hardwood, also because then I could call the project CherryPi. 
### Power Source
This is something I would *definitely* change in a later build, while Adafruit's PowerBoost is a great little board that allowed me not the think about how to power the tablet from a Lipo safely, and recharge said Lipo without having to remove it. It even allow's hotswapping from internal power (from the battery) to external power, charging the battery and powering the Tablet at the same time! This may sound like an expectation rather than a bonus, but a lot of other solutions didn't have such features. However, the battery is *way* too small. 500mA is only enough for the Tablet to last for 10-15min max.

## Improvements
As with any project, hindsight is 20/20, so there are a couple of changes I would make if I was to redo/upgrade this project.
### Electronic improvements
As mentioned earlier, the two main changes would be the replacing the RPi2 with a RPi3 as the logic board and replacing the current power source with something with higher capacity. Switching to a RPi3 would allow the tablet to have one more usb port avaliable externally and would add bluetooth which would be a nice addition, especially with RetroPi and bluetooth controllers.
As for the power source, I've considered just replacing the current battery with one of the larger batteries sold by Adafruit, however they're larger battery is cylindrical, where the current is a flat square, and I worry that there might not be enough space vertically in the body. A safer route, expense wise, is probably to take Castor's approach for the PIPAD 1.0 and use a phone battery pack (specifically one that allows hotswapping and passthru) and a micro-usb extension cable. That way if the pack doesn't work out I could use it elsewhere (like maybe for it's intended purpose).

### Chassis improvements
The biggest gripe with the device is that it's really thick and kinda heavy for it's size. The thickness of the device is due to the fact that the body is built out of two stacked pieces of 1"x8" board giving it a rough thickness of 1 1/2" (since the actual thickness of a 1"x8" board is 3/4"). What would be great is if the body could be built out of a single layer of board. However that presents a couple of problems, first, it would be an extremly tight squeezeto fit all the current ports, and the screen into 3/4" along with sacrificing some space for the back of the cavity within the case. Secondly, one of the electronic improvements was to increase the battery life of the tablet, decreasing the vertical internal space would make solving that issue harder. Finally, the ability to open up the body to make fixes and adjustments is crucial, with the two piece design the top and bottom are held together by screws. With the one piece design the project would probably have to have a door cut in the rear which would require two milling jobs which is difficult to align each properly with hard-to-calibrate tools.

There are two viable solutions to the problems above, The first would be to take the hybrid of the current and the ideal. Still use the two layer design but make the bottom layer simply a "lid" out of extremly thin wood, like luan, or a different material. This would allow for easy access to the internals, remove the issue sacrificing cavity space, and would only require one milling job. While it doesn't exactly solve the space issue for the battery, I could probably find a battery that could be made to work.

The second option would be making the touch screen a removable from the body. Currently the screen is glued to the top frame, which is not advisable in the long run due to the fact that the adhesives between the glass and the screen cannot support the screen's weight long term. However there are mounting holes in on the rear of the frame. If the screen were attached to the rear of the body using those mounting holes the display could be removed if access to the internal was required. The problem with this solution is it only really solves two of the problems, milling and access to internals, and really doesn't provide an answer to the others.
