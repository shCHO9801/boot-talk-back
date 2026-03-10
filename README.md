<div align="center">
<img width="256" height="256" alt="image" src="https://github.com/user-attachments/assets/6379e114-262b-4b98-89ee-5b4c355dd83a" />
</div>

# BootTalk : 부트캠프 정보 탐색 및 커뮤니티 서비스

## 목차
- [서비스 소개](#서비스-소개)
- [기술 스택](#기술-스택)
- [기획 배경](#기획-배경)
- [핵심 기능](#핵심-기능)
- [기술적 특징](#기술적-특징)
- [ERD](#erd)
- [시스템 아키텍처](#시스템-아키텍처)
- [서비스 시연 영상](#서비스-시연-영상)
- [제작 기간 및 참여 인원](#제작-기간-및-참여-인원)

---

# 서비스 소개

BootTalk은 부트캠프 및 국비 교육 과정 정보를 탐색하고,  
수료생의 실제 경험을 기반으로 리뷰와 커피챗 기능을 제공하는 플랫폼입니다.

부트캠프 선택 과정에서 발생하는 정보 부족과 후기 신뢰성 문제를 해결하고,  
수료생 및 현업자와 직접 소통할 수 있는 환경을 제공하여  
예비 교육생이 더 합리적인 선택을 할 수 있도록 돕는 것을 목표로 합니다.

BootTalk은 다음과 같은 기능을 제공합니다.

- 수료 인증 기반 리뷰 시스템
- 수료생 및 현업자와의 1:1 커피챗
- 검색 및 필터 기능을 통한 부트캠프 탐색

---

# 기술 스택

<div align="center">

### Backend
<img src="https://img.shields.io/badge/java-17-007396?style=for-the-badge&logo=openjdk&logoColor=white">
<img src="https://img.shields.io/badge/spring%20boot-3.4.4-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
<img src="https://img.shields.io/badge/spring%20security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white">
<img src="https://img.shields.io/badge/jwt-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white">
<br>
<img src="https://img.shields.io/badge/jpa-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
<img src="https://img.shields.io/badge/querydsl-0769AD?style=for-the-badge&logoColor=white">
<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/redis-DC382D?style=for-the-badge&logo=redis&logoColor=white">
<br>
<img src="https://img.shields.io/badge/spring%20batch-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
<img src="https://img.shields.io/badge/websocket-010101?style=for-the-badge&logo=socketdotio&logoColor=white">
<img src="https://img.shields.io/badge/swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black">

### Infra
<img src="https://img.shields.io/badge/aws%20ec2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white">
<img src="https://img.shields.io/badge/aws%20s3-569A31?style=for-the-badge&logo=amazons3&logoColor=white">
<img src="https://img.shields.io/badge/docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">

### Tools
<img src="https://img.shields.io/badge/intellij%20idea-000000?style=for-the-badge&logo=intellijidea&logoColor=white">
<img src="https://img.shields.io/badge/postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white">
<img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
<img src="https://img.shields.io/badge/notion-000000?style=for-the-badge&logo=notion&logoColor=white">

</div>

---

# 기획 배경

부트캠프와 국비 교육 과정이 다양해지면서  
학습자는 어떤 과정을 선택해야 할지 판단하기 어려운 상황에 놓이게 되었습니다.

과정 소개 페이지나 홍보 자료만으로는 실제 수강 경험이나 만족도를 확인하기 어렵고,  
수료생의 실제 경험을 참고하거나 직접 질문할 수 있는 창구도 부족합니다.

이에 BootTalk은 다음과 같은 문제를 해결하기 위해 기획되었습니다.

- 부트캠프 정보 탐색
- 수료생 리뷰 기반 정보 제공
- 커피챗을 통한 직접적인 소통

---

# 핵심 기능

### 소셜 로그인 및 인증

네이버 OAuth 2.0 기반 소셜 로그인과 JWT 기반 인증 구조를 적용하였습니다.

<img width="800" src="https://github.com/user-attachments/assets/3bc595a4-3329-4604-a356-e7d20be2cfa6" />

---

### 부트캠프 정보 자동 등록

Spring Batch를 활용하여 외부 API 기반 부트캠프 정보를 자동으로 수집하고 등록하는 배치 시스템을 구축하였습니다.

<img width="800" src="https://github.com/user-attachments/assets/97f81f25-8504-4004-bed1-4909d872e7f4" />

---

### 부트캠프 검색 및 필터

지역, 카테고리, 평점, 기간 등의 조건을 기반으로 부트캠프를 검색하고 탐색할 수 있습니다.

부트캠프 필터링 조회

<img width="800" src="https://github.com/user-attachments/assets/99139c55-3362-42bc-a6b0-77b218617d57" />

부트캠프 자동완성 검색

<img width="800" src="https://github.com/user-attachments/assets/2784b9c4-3490-4a62-9607-f627d811c996" />

---

### 커피챗 멘토 탐색

사용자는 관심 있는 멘토를 조회하고 커피챗을 신청할 수 있습니다.

<img width="800" src="https://github.com/user-attachments/assets/c2c2103d-5616-4f86-80f0-8695b60562cd" />

---

### 실시간 채팅 및 알림

WebSocket 기반 채팅과 SSE 기반 알림을 통해 사용자 간 실시간 상호작용을 제공합니다.

멘토-멘티 간 실시간 채팅

<img width="800" src="https://github.com/user-attachments/assets/308ec404-bbf5-40cb-b4e9-96c32c8deb39" />

실시간 알림

<img width="800" src="https://github.com/user-attachments/assets/a284155e-64e6-478c-a16d-4c72f62bda30" />

<img width="484" src="https://github.com/user-attachments/assets/81ac2b62-736e-4421-bea7-5f887e5b3b63" />

---

### 이미지 업로드

AWS S3를 활용하여 리뷰 및 인증 이미지 업로드 기능을 구현하였습니다.

<img width="800" src="https://github.com/user-attachments/assets/73575c93-1a6b-4563-a877-5b6fcf39d1e9" />

---

# 기술적 특징

### Spring Batch 기반 부트캠프 데이터 수집

외부 고용24 API를 통해 부트캠프 데이터를 수집하는 배치 시스템을 구현하였습니다.  
정기적으로 데이터를 수집하여 최신 부트캠프 정보를 유지하도록 구성하였습니다.

### QueryDSL 기반 검색

지역, 카테고리, 평점, 기간, 키워드 등 복합 조건 검색을 처리하기 위해 QueryDSL을 적용하였습니다.

### SSE 기반 실시간 알림

커피챗 신청 및 상태 변경 등의 이벤트를 실시간으로 전달하기 위해 SSE(Server-Sent Events)를 적용하였습니다.

### WebSocket 기반 채팅

WebSocket(STOMP)을 활용하여 멘토와 멘티 간 실시간 채팅 기능을 구현하였습니다.

### 인증 및 보안

Spring Security와 JWT 기반 인증 구조를 적용하여 API 접근 권한을 관리하였습니다.

---

# ERD

<img src="https://github.com/user-attachments/assets/9a74be90-e3b2-471b-b073-3273f56dbd38">

---

# 시스템 아키텍처

<img src="https://github.com/user-attachments/assets/d24e6be1-4bb9-43e0-9c41-b4332634cd31">

---

# 서비스 시연 영상

https://www.youtube.com/watch?v=B4xHVZl11Qc

---

# 제작 기간 및 참여 인원

### 제작 기간

2025.03.17 ~ 2025.04.23 (6주)

### 참여 인원

| **조성현** | **박태영** | **신주연** | **이건우** |
| :------: | :------: | :------: | :------: |
| 백엔드 | 백엔드 | 백엔드 | 백엔드 |
| 부트캠프 / 리뷰 | 유저 / 알림 | 커피챗 신청 / 수신 | 커피챗 정보 / 일정 관리 / 채팅 |
