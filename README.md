<div align="center">
  <img width="256" height="256" alt="BootTalk Logo" src="https://github.com/user-attachments/assets/6379e114-262b-4b98-89ee-5b4c355dd83a" />
  <h1>BootTalk</h1>
  <p>부트캠프 정보 탐색 & 수료생 리뷰 + 커피챗 커뮤니티 플랫폼</p>
  
  <p>
    <a href="https://github.com/너의유저네임/bootTalk-backend">
      <img src="https://img.shields.io/badge/Backend%20Repo-181717?style=for-the-badge&logo=github&logoColor=white" alt="Backend Repo">
    </a>
    <!-- 프론트 repo 있으면 추가 -->
    <!-- <a href="..."><img src="https://img.shields.io/badge/Frontend%20Repo-181717?style=for-the-badge&logo=github&logoColor=white"></a> -->
  </p>
</div>

## 목차
- [서비스 소개](#서비스-소개)
- [기술 스택](#기술-스택)
- [핵심 기능](#핵심-기능)
- [기술적 특징](#기술적-특징)
- [ERD](#erd)
- [시스템 아키텍처](#시스템-아키텍처)
- [서비스 시연 영상](#서비스-시연-영상)
- [제작 기간 및 참여 인원](#제작-기간-및-참여-인원)

## 서비스 소개

BootTalk은 **부트캠프/국비지원 과정 정보 부족**과 **후기 신뢰성 문제**를 해결하기 위해 만들어진 플랫폼입니다.  
고용24 OpenAPI를 활용한 **자동 데이터 수집**, **수료 인증 기반 리뷰 시스템**, **실시간 커피챗(채팅+알림)** 을 핵심으로 예비 수강생의 합리적인 선택을 돕습니다.

주요 목표  
- 최신 부트캠프 정보 자동 업데이트  
- 실제 수료생의 신뢰할 수 있는 리뷰 제공  
- 현업자/수료생과의 1:1 커피챗으로 직접 소통

## 기술 스택
<img src="https://img.shields.io/badge/Java_17-007396?style=for-the-badge&logo=openjdk&logoColor=white"> <img src="https://img.shields.io/badge/Spring_Boot_3.4-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white"> <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white">  
<img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> <img src="https://img.shields.io/badge/QueryDSL-0769AD?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/Spring_Batch-6DB33F?style=for-the-badge&logo=spring&logoColor=white">

### Database & Cache
<img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white">

### Real-time
<img src="https://img.shields.io/badge/WebSocket(STOMP)-010101?style=for-the-badge&logo=socketdotio&logoColor=white"> <img src="https://img.shields.io/badge/SSE-010101?style=for-the-badge&logoColor=white">

### Infra & DevOps
<img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white"> <img src="https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">

### Tools
<img src="https://img.shields.io/badge/IntelliJ_IDEA-000000?style=for-the-badge&logo=intellijidea&logoColor=white"> <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white"> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black">

## 핵심 기능

### 1. 네이버 소셜 로그인 & JWT 인증
<img width="800" src="https://github.com/user-attachments/assets/9cf79d6c-c829-49cf-a0b1-c476b72eb18f" />

### 2. 부트캠프 정보 자동 수집 & 업데이트  
Spring Batch + Quartz Scheduler로 매일 고용24 OpenAPI 데이터 수집 (약 1,200건 이상 유지)  
<img width="800" src="https://github.com/user-attachments/assets/97f81f25-8504-4004-bed1-4909d872e7f4" />

### 3. 복합 조건 검색 & 자동완성  
QueryDSL 동적 쿼리로 지역/카테고리/평점/기간/키워드 필터링 지원  
<img width="800" src="https://github.com/user-attachments/assets/e945423c-a3bb-4473-9495-5e9f9e716219" />  
<img width="800" src="https://github.com/user-attachments/assets/e850b313-2fe3-4631-89ec-945313708842" />

### 4. 수료 인증 기반 리뷰 시스템  
AWS S3 이미지 업로드 + 인증 로직  
<img width="800" src="https://github.com/user-attachments/assets/9a4e2309-e10c-4589-85d8-116f08f88d08" />

### 5. 실시간 커피챗 & 채팅  
WebSocket(STOMP) 채팅 + SSE 실시간 알림  
<img width="800" src="https://github.com/user-attachments/assets/550e8fd3-1c70-4b56-bdc9-866503eb3e60" />  
<img width="800" src="https://github.com/user-attachments/assets/1b486125-7dde-4564-abad-610861604e3a" />

## 기술적 특징
- **Spring Batch** 기반 고용24 API 배치 수집 (Cron 스케줄링, Tasklet/Chunk 혼합)  
- **QueryDSL**로 10가지 이상 복합 조건 동적 쿼리 구현  
- **WebSocket + STOMP**로 양방향 실시간 채팅  
- **SSE**로 신청/승인/메시지 알림 실시간 푸시  
- **Spring Security + JWT**로 인증/인가 관리

## ERD
수료 인증, 리뷰, 커피챗 신청·채팅·알림 중심 엔티티 관계 (2025.04 기준)  
<img src="https://github.com/user-attachments/assets/9a74be90-e3b2-471b-b073-3273f56dbd38" />

## 시스템 아키텍처
Docker 멀티 컨테이너 + AWS EC2 배포, WebSocket/SSE 실시간 통신 구조  
<img src="https://github.com/user-attachments/assets/d24e6be1-4bb9-43e0-9c41-b4332634cd31" />

## 서비스 시연 영상

https://www.youtube.com/watch?v=B4xHVZl11Qc

## 제작 기간 및 참여 인원

**기간** : 2025.03.17 ~ 2025.04.23 (6주)  

| 이름     | 역할                  | 주요 담당 기능                              |
|----------|-----------------------|---------------------------------------------|
| 조성현   | 백엔드 / 팀장         | 부트캠프 데이터 수집·배치, 리뷰 시스템, 인증 |
| 박태영   | 백엔드                | 사용자·알림(SSE)                            |
| 신주연   | 백엔드                | 커피챗 신청·수신                            |
| 이건우   | 백엔드                | 커피챗 일정·채팅(WebSocket)                 |
