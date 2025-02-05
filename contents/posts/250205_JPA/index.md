---
title: "🌱 JPA란?"
description: "Java Persistence API"
date: 2025-02-05 23:05
update: 2025-02-05 23:05
tags:
  - MSA
  - Microservice
  - Monolithic
series: "🌱 JPA(Java Persistence API)"
---

## JPA란?

```
1. JPA는 개발자의 sql 쿼리 작업을 최소화 해준다.

2. 컬럼 추가 시 쿼리문을 일괄 수정해야하는 상황을 해결해준다.

3. CRUD 쿼리를 간단하게 생성할 수 있도록 도와준다

4. 객체를 자바 컬렉션에 저장하 듯 DB에 저장하고자 하는 목적으로 만들어졌다.
```

## Java Persistence API

**자바 진영의 ORM 기술 표준**

- Object-Relational Mapping(객체 관계 매핑)
  - 객체는 객체대로 설계
  - 관계형 데이터베이스는 관계형 데이터베이스대로 설계
  - ORM 프레임워크가 중간에서 매핑


## JPA를 사용하는 이유

- SQL 중심 개발에서 객체 중심으로 개발
  - ORM이 중간에서 문제 해결
  - 자바 객체 컬렉션 조회하듯 던지면 된다.
- 생산성
  - SQL 반복 작업을 하지 않음
- 유지보수
  - JPA가 직접 SQL 작업을 수행하기에 유지보수 측면에서 장점이 있음
- 패러다임의 불일치 해결
- 데이터 접근 추상화와 벤더 독립성
  - JPA는 추상화된 데이터 접근 계층을 제공해 특정 벤더에 종속적이지 않음
  - 어떤 DB를 사용하는 지 설정만 해주면 됨


## 유지보수
- JPA 필드만 추가해주면 SQL은 JPA가 처리해준다.
- 트랜젝션 안에서 조회후 변경 진행하면 트랜젝션 변경 시점에서 업데이트 쿼리가 진행되며 커밋이 진행된다.
```java
public class Member {
	private String memberId;
	private String name;
	private String tel;  // 추가된 필드
}
```

