# Gas Sensor Breakout

A PIC16F18344-based gas-sensor board design combining SCD40 CO2 sensing, LuminOX oxygen sensing, CCS811 air-quality sensing, protected power input, and programming and expansion headers.

![PCB front copper and silkscreen layout](docs/images/pcb-front.svg)

**Status:** CAD design study; not yet fabricated or bench-tested. ERC, DRC, and schematic-to-board checks report zero findings in KiCad 10.0.5 under the saved project rules.

This is my manually developed circuit and PCB design. Component libraries, manufacturer models, and other supplied assets retain their original attribution.

- [Hardware source](hardware/): hierarchical schematics, PCB, and project settings.
- [Schematic PDF](exports/schematic.pdf) and [component list](exports/bom.csv).
- [Visual guide](docs/README.md): labeled board and schematic views.
- [Check notes](docs/checks/README.md): automated-check results and circuit notes.

Open `hardware/gas-sensor-breakout.kicad_pro` with KiCad 10 and its standard symbol, footprint, and 3D model libraries.
