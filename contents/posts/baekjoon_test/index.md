---
title: "🐶 백준 알고리즘 - 1152 단어의 개수"
description: "백준 알고리즘 연습문제 - 1152 단어의 개수"
date: 2025-01-12
update: 2025-01-12
tags:
  - Backjoon
  - Algorithm
  - 구현
  - 문자열
series: "🐶백준 알고리즘 팁"
---

## 풀이
<br/>

```java
import java.io.*;
import java.util.StringTokenizer;

public class Main {
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
        
        String text = br.readLine().trim(); // 입력받고 앞뒤 공백 제거
        StringTokenizer st = new StringTokenizer(text, " "); // 공백 기준으로 토큰화

        bw.write(String.valueOf(st.countTokens())); // 토큰 개수 출력
        
        bw.flush(); // 출력 버퍼 비우기
        br.close(); // 자원 해제
        bw.close(); // 자원 해제
    }
}
```

### 시간 복잡도
- O(N)

[^1]: https://www.acmicpc.net/problem/1152

