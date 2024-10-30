## 1. 프로젝트 소개
### 1.1. 배경 및 필요성
클라우드 게이밍(Cloud Gaming)은 게임을 클라이언트에 설치하지 않고 스트리밍을 통해 게임을 제공하는 방식이다. 사용자는 네트워크를 통해 서버에서 처리된 게임 영상을 전송받아 게임을 즐길 수 있다. 최근 고성능 게임에 대한 요구가 증가하고 있으며, 다양한 기기에서 게임을 실행하려는 수요가 늘면서 클라우드 게이밍은 빠르게 성장하는 분야가 되었다. 클라우드 게이밍은 사용자가 장치 성능으로 부터 받는 영향을 최소화하고 고화질, 고사양의 게임을 즐길 수 있는 장점을 제공한다. 


### 1.2. 목표 및 주요 내용
본 과제의 목표는 클라우드 게이밍 성능을 최적화하고 사용자에게 다양한 환경에서 안정적인 서비스를 제공하는 것이다. Unity Render Streaming 기술을 활용하여 서버에서 실시간으로 고화질의 게임 영상을 렌더링하고 스트리밍한다. 이를 통해 클라이언트 장치의 하드웨어 성능과 운영체제에 영향을 받지 않고 고품질의 게임 경험을 제공할 수 있다. 또한 그래픽 처리 부담을 서버로 이전하여 일관된 게임 품질을 유지할 수 있도록 한다. 

WebRTC(Web Real-Time Communication)를 사용하여 실시간 게임 데이터의 전송 및 스트리밍을 개선한다. 이를 통해 지연 시간을 최소화하고 게임 플레이의 반응성을 향상시킨다. 클라우드 게임에서 중요한 성능 요소인 지연 시간을 줄이기 위해 위의 기술을 통합적으로 활용하여 실시간 데이터 전송 지연을 최소화하는 것을 목표로 한다. 


## 2. 상세 설계

### 2.1. 시스템 구성도
![시스템 구성도](https://github.com/user-attachments/assets/b03f4f9b-33b0-41e0-bf5e-91b0c03183ac)

### 2.2. 사용 기술
**Infra**
- Terraform - v1.9.8
- Kubernetes - v1.31.1
- Prometheus - v2.47.0
- Grafana - v10.1.2

**Front**
- Node - v20.11.0

**Unity**
- Unity - v2022.3.28f1

**Backend**
- Spring boot - v3.3.4
- Spring Webflux - v6.1.13
- Spring Security - v6.3.3
- R2DBC - v1.0.5
- PostgreSQL - v14

## 3. 설치 및 사용 방법
172.171.134.176 접속

## 4. 소개 및 시연 영상

[![2024년 전기 졸업과저 30 Tree](https://github.com/user-attachments/assets/a6963421-c98e-4ec6-a6d1-0de552c65a97)](https://www.youtube.com/watch?v=HeQP4ZvuC5g&list=PLFUP9jG-TDp-CVdTbHvql-WoADl4gNkKj&index=30&pp=iAQB)

## 팀 소개
이수빈, 02ggang9@gmail.com 인프라 구축

이다은, laliddang@gmail.com 프론트, Unity 개발

이지민, min102602@naver.com 백엔드 개발, DB 구축
