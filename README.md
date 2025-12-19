# 📅 출석 관리 시스템 (Attendance Management System)

> **동의과학대학교 컴퓨터소프트웨어과** > **개발자:** 최민재 (202520509)  
> **개발 기간:** 2025.01 ~ 2025.02

Java와 MySQL을 활용하여 기존 학사 관리 시스템의 복잡한 UI를 개선하고, 사용자 편의성을 극대화한 **효율적인 출결 관리 솔루션**입니다.

---

## 📺 Project Overview

| 로그인 화면 | 메인 대시보드 |
| :---: | :---: |
| <img width="379" height="187" alt="Image" src="https://github.com/user-attachments/assets/82adbcb3-7c9d-4c11-9304-848936d7f299" /> |<img width="937" height="326" alt="Image" src="https://github.com/user-attachments/assets/1016b061-f0a7-4de4-adb6-d018d1fc6b14" />](https://github.com/yoon202/JavaProject/issues/2#issue-3747477444)|
| **보안 인증 및 권한 관리** | **직관적인 데이터 현황판** |

---

## ✨ Key Features (주요 기능)

### 1. 사용자 맞춤형 권한 시스템
* **ADMIN (관리자):** 모든 데이터(학생, 교수, 강의, 출결)의 생성, 수정, 삭제 권한 부여
* **USER (사용자):** 배정된 강의 및 개인 출결 정보 조회 전용 모드

### 2. 효율적인 정보 관리 (CRUD)
* **학생 및 교수 관리:** 학번과 내부 고유 ID를 분리하여 데이터의 무결성 확보
* **강의 통합 관리:** 담당 교수 배정 및 강의 스케줄링 시스템 구축
* **일관된 UI/UX:** 모든 관리 탭에서 동일한 인터페이스를 제공하여 사용자의 학습 비용 최소화

### 3. 스마트 출결 시스템
* **조건별 검색:** 날짜별, 학생별 필터링을 통해 수많은 데이터 중 필요한 정보만 즉시 추출
* **데이터 영속성:** 학생의 인적 사항(이름, 학번 등)이 변경되어도 기존 출결 기록은 안전하게 유지

---

## 🗄 Database Design (DB 구조)

데이터 간의 유기적인 관계를 고려하여 정규화된 DB 설계를 적용했습니다.

<p align="center">
  <img src="images/erd.png" width="600">
</p>

* **`users`**: 시스템 접속 계정 및 관리자/사용자 권한 구분
* **`students` / `professors`**: 인적 사항 관리
* **`courses`**: 강의 정보와 담당 교수를 외래키(`professor_id`)로 연결
* **`attendance`**: 학생 정보와 연동된 출결 데이터 (이름 변경 시에도 기록 보존)

---

## 🛠 Tech Stack

- **Language:** Java (JDK 17)
- **Library:** Swing (GUI), JDBC
- **Database:** MySQL
- **IDE:** Eclipse

---

## 🚀 향후 개발 계획
- [ ] **알림 시스템:** 출결 누락 발생 시 실시간 푸시 알림
- [ ] **데이터 시각화:** 주차별/과목별 출석률 차트 도입
- [ ] **내보내기 기능:** 관리자용 출석 통계 리포트 (Excel/PDF) 출력

---

## 💡 개발 소감
"현장에서 느끼는 작은 불편함이 개발의 시작이었습니다. 클릭 횟수를 단 한 번이라도 줄여 사용자에게 편리함을 주는 것이 이 프로젝트의 핵심 목표였습니다."
