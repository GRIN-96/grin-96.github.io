---
title: "🐶 백준 알고리즘 팁"
description: "백준 알고리즘 팁!"
date: 2025-01-11
update: 2025-01-12
tags:
  - Backjoon
  - Algorithm
series: "🐶백준 알고리즘 팁"
---

## 1. 클래스명은 Main,

```java
public class Main {
	
}
```

이와같이 클래스명을 Main으로 두고 작성한다

## 2. Main 함수에서 바로 작성 시, 모든것은 static으로 선언 후 작성한다.

```java
public class Main {
	private static int max = 0;
	private static int n, k;
	
	private static void dfs(int cnt, int num) {
	
	}
}
```

main문 자체가 static 함수 이므로 내부에서 사용하는 전역변수 및 모든 함수 또한 static 이어야 한다.

## 3. 입력 값을 받을 땐 Scanner 보단 BufferedReader

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
	public void solution() throws Exeption {
		 BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		 int n = Integer.parseInt(br.readLine());
	}
	
	public static void main(String[] args) throws Exception {
		new Main().solution();
	}
}
```

Scanner는 내부적으로 다음 입력값을 찾을 때 정규식을 사용해 속도가 느리다.

## 4.문자열 구분

String 문자열 구분 시 split()보단 StringTokenizer를 사용하는 것이 속도가 더 빠르다.

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Main {
    public void solution() throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        
        for (int i = 0; i < n; i++) {
            StringTokenizer st = new StringTokenizer(br.readLine());
            int s = Integer.parseInt(st.nextToken());

            for (int j = 0; j < s; j++) {
                int data = Integer.parseInt(st.nextToken());
                System.out.println(data);
            }
        }
    }

    public static void main(String[] args) throws Exception {
        new Main().solution();
    }
}

```

위와 같이 BufferedReader와 StringTokenizer로 입력받는다면 빠르게 입력받을 수 있다.

## 5. 입력을 위한 클래스는 하나만

- System.in이 들어간 클래스는 단 하나만 생성하는 것이 좋다.

## 6. 출력 시 System.out.printIn() 보다 BufferedWriter가 빠르다

```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.StringTokenizer;

public class Main {
    public void solution() throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        int n = Integer.parseInt(br.readLine());

        for (int i = 0; i < n; i++) {
            StringTokenizer st = new StringTokenizer(br.readLine()); // 토큰화
            int s = Integer.parseInt(st.nextToken());

            for (int j = 0; j < s; j++) {
                int data = Integer.parseInt(st.nextToken());
                bw.write(String.valueOf(data)); // 출력
                bw.newLine(); // 줄바꿈            }
        }

        bw.flush(); // 출력 버퍼 비우기
        br.close(); // 자원 해제
        bw.close(); // 자원 해제
    }

    public static void main(String[] args) throws Exception {
        new Main().solution();
    }
}

```