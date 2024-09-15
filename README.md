# Nissan-Leaf-Battery-to-OBD2
An opensource solution for connecting OBD2 straight to a Nissan Leaf battery. Very useful gadget to have if you're thinking about buying a battery and want to check the state-of-health beforehand.

Please note, there are two versions of the 'Yazaki' connector found on Nissan Leaf batteries. This connector is refered to as the B24 connector in service manuals. The 2011-2012 version uses a 21-pin, and the 2013-2019 uses a 36-pin connector. See the documentation folder for the schematic differences

## 2013+
![2013+](Documentation/2013%20STL%20file.PNG)

## 2011-2012
![2011-2012](Documentation/2011%20STL%20file%20with%20tabs.png)

A proper Yazaki 22-pin as reference:
![image](https://github.com/user-attachments/assets/f7ab3e50-ddfc-4927-bd08-cea5e2f2bc67)



# How to make your own
It's really easy to make, you'll need the following items:
1. 3d-printed 'B24' connector, found in this repository (for those without a 3d-printer, a ready to go 2013-2019 36 pin connector is available here: https://aliexpress.com/item/1005004180391674.html => in this case you don't need the items needed described in 2. and 3.
2. Dupont style connectors (found in most arduino kits or old PCs) [2013+ use 1x2, 1x3, 1x4, or 2011-2012 version 1x1 only] [Here's what they look like](Documentation/WhatDoDupontCablesLookLike.PNG)
3. Superglue / Epoxy
4. An OBD2 port along with the pins (can be bought new or salvaged from a scrap car)
5. Wires to connect it all
6. A 12V power source (small lead acid battery does the trick OR a few 18650s in series)

# Printing tips
This design has been printed with PLA and PETG. Very likely to work with ABS too! Print with low speed to get the mounting holes to be perfectly shaped. There isn't much to gain with higher quality, the connector will work just fine at .12/.16/.20/.28 mm layer height. Infill settings doesn't matter much as long as it's above 20%. No supports needed! Printing should take ~1.5h

# Detailed instructions
To start of with, gather all the parts needed. Take the correct B24 connector from this repository. Once you have the model printed, attach dupont connectors to it by supergluing/epoxying them in place. Be careful not to get any glue inside the connector, especially the pins. Less is more when it comes to the glue. Once the glue has dried its time to connect the B24 wiring to the OBD2 port wiring. Solder or crimp the connectors together according to the schematic diagram. Power it up with an external +12V source or battery. 12V lead acid or 3x18650s in series works well.

To read data from the pack, plug in an OBD2 bluetooth dongle to the port and fire up Leafspy. Go into the settings menu, and switch to 'BMS only' mode. This can be found where you select your model year, scroll up the list and where 2010 should be there is a 'BMS only' option.

If you did everything correctly, you schould end up with this.
![fully assembled](Documentation/BatterySniffer.jpg)

![leaf spy screenshot](Documentation/LeafSpy%20in%20BMS%20only%20mode.jpg)



# Schematic
Here's the schematic for how to wire up the 2013+ connector to an OBD2 port
![2013+](Documentation/HowToWireItUp_2013%2B.png)

For the 2011-2012, it's the same, but note the B24 connector pin locations differ - see the [2011-2012 pinouts](Documentation/2011_B24.jpg).

