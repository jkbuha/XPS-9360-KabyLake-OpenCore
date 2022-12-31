# Dell XPS 9360 macOS Monterey with OpenCore

# Details

| OpenCore Version | 0.8.7 |
| --- | --- |
| macOS Version | 12.6.2 (Monterey) |
| SMSBios | MacBookPro15,2 |

# Hardware Specifications

| Hardware | Specification | Status |
| --- | --- | --- |
| CPU | Intel Core i7-7500U | ✅ Working |
| RAM | LPDDR3 16GB | ✅ Working |
| Audio | Realtek ALC3246 | ✅ Working |
| WiFi | Dell DW1515 | ✅ Working |
| Bluetooth | Dell DW1515 | ✅ Working |
| SSD | Crucial P5 2TB | ✅ Working |
| Keyboard | UK Layout | ✅ Working |
| Trackpad | I2C Connection | ✅ Working |
| Webcam | Dell HD camera | ✅ Working |
| MicroSD Card | Standard Card Reader | ✅ Working |
| S3 | Sleep/Wake | ✅ Working |
| GPU | Intel HD620 | ✅ Working |
| eGPU | AMD Sapphire Radeon RX580 | ✅ Working |
| Display | 1920 x 1200 FHD LCD | ✅ Working |

# Overview

This is an updated configuration of one of the most hackintoshable Dell 
machines, the XPS 9360. Still going strong after 6 years, with a battery 
life >8h (with FHD), this is a solid workhorse that needs minimal 
maintenance.

# BIOS Settings
Will be provided shortly.

# UEFI IFR edits
Using your favourite UEFI editor, you will need to make the relevant changes below as required:

```bash
setup_var
Undervolt CPU: 0x653-> 0x4B (offset by 75mV)
Undervolt -ve: 0x655-> 0x01
Undervolt GPU: 0x85A-> 0x4B
Undervolt -ve: 0x85C-> 0x01
Undervolt GPU: 0x863-> 0x4B
Undervolt -ve: 0x865-> 0x01
Undervolt UNC: 0x852-> 0x4B
Undervolt -ve: 0x854-> 0x01

Disable CFG  : 0x4DE-> 0x00
Enable OC    : 0x64D-> 0x01
Enable XTU   : 0x64E-> 0x01

DVMT 192MB   : 0x785-> 0x06
DVMT MAX     : 0x786-> 0x03

CTDP boot max: 0x4DF-> 0x02

```

# Known Issues
None

