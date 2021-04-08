# HP 538xA frequency counter OCXO adapter board

This project allows a cheap CTI OSC5A2B02 to be installed in an HP 5384A, 
5385A or 5386A frequency counter instead of the original crystal or TCXO 
reference.

![Render 1](images/render-1.png)
![Render 2](images/render-2.png)

## Notes

Status: BETA

KiCad project will be uploaded here eventually but Gerbers only for now.

## BOM

| Reference | Part |
| -- | -- |
| C1-6 | 0805 100nF 50V X7R MLCC |
| L1 | 1812 1.2uH >800mA i.e. Murata LQH43NH1R2K03L |
| O1 | CTI OSC5A2B02 |
| U1 | MAX6064BEUR+T |
| RV1 | 5K Bourns 3296Y vertical |
| J1-4 | standard 2.54mm header pins (8 needed in total) |

## Construction

1. Obtain the parts.
2. Install C1-6
3. Install L1
4. Install U1
5. Install J1-4 so they stick out from the bottom.
6. Remove the plastic spacers off 4 more pins and push onto the protruding pins to raise the height of the board from the host counter.
7. Install RV1
8. Orient the board SMD parts facing you, text upright and apply 5v to the top right (+) and middle right pins (-)
9. Measure voltage at U1/C6 junction. Should be approx 4V
10. Install O1.
11. Reconnect 5v supply and validate current < 600mA and > 300mA.
12. Wait for current to reduce to < 300mA. OCXO should be warm.
13. Orient the board SMD parts facing you, text upright and connect scope to bottom right pin and ground. Validate 10MHz square wave. Approx 5v p-p.

## Installation

TBD

## Adjustment

TBD

## Reference documentation

* [CTI OSC5A2B02 datasheet](data/cti-osc5a2b02-datasheet.pdf)
* [CTI OSC5A2B02 drawings](data/cti-osc5a2b02-drawing.jpg)
* [MAX6064 datasheet](data/max606x-datasheet.pdf)