---
title: 피연산자
layout: default
grand_parent: 어셈블리어
parent: x86-64
nav_order: 3
last_modified_date: 2024-07-29
---

# 피연산자
{: .no_toc }

대부분의 명령어에는 연산을 수행할 때 사용할 **source**의 값과 연산의 결과를 저장할 **destination**의 위치를 지정하는 피연산자가 하나 이상 존재한다.

x86-64에서 **source**는 **상수**로 지정하거나 **레지스터** 또는 **메모리**에서 읽은 값이고 **destination**은 **레지스터**나 **메모리**의 위치이다.

따라서 피연산자는 아래 표와 같이 세 가지 타입으로 분류할 수 있다. 

| 타입         | 형태                                          | 값                                                     | 
|:-------------|:----------------------------------------------|:------------------------------------------------------|
| Immediate    | $_Imm_                                        | _Imm_                                                 |
| Register     | r<sub>a</sub>                                 | R[r<sub>a</sub>]                                      |
| Memory       | _Imm_                                         | M[_Imm_]                                              |
| Memory       | (r<sub>a</sub>)                               | M[R[r<sub>a</sub>]]                                   |
| Memory       | _Imm_(r<sub>b</sub>)                          | M[_Imm_ + R[r<sub>b</sub>]]                           |
| Memory       | (r<sub>b</sub>, r<sub>i</sub>)                | M[R[r<sub>b</sub>] + R[r<sub>i</sub>]]                |
| Memory       | _Imm_(r<sub>b</sub>, r<sub>i</sub>)           | M[_Imm_ + R[r<sub>b</sub>] + R[r<sub>i</sub>]]        |
| Memory       | (, r<sub>i</sub>, _s_)                        | M[R[r<sub>i</sub>] · _s_]                             |
| Memory       | _Imm_(, r<sub>i</sub>, _s_)                   | M[_Imm_ + R[r<sub>i</sub>] · _s_]                     |
| Memory       | (r<sub>b</sub>, r<sub>i</sub>, _s_)           | M[R[r<sub>b</sub>] + R[r<sub>i</sub>] · _s_]          |
| Memory       | _Imm_(r<sub>b</sub>, r<sub>i</sub>, _s_)      | M[_Imm_ + R[r<sub>b</sub>] + R[r<sub>i</sub>] · _s_]  |

첫 번째 타입인 *immediate* 은 상수 값을 위한 타입이다.

ATT 형식의 어셈블리 코드에서는 '$' 뒤에 표준 C 표기법으로 나타낸 정수를 붙여서 작성한다(예: $-577 또는 $0x1F).

명령어에 따라 다양한 범위의 immediate 값을 허용하며, 어셈블러는 값을 인코딩하는 가장 압축된 방법을 자동으로 선택한다.

두 번째 타입인 *register* 는 16개의 레지스터 중 하나의 8, 4, 2, 1바이트 내용을 위한 타입이다.

r<sub>a</sub>로 임의의 레지스터 a를 나타내고 그 값은 R[r<sub>a</sub>]로 나타내어 레지스터 집합을 레지스터 식별자로 인덱싱된 배열 R로 간주한다.
