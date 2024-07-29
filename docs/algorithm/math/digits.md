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
void Digits(int Number)
{
    while (Number != 0)
    {
        int Digit = Number % 10;
        Number = Number / 10;
    }
}
```
