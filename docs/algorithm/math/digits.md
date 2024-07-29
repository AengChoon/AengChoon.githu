---
title: 자릿수
layout: default
grand_parent: 알고리듬
parent: 수학
nav_order: 1
last_modified_date: 2024-07-29
---

# 자릿수
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## 코어 로직
```cpp
void Digits(int Number, int Base)
{
    while (Number != 0)
    {
        int Digit = Number % Base;
        Number = Number / Base;
    }
}
```

## 문제

### 자릿수의 합
{: .d-inline-block }

Basic
{: .label .label-blue }

[GeeksforGeeks](https://www.geeksforgeeks.org/problems/sum-of-digits1742/1){: .btn .btn-green .mr-2 }
[LeetCode](https://leetcode.com/problems/sum-of-digits-in-base-k/){: .btn .btn-yellow }
