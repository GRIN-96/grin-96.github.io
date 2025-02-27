---
title: "🍃 Cloud Native Architecture"
description: "Cloud Native Architecture"
date: 2025-01-13 23:57
update: 2025-01-13 23:57
tags:
  - MSA
  - Cloud Native Architecture
series: "🍃 Microservice와 Spring Cloud"
---

> Cloud Native Architecture(클라우드 네이티브 아키텍처)란 **클라우드 환경을 최대한 활용**하도록 설계된 소프트웨어 아키텍처 패턴
>

- 확장 가능한 아키텍처
    - 시스템의 수평적 확장에 유연
    - 확장된 서버로 시스템의 부하 분산, 가용성 보장
    - 시스템 또는, 서비스 애플리케이션 단위의 패키지 (컨테이너 기반 패키지)
    - 모니터링
- 탄력적 아키텍처
    - 서비스 생성 - 통합 - 배포, 비즈니스 환경 변화에 대응 시간 단축
        - 자동 CI / CD
    - 분할 된 서비스 구조
    - 무상태 통신 프로토콜
    - 서비스의 추가와 삭제 자동으로 감지
    - 변경된 서비스 요청에 따라 사용자 요청 처리 (동적 처리)
- 장애 격리 (Fault isolation)
    - 특정 서비스에 오류가 발생해도 다른 서비스에 영향 주지 않음