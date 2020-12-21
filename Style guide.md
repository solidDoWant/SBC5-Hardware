# General component rules
* All parts should have the correct reference designator set. See [Wikipedia](https://en.wikipedia.org/wiki/Reference_designator#Designators).
* All parts should have the comment set as the part number.
* All parts should have a datalink parameter set.
* All parts should have pricing information attached.

# Naming rules
* Passives should have a SI prefix appended to them with correct capitalization. See [Wikipedia](https://en.wikipedia.org/wiki/Metric_prefix#List_of_SI_prefixes).
* Passives should not have a SI prefix appended to them if there isn't one (i.e. a resistor with 100 ohms of resistance would be labeled '100')
* Passives should not have a unit appended to them (i.e. a 100 nano Farad capacitor should be marked as 100n, not 100nF or 100nf).
* SI prefixes appended to components should not have a space between the value and the unit (i.e. 100m not 100 m).
* The SI prefix for micro should be replaced with 'u' (i.e. 100u not 100μ).

# Pin rules
* 'Simple' passives should have pin designator hidden.
* Pin names should have be the pin's primary function (i.e. a SPI clock pin that can also operate as GPIO pin should be listed as an SPI clock pin).
* Pins should be grouped according to purpose (i.e. address pins in one group, data pins in another).
* Pins should be spaced evenly on a 100 mil grid.
* Pin groups should be oriented in direction of primary data flow. Pins that are primarily input should be on left, and pins that are primarily output should be on the right.
* Inverted signal pins (such as SPI CS) should have an overhead bar (suffix each letter with '\', i.e. C\S\).

# Schematic symbol rules
* Reuse schematic symbols for 'simple' components (i.e. passives, discrete semiconductors) wherever possible.
* All symbols should have associated footprints.
* High speed components should have IBIS models associated.
* Large and complex parts (i.e. MPUs) or parts with repeated functions (i.e. OP amp packages with multiple amps) should be split into separate subparts according to function.

# PCB footprint rules
* All parts should have a 3D model.
* No pads should have the same name (i.e. multiple grounds should be marked as 'GND1', 'GND2', etc.).
* A silkscreen outline should be drawn around the part
* A mechanical layer 13 outline should be drawn around the entire body of the part. This may differ from the silkscreen outline where there is overhang.
* A mechanical layer 13 '+' should be drawn in the center of the part.

# Schematics
* Each schematic file should have one function
* Each schematic file should be broken out into separate 'blocks' according to function, if needed.
* Blocks should be outlined with a dashed line.
* Blocks should have a title shortly explaining their function.