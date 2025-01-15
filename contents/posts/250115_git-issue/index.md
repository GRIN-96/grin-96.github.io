---
title: "🐙 Git-flow issue"
description: "git branch 전략 : 이슈발생"
date: 2025-01-16 00:00
update: 2025-01-16 00:00
tags:
  - git
  - git flow
series: "🐙 Git-flow"
---

## Issue

<br/>

- 추가 기능 개발로 FEATURE_A 브랜치를 DEV에 **Rebase + Merge** 후 QA 요청
- QA가 완료되기 전에 동일한 파일에서 추가 수정 사항 발생
- 해당 수정 사항을 FEATURE_B 브랜치에서 DEV에 **Rebase + Merge**
    - Rebase 과정에서 FEATURE_A의 코드가 운영 서버에 반영되면 에러 발생 가능성이 있어 일부 코드 누락
        - **<span style="color:red;">결과적으로 기존 코드 일부가 누락되는 문제 발생</span>**

<br/>

> 추후 신규 개발 및 유지보수 과정에서 유사한 문제가 반복될 가능성이 높아 Git-flow 전략을 재점검하게 되었습니다.