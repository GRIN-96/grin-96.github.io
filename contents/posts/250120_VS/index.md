---
title: "🍃 Monolithic VS MSA"
description: "Monolithic VS MSA"
date: 2025-01-20 00:31
update: 2025-01-20 00:31
tags:
  - MSA
  - Microservice
  - Monolithic
series: "🍃 Microservice와 Spring Cloud"
---

## Monolithic

> 애플리케이션을 하나의 소프트웨어 안에 포함시켜 개발하는 방식
>

- 모든 업무 로직이 하나의 애플리케이션 형태로 패키지 되어 서비스
  - 서비스 하나가 수정되면 전체가 재 패키징 되어 배포
- 애플리케이션에서 사용하는 데이터가 한곳에 모여 참조되어 서비스 되는 형태

<br>

---

## MSA - Micro Service Aplication

> 복잡한 애플리케이션을 독립적인 작은 서비스들로 나누어 개발, 배포 및 유지보수하는 방식
>

- 서비스가 분리되어 있어 전체가 다운되는 상황이 없음.
- 서비스 간 resource API  (HTTP 통신)
- 최소한의 중앙 집중 식 관리가 되어야 한다.
- 서로 다른 언어, 저장기술을 사용할 수 있음
  - 서비스 특색에 맞게 작업 진행이 가능하다.