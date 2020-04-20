# KLE PCB Generator

This script takes a json file exported from the online [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/) and generates a KiCAD schematic and layout out of this. The resulting schematic is pretty much complete: it contains all key switches connected in rows and columns, a functional control circuit built around the ATmega32U4 (including external crystal, reset switch and a USB connector) and mounting holes. The layout is only partly connected, but most crucially it contains all switches in the right positions (including holes for stabilizers for keys that need it), and a board outline compatible with [swillkb's online Plate&Case Builder](http://builder.swillkb.com/), which accepts the same KLE json input and produces several CAD files with which one can build a keyboard.

# Features

At this point klepcbgen supports only the bare minimum of features:

* Keys of different widths and/or heights
* Stabilizers for keys 2 units or more wide
* Cherry MX switch mount

Features available in KLE that would impact a PCB but are currently **not** supported are:

* Secondary width/height (So no ISO/big-ass ENTER keys for now, sorry!)
* Rotated keys
* Alps switch mount
* Plate mounted switches (although I think the footprints for PCB mounted switches are compatible with plate mounted switches)

# Manual

While this script takes care of a lot of the tedious drudge-work (most notably correctly positioning all switches), the end-result is not a finished layout you can immediately send off to be manufactured. There are a few steps required to get the schematic and layout.

<TODO>

# Future improvements

I have a bunch of ideas for this generator, such as:

* Lighting: obviously RGB is all the rage, so I would like to add options to generate a PCB which includes lighting
* Split layout: I'm a big fan of ergonomic/split layouts (I'm currently typing this on a Kinesis Freestyle Pro)
* Wireless: Cables are a nuisance. I'd love to make my own wireless keyboard

