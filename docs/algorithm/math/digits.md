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
void Digits(int Base, int Number)
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

Easy
{: .label .label-blue }

[![Static Badge](https://img.shields.io/badge/GeeksforGeeks-2F8D46?style=for-the-badge&logo=geeksforgeeks&logoColor=white)](https://www.geeksforgeeks.org/problems/sum-of-digits1742/1)
[![Static Badge](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=white)](https://leetcode.com/problems/sum-of-digits-in-base-k/)
