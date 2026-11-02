# Source and reproduction notes

The original ladder PDFs identify SIMATIC S7-300 CPU 314C-2 DP and OB1. They are printable exports, not importable editable STEP 7 projects. No `.s7p` project archive, simulator scene, complete symbol table, or hardware configuration was attached. Do not infer successful compilation or simulation from the presence of PDFs.

Original source mapping:

| Source | Published export |
| --- | --- |
| PLC-1.pdf | ladder/01_traffic_signals.pdf |
| PLC-2.pdf | ladder/02_height_based_box_sorting.pdf |
| plc-3.pdf | ladder/03_conveyor_actuator_sequence.pdf |
| PLC-4.pdf | ladder/04_motor_temperature_logic.pdf |

All four PDFs are preserved byte-for-byte. The relevant explanation pages (source pages 9-16) form the separate eight-page PLC report. Its original cover and combined contents page are omitted; attribution appears in `CREDITS.md`.

## Details to verify when a native project is available

- Interpret S5 timer values using the configured time base, and check the strict traffic-phase thresholds at equality boundaries.
- Confirm box-class boundaries, pusher front/back limit contacts, timer overlap, and counter reset behavior.
- Add the missing case-3 film/task description before assigning physical names to its unlabeled sensors/actuators.
- Resolve the case-4 FC105 high/low limit reversal relative to the prose. Confirm `BIPOLAR`, the analog input range, REAL versus DINT comparator operands, and how a command in `QD20` reaches an actual output channel.

No Ladder program was reconstructed or modified during repository preparation. Record the engineering environment, active configuration, input forcing, timing, and expected output sequence when adding a new simulation film.
