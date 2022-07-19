# Build

The build of the Magnum *should* be relatively straight forward. Just populate the boards, put them together, make sure the normalling and output level headers have jumpers, and then that should be everything.

That said, the following information will probably be useful. Eventually there will be a full picture guide, but for the time being you'll just have to pay attention.

## Extra Parts

There are a couple of parts that are required to build the magnum that aren't listed in the BOM.

* 1 8 pin DIP IC Socket
* 2 14 pin DIP IC Sockets
* 3 16 pin DIP IC Sockets
* 2 jumpers
* A cap for the DPDT push switch (no idea on part number yet sorry)
* A 25mm diameter piezo
* Some red and black wire to connect the piezo to the board
* 2 11mm standoffs
* 4 M3 screws to use with the standoffs
* Some knobs for the controls
* A eurorack power cable

## Sourcing Parts

Most of the parts needed are pretty standard and can be found on Mouser, Farnell, Digikey, etc. There's a couple things worth noting.

The LM13700 DIP chips are getting trickier to find as they've been End Of Lifed. [Thonk](https://www.thonk.co.uk/shop/lm13700/) has them, as do a few other smaller synth oriented shops.

The inter-board connectors can be found at mouser in the right sizes, but Thonk has cheaper alternatives if you're willing to cut them down. They're also good for the standoffs and various other bits.
[https://www.thonk.co.uk/shop/eurorack-diy-essentials/](https://www.thonk.co.uk/shop/eurorack-diy-essentials/)

The Cap on the DPDT switch being used has been tricky to find a part number for. Currently we're using the large number available at the Bristol Hackspace, but will need to figure something out eventually. For the time being either grab one from the hackspace, or find something about the right size and use some glue maybe?

The piezo can be attached to the faceplate by soldering it onto the metal patch. Be careful when doing this, and when soldering wires onto the piezo discs as they can be quite delicate. Using flux is a good idea.

The *partnumbers.csv* file in this folder has partnumbers for most components, along with mouser order numbers and notes on what's probably better to get from Thonk.

## Part Choices

There are really only two places part choices are important.

* Reverse power protection diodes
* Capacitors

The protection diodes should ideally be schottky diodes with a low voltage drop.

Most of the capacitors are either ceramic or electrolytic, but the 100pf filter capacitors should be film. Good quality, metallized polypropylene is the best, but any decent quality film cap that fits will be fine.
There is one electrolytic capacitor that needs to be non-polarised (C16).

## Building

When soldering the boards, it's almost always easiest to start with the physically shortest components and then work upwards. In this case that would be :-

* diodes
* resistors
* DIP sockets
* ceramic capacitors
* transistors
* film capacitors
* electrolytic capacitors
* anything else

When soldering in the inter-board headers, it's a good idea to connect the pin and socket headers, carefully sandwich the boards together with them held in place, and ideally use the standoffs and screws to keep them together. Once that's done, solder the pins, and then *very carefully* pull the boards apart, trying not to bend any pins. Soldering the headers and sockets into the two boards separately will probably end up with them not lining up quite correctly.

Similarly, when soldering pots and jacks, insert them into the pcb, then put the faceplate on, make sure everything is lined up, and then lightly screw them into place to hold steady whilst you solder.

Finally, when soldering resistors and diodes in, it's often easier to solder them in from the front and then fixing up any sub-part joints from the back when trimming of leads. This avoids having the keep flipping the PCB over with parts in and trying to stop them falling out.

## Calibration

The sensitivity of the piezo tap trigger can be adjusted using the trimmer. There's no other calibration to perform.
