---
title: 데이터 형식
layout: default
grand_parent: 어셈블리어
parent: x86-64
nav_order: 1
---

# 데이터 형식
{: .no_toc }

16비트 아키텍처에서 시작하여 32비트 아키텍처로 확장되었기 때문에 인텔은 16비트 데이터 타입은 `word`, 32비트는 `double words`, 64비트는 `quad words`라고 지칭한다.

아래의 표는 C의 기본 데이터 타입에 사용되는 x86-64 표현을 보여준다.

| C 선언    | 인텔 데이터 타입        | 어셈블리 접미사 | 크기(바이트) | 
|:----------|:----------------------|:--------------:|:-----------:|
| `char`    | Byte                  | b              | 1           |
| `short`   | Word                  | w              | 2           |
| `int`,    | Double Word           | l              | 4           |
| `long`,   | Quad Word             | q              | 8           |
| `char*`,  | Quad Word             | q              | 8           |
| `float`,  | Single precision      | s              | 4           |
| `double`  | Double precision      | l              | 8           |

부동소수점 코드는 완전히 다른 명령어와 레지스터 세트를 포함하므로 4바이트 정수와 8바이트 배정밀도 부동 소수점 숫자 모두를 접미사 'l'로 구분해도 상관없다.
