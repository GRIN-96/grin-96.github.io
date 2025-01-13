---
title: "🍃 12 Factors"
description: "12 Factors"
date: 2025-01-13 23:59
update: 2025-01-13 23:59
tags:
  - MSA
  - Microservice
  - Spring Cloud
series: "🍃 Microservice와 Spring Cloud"
---

> **Cloud Native Application 개발을 위한 12가지 원칙**
>

## 1.  CODEBASE

- 코드베이스는 **Git 저장소 하나로 관리**
- 여러 환경(개발/테스트/운영)은 **동일한 코드에서 분기(branch)하여 관리**
- 한 코드베이스 = 하나의 애플리케이션

## 2.  DEPENDENCY

- 애플리케이션 내에서 종속성을 해결
- 컨테이너화된 환경에서는 **의존성이 포함된 Docker 이미지 사용**

## 3. CONFIGURATIONS

- 시스템 코드 외부에서 구성 관리 도구를 통해 마이크로 서비스에 필요한 작업들을 제어
- 환경 변수(ENV)로 설정 관리

## 4. LINKABLE BACKING SERVICES

- DB, Redis, S3 등의 백엔드 서비스는 독립적인 리소스로 취급( 의존성 제거 )
- 언제든지 교체 가능하도록 **환경 변수 기반 연결**

## 5. STAGES OF CREATION

- 빌드, 릴리즈, 실행 단계를 분리하여 배포
- 각각 고유한 아이디를 태그로 가져야함
- 롤백 기능 제공
- CI / CD 를 통한 자동화 구축 필요

## 6. STATELESS PROCESSES

- 각각의 마이크로 서비스는 분리된 채 독립적으로 운영
- 필요한 자원이 있다면 캐시, 데이터 저장소를 통해 외부와 교환

## 7. PORT BINDING

- 각 서비스가 HTTP 요청을 직접 처리하며, 필요에 따라 Nginx나 API Gateway를 통해 라우팅만 처리
- 마이크로서비스는 **독립적인 프로세스**로 실행되며, 각 서비스가 고유한 포트를 바인딩

## 8. CONCURRENCY

- 마이크로서비스 + 컨테이너 조합
- Kubernetes, Docker Swarm을 사용한 **자동 확장 지원**
- 단일 애플리케이션 인스턴스 대신 여러 인스턴스를 실행.

## 9. DISPOSABILITY

- 애플리케이션은 몇 초 내로 시작 가능해야 하며, SIGTERM 신호를 받아 정상 종료 가능해야 함
- 서비스 인스턴스 삭제가 가능해야함

## 10. DEVELOPMENT & PRODUCTION PARITY

- 개발 단계와 프로덕션 단계를 구분
- 개발, 스테이징, 운영 환경 간의 격차를 줄이고, 최대한 유사한 환경에서 애플리케이션을 개발, 테스트 및 배포

## 11. LOGS

- 애플리케이션은 로그를 파일로 관리하지 않고, 표준 출력으로 전달
- 애플리케이션 로직과 분리되어 애플리케이션이 실행되지 않는 상태여도 로그는 정상 작동 해야함
- 모니터링 시스템을 통해 장기적으로 보관된 로그를 분석

## 12. ADMIN PROCESSES FOR EVENTUAL PROCESSES

- 관리 프로세스는 애플리케이션과 동일한 환경에서 실행
- 관리 작업은 운영 중인 애플리케이션과 분리된 임시 작업으로, 데이터 마이그레이션, 일회성 스크립트 실행, 대량 데이터 처리 등이 포함
- Eventual Processes는 특정 시점에 실행되며, 이벤트 기반의 비동기 또는 일회성 프로세스
    - 데이터베이스 마이그레이션
    - 백그라운드 데이터 처리
    - 비동기 이메일 전송
    - 대량 파일 처리 (예: AWS S3와 연동된 작업)