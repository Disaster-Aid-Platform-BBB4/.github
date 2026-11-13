# 🚒 삐뽀삐4 (B4B4)

### 재난의 골든타임을 지킨다, “모두가 함께”

개인(IND) · 공공기관(GOV) · 민간단체(NGO)를 하나로 연결하는 **실시간 재난 긴급 지원 플랫폼**

## 📌 서비스 소개 (Service Overview)

**“삐뽀삐4”** 는 재난 발생 직후부터 복구·지원까지 모든 단계를 아우르는 통합 플랫폼입니다.

한 개인의 신고가 공공기관과 민간단체를 움직이고, 봉사자들은 안전하게 조직되어 현장으로 향합니다.

👉 **우리의 목표**는 기술로 사람을 연결하고 생명을 구하는 것입니다.

## 📌 주요 기능 (Key Features)

### ⚪ 인증 / 인가

- JWT 기반 로그인 / 회원가입
- AccessToken + RefreshToken 구조
- Redis 기반 RefreshToken 저장 및 재발급
- Role 기반 접근 제어 (IND, GOV, NGO)

### ⚪ 위치

- 사용자 주변 nkm 반경 내 재난 히트맵 표시
- 사용자 근처 대피소 정보 제공 (카카오 맵 연동)

### ⚪ 신고

- 재난 신고 등록 기능
- Kafka 기반 실시간 알림 → 공공기관 전달
- 신고 상태 관리 (PENDING → RECEIVED → CLOSED)
- 신고 목록 및 상세 조회
- Kafka DLQ 기반 실패/예외 처리

### ⚪ 봉사

- 민간단체: 봉사 모집글 생성 / 수정 / 조회
- 개인: 모집글 참가 / 취소
- Redis Lua Script 기반 실시간 팀 인원 관리 (INCR/DECR)
- 중복 및 정원 초과 방지
- Kafka + DLQ 기반 재처리

### ⚪ 알림

- FCM 디바이스 토큰 등록
- 재난 신고 실시간 알림 (관할 공공기관 → 푸시 전송)
- 동일 유형 신고 다수 발생 시 전국 단위 알림 전송
- 봉사 모집글 수정 시 신청자 대상 알림
- 사용자별 수신 알림 조회 (최대 30건)

## 📌 기술 스택 (Tech Stack)

- ### Backend
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot%203.x-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-%2302303A.svg?style=for-the-badge&logo=Gradle&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-%230769AD.svg?style=for-the-badge&logoColor=white)

- ### Security
![Spring Security](https://img.shields.io/badge/Spring%20Security-%236DB33F.svg?style=for-the-badge&logo=springsecurity&logoColor=white)
![JWT](https://img.shields.io/badge/json%20web%20tokens-%23000000.svg?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

- ### DB & ORM
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![PostGIS](https://img.shields.io/badge/PostGIS-%233982CE.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/redis%207.0-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![ElastiCache](https://img.shields.io/badge/Amazon%20ElastiCache-%23C925D1.svg?style=for-the-badge&logo=amazonelasticache&logoColor=white)

- ### Message Broker
![Apache Kafka](https://img.shields.io/badge/apachekafka-%23231F20.svg?style=for-the-badge&logo=apachekafka&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/rabbitmq-%23FF6600.svg?style=for-the-badge&logo=rabbitmq&logoColor=white)

- ### Real-Time
![WebSocket](https://img.shields.io/badge/websocket-%23010101.svg?style=for-the-badge&logo=socketdotio&logoColor=white)
![Firebase Cloud Messaging](https://img.shields.io/badge/firebase%20cloud%20messaging-%23DD2C00.svg?style=for-the-badge&logo=firebase&logoColor=white)

- ### Infra
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-%23FF9900.svg?style=for-the-badge&logo=amazonec2&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-%23569A31.svg?style=for-the-badge&logo=amazons3&logoColor=white)

- ### Collaboration
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-%234A154B.svg?style=for-the-badge&logo=slack&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)
![ERDCloud](https://img.shields.io/badge/ERDCloud-%233B82F6.svg?style=for-the-badge&logoColor=white)
<br><br>

## 📌 아키텍처 (Cloud Architecture)

### V1
<img width="500" alt="v1" src="https://github.com/user-attachments/assets/2d46c801-5818-4d77-9d9a-8a674c6243d8" />

### V2
<img width="500" alt="v2" src="https://github.com/user-attachments/assets/19630c2e-e16b-4010-8ae1-8b3e3b7b37f8" />

## 📌 ERD (Full Database Schema)
<img width="400" alt="erd" src="https://github.com/user-attachments/assets/0e4f4d2d-60fb-4470-855c-47c5150d8858" />

## 📌 API 명세서 (API Documentation)

- 📍 [API Docs](https://app.notion.com/p/API-2721e5c0190780b7b11bef3256ee1cae?__dm_a=1)

## 📌 화면 구성 (Screens Overview)

### ⚪ App 화면 (일반사용자 전용)

- **회원가입 화면**
<img width="180" alt="1" src="https://github.com/user-attachments/assets/217d74df-d26d-4a54-b6be-e9b10b835d5a" />

- **로그인 화면**
<img width="180" alt="2" src="https://github.com/user-attachments/assets/05419368-c69d-4bdd-b13c-51ec46246ae2" />
  
- **홈 화면 (대피소)**
<img width="180" alt="3" src="https://github.com/user-attachments/assets/d3bf5c12-8979-4e44-be83-bcb85306d0fa" />
  
- **홈 화면 (재난정보)**
<img width="180" alt="4" src="https://github.com/user-attachments/assets/38d74fb4-2bb8-4899-9c65-9ea8d8a2ec96" />
  
- **신고하기 화면**
<img width="180" alt="5" src="https://github.com/user-attachments/assets/9374bd99-1abb-4e30-a349-b57be389aca1" />
  
- **자원봉사 화면**
<img width="180" alt="6" src="https://github.com/user-attachments/assets/736e2547-8efc-498a-afeb-7f0f8ced1e09" />

- **자원봉사 신청 화면**
<img width="180" alt="7" src="https://github.com/user-attachments/assets/777e4d94-2fde-46f0-8c91-44c06f978ce6" />
  
- **나의 활동 화면**
<img width="180" alt="8" src="https://github.com/user-attachments/assets/15dd54e8-b0ec-40b1-ac21-d92cb19aefdc" />
  
- **내 신고 목록 화면**
<img width="180" alt="9" src="https://github.com/user-attachments/assets/d59ab254-3d61-4042-bfc0-a49c514298f2" />
  
- **자원봉사 신청내역 화면**
<img width="180" alt="10" src="https://github.com/user-attachments/assets/75bf1e38-00c9-412f-bed9-a2126237b033" />
  
- **알림 내역 화면**
<img width="180" alt="11" src="https://github.com/user-attachments/assets/5153b045-e27e-42aa-8e34-c4c0f97d41b4" />
<img width="180" alt="12" src="https://github.com/user-attachments/assets/122e17a0-70d2-42ee-8542-f20eeb84ad5b" />
  
- **FCM 알림**
<img width="180" alt="13" src="https://github.com/user-attachments/assets/8428185c-5d3f-431e-b458-4d591ae433b7" />
<img width="180" alt="14" src="https://github.com/user-attachments/assets/ec4e5402-7ae5-4af1-981e-dc201afbc8a6" />
<img width="180" alt="15" src="https://github.com/user-attachments/assets/e154376d-e929-4f2f-baa0-2d60f20c82a3" />

### ⚪ Web 화면 (공공기관, 민간봉사단체 전용)

- **회원가입 화면**
<img width="450" alt="16" src="https://github.com/user-attachments/assets/70f009f1-a315-4047-bad7-918349f12acc" />
<img width="450" alt="17" src="https://github.com/user-attachments/assets/b6f293b7-3ad8-445a-9184-6511b00b1ada" />
<img width="1910" height="984" alt="36" src="https://github.com/user-attachments/assets/848f83f0-db53-4a82-98e9-6354a5a2f779" />

  
- **로그인 화면**
<img width="450" alt="18" src="https://github.com/user-attachments/assets/aeb5e306-0b58-4ba0-a32b-f2b364632d60" />

- **홈 화면 (공공기관)**
<img width="450" alt="19" src="https://github.com/user-attachments/assets/d8f26407-16fd-4f3a-b84d-c51285f28290" />
  
- **신고 목록 화면 (공공기관)**
<img width="450" alt="20" src="https://github.com/user-attachments/assets/55bef510-701e-4522-8b67-0284837035be" />
  
- **신고 상세 화면 (공공기관)**
<img width="450" alt="21" src="https://github.com/user-attachments/assets/b704191b-060e-40a5-ae6f-16607fa8030e" />
<img width="450" alt="22" src="https://github.com/user-attachments/assets/2c4369d4-de1b-4b18-a6e9-eca941f66fd2" />
  
  
- **지도 화면 (공공기관)**
<img width="450" alt="23" src="https://github.com/user-attachments/assets/d8dd5323-0dc6-4f66-a352-b66068d49eea" />
<img width="450" alt="24" src="https://github.com/user-attachments/assets/01d79e67-6347-49d2-a2e1-a97db9d98037" />
<img width="450" alt="25" src="https://github.com/user-attachments/assets/74eea558-7ab0-42d8-aa5b-b480de0fe2a5" />

- **봉사활동 게시글 관리 화면 (민간봉사단체)**
<img width="450" alt="26" src="https://github.com/user-attachments/assets/e8e8da8d-572a-4ceb-8aad-da121448b085" />
  
- **봉사모집 게시글 작성 화면 (민간봉사단체)**
<img width="450" alt="27" src="https://github.com/user-attachments/assets/d2327955-dff1-4835-b35a-ab70ecc2c024" />
<img width="450" alt="28" src="https://github.com/user-attachments/assets/db05dfa4-ed5b-4d47-b5c7-29a5fc495a46" />
<img width="450" alt="29" src="https://github.com/user-attachments/assets/9a2f177c-c63a-4dcd-a794-71a7507cf4ef" />
<img width="450" alt="30" src="https://github.com/user-attachments/assets/826442a8-ef69-412b-9477-5d476f10e67a" />

  
- **봉사활동 상세정보 화면 (민간봉사단체)**
<img width="450" alt="31" src="https://github.com/user-attachments/assets/aae88a86-4b27-439f-bc78-7d6af3f43682" />
<img width="450" alt="32" src="https://github.com/user-attachments/assets/7025dce4-4d6a-47b7-b364-57df820ff4ad" />
<img width="450" alt="33" src="https://github.com/user-attachments/assets/091484d3-e7e8-496d-b212-b4f07b4205ec" />
<img width="450" alt="34" src="https://github.com/user-attachments/assets/30f5c903-4981-4802-96c1-f28766787380" />

  
- **FCM 알림**
<img width="200" alt="35" src="https://github.com/user-attachments/assets/7272ab6b-c5fa-4b91-8deb-a893f76cc73a" />









