---
layout: archive
lang: kr
ref: rx-24f
read_time: true
share: true
author_profile: false
permalink: /docs/kr/dxl/rx/rx-24f/
sidebar:
  title: RX-24F
  nav: "rx-24f"
product_group: dxl_rx
---

![](/assets/images/dxl/rx/rx-24f_product.png)

> RX-24F

**WARNING** : RX-24F 은 현재 단종되어 더 이상 판매되지 않습니다.
{: .notice--warning}

# [주요 사양](#주요-사양)

| 항목           | 내용     |
| :------------- | :------------- |
| 무게 | 67g |
| 크기 | 35.6mm x 50.6mm x 35.5mm |
| 최소 제어각 | 0.29&deg;  |
| 모터 | Coreless|
| 기어비 | 193 : 1  |
| Stall Torque | 2.6 [N.m] (at 12V, 2.4A) |
| 무부하 속도 | 126rpm (at 12V) |
| 동작 모드| 관절 모드 (0&deg; ~ 300&deg;) / 바퀴 모드(무한 회전)|
| 동작 온도   | -5&deg;C ~ +80&deg;C |
| 사용 전압| 9 ~ 12V (**권장 전압 : 11.1V**) |
| 제어 명령 | Digital Packet |
| 프로토콜 타입 | Half Duplex Asynchronous Serial Communication<br />(8bit, 1stop, No Parity) |
| 통신 연결  | RS485 Multi Drop Bus(Daisy Chain Type Connector) |
| ID |254 ID (0~253)|
| 피드백 | Position, Temperature, Load, Input Voltage 등 |
| 재질 | Full Metal Gear, Engineering Plastic Body |
| 대기 전류 | 50mA |

**주의**: Stall Torque 는 순간적으로 낼수있는 최대정지토크를 의미합니다.실제 구동을 위해 로봇을 설계하신다면 Stall Torque의 1/5 이하의 로드가 걸리도록 설계하셔야 안정적인 움직임이 가능합니다.
{: .notice}

{% include kr/dxl/warning.md %}

{% include kr/dxl/control_table.md %}

## [EEPROM 영역](#eeprom-영역)

| 주소     | 크기(Byte)     | 명칭     | 의미    | 접근     | 기본값  |
| :---------: | :-----------:  | :----------- | :------------ | :--------: | :------------: |
|0|2|[Model Number](#model-number)         | 모델 번호      | R       | 24 |
|2|1|[Firmware Version](#firmware-version)    |펌웨어 버전 정보|R|-|
|3|1|[ID](#id)                  |다이나믹셀 ID      |RW|1|
|4|1|[Baud Rate](#baud-rate)           |다이나믹셀 통신 속도|RW|34|
|5|1|[Return Delay Time](#return-delay-time)   |응답 지연 시간|RW|250|
|6|2|[CW Angle Limit](#cw-angle-limit)          |시계 방향 한계 각도 |RW|0|
|8|2|[CCW Angle Limit](#ccw-angle-limit)          |반시계 방향 한계 각도 |RW|1023|
|11|1|[Temperature Limit](#temperature-limit)   |내부 한계 온도|RW|80|
|12|1|[Min Voltage Limit](#min-voltage-limit)   |최저 한계 전압|RW|60|
|13|1|[Max Voltage Limit](#max-voltage-limit)   |최고 한계 전압|RW|190|
|14|2|[Max Torque](#max-torque)           |토크 한계 |RW|1023|
|16|1|[Status Return Level](#status-return-level)      |응답 레벨|RW|2|
|17|1|[Alarm LED](#alarm-led)                             |알람용 LED 기능|RW|36|
|18|1|[Shutdown](#shutdown)            |알람용 셧 다운(Shut down) 기능|RW|36|


## [RAM 영역](#ram-영역)

| 주소     | 크기(Byte)     | 명칭    | 의미     | 접근    | 기본값   |
| :---------: | :------------: | :----------- | :------------- | :--------: | :--------------: |
|24|1|[Torque Enable](#torque-enable)            |토크 켜기|RW|0|
|25|1|[LED](#led)                             |LED On/Off|RW|0|
|26|1|[CW Compliance Margin](#cw-compliance-margin)   |CW Compliance Margin|RW|1|
|27|1|[CCW Compliance Margin](#ccw-compliance-margin)   |CCW Compliance Margin|RW|1|
|28|1|[CW Compliance Slope](#cw-compliance-slope)   |CW Compliance Slope|RW|32|
|29|1|[CCW Compliance Slope](#ccw-compliance-alope)   |CCW Compliance Slope|RW|32|
|30|2|[Goal Position](#goal-position)                 |목표 위치 |RW|-|
|32|2|[Moving Speed](#moving-speed)             |목표 속도 |RW|-|
|34|2|[Torque Limit](#torque-limit)            |토크 한계 |RW|Max Torque|
|36|2|[Present Position](#present-position)     |현재 위치 |R|-|
|38|2|[Present Speed](#present-speed)           |현재 속도 |R|-|
|40|2|[Present Load](#present-load)             |현재 하중 |R|-|
|42|1|[Present Voltage](#present-voltage)       |현재 전압|R|-|
|43|1|[Present Temperature](#present-temperature)|현재 온도|R|-|
|44|1|[Registered](#registered)                 |Instruction의 등록 여부|R|0|
|46|1|[Moving](#moving)                   |움직임 유무|R|0|
|47|1|[Lock](#lock)                   |EEPROM 잠금|RW|0|
|48|2|[Punch](#punch)                   |Punch |RW|32|


## [컨트롤 테이블 설명](#컨트롤-테이블-설명)

### <a name="model-number"></a>**[Model Number (0)](#model-number-0)**
다이나믹셀의 모델 번호입니다.

### <a name="firmware-version"></a>**[Firmware Version (2)](#firmware-version-2)**
다이나믹셀 펌웨어 버전입니다.

### <a name="id"></a>**[ID (3)](#id-3)**
{% include kr/dxl/control_table_id.md %}

### <a name="baud-rate"></a>**[Baud Rate (4)](#baud-rate-4)**
{% include kr/dxl/control_table_baudrate.md %}

### <a name="return-delay-time"></a>**[Return Delay Time (5)](#return-delay-time-5)**
{% include kr/dxl/control_table_return_delay_time.md %}

### <a name="cw-angle-limit"></a><a name="ccw-angle-limit"></a>**[CW/CCW Angle Limit(6, 8)](#cwccw-angle-limit6-8)**
{% include kr/dxl/control_table_angle_limit.md %}

### <a name="temperature-limit"></a>**[Temperature Limit (11)](#temperature-limit-11)**
{% include kr/dxl/control_table_temp_limit.md %}

### <a name="min-voltage-limit"></a><a name="max-voltage-limit"></a>**[Min/Max Voltage Limit (12, 13)](#minmax-voltage-limit-12-13)**
{% include kr/dxl/control_table_volt_limit_rx.md %}

### <a name="max-torque"></a>**[Max Torque (14)](#max-torque-14)**
{% include kr/dxl/control_table_max_torque.md %}

### <a name="status-return-level"></a>**[Status Return Level (16)](#status-return-level-16)**
{% include kr/dxl/control_table_status_return_lv.md %}

### <a name="alarm-led"></a><a name="shutdown"></a>**[Alarm LED(17), Shutdown(18)](#alarm-led17-shutdown18)**
{% include kr/dxl/control_table_shutdown.md %}

### <a name="torque-enable"></a>**[Torque Enable (24)](#torque-enable-24)**
{% include kr/dxl/control_table_torque_enable.md %}

### <a name="led"></a>**[LED (25)](#led-25)**
{% include kr/dxl/control_table_led.md %}

### <a name="cw-compliance-margin"></a><a name="ccw-compliance-margin"></a>**[Compliance Margin (26, 27)](#compliance-margin-26-27)**
{% include kr/dxl/control_table_compliance_margin.md %}

### <a name="cw-compliance-slope"></a><a name="ccw-compliance-slope"></a>**[Compliance Slope (28, 29)](#compliance-slope-28-29)**
{% include kr/dxl/control_table_compliance_slope.md %}

### <a name="goal-position"></a>**[Goal Position (30)](#goal-position-30)**
{% include kr/dxl/control_table_dx_goal_position.md %}

### <a name="moving-speed"></a>**[Moving Speed (32)](#moving-speed-32)**
{% include kr/dxl/control_table_moving_speed.md %}

### <a name="torque-limit"></a>**[Torque Limit (34)](#torque-limit-34)**
{% include kr/dxl/control_table_torque_limit.md %}

### <a name="present-position"></a>**[Present Position (36)](#present-position-36)**
{% include kr/dxl/control_table_potentio_present_position.md %}

### <a name="present-speed"></a>**[Present Speed (38)](#present-speed-38)**
{% include kr/dxl/control_table_present_speed.md %}

### <a name="present-load"></a>**[Present Load (40)](#present-load-40)**
{% include kr/dxl/control_table_present_load.md %}

### <a name="present-voltage"></a>**[Present Voltage (42)](#present-voltage-42)**
{% include kr/dxl/control_table_present_volt.md %}

### <a name="present-temperature"></a>**[Present Temperature (43)](#present-temperature-43)**
{% include kr/dxl/control_table_present_temp.md %}

### <a name="registered-instruction"></a>**[Registered Instruction (44)](#registered-instruction-44)**
{% include kr/dxl/control_table_reg_instruction.md %}

### <a name="moving"></a>**[Moving (46)](#moving-46)**
{% include kr/dxl/control_table_moving.md %}

### <a name="lock"></a>**[Lock (47)](#lock-47)**
{% include kr/dxl/control_table_lock.md %}

### <a name="punch"></a>**[Punch (48)](#punch-48)**
{% include kr/dxl/control_table_punch.md %}

# [조립 예시](#조립-예시)

+ FR07-B1 Option Frame

  ![](/assets/images/dxl/rx/rx-28_of-28b.png)

+ FR07-H1 Option Frame

  ![](/assets/images/dxl/rx/rx-28_of-28h.png)

+ FR07-S1 Option Frame

  ![](/assets/images/dxl/rx/rx-28_of-28s.png)

+ FR07-B101 Option Frame

  ![](/assets/images/dxl/rx/rx-28_fr07-b101.png)

+ FR07-F101, FR07-X101 Option Frame

  ![](/assets/images/dxl/rx/rx-28_fr07-f101_fr07-x101.png)

+ FR07-H101 Option Frame

  ![](/assets/images/dxl/rx/rx-28_fr07-h101.png)

+ FR07-S101 Option Frame

  ![](/assets/images/dxl/rx/rx-28_fr07-s101.png)

+ HN07-N1 Horn

  ![](/assets/images/dxl/rx/rx-28_hn07-n1.png)

+ HN07-I1 Horn

  ![](/assets/images/dxl/rx/rx-28_hn07-i1.png)

+ HN07-T1 Horn

  ![](/assets/images/dxl/rx/rx-28_hn07-t1.png)

+ HN07-N101 Horn

  ![](/assets/images/dxl/rx/rx-28_hn07-n101.png)

+ HN07-I101 Horn

  ![](/assets/images/dxl/rx/rx-28_hn07-i101.png)

+ HN07-T101 Horn

  ![](/assets/images/dxl/rx/rx-28_hn07-t101.png)

+ 기구결합 : 아래는 옵션 프레임과 혼을 이용한 결합구조의 예입니다.

  ![](/assets/images/dxl/rx/rx-10_combinations.png)

# [유지보수](#유지보수)

{% include kr/dxl/horn_bearing_replacement.md %}

# [참고자료](#참고자료)

**주의**: [호환성 가이드]{: .blank}
{: .notice}

## [커넥터 정보](#커넥터-정보)
{% include kr/dxl/molex_485.md %}

## [도면](#도면)

{% include kr/dxl/download_center_notice.md %}

{% include kr/dxl/485_ttl_connection.md %}

[호환성 가이드]: http://www.robotis.com/service/compatibility_table.php?cate=d
{% include kr/dxl/common_link.md %}
