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

### V2

## 📌 ERD (Full Database Schema)

## 📌 API 명세서 (API Documentation)

- 📍 API Docs
- 📍 Postman

## 📌 화면 구성 (Screens Overview)

### ⚪ App 화면 (일반사용자 전용)

- **회원가입 화면**
- **로그인 화면**
- **홈 화면 (대피소)**
- **홈 화면 (재난정보)**
- **신고하기 화면**
- **자원봉사 화면**
- **자원봉사 신청 화면**
- **나의 활동 화면**
- **내 신고 목록 화면**
- **자원봉사 신청내역 화면**
- **알림 내역 화면**
- **FCM 알림**

### ⚪ Web 화면 (공공기관, 민간봉사단체 전용)

- **회원가입 화면**
- **로그인 화면**
- **홈 화면 (공공기관)**
- **신고 목록 화면 (공공기관)**
- **신고 상세 화면 (공공기관)**
- **지도 화면 (공공기관)**
- **봉사활동 게시글 관리 화면 (민간봉사단체)**
- **봉사모집 게시글 작성 화면 (민간봉사단체)**
- **봉사활동 상세정보 화면 (민간봉사단체)**
- **FCM 알림**
