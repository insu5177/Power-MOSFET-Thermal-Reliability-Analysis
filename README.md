# Power-MOSFET-Electro-Thermal-Protection-Analysis
## 프로젝트 배경

기존 프로젝트에서 Python을 활용하여 MOSFET의 기본적인 전기적 특성과 비이상성을 분석하였다.

이후 실제 Power MOSFET에서는 온도 변화가 전기적 특성 및 신뢰성에 영향을 줄 수 있다는 점에 관심을 가지게 되었다.

또한 EV Trend Korea에서 Power Semiconductor 근처에 온도센서를 배치하여 열응답성을 개선하는 기술을 보고, 센서의 응답 차이가 MOSFET의 보호 성능에 미치는 영향을 분석하고자 한다.

## 선행 프로젝트

- [MOSFET Id-Vgs 및 gm 분석](https://github.com/insu5177/MOSFET_IdVgs_Analysis)
- [MOSFET Subthreshold 분석](https://github.com/insu5177/MOSFET_NonIdeal_IdVgs_Analysis)

## 프로젝트 진행 방향

MOSFET 온도 의존성

↓

전력손실 및 Junction Temperature

↓

온도센서 열응답

↓

Protection / Throttling

↓

신뢰성 평가

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