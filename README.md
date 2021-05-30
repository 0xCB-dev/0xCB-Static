# 0xcb-static
## 40% with OLED and Encoder running QMK

Licence | OSHWA | Tindie
:-------------------------:|:-------------------------:|:-------------------------:
![](https://github.com/0xCB-dev/0xcb-static/blob/main/LICENSE.svg) | [![](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev3.0/OSHWA.svg)](https://certification.oshwa.org/de000113.html) | <a href="https://www.tindie.com/stores/0xcb/?ref=offsite_badges&utm_source=sellers_conorlburns&utm_medium=badges&utm_campaign=badge_large"><img src="https://d2ss6ovg47m0r5.cloudfront.net/badges/tindie-larges.png" alt="I sell on Tindie" width="200" height="104"></a>

#### Flashing

* `qmk clone`
* `cd qmk_firmware`
* `export LTO=Y` (if you compile production files)
* To go to bootloader hold the RESET switch, then hold the BOOT switch, release RESET, release BOOT.
The board should now appear in lsusb (or device manager).
* `make 0xcb/static:via:flash`

### PCB:
KiCad 5.99
[Schematic](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev1.0/Schematic_Static.pdf)

Top | Bottom
:-------------------------:|:-------------------------:
![](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev1.0/top.png)  |  ![](https://github.com/0xCB-dev/0xcb-static/blob/main/PCB/rev1.0/bottom.png)

#### BOM:
|Qty|Reference(s)|Value                  |Part Nb.              |
|---|------------|-----------------------|----------------------|
|2  |C1, C2      |0.1uF                  |C277965               |
|2  |C3, C4      |20pF                   |C254096               |
|48 |D1 -D50     |1N4148                 |C14538                |
|2  |D46, D47    |1N4729                 |C2532                 |
|1  |F1          |500mA                  |C268799               |
|1  |J1          |USB_C_Receptacle_USB2.0|2073-USB4085-GF-ACT-ND|
|37 |MX1 – MX44  |MX-NoLED               |Cherry MX switches    |
|1  |MX12        |EC11                   |ec11 encoder          |
|1  |OL1         |OLED                   |SSD1306 128x32        |
|2  |R1, R2      |5.1K                   |C58676                |
|2  |R3, R4      |75                     |C713897               |
|1  |R5          |10k                    |C58673                |
|1  |R6          |1.5k                   |C433494               |
|1  |SW1         |RESET                  |C127509               |
|1  |SW2         |BOOT                   |C127509               |
|1  |U1          |ATmega328-P            |C613508               |
|1  |Y1          |16MHz                  |C16212                |