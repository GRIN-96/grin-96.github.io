---
title: "🐶 백준 알고리즘 - 1316 그룹 단어 체커"
description: "백준 알고리즘 - 1316 그룹 단어 체커"
date: 2025-01-13 14:57
update: 2025-01-13 14:57
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
import java.util.HashSet;
import java.util.List;
import java.util.Set;
import java.util.stream.Collectors;

public class Main {
    public static void main(String[] args) throws IOException {

        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        int number = Integer.parseInt(br.readLine()); // 단어 수
        int count = 0; // 그룹 단어 수

        for (int i = 0; i < number; i++) {
            String input = br.readLine();
            List<Character> charList = input.chars()
                    .mapToObj(c -> (char)c)
                    .collect(Collectors.toList());

            if (groupWord(charList)) {
                count++;
            }
        }
        bw.write(count + "\n");

        bw.flush();
        br.readLine();
        bw.close();

    }

    // 그룹 단어 여부
    public static boolean groupWord(List<Character> charList) {
        Set<Character> seen = new HashSet<>(); // 등장한 문자를 저장하는 Set
        char prev = charList.get(0); // 첫 번째 문자 저장

        for (char c : charList) {
            if (seen.contains(c) && prev != c) { // 이미 등장한 문자지만 연속되지 않은 경우
                return false;
            }
            seen.add(c); // 현재 문자 저장
            prev = c; // 이전 문자 업데이트
        }
        return true;
    }
}
```

### 시간 복잡도
- O(N * W) 
  - 총 단어 개수(N) 중 해당 길이(W) 만큼 연산 발생

[^1]: https://www.acmicpc.net/problem/1316

