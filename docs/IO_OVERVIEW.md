# I/O overview from the printed ladder exports

Addresses are **local to each independent case**. Reuse of an address between cases does not imply the same physical connection.

| Case | Inputs | Outputs / data | Internal elements |
| --- | --- | --- | --- |
| Traffic signals | I0.0 start; I0.1 stop | Q0.0 red 1; Q0.1 yellow 1; Q0.2 green 1; Q0.4 red 2; Q0.5 yellow 2; Q0.6 green 2; Q0.7 run latch | T0, M0.1, MW10 |
| Box sorting | ID30 height; I0.2/I0.3/I0.4 box detections; I1.0/I1.1/I1.2 front limits; I1.3 reset; further back-limit contacts in diagrams | Q0.0 conveyor/run indication; Q0.5 M pusher; Q0.6 L pusher; Q0.7 P pusher; QD30/QD34/QD38 count values | M0.2/M0.3/M0.4; T0/T1/T2/T3; C0/C1/C2 |
| Conveyor/actuator sequence | I0.0/I0.1 start/stop; sensor contacts I0.2-I0.6 | Q0.0-Q0.4 sequence outputs; Q0.7 run latch | T0, C0, MW10, M0.0/M0.1/M0.3 |
| Motor/temperature logic | I0.0 start; I0.1 stop-count trigger; I0.2 counter reset; IW10 analog input | Q0.0/Q0.1 motor paths; QD20 command; MD20 scaled value; MW12 return value | C0, T0, MW10, M0.0/M0.1 |

This table is a navigation aid, not a substitute for the original symbol table, signal wiring, module configuration, or ladder connectivity. Contact inversion and edge behavior must be read from the diagrams and checked in the native engineering environment.
