---
title: "🍃 Cloud Native Application"
description: "Cloud Native Application"
date: 2025-01-13 23:58
update: 2025-01-13 23:58
tags:
  - MSA
  - Microservice
  - Spring Cloud
series: "🍃 Microservice와 Spring Cloud"
---

> **클라우드 환경에서 최적화되어 동작하도록 설계된 애플리케이션**
>
- **컨테이너, 마이크로서비스, CI/CD, DevOps, 동적 오케스트레이션(Kubernetes)** 등을 활용하여 유연성과 확장성을 극대화하는 것이 특징

## 특징

### 1. 지속적인 통합, CI (Continuous Integration)
  - 통합 서버, 소스관리 (SCM), 빌드 도구, 테스트 도구
  - ex ) Jenkins, Team CI, Travis Ci

### 2. 지속적 배포, CD
  - Continuous Delivery
    - 패키지화 된 결과물 실행 환경에 수동 반영
  - Continuous Deplyment
    - 자동 배포
  - Pipe line

### 3. 카나리 배포와 블루그린 배포
  - 카나리 배포(Canary Deployment)
    - 새 애플리케이션을 소수에게 배포한 후 안정성이 확보되면 점진적으로 모든 사용자에게 배포
  - 블루-그린 배포(Blue-Green Deployment)
    - 두 개의 환경(Blue: 기존 버전, Green: 새로운 버전)을 동시에 운영하여 새로운 버전이 준비되면 한번에 모든 트래픽을 이동시키는 방식
    - rollback 가능

### 4. DevOps
  - 소프트웨어 개발(Development)과 운영(Operations)을 통합하는 문화 및 방법론
  - **자동화**, **협업**, 지속적 통합/배포(CI/CD)를 통해 **빠르고 안정적인 소프트웨어 개발 및 운영을 목표**

### 5. Container 가상화
  - 운영체제(OS) 수준에서 애플리케이션을 격리하고 실행하는 가상화 기술
  - 하이퍼바이저 기반 VM(Virtual Machine) 보다 **더 가볍고 빠르며, 확장성이 뛰어남**