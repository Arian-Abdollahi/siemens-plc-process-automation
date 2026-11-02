# Two-direction traffic signals

The program uses a start/stop latch (`I0.0`, `I0.1`, `Q0.7`) and an `S_ODT` timer with `S5T#47S`. Timer information is written to `MW10` and compared with 270, 200, and 0 to select lamp groups.

| Intended stage in the report | Duration | Lamp group |
| --- | --- | --- |
| First direction | 20 s | Green 1 and Red 2 |
| Transition | 7 s | Yellow 1 and Yellow 2 |
| Second direction | 20 s | Red 1 and Green 2 |

The 47-second value is unambiguous in the ladder export; some Persian PDF text extraction reverses digit order. Verify the timer's integer/time-base interpretation and behavior at the strict comparison boundaries when reproducing the cycle. No conflict-free timing proof or new runtime test is claimed.

[Ladder export](../ladder/01_traffic_signals.pdf) · [Film slot](../videos/README.md)
