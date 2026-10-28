# Check Notes

Verified with KiCad 10.0.5 on 2026-10-28, using the saved project rules and including schematic-to-board comparison. Error, warning, and exclusion severities were included. The reports retain the list of checks disabled in the project settings.

| Check | Findings |
| --- | ---: |
| Schematic electrical rules (ERC) | 0 |
| PCB design rules (DRC) | 0 |
| Unconnected PCB items | 0 |
| Schematic-to-board consistency | 0 |

Reports: [ERC](erc.json) and [DRC / schematic comparison](drc.json).

**Sensor supplies:** U4 LuminOX and C6 use the protected 5 V branch. SCD40, CCS811, their 3.3 V bypass capacitors, the CCS811 reset pull-up, and the I2C pull-ups use 3.3 V. The auxiliary load supply at J4/D3 is restored to 3.3 V. Schematic and PCB routing were updated together.

The input supply and F1/D2 protection losses must leave U4 within its 4.5-5.5 V operating range. References: [LuminOX datasheet](https://www.processsensing.com/docs/datasheet/DS0030REV17_LuminOx.pdf) and [CCS811 hardware guidance](https://github.com/sciosense/CCS811_driver#hardware).

**Programming header:** J2 has a custom 2x3 pinout: 1 = +3V3, 2 = GND, 3 = MCLR/VPP, 4 = PGC, 5 = PGD, 6 = unconnected. Use an adapter mapped to these signals.

The rail correction preserves the existing board outline, component placement, and rule settings. Copper fills and automated reports were refreshed after rerouting.

The schematic PDF, component list, PCB views, and 3D render were regenerated from this revision. Both schematic sheets are included; all symbol and footprint references resolve in the standard KiCad 10 libraries. The [file manifest](files-sha256.json) records the packaged files.
