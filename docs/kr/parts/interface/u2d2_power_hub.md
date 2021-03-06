---
layout: archive
lang: kr
ref: u2d2_power_hub
read_time: true
share: true
author_profile: false
permalink: /docs/kr/parts/interface/u2d2_power_hub/
sidebar:
  title: U2D2 파워 허브 보드
  nav: "u2d2_power_hub"
---

# [개요](#개요)
U2D2와 결합하여, 여러 종류의 외부 전원을 연결하여 다이나믹셀에 안정적으로 전력을 공급해주는 역할을 한다.

![](/assets/images/parts/interface/u2d2_power_hub/product_image.png)

# [제품 사양](#제품-사양)

|   항목    |     사양      |
|:---------:|:-------------:|
| 동작 전압 | 3.5 V ~ 24.0 V |
| 최대 전류 |     10.0 A     |

# [각 부 명칭](#각-부-명칭)

![](/assets/images/parts/interface/u2d2_power_hub/layout.png)

## [설명](#설명)

1. **DYNAMIXEL Connectors**: TTL 및 RS-485 통신을 위해, 3핀 및 4핀 JST 커넥터 사용. (**[커넥터 정보](#커넥터-정보)** 확인하기)

2. **TTL / RS485 Test Points**: TTL의 Data 라인, RS485의 D+, D- 라인의 신호를 확인할 수 있도록 별도의 Test Points 가 제공된다.

3. **Power Connectors**: U2D2 PHB는 다양한 전원을 제공 하기위해 3종류의 커넥터를 지원한다.  
    - SMPS DC Connector (2.5mm ID / 5.5mm OD, **[Center Positive](https://en.wikipedia.org/wiki/Polarity_symbols)**)
    - MOLEX Power connector (**[커넥터 정보](#커넥터-정보)** 확인하기)
    - PCB Screw Terminal Block Connector
      - 좌측: -
      - 우측: +

{% capture caution_01 %}
**주의**: 
- 터미널 블록 (PCB Screw Terminal Block Connector)을 사용할때에는, 반드시 극성에 유의할것. 
- 보드 뒷면에 여러가지 핀들이 노출되어 있으므로, 밑면에 도체가 닿을 위험을 어느 정도 차단하기 위해, [조립 예시](#조립-예시)를 참고하여 제공된 서포터를 결합시키는 것을 권장한다. 
{% endcapture %}
<div class="notice--warning">{{ caution_01 | markdownify }}</div>

# [조립 예시](#조립-예시)

1. 네 개의 플라스틱 서포터를 `U2D2 파워 허브 보드`의 각 모퉁이에 조립한다.  

    ![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_06.jpg)

2. 플라스틱 리벳을 사용해서 `U2D2`를 `U2D2 파워 허브 보드`에 조립한다.

    ![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_07.jpg)

3. `U2D2`와 `U2D2 파워 허브 보드`를 연결하기 위해 3P 또는 4P 케이블을 그림과 같이 연결한다 (3P와 4P 케이블을 동시에 사용할 수 있음).

    ![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_03.jpg)

4. `다이나믹셀`과 `U2D2`를 연결하기 위한 별도의 케이블을 연결한다 (다이나믹셀 모델에 따라 변환케이블이 필요할 수 있음).

    ![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_04.jpg)

5. 케이블의 반대쪽을 `다이나믹셀`에 연결한다 (다이나믹셀 모델에 따라 변환케이블이 필요할 수 있음).

    ![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_05.jpg)

6. `U2D2 파워 허브 보드`에 전원을 연결한다.

    **경고** : 양쪽 전원 입력단자를 동시에 사용하지 마시오. 한번에 한 개의 입력단자만 사용할 것.
    {: .notice--danger}

    **주의** : 전원을 공급하기 전에 다이나믹셀의 권장 전압을 확인할 것.
    {: .notice--warning}

    ![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_01.jpg)![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_02.jpg)

7. 다이나믹셀에 전원을 공급하려면 `U2D2 파워 허브 보드`의 전원 스위치를 켠다.

    ![](/assets/images/parts/interface/u2d2_power_hub/u2d2_phb_08.jpg)

## [커넥터 정보](#커넥터-정보)

{% include kr/dxl/jst_485_ttl.md %}
