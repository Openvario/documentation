# OpenVario assembly

Assembly of the Cubieboard OpenVario: adapter board stacked on a Cubieboard,
sensorboard, four-socket connectorboard, and sheet-metal case.

Based on Guido Probst’s assembly guide of 1 December 2014,
[CC BY-SA](https://ftp.openvario.org/Open%20Vario%20Assembly%20Guide.pdf).

BOM, schematics, and variant CAD: [Manufacturing](../manufacturing/).
After assembly: [Installation guide](../installation/).
Separate 7″ assembly PDF:
[Openvario_7in_assembly.pdf](https://ftp.openvario.org/Openvario_7in_assembly.pdf).

## Contents

- [Parts](#parts)
- [Case](#case)
- [Power](#power)
- [Stack](#stack)
- [Display cable](#display-cable)
- [Fit the electronics](#fit-the-electronics)
- [Finished unit](#finished-unit)

## Parts

**Electronic parts**

- Adapter board
- Connectorboard
- Sensorboard
- Pressure-hose barbs

![Electronic parts](figures/parts-boards.png)

**Cubieboard**

![Cubieboard](figures/parts-cubieboard.png)

**LCD and touchscreen**

![LCD and touchscreen](figures/parts-lcd-touch.png)

**Housing**

Front frame, back frame, distance plates, lower and upper housing covers,
upper backplate, and lower backplate.

![Housing](figures/parts-housing.png)

**Front plate**

![Front plate](figures/parts-frontplate.png)

**Faceplate**

![Faceplate](figures/parts-faceplate.png)

## Case

Countersink before bending the parts.

**Countersinks on the frames**

![Countersinks on the frames](figures/case-countersink-rivet.png)

**Countersinks and threads**

![Countersinks and threads](figures/case-countersink-sheet.png)

Red marks are a 120° countersink for the rivets, about 6 mm. On 1.5 mm sheet
the black marks are a 90° countersink. On 3 mm sheet the black marks are an
M3 thread.

Eight rivets join the two frames to the two distance plates.

**Frames and distance plates**

![Frames and distance plates](figures/case-rivets.png)

Mount the front plate and the lower backplate on the frames. The USB and LCD
cable holes face the bottom.

**Front plate and lower backplate**

![Front plate and lower backplate](figures/case-frames.png)

Four threaded standoffs hold the Cubieboard.

**Cubieboard standoffs**

![Cubieboard standoffs](figures/case-standoffs.png)

Four M3×16 studs go through the front plate with high-strength thread locker.
Flush on the front, hexagon head aft. A nut and washer hold each stud until
the locker cures.

**Front-plate studs**

![Front-plate studs](figures/case-studs.png)

## Power

Set the adapter-board DC/DC converter to 5 V with the blue trimmer.

**5 V and 3.3 V check**

![5 V and 3.3 V check](figures/power-5v.png)

The output capacitor is +5 V. The pin row beside it is +3.3 V. Connect the
Cubieboard and the LCD only after both rails are right.

## Stack

Solder the supply from the adapter board.

**Supply, adapter end**

![Supply, adapter end](figures/stack-solder-a.png)

**Supply, other end**

![Supply, other end](figures/stack-solder-b.png)

…to the Cubieboard.

**Supply on the Cubieboard**

![Supply on the Cubieboard](figures/stack-solder-cubie.png)

The outer edges of the two boards must line up. The headers can mate 2 mm off.

**Board alignment**

![Board alignment](figures/stack-align.png)

Jumper UART0 RX and TX from the Cubieboard.

**UART0 on the Cubieboard**

![UART0 on the Cubieboard](figures/stack-uart-cubie.png)

…to the adapter, which has the same pin layout. The photos do not label which
wire is RX.

**UART0 on the adapter**

![UART0 on the adapter](figures/stack-uart-adapter.png)

Cut one jumper and solder it to the middle contact of the Cubieboard
headphone jack.

**Headphone jack**

![Headphone jack](figures/stack-headphone.png)

That wire later goes to the amplifier pin on the sensorboard.

Connect three wires to the 12 V outlet on the adapter:

- +12 V supply
- ground
- +12 V for an external device, such as FLARM

**12 V outlet**

![12 V outlet](figures/stack-12v.png)

Knot the cable as the strain relief.

**Strain relief**

![Strain relief](figures/stack-strain-relief.png)

Check the jumpers. In the guide, JP1 is closed and JP2 and JP3 are open.

**Jumpers**

![Jumpers](figures/stack-jumpers.png)

- JP1 mirrors up / down
- JP2 mirrors left / right
- JP3 selects backlight PWM, or 3.3 V fixed

## Display cable

Connect the display cable. The two ends are not the same.

On the adapter the latch slides out and the contacts face away from the board.

**Display cable on the adapter**

![Display cable on the adapter](figures/display-adapter.png)

On the LCD the latch flips up and the contacts face the panel.

**Display cable on the LCD**

![Display cable on the LCD](figures/display-lcd.png)

Run the whole system before it goes into the case.

## Fit the electronics

Spacer bushings go between the Cubieboard and the adapter.

**Spacer bushings**

![Spacer bushings](figures/fit-spacers.png)

Screw that stack onto the standoffs.

**Stack on the standoffs**

![Stack on the standoffs](figures/fit-standoffs.png)

Check the alignment.

**Alignment in the housing**

![Alignment in the housing](figures/fit-alignment.png)

The sensorboard is held to the upper backplate by the three hose barbs.

**Hose barbs**

![Hose barbs](figures/fit-hose-barbs.png)

**Sensorboard**

![Sensorboard](figures/fit-sensorboard.png)

Screw the connectorboard to the same plate.

**Connectorboard**

![Connectorboard](figures/fit-connectorboard.png)

Connect the audio wire to the amplifier pin on the sensorboard.

**Audio wire**

![Audio wire](figures/fit-audio.png)

Join the sensorboard with a 10-pin ribbon, pin 1 to pin 1. The photo does not
mark which end is pin 1.

**Sensorboard ribbon**

![Sensorboard ribbon](figures/fit-ribbon-sensor.png)

Join the connectorboard with a 12-pin ribbon, pin 1 to pin 1.

**Connectorboard ribbon**

![Connectorboard ribbon](figures/fit-ribbon-connector.png)

**Ribbon on the adapter**

![Ribbon on the adapter](figures/fit-ribbon-adapter.png)

Connect the LCD and the touchscreen.

**LCD and touchscreen cables**

![LCD and touchscreen cables](figures/fit-lcd-cables.png)

Tape the LCD to the front plate with double-sided tape on the marked strips.
Keep the touchscreen cable clear.

**LCD tape**

![LCD tape](figures/fit-lcd-tape.png)

Bond the LCD on the marked edges. The front frame, mounted next, clamps the
touchscreen.

**LCD on the front plate**

![LCD on the front plate](figures/fit-lcd-aligned.png)

Two aluminium profiles, about 98×10×5 mm, go on the back of the front plate.
Adjust the frame for the thickness of the LCD, the touchscreen, and the tape.
Drill 1.6 mm through the frame and the profiles, cut M2 threads in the
profiles, countersink the frame, and fix it with M2×5 flat-head screws.

**Front frame**

![Front frame](figures/fit-front-frame.png)

A grommet goes in the lower backplate cable hole.

**Grommet**

![Grommet](figures/fit-grommet.png)

Fit the lower and upper covers.

**Housing covers**

![Housing covers](figures/fit-covers.png)

## Finished unit

**Finished OpenVario**

![Finished OpenVario](figures/done-front.png)

**Back panel**

![Back panel](figures/done-back.png)

- Four RJ45 serial ports, IGC pinout, each with its own fuse, for FLARM and
  IGC loggers on a standard RJ45 cable
- Front frame on two aluminium profiles, about 98×10×5 mm, with M2×5 flat-head
  screws
- Cinch socket for a 4–32 Ω speaker
- RJ12 with power and I2C for an external sensor
- 3.5 mm jack for a single-wire temperature sensor
- Two USB ports
- Slot through to the Cubieboard microSD socket
