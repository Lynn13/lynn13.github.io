---
layout: post
title: "字符串匹配"
date: 2023-06-04 11:09:11 -0800
categories: search
---

## Trie
字典树，英文名 trie。
![Trie](/assets/trie1.png)

# KMP
该算法由 Knuth、Pratt 和 Morris 在 1977 年共同提出。

### 前缀函数
- 定义：对于一个长度为 n 的字符串，前缀函数/前缀数组p是一个长度为 n 的数组。
其中其中 p[i] 的定义是：子串 s[0 ... i] 最长的相等的真前缀与真后缀的长度。
- 举例来说，对于字符串 abcabcd :
    - p[0]=0，p[1]=0，p[2]=0，
    - p[3]=1，因为 abca 只有一对相等的真前缀和真后缀：a，长度为 1
    - p[4]=2，因为 abcab 相等的真前缀和真后缀只有 ab，长度为 2
    - p[6]=0，因为 abcabcd 无相等的真前缀和真后缀
    - 可以计算字符串 aabaaab 的前缀函数为 [0, 1, 0, 1, 2, 2, 3]

#### 简单版实现
```
def prefix_function(s):
    n = len(s)
    pi = [0] * n
    for i in range(1, n):
        for j in range(i, -1, -1):
            if s[0 : j] == s[i - j + 1 : i + 1]:
                pi[i] = j
                break
    return pi

```


#### 优化1

#### 优化2

### KMP

## AC自动机

## FST

## 其他
https://oi-wiki.org/string/