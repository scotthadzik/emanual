---
layout: popup
---

# DYNAMIXEL Protocol Compatibility Table

- More info about [DYNAMIXEL Protocol 1.0]
- More info about [DYNAMIXEL Protocol 2.0]

**Compatibility Legend**  
O : Compatible  
X : Incompatible  
\* : Configuration Required
{: .notice --info}

# [DYNAMIXEL](#dynamixel)

## AX Series

| Model  | DYNAMIXEL Protocol 1.0 | DYNAMIXEL Protocol 2.0 |
|:-------|:----------------------:|:----------------------:|
| AX-12W |           O            |           X            |
| AX-12A |           O            |           X            |
| AX-18A |           O            |           X            |

## MX Series

| Model  | DYNAMIXEL Protocol 1.0 | DYNAMIXEL Protocol 2.0 |
|:-------|:----------------------:|:----------------------:|
| MX-12W |           O            |           X            |
| MX-28  |           O            |           O*           |
| MX-64  |           O            |           O*           |
| MX-106 |           O            |           O*           |

{% capture notice_01 %}
**NOTE**: Read the following to ensure proper use.
- In order to use DYNAMIXEL Protocol 2.0 firmware version with MX series, proceed to **Firmware Recovery** via [DYNAMIXEL Wizard 2.0](/docs/en/software/dynamixel/dynamixel_wizard2/#firmware-recovery) or [R+ Manager 2.0](/docs/en/software/rplus2/manager/#firmware-recovery).
- DYNAMIXEL Protocol 2.0 is available with v39 Firmware version (or above). Proceed to **Firmware Update** via [DYNAMIXEL Wizard 2.0](/docs/kr/software/dynamixel/dynamixel_wizard2/#firmware-update) or [R+ Manager 2.0](/docs/en/software/rplus2/manager/#firmware-recovery).
- DYNAMIXEL Protocol 2.0 supports various Operating Modes, Secondary ID, Drive Mode, Bus Watchdog and etc.
{% endcapture %}
<div class="notice">{{ notice_01| markdownify }}</div>

{% capture info_01 %}
**INFO** : 
- MX(2.0) Firmware uses different control table and address from default MX firmware with DYNAMIXEL Protocol 1.0.
- MX(2.0) Firmware inherits DYNAMIXEL-X function.
{% endcapture %}
<div class="notice--info">{{ info_01| markdownify }}</div>

# DYNAMIXEL X

{% capture notice_01 %}
**NOTE** : 
- X-series can switch DYNAMIXEL Protocol 2.0 into DYNAMIXEL Protocol 1.0 aside from [XL320](/docs/en/dxl/x/xl320/)
- Refer to DYNAMIXEL Protocol Type(13) in control table of model of its DYNAMIXEL. 
{% endcapture %}
<div class="notice">{{ notice_01| markdownify }}</div>

## [XW Series](#xw-series)

| Model        | DYNAMIXEL Protocol 1.0  | DYNAMIXEL Protocol 2.0 |
|:-------------|:-----------------------:|:----------------------:|
| XW540-T140   | O* <br>(F/W address 13) |           O            |
| XW540-T260   | O* <br>(F/W address 13) |           O            |
| XW430-T333-R | O* <br>(F/W address 13) |           O            |
| XW430-T260-R | O* <br>(F/W address 13) |           O            |

## [XD Series](#xd-series)

| Model        | DYNAMIXEL Protocol 1.0  | DYNAMIXEL Protocol 2.0 |
|:-------------|:-----------------------:|:----------------------:|
| XD540-T270-R | O* <br>(F/W address 13) |           O            |
| XD540-T150-R | O* <br>(F/W address 13) |           O            |
| XD430-T350-R | O* <br>(F/W address 13) |           O            |
| XD430-T210-R | O* <br>(F/W address 13) |           O            |

## [XH Series](#xh-series)

| Model      | DYNAMIXEL Protocol 1.0  | DYNAMIXEL Protocol 2.0 |
|:-----------|:-----------------------:|:----------------------:|
| XH430-W210 | O* <br>(F/W address 13) |           O            |
| XH430-W350 | O* <br>(F/W address 13) |           O            |
| XH430-V210 | O* <br>(F/W address 13) |           O            |
| XH430-V350 | O* <br>(F/W address 13) |           O            |
| XH540-W150 | O* <br>(F/W address 13) |           O            |
| XH540-W270 | O* <br>(F/W address 13) |           O            |
| XH540-V150 | O* <br>(F/W address 13) |           O            |
| XH540-V270 | O* <br>(F/W address 13) |           O            |

## [XM Series](#xm-series)

| Model      | DYNAMIXEL Protocol 1.0  | DYNAMIXEL Protocol 2.0 |
|:-----------|:-----------------------:|:----------------------:|
| XM430-W210 | O* <br>(F/W address 13) |           O            |
| XM430-W350 | O* <br>(F/W address 13) |           O            |
| XM540-W150 | O* <br>(F/W address 13) |           O            |
| XM540-W270 | O* <br>(F/W address 13) |           O            |

## [XC Series](#xc-series)

| Model       | DYNAMIXEL Protocol 1.0  | DYNAMIXEL Protocol 2.0 |
|:------------|:-----------------------:|:----------------------:|
| XC430-W150  | O* <br>(F/W address 13) |           O            |
| XC430-W240  | O* <br>(F/W address 13) |           O            |
| 2XC430-W250 | O* <br>(F/W address 13) |           O            |
| XC330-T181  |            X            |           O            |
| XC330-T288  |            X            |           O            |
| XC330-M181  |            X            |           O            |
| XC330-M288  |            X            |           O            |

## [XL Series](#xl-series)

| Model       | DYNAMIXEL Protocol 1.0  | DYNAMIXEL Protocol 2.0 |
|:------------|:-----------------------:|:----------------------:|
| XL-320      |            X            |           O            |
| XL330-M288  |            X            |           O            |
| XL330-M077  |            X            |           O            |
| XL430-W250  | O* <br>(F/W address 13) |           O            |
| 2XL430-W250 | O* <br>(F/W address 13) |           O            |

# [DYNAMIXEL PRO](#dynamixel-pro)

## [H Series](#h-series)

| Model        | DYNAMIXEL Protocol 1.0 | DYNAMIXEL Protocol 2.0 |
|:-------------|:----------------------:|:----------------------:|
| H42-20-S300  |           X            |           O            |
| H54-100-S500 |           X            |           O            |
| H54-200-S500 |           X            |           O            |

## [M Series](#m-series)

| Model       | DYNAMIXEL Protocol 1.0 | DYNAMIXEL Protocol 2.0 |
|:------------|:----------------------:|:----------------------:|
| M42-10-S260 |           X            |           O            |
| M54-40-S250 |           X            |           O            |
| M54-60-S250 |           X            |           O            |

## [L Series](#l-series)

| Model         | DYNAMIXEL Protocol 1.0 | DYNAMIXEL Protocol 2.0 |
|:--------------|:----------------------:|:----------------------:|
| L54-50-S500-R |           X            |           O            |
| L54-50-S290-R |           X            |           O            |
| L54-30-S500-R |           X            |           O            |
| L54-30-S400-R |           X            |           O            |
| L42-10-S300-R |           X            |           O            |

# [P Series](#p-series)

## [PH Series](#ph-series)

| Model           | DYNAMIXEL Protocol 1.0 | DYNAMIXEL Protocol 2.0 |
|:----------------|:----------------------:|:----------------------:|
| PH54-200-S500-R |           X            |           O            |
| PH54-100-S500-R |           X            |           O            |
| PH42-020-S300-R |           X            |           O            |

## [PM Series](#pm-series)

| Model           | DYNAMIXEL Protocol 1.0 | DYNAMIXEL Protocol 2.0 |
|:----------------|:----------------------:|:----------------------:|
| PM54-060-S250-R |           X            |           O            |
| PM54-040-S250-R |           X            |           O            |
| PM42-010-S260-R |           X            |           O            |

# [ETC](#etc)

| Model                |    DYNAMIXEL Protocol 1.0    |    DYNAMIXEL Protocol 2.0     |
|:---------------------|:----------------------------:|:-----------------------------:|
| RoboPlus 1.0 Suite   |              O               |   X* (XL-320 and PRO only)    |
| R+ Manager 2.0       |              O               |               O               |
| R+ Task 2.0          |              O               |               O               |
| R+ Motion 2.0        |              O               |               O               |
| R+ Design            |              O               |               O               |
| DYNAMIXEL Wizard 2.0 |              O               |               O               |
| ROBOTIS OP2          |              O               | O* <br>(Requires F/W Upgrade) |
| ROBOTIS OP3          |              X               |               O               |
| ROBOTIS STEM         |              O               |               X               |
| BIOLOID Premium      |              O               |               X               |
| TurtleBot3 Burger    |    O*<br>(F/W address 13)    |               O               |
| TurtleBot3 WafflePi  |    O*<br>(F/W address 13)    |               O               |
| RH-P12-RN            |              X               |               O               |
| Manipulator-H        |              X               |               O               |
| THORMANG3            |              X               |               O               |
| OpenManipulator-X    |    O*<br>(F/W address 13)    |               O               |
| CM-530               |              O               |               X               |
| CM-550               |              X               |               O               |
| CM-700               |              O               |               X               |
| OpenCM9.04           |  O*<br>(Library-dependent)   |   O*<br>(Library-dependent)   |
| OpenCM485 EXP        | O <br>(Controller-dependent) |  O<br>(Controller-dependent)  |
| OpenCR1.0            |  O*<br>(Library-dependent)   |   O*<br>(Library-dependent)   |

[DYNAMIXEL Protocol 1.0]: /docs/en/dxl/protocol1/
[DYNAMIXEL Protocol 2.0]: /docs/en/dxl/protocol2/
