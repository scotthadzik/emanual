제어기와 통신하기 위한 통신 속도 입니다.

| 값     | 통신 속도     |
| :-------: | :-----------: |
|8|10.5M|
|7|4.5M|
|6|4M|
|5|3M|
|4|2M|
|3|1M|
|2|115,200|
|1(기본값)|57,600|
|0|9,600|

**참고** : UART는 Baudrate 오차가 3 [%] 이내이면 통신에 지장이 없습니다.
{: .notice}

**참고**: U2D2을 이용 시, 높은 통신 Baud rate에서 안정적인 통신을 위해서는 [USB 포트의 응답지연시간(Latency)](/docs/kr/software/dynamixel/dynamixel_wizard2/#포트-응답-속도-설정) 을 낮춰주세요. 
{: .notice}
