# Motor sequencing and temperature-dependent outputs

The report describes a motor sequence controlled by start/stop actions and a count of stop presses. The ladder export uses `C0`, `MW10`, and flags `M0.1` (count at least 1) and `M0.0` (count at least 2). The second motor path includes an `S_ODT` delay of 10 seconds.

The temperature section passes `IW10` through `FC105 SCALE`, writes a scaled value to `MD20`, and uses comparison/MOVE networks to write commands to `QD20`. The printed commands range from 4 through 18 in the supplied networks.

The report describes a -100 to 1000°C engineering range, but the export shows `HI_LIM=-100` and `LO_LIM=1000`. `BIPOLAR` is connected to `M0.0`, which is also used in the stop-count logic. The export also shows D-type comparison blocks acting on `MD20` while displaying real-number constants. These details need checking against the original project, data types, analog module range, and intended I/O mapping before claiming a correct physical temperature/current conversion.

Values written to `QD20` are program commands; their conversion to a real valve current is not verified by the supplied material.

[Ladder export](../ladder/04_motor_temperature_logic.pdf) · [Film slot](../videos/README.md)
