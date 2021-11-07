---
title: "[C] 백준 10171번(고양이), 10172번(강아지)"
author: Hoyon Kim
date: 2021-11-06 19:00:00 +0000
categories: [baekjoon]
permalink: /baekjoon/10171/
---

## 문제

![백준 10171번, 10172번 문제 캡쳐](/images/baekjoon/10171/문제-사진.png)

주어진 대로 출력하면 되는 간단한 문제입니다.

그런데, ```예제 출력 1```의 문장을 그대로 복사해서, 한줄마다 \n(개행문자)을 붙여준 뒤 ```printf``` 함수를 이용해서 출력하면(!) 그대로 컴파일 에러가 발생합니다.

## 왜 안될까? 

방금 작성했던 코드를 다시 살펴보겠습니다.

```
#include <stdio.h>
int main() {
	printf("\    /\\n )  ( ')\n(  /  )\n\n \(__)|");
	return 0;
}
```

이 글을 검색을 통해 들어오셨다면, 아마 이러한 형태의 코드로 작성하셨을 겁니다.


C언어 표준(C99 standard)에서 정하고 있는 제어문자(Escape Sequence)로는 다음과 같은 문자들이 있습니다.

| 종류 | 사용 방법 | 설명 |
|:---|:---:|:---|
| alert | \a | 경고음이나 경고창을 출력합니다 |
| backspace | \b | 커서를 한 칸 앞으로(왼쪽으로) 이동시킵니다 |
| form feed | \f |  |
| new line | \n | 커서를 다음 줄의 처음으로 이동시킵니다 |
| carriage return | \r | 커서를 현재 줄의 처음으로 이동시킵니다 |
| horizontal tab | \t | !|
| vertical tab | \v | |
| single quote ' | \\' | |
| double quote " | \\" | |
| question mark ? | \\? | |
