# Height-based box sorting

The report describes a conveyor sorter with three height classes, identified as L, M, and P. Height enters through `ID30`; comparisons with 200 and 150 select class flags. Three extended pulse timers (`S_PEXT`, `S5T#24S`) retain the class indication during transport.

| Class | Class flag | Pusher | Count output |
| --- | --- | --- | --- |
| L | M0.3 | Q0.6 | QD30 |
| M | M0.2 | Q0.5 | QD34 |
| P | M0.4 | Q0.7 | QD38 |

Photoelectric/position inputs trigger the matching pusher, front limits end its action, and counters record class events. The M pusher includes a one-second `S_ODT` delay (`T3`). `I1.3` resets the class counters. Confirm exact comparison boundaries and contact polarity from the PDF networks; the native I/O configuration was not supplied.

[Ladder export](../ladder/02_height_based_box_sorting.pdf) · [Film slot](../videos/README.md)
