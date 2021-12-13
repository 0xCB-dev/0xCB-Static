# 0xcb-static
## 40% with OLED and Encoder running QMK

Licence | OSHWA | Tindie
:-------------------------:|:-------------------------:|:-------------------------:
![](https://github.com/0xCB-dev/0xcb-static/blob/main/LICENSE.svg) | [![](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev1.0/OSHWA.svg)](https://certification.oshwa.org/de000114.html) | <a href="https://www.tindie.com/stores/0xcb/?ref=offsite_badges&utm_source=sellers_conorlburns&utm_medium=badges&utm_campaign=badge_large"><img src="https://d2ss6ovg47m0r5.cloudfront.net/badges/tindie-larges.png" alt="I sell on Tindie" width="200" height="104"></a>

#### Flashing

* `qmk clone`
* `cd qmk_firmware`
* `export LTO=Y`
* To go to bootloader hold the ESC key while plugging in (or RESET switch, then hold the BOOT switch, release RESET, release BOOT).
The board should now appear in lsusb (or device manager).
* `make 0xcb/static:via:flash`

### Assembly:

You can use the [humanpnp](https://files.0xcb.dev/0xCB/static/humanpnp.html) to easily place components.

### PCB:
KiCad 5.99
[Schematic](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev1.0/Schematic-Static.pdf)

Top | Bottom
:-------------------------:|:-------------------------:
![](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev1.0/top.png)  |  ![](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev1.0/bottom.png)

#### BOM:
| References     | Value          | Quantity |Part Nb.             |
|----------------|----------------|----------|---------------------|
| C3, C4         | 20pF           | 2        |C415398              |
| C1, C2         | 0.1uF          | 2        |C409821              |
| R1, R2         | 5.1K           | 2        |C58676               |
| R3, R4         | 75             | 2        |C713897              |
| R5             | 10k            | 1        |C58673               |
| R6             | 1.5k           | 1        |C433494              |
| D1, ..., D48   | 1N4148         | 48       |C14516               |
| D49, D50       | 1N4729         | 2        |C2532                |
| U1             | ATmega328-P    | 1        |ATMEGA328P-PU-ND     |
| Y1             | 16MHz          | 1        |C16212               |
| F1             | 500mA          | 1        |C268799              |
| SW1, SW2       | RESET, BOOT    | 1        |450-1650-ND          |
| MX1, ..., MX44 | MX-NoLED       | 43       |Cherry MX switches   |
| OL1            | OLED           | 1        |SSD1306 128x32       |
| MX12           | EC11           | 1        |PEC11R-4220F-S0024-ND|
| J1             | USB4085 Type C | 1        |640-USB4085-GF-A     |
