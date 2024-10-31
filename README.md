# 클라우드 게이밍 시스템 개발

## 팀원 소개
<div align="left">
  <table>
  <tr>
    <td align="center">
      이수빈
    </td>    
    </td>
    <td align="center">
      이다은 
    </td>
    <td align="center">
      이지민
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/02ggang9">
        <img src="https://github.com/02ggang9.png" width="80" alt="02ggang9"/>
        <br/>
        <sub><b>02ggang9@gmail.com</b></sub>
      </a>
      <br/>
    </td>
    <td align="center">
      <a href="https://github.com/llddang">
      <img src="https://github.com/llddang.png" width="80" alt="llddang"/>
      <br />
      <sub><b>laliddang@gmail.com</b></sub>
      </a>
      <br/>
    </td>
    <td align="center">
      <a href="https://github.com/JJimini">
      <img src="https://github.com/JJimini.png" width="80" alt="JJimini"/>
      <br />
      <sub><b>min102602@naver.com</b></sub>
      </a>
      <br/>
    </td>
  </tr>
      <tr>
    <td align="center">
      Infra
    </td>    
    <td align="center">
      Frontend, Unity
    </td>
    <td align="center">
      Backend, Database
    </td>
  </tr>
  </table>
</div>

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


### 프론트엔드 서버

`npm run start` 명령어를 통해 로컬 개발 서버를 실행합니다.

### 백엔드 서버(Spring Boot)

Spring Boot 백엔드 서버는 `./mvnw spring-boot:run` 명령어를 통해 실행합니다. 프로젝트 디렉토리 내에서 실행해야 하며, 정상 실행 여부는 로그로 확인합니다.

### 데이터베이스 서버(PostgreSQL)

PostgreSQL 데이터베이스 서버를 Docker로 설정합니다. 필요한 환경 변수는 다음과 같습니다:
- `POSTGRES_USER`: 데이터베이스 사용자 이름
- `POSTGRES_PASSWORD`: 데이터베이스 비밀번호
- `POSTGRES_DB`: 생성할 데이터베이스 이름

Docker를 통해 컨테이너를 생성하고 실행합니다.

### 유니티 게임 렌더링

Unity Hub를 사용하여 GitHub에서 클론한 프로젝트를 연 다음, 구글 STUN 서버(`stun:stun.l.google.com:19302`)를 이용해 Render Streaming URL을 설정합니다. Unity Hub에서 렌더링 시작 버튼을 클릭하여 스트리밍을 시작합니다.

## 4. 소개 및 시연 영상
### 1. 홈
![홈화면](https://github.com/user-attachments/assets/6de33f60-8fb8-45b9-97e5-e8fbfbab60f9)

사용자는 언제든지 웹 브라우저를 통해 서비스에 접속하여 게임을 실행할 수 있다.

### 2. 회원가입
![회원가입 화면](https://github.com/user-attachments/assets/3a4b5c69-3df5-4749-8b28-503d78ddd14f)

사용자는 닉네임, 비밀번호를 형식에 맞게 입력한 후 회원가입을 할 수 있다.

### 3. 로그인
![로그인 화면](https://github.com/user-attachments/assets/eeaf4fb6-01cf-4e43-ab32-fe887f2ea0db)

사용자는 회원가입한 계정으로 로그인할 수 있다. 

로그인 결과 반환되는 정보를 localStorage에 저장하여 다시 접속했을 때에도 로그인 정보가 남아있도록 하였다.

### 4. 게임 플레이
![게임플레이화면](https://github.com/user-attachments/assets/1f63c05c-4d77-4b9a-ba55-476a19023943)

WebRTC를 통해 스트리밍 되는 게임 영상을 받을 수 있다. 

전체 화면 버튼을 클릭하여 여백없는 화면으로 게임을 실행할 수도 있다.

### 5. 랭킹
![랭킹화면](https://github.com/user-attachments/assets/49aeefd9-9d31-49f9-a3e3-7f92698a7f89)

사용자가 게임을 클리어한 시간에 따른 순위를 볼 수 있다.

### 6. 영상
[![2024년 전기 졸업과저 30 Tree](https://github.com/user-attachments/assets/a6963421-c98e-4ec6-a6d1-0de552c65a97)](https://www.youtube.com/watch?v=HeQP4ZvuC5g&list=PLFUP9jG-TDp-CVdTbHvql-WoADl4gNkKj&index=30&pp=iAQB)
