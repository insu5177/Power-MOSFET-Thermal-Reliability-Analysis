# Power-MOSFET-Electro-Thermal-Protection-Analysis
## 프로젝트 배경

기존 프로젝트에서 Python을 활용하여 MOSFET의 기본적인 전기적 특성과 비이상성을 분석하였다.

이후 실제 Power MOSFET에서는 온도 변화가 전기적 특성 및 신뢰성에 영향을 줄 수 있다는 점에 관심을 가지게 되었다.

또한 EV Trend Korea에서 Power Semiconductor 근처에 온도센서를 배치하여
열전달 경로를 줄이고 온도 추종성을 개선하는 기술을 확인하였다.

이를 바탕으로 센서의 배치 및 열응답 경로 차이가
MOSFET의 온도 검지 정확도와 과열 보호 성능에 미치는 영향을 분석하고자 한다.

## 선행 프로젝트

- [MOSFET Id-Vgs 및 gm 분석](https://github.com/insu5177/MOSFET_IdVgs_Analysis)
- [MOSFET Subthreshold 분석](https://github.com/insu5177/MOSFET_NonIdeal_IdVgs_Analysis)

## 프로젝트 아이디어

EV Trend Korea에서 Murata의 Power Semiconductor 온도센싱 Responsiveness Test를 확인하였다.

MOSFET 근처에 배치된 FTN이 Conventional Thermistor보다 MOSFET 온도를
더 빠르고 가깝게 추종하는 경향을 확인하였으며, 이를 프로젝트의 문제 정의에 활용하였다.

※ 현장 촬영 자료는 프로젝트 Motivation 용도로만 사용하며,
정량 모델 파라미터는 공식 Datasheet 및 기술자료를 기준으로 설정한다.

## 프로젝트 진행 방향

MOSFET 온도 의존성
↓
전력손실 및 Junction Temperature
↓
센서 배치/열경로에 따른 온도 추종
↓
Protection / Throttling
↓
과열 보호 성능 평가

## 분석 대상 소자

 Infineon의 **IAUTN12S5N018T** Si Power MOSFET을 분석 대상으로 선정

- N-channel Si Power MOSFET
- OptiMOS™ 5 기술
- 최대 Drain-Source Voltage: 120 V
- 최대 RDS(on): 1.8 mΩ
- 최대 Junction Temperature: 175°C

### 선정 이유

기존 MOSFET Id-Vgs 및 Subthreshold 분석과 자연스럽게 연결할 수 있는 실제 Si MOSFET이며,
Datasheet에서 온도에 따른 Id-Vgs, Vth, RDS(on) 및 Thermal Impedance 정보를 제공하여
온도 의존 특성과 열적 신뢰성을 분석하기에 적합하다고 판단하였다.