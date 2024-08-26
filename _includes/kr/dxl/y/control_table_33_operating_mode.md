제어 모드를 설정할 수 있습니다. DYNAMIXEL-Y는 3가지 제어모드를 지원합니다.

| 값        | 동작 모드           | 설명                                                                                                                                         |
|:----------|:--------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| 0         | 전류 제어 모드      | 전류를 제어합니다. 속도와 위치는 제어하지 않습니다.                                                                                          |
| 1         | 속도 제어 모드      | 속도와 전류를 제어합니다. 위치는 제어하지 않습니다.                                                                                          |
| 3(기본값) | 위치 제어 모드      | 위치, 속도 그리고 전류를 제어합니다. [Max Position Limit(76)], [Min Position Limit(84)]에 의해서 동작 범위가 제한됩니다                            | 

각 제어 모드별 제어기 블록다이어그램은 아래와 같습니다.

#### [전류 제어 모드](#전류-제어-모드)
![](/assets/images/dxl/y/operating_mode_1.PNG)

#### [속도 제어 모드](#속도-제어-모드)
![](/assets/images/dxl/y/operating_mode_2.PNG)

#### [위치 제어 모드](#위치-제어-모드)
![](/assets/images/dxl/y/operating_mode_3.PNG)

**참고:** DYNAMIXEL-Y는 Multi-turn이 저장됩니다. **Extended Position Mode가 별도로 없으며, Position Mode에서도 Multi-turn으로 회전이 가능**합니다. 전원을 끄고 켜거나, Reboot Instruction 사용, 전원이 꺼진 상태에서 외력으로 회전시켜도 Multi-turn이 감지되며 절대 위치가 유지되고, Clear Instruction을 통해서 Multi-turn을 ‘0’으로 초기화 할 수 있습니다.
{: .notice}