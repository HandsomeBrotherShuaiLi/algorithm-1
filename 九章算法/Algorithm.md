<!-- TOC -->

- [1. 二分法 Binary Search](#1-%E4%BA%8C%E5%88%86%E6%B3%95-binary-search)
    - [1.1. Binary Search](#11-binary-search)
    - [1.2. 独孤九剑——破剑式 比O(n)更优的时间复杂度 几乎只能是O(logn)的二分法](#12-%E7%8B%AC%E5%AD%A4%E4%B9%9D%E5%89%91%E7%A0%B4%E5%89%91%E5%BC%8F-%E6%AF%94on%E6%9B%B4%E4%BC%98%E7%9A%84%E6%97%B6%E9%97%B4%E5%A4%8D%E6%9D%82%E5%BA%A6-%E5%87%A0%E4%B9%8E%E5%8F%AA%E8%83%BD%E6%98%AFologn%E7%9A%84%E4%BA%8C%E5%88%86%E6%B3%95)
    - [1.3. 第一境界 二分法模板](#13-%E7%AC%AC%E4%B8%80%E5%A2%83%E7%95%8C-%E4%BA%8C%E5%88%86%E6%B3%95%E6%A8%A1%E6%9D%BF)
    - [1.4. 第二境界 二分位置 之 OOXX](#14-%E7%AC%AC%E4%BA%8C%E5%A2%83%E7%95%8C-%E4%BA%8C%E5%88%86%E4%BD%8D%E7%BD%AE-%E4%B9%8B-ooxx)
    - [1.5. 第三境界 二分位置 之 Half Half](#15-%E7%AC%AC%E4%B8%89%E5%A2%83%E7%95%8C-%E4%BA%8C%E5%88%86%E4%BD%8D%E7%BD%AE-%E4%B9%8B-half-half)
    - [1.6. 第四境界(至高境界): 二分答案 Binary Search on Result, 二分法难题 (Hard)](#16-%E7%AC%AC%E5%9B%9B%E5%A2%83%E7%95%8C%E8%87%B3%E9%AB%98%E5%A2%83%E7%95%8C-%E4%BA%8C%E5%88%86%E7%AD%94%E6%A1%88-binary-search-on-result-%E4%BA%8C%E5%88%86%E6%B3%95%E9%9A%BE%E9%A2%98-hard)
- [2. 搜索 Search](#2-%E6%90%9C%E7%B4%A2-search)
    - [2.1. 宽度优先搜索 Breadth First Search](#21-%E5%AE%BD%E5%BA%A6%E4%BC%98%E5%85%88%E6%90%9C%E7%B4%A2-breadth-first-search)
        - [2.1.1. 二叉树上的宽度优先搜索 BFS in Binary Tree](#211-%E4%BA%8C%E5%8F%89%E6%A0%91%E4%B8%8A%E7%9A%84%E5%AE%BD%E5%BA%A6%E4%BC%98%E5%85%88%E6%90%9C%E7%B4%A2-bfs-in-binary-tree)
        - [2.1.2. Serialization 序列化](#212-serialization-%E5%BA%8F%E5%88%97%E5%8C%96)
        - [2.1.3. 图上的宽度优先搜索 BFS in Graph & 拓扑排序 Topological Sorting(必考)](#213-%E5%9B%BE%E4%B8%8A%E7%9A%84%E5%AE%BD%E5%BA%A6%E4%BC%98%E5%85%88%E6%90%9C%E7%B4%A2-bfs-in-graph--%E6%8B%93%E6%89%91%E6%8E%92%E5%BA%8F-topological-sorting%E5%BF%85%E8%80%83)
        - [2.1.4. 棋盘上/矩阵中的宽度优先搜索 BFS in Matrix (格子图)](#214-%E6%A3%8B%E7%9B%98%E4%B8%8A%E7%9F%A9%E9%98%B5%E4%B8%AD%E7%9A%84%E5%AE%BD%E5%BA%A6%E4%BC%98%E5%85%88%E6%90%9C%E7%B4%A2-bfs-in-matrix-%E6%A0%BC%E5%AD%90%E5%9B%BE)
    - [2.2. 深度优先搜索 Depth First Search](#22-%E6%B7%B1%E5%BA%A6%E4%BC%98%E5%85%88%E6%90%9C%E7%B4%A2-depth-first-search)
        - [2.2.1. 组合搜索问题 Combination 2**n](#221-%E7%BB%84%E5%90%88%E6%90%9C%E7%B4%A2%E9%97%AE%E9%A2%98-combination-2n)
        - [2.2.2. 排列搜索问题 Permutation](#222-%E6%8E%92%E5%88%97%E6%90%9C%E7%B4%A2%E9%97%AE%E9%A2%98-permutation)
        - [2.2.3. Search in a Graph 图中的搜索](#223-search-in-a-graph-%E5%9B%BE%E4%B8%AD%E7%9A%84%E6%90%9C%E7%B4%A2)
        - [2.2.4. Non Recursion](#224-non-recursion)
        - [2.2.5. DFS时间复杂度](#225-dfs%E6%97%B6%E9%97%B4%E5%A4%8D%E6%9D%82%E5%BA%A6)
    - [2.3. dijkstra's algorithm](#23-dijkstras-algorithm)
- [3. Sweep Line 扫描线算法 处理区间问题的扫描线](#3-sweep-line-%E6%89%AB%E6%8F%8F%E7%BA%BF%E7%AE%97%E6%B3%95-%E5%A4%84%E7%90%86%E5%8C%BA%E9%97%B4%E9%97%AE%E9%A2%98%E7%9A%84%E6%89%AB%E6%8F%8F%E7%BA%BF)
- [4. 两根指针 Two Pointers](#4-%E4%B8%A4%E6%A0%B9%E6%8C%87%E9%92%88-two-pointers)
    - [4.1. 同向双指针](#41-%E5%90%8C%E5%90%91%E5%8F%8C%E6%8C%87%E9%92%88)
    - [4.2. 相向双指针](#42-%E7%9B%B8%E5%90%91%E5%8F%8C%E6%8C%87%E9%92%88)
    - [4.3. Two Sum & its variation](#43-two-sum--its-variation)
    - [4.4. Partition Array 分割数组](#44-partition-array-%E5%88%86%E5%89%B2%E6%95%B0%E7%BB%84)
- [5. 递归 Recursion](#5-%E9%80%92%E5%BD%92-recursion)
    - [5.1. 递归的概念](#51-%E9%80%92%E5%BD%92%E7%9A%84%E6%A6%82%E5%BF%B5)
        - [5.1.1. 递归的三要素](#511-%E9%80%92%E5%BD%92%E7%9A%84%E4%B8%89%E8%A6%81%E7%B4%A0)
        - [5.1.2. 递归与非递归方法的比较](#512-%E9%80%92%E5%BD%92%E4%B8%8E%E9%9D%9E%E9%80%92%E5%BD%92%E6%96%B9%E6%B3%95%E7%9A%84%E6%AF%94%E8%BE%83)
    - [5.2. 递归调用栈](#52-%E9%80%92%E5%BD%92%E8%B0%83%E7%94%A8%E6%A0%88)
        - [5.2.1. 回溯法Backtracking](#521-%E5%9B%9E%E6%BA%AF%E6%B3%95backtracking)
        - [5.2.2. 二分查找/搜索 Binary Search 的递归写法 (二分)](#522-%E4%BA%8C%E5%88%86%E6%9F%A5%E6%89%BE%E6%90%9C%E7%B4%A2-binary-search-%E7%9A%84%E9%80%92%E5%BD%92%E5%86%99%E6%B3%95-%E4%BA%8C%E5%88%86)
    - [5.3. 值传递和引⽤传递](#53-%E5%80%BC%E4%BC%A0%E9%80%92%E5%92%8C%E5%BC%95%E2%BD%A4%E4%BC%A0%E9%80%92)
        - [5.3.1. 值传递](#531-%E5%80%BC%E4%BC%A0%E9%80%92)
        - [5.3.2. 引⽤传递](#532-%E5%BC%95%E2%BD%A4%E4%BC%A0%E9%80%92)
    - [5.4. 递归综合训练](#54-%E9%80%92%E5%BD%92%E7%BB%BC%E5%90%88%E8%AE%AD%E7%BB%83)
- [6. 贪心 Greedy Algorithms](#6-%E8%B4%AA%E5%BF%83-greedy-algorithms)
- [7. 分治 Divide & Conquer](#7-%E5%88%86%E6%B2%BB-divide--conquer)
- [8. Graph](#8-graph)
    - [8.1. BFS & DFS](#81-bfs--dfs)
    - [8.2. Dijkstra,](#82-dijkstra)
    - [8.3. Flloyd Warshall](#83-flloyd-warshall)
    - [8.4. MST](#84-mst)
    - [8.5. flow](#85-flow)
- [9. String问题](#9-string%E9%97%AE%E9%A2%98)
    - [9.1. Rabin Karp](#91-rabin-karp)
    - [9.2. KMP](#92-kmp)
    - [9.3. Aho-Crosaick](#93-aho-crosaick)
- [10. Number Theory](#10-number-theory)

<!-- /TOC -->


# 1. 二分法 Binary Search
1. 第一境界: 二分法模板
    递归与非递归的权衡
    二分的三大痛点 (while < 还是 while <=; 超出time limit)
    通用的二分法模板
2. 第二境界: 二分位置 之 圈圈叉叉 Binary Search on Index - OOXX (抽象化满足条件)
    找到满足某个条件的第一个位置或者最后一个位置
3. 第三境界: 二分位置 之 保留一半 Binary Search on Index - Half Half (log(n)的思想来源, 如何做到二分)
    保留有解的一半, 或者去掉无解的一半
4. 第四境界(至高境界): 二分答案

## 1.1. Binary Search
Given a sorted integer array nums, and an integer target.
Find the any/first/last position of target in nums. Return -1 if target does not exist.
(问last时, 容易出现死循环, 超时)
两个指针一头一尾 (left/right) 和target比较, 后将left/right移到中间, 直到left/right并到一起
if (nums[mid] < target)     O(1)的if语句

**时间复杂度 Time Complexity (面试必问)**
不要说 O(2n), O(n+10), O(n3+n2).. 
时间复杂度不论系数, 不论常数项, 只看最高项, 只关心数量级
n = 数据规模  O(2n)=O(n) 		O(n+10)=O(n) 		O(n3+n2)=O(n3)	 O(n2+nlogn)=O(n2)

T(n) = T(n/2) + O(1) = O(logn) 		通过O(1) 把n → n/2 规模的问题
通过O(1)的时间, 把规模为n的问题变为n/2
T(n) = T(n/2) + O(1) = T(n/4) + O(1) + O(1) = T(n/8) + 3O(1) =.. = T(n/n) + log2(n)×O(1) = T(1) + log2(n)×O(1)
T(n) = 规模为n的算法的时间复杂度  T(1)=输入规模为1时, 算法的时间复杂度

O(log2 n)=O(log4 n) = 2O(log2 n)   O(logn)=O(logn^2) = 2O(logn)	时间复杂度不管系数, log以什么为底无所谓

通过O(n)的时间, 把规模为n的问题变为n/2  (不是O(nlogn)!!!)
T(n) = T(n/2) + O(n) = T(n/4) + O(n/2) + O(n) = T(n/8) + O(n/4) +  O(n/2) + O(n) =.. (先不约去O(n/4)和O(n/2), 展开到最后再约去)
= T(1) + O(n) + O(n/2) + O(n/4) +.. O(1) = O(n+n/2+n/4+…+2+1) ≈ O(2n-1) = O(2n)= O(n)

空间复杂度 Space Complexity (很少问) —> 程序开了几个数组, 每个数组长度多少, 相加即可

Time Complexity in Coding Interview
* O(1)              极少    return 一个公式即可, 不用写程序
* O(logn)           几乎都是二分法	
* O(√n)             几乎是分解质因数	e.g 6=2×3 枚举至√n
* O(n)              高频     → 暴力 for 循环, O(n)之下只有O(logn)
* O(nlogn)          一般都可能要排序    先将数组排序, 解法豁然开朗~
* O(n^2)            数组, 枚举, 动态规划
* O(n^3)            数组, 枚举, 动态规划
* O(2^n)            与组合有关的搜索	e.g. subset题目
* O(n!)             与排列有关的搜索
考察如何计算时间复杂度, 面试中常考O(n), O(nlogn), O(n2)

## 1.2. 独孤九剑——破剑式 比O(n)更优的时间复杂度 几乎只能是O(logn)的二分法
*经验之谈: 根据时间复杂度倒推算法是面试中的常用策略*
若一眼看就是O(n), 就要考虑O(logn)的实现方式了 → 两个指针一头一尾, 中间取点, 去一半

哪种方法实现二分法 Recursion or While Loop? 		R: Recursion W: While loop B: Both work 
(建议, 能不用recursion就不用, recursion是一个不好的coding pattern, 递归易造成stack overflow 栈溢出, 程序crash)

面试中是否使用 Recursion 的几个判断条件, 使用递归与非递归的权衡方法
* ①面试官是否要求了不使用 Recursion (如果你不确定, 就向面试官询问)
* ②不用 Recursion 是否会造成实现变得很复杂 (二分法一般不会很复杂)
* ③Recursion 的深度是否会很深
* ④题目的考点是 Recursion vs Non-Recursion, 还是就是考你是否会Recursion?
Note: 不要自己下判断, 要跟面试官讨论!

二分法常见痛点
* ①又死循环了! what are you 弄撒捏!
* ②循环结束条件到底是哪个?
    start <= end
    start < end	       两根指针指向同一个数时, 才会结束 (容易死循环)
    start + 1 < end    两个指针相邻即可结束 (避免死循环)
* ③指针变化到底是哪个?
    start = mid
    start = mid + 1
    start = mid - 1

## 1.3. 第一境界 二分法模板
- start + 1 < end               中间隔着一个时即可结束, 避免死循环; 精度不为1(i.e. 整数), 则 while end - start > precision
- mid = start + (end - start) / 2   等于mid=(start+end)/2 但避免s和e过大时造成越界; 一定是整数则 mid = s + (e - s) // 2
- A[mid] ==, <, >               三种情况分开讨论
- A[start] A[end] ? target      出了while循环后, 寻找结果; 二分法 → 不断缩小区间, 不一定直接return答案

Lintcode 457.[Classical Binary Search]()
Lintcode 14.[First Position of Target]()
Lintcode 458.[Last Position of Target]()

## 1.4. 第二境界 二分位置 之 OOXX
一般会给你一个数组, 让你找数组中第一个/最后一个满足某个条件的位置 OOOOOOO..O**OX**X....XXXXXX
O=小于target的数, X=大于等于target的数, 找第一个X或者最后一个O

Lintcode 74.[First Bad Version]()

Lintcode 447.[Search in a Big Sorted Array]()
排序数组二分法 → 二分, 起点+终点, 取中点
现在没有终点怎么办? 找终点, 令点 ≥ target (终点要在k的级别上)
Vector/ArrayList: 动态数组实现方式, 不用声明多大多长, 倍增思想, 和网络访问的exponential backoff类似
	*Note: 一道题问完用什么数据结构, 还会追问数据结构的实现方式*
要求复杂度O(log k) 	k是数所在位置
以2倍递增 1→2→4→8 直到 ≥target, 共递增logk次  (可以确定数在 [k, 2k]范围里)

Lintcode 159.[Find Minimum in Rotated Sorted Array]()  oooooxxxxx
![](.pic/binarysearch_minrsa.png) 
- Sorted Array ⊆ Rotated Sorted Array (在做RSA的题时, 需要考虑没有rotated的情况)
- RSA: 
    x is the First Position <= last number? ✔️
    x is the First Position <= or < First Number? (WRONG)

Lintcode 28.[Search a 2D Matrix]() 不是二分法, 但是是常考题
Lintcode 38.[Search a 2D Matrix II]() 不是二分法, 但是是常考题
- 从左下角开始, 往右上角逼近

Lintcode 61.[Search for a Range]() First Position of Target + Last Position of Target

Lintcode 600.[Smallest Rectangle Enclosing Black Pixels]()
在列中需要找出第一个'1'出现的最左侧坐标和最右侧坐标, 在行中需要找出第一个'1'出现的最上面坐标和最下面坐标。采用二分的方法在区间查找即可。最后返回(right - left + 1) * (down - up + 1)即可。

## 1.5. 第三境界 二分位置 之 Half Half
无法找到一个条件, 形成 OOXX 的模型; 但可以根据判断, 保留下有解的那一半或者去掉无解的一半

Lintcode 585.[Maximum Number in Mountain Sequence]() 在先增后减的序列中找最大值

Lintcode 75.[Find Peak Element]()
先增后减数组, 一定有peak(局部最大); 找所有peak→for循环, O(n) 		
找一个peak → 非排序数组如何二分?
四种情况  
- mid-1 < mid < mid+1 (递减区间, 左半部分一定有峰)   
- mid-1>mid>mid+1 (有半部分一定有峰) 
- mid > mid-1 & mid+1 (mid就是峰, return it)      
- mid < mid-1 & mid+1 (左右两边都至少存在一个解)

有时选算法, 看要求的答案个数(为下限)

Lintcode 62.[Search in Rotated Sorted Array]()  会了这道题, 才敢说自己会二分法
4 5 6 7 0 1 2   target=6
o o x x o o o   (not ooxx)

二分思想要求, 去掉一半后, 剩下的一半必须还是刚开始的构型。
    → 二分之后必须还是RSA (SA⊆RSA)
* Soln 1: 找最小的数(找到o/找最小) O(logn), 然后还原成 ooxx, 但还原操作为O(n) 不🉑
* Soln 2: 用两次二分的方法
    第一次二分找到最小数的位置, find minimum number in rotated sorted array
    第二次二分确定 target, 在左侧区间还是右侧 (start ≤ target ≤ mid 答案在左边,  target > mid && target < start 答案在右边) 
    再用一个普通的二分法即可找到
* Soln 3: 用一次二分法
    start ≤ target ≤ mid 答案在左边;  target > mid && target < start 答案在右边

二分思想要求, 去掉一半后, 剩下的一半必须还是刚开始的构型 → 二分之后必须还是RSA (SA⊆RSA)

Lintcode 39.[Recover Rotated Sorted Array]() in-place
Lintcode 8.[Rotate String]() in-place
三步翻转法 3 step reverse: [4,5,1,2,3] → [5,4,1,2,3] → [5,4,3,2,1] → [1,2,3,4,5] offset=2

Lintcode 459.[Closest Number in Sorted Array]()
Lintcode 460.[Find K Closest Elements]()
oooxxxx 先找到x 然后左右两个指针分别往两边移动  O(logn + k)  因为不知道logn和k哪个大

## 1.6. 第四境界(至高境界): 二分答案 Binary Search on Result, 二分法难题 (Hard)
往往没有给你一个数组让你二分, 同样是找到满足某个条件的最大或者最小值 (原题求最大/最小不太好做时, 可以考虑二分答案)

解题方法: 通过猜值判断是否满足题意不对去搜索可能解  (原问题 max/min是多少 转换为 判定问题 Yes/No)
1.找到可行解范围 2.猜答案 3.检验条件 4.调整搜索范围

按值二分, 找到单调的地方

二分查找某个元素在数组中的位置的时间复杂度 O(logn). 每次操作都选择当前数组的中位数与目标元素值比较, 若比目标值更大, 则在中位数前继续寻找, 反之在中位数后寻找, 这样每次可以将搜索范围缩小一半

哪种写法会出现死循环? A 若left=0, right=1, mid=0, 且nums[mid] < target的条件下, 出现死循环
```python
while left < right:
    mid = left + (right - left) // 2
    if nums[mid] < target:
        left = mid
    else:
        right = mid

while left + 1 < right:
    mid = left + (right - left) // 2
    if nums[mid] < target:
        left = mid
    else:
        right = mid 

while left < right:
    mid = left + (right - left) // 2
    if nums[mid] < target:
        left = mid + 1
    else:
        right = mid - 1

while left <= right:
    mid = left + (right - left) // 2
    if nums[mid] < target:
        left = mid + 1
    else:
        right = mid - 1
```

LintCode 75. [Find Peak Element]()
给定A[0..n-1], 其中没有相邻元素相同, 并且A[0] < A[1], A[n-2] > A[n-1], 找到任意一个P, 满足A[P-1] < A[P] > A[P+1]
输入: [1, 5, 6, 8, 7, 9, 4]  输出: 3

- 首先, 这样的P肯定存在  (尝试举一个反例 a0 < a1 < .. < an-2 < an-1, 但与A[n-2] > A[n-1]矛盾, 故一定可以找到)
- 因为A[0] < A[1], 如果A[1]不是要找的元素, A[1] < A[2]; ... A[2] < A[3]; ... 但是A[n-2] > A[n-1]
- 二分查找: 对于mid位置, 如果A[mid] < A[mid+1], 右边一定有答案, 继续向右找; 否则左边一定有答案, 向左

Lintcode 390.[Find Peak Element II]() TODO

Lintcode 141.[Sqrt(x)]()
Last number that number^2 <= x
follow up: what if return a double, not an integer?

Lintcode 586.[Sqrt(x) II]()
一直二分直到 |number^2 - x| <= 1e-10
- 先找下界(0), 在找下界(x), 再二分
- 总长度L; 二分一次 L/2, 二分两次 L/2^2
- 若ε=10^-t, L/2^x ≤ 1e-t, 2^x ≥ L/1e-t, 则 x ≥ log(L/1e-t) = logL - log(1e-t) = logL + t log10 ≥ logL + 3t

LintCode 183. [Wood Cut]()
长度分别是L[0]..L[n-1]的n块木头, 要求找到最长的长度s, 使得这些木头可以切出至少k块长度为s的木头(不可以拼接)
输入: L=[232, 124, 456], k=7 输出: 114  ( ⎣232/114⎦ + ⎣124/114⎦ + ⎣456/114⎦ = 2 + 1 + 4 = 7 )
- 规律: 对于一个长度s, 如果可以切出t段; 而对于另一个长度S>s, 可以切出T段, 则一定有t>=T
- 所以如果长度s切出的段数不够k, 答案肯定比s小; 同理, 如果长度s切出的段数>=k, 答案肯定>=s  
- 二分答案: 二分切割后获得的每一段木头的长度 (该题需要求出每一小段木头的最长长度, 因此应二分切割后获得的每一段木头的长度)

- 原问题(不好做) -> max S, 使得 ⎣L[0]/S⎦ + ⎣L[1]/S⎦ + .. ⎣L[n-1]/S⎦ ≥ k
- 二分答案的判断性问题 -> 给定 S, 切出木头数目是否 ≥ k   
- 上界, 能切出的木头最长 max L[i]; 下界, 最短 1 (必须是整数)
- 时间复杂度: O(f(n) · log 答案范围/答案精度) 
    f(n) = 每次问是/否这件事的时间复杂度  (求⎣L[0]/S⎦ + ⎣L[1]/S⎦ + .. ⎣L[n-1]/S⎦ ≥ k ?  -->  O(n))
    二分的时间复杂度: 答案范围=上界-下界=L-1; 答案精度=1
    TC = O(nlogL)

LintCode 437.[Copy Books]()
有N本书需要被抄写, 第i本书有A, i=0, 1, ..., N-1; 有K个抄写员, 每个抄写员可以抄写连续的若干本书 (例如: 第3~5本书, 或者第10本书); 每个抄写员的抄写速度都一样, 最少需要多少时间抄写完所有的书 (取决于抄的最慢的人)
输入: A = [3, 2, 4], K=2  输出: 5 (第一个抄写员抄写第1本和第2本书, 第二个抄写员抄写第3本书) 
* Soln 1: DP (TC高)
* Soln 2: 
- 题目要求K个抄写员抄完最少需要的时间; 反过来想, 如果我们限定时间不超过T, 最少需要的抄写员 → 贪心法
    证明贪心法正确性: 假如最优答案不这么做, 可以把它变成这么做, 且最优性不变
- 从第一本书开始, 第一个人一直抄到时间即将超过T; 第二个人, ...
- 如果需要的抄写员>K, 说明答案一定>T (条件太苛刻, 放宽条件 --> 增加T); 反之答案<=T (条件太宽松 --> 减少T) → 二分答案
    两个序列, 抄完需要的人 (单调递减), 抄完需要的时间 (单调递增)
- 上界: 一个人抄, A[0]+ .. +A[n-1]; 下界: 很多人抄 max{A[i]}

LintCode 633.[Find the Duplicate Number]()
给定一个长度为n+1的数组, 其中均为1到n之间的整数; 保证只有一个数字重复了多次; 找到这个数字 (辅助空间只能O(1); 只能开几个变量..)
输入: [5,5,5,1,2,3] 输出: 5
* Soln 1: 双重for循环
* Soln 2:
    [1, 2, .. P-1, P, P, P, P+1, n] 共n-1个数, 则大于P的最多n-P个数字; 小于等于P的数字多于n+1-n-P=P+1个
    若x > P, 小于等于x的数字多于x+1个; 若x < P, 小于等于x的书最多x个   → 找到了 ‘分水岭’
    - ≤w的数小于w个, P在右边; ≤w的数大于w个, w=P 或 P≤w (左边)

    - 假设答案是S, 数组一定是(假设排好序) [1,3,...,S,...,S,S+1,...,n], 那么其中<=S的数大于S
    - 对于所有T >= S, <=T的个数大于T
    - 对于所有T < S, <=T的个数小于等于T
    - TC=O(nlogn) (求小于等于某数的数字有多少个, O(n); 二分, O(logn))

LintCode 617.[Maximum Average Subarray II]() 二分答案的典型题目
给定一个数组A, 找到其中平均值最大的子数组, 要求长度>=k
输入: [1, 12, -5, -6, 50, 3], k = 3  输出: 15.667   (-6+50+3)/3=15.667

如果要求和最大, 可以用前缀和数组。但是平均值最大不好求 (数组问题, 求平均值一般都较难, 因为既和总和有关, 又和个数有关)
* Soln 1: 枚举起点和重点, 使用前缀和数组 (双指针不行)
* Soln 2: 二分答案
    - 判断性问题: 子数组平均值能否 ≥ T?
    - 如果最大平均值是T, 则目标是找到(A[left] + ... + A[right]) / (right - left + 1) >= T, 且right - left + 1 >= k
    - 即(A[left]-T) + ... + (A[right]-T) >= 0
        对于一个T, 把每个元素A[i]减去T得到B[i]
        希望找到最大的B[left] + ... + B[right] >= 0, 且right - left + 1 >= k
        可以通过前缀和实现
        如果找不到这样的(left, right), 说明答案小于T → 二分答案

# 2. 搜索 Search
* BFS 的主要数据结构是 Queue, DFS 的主要数据结构是 Stack
* 使用 BFS → 图的遍历问题(层级遍历, 联通问题灌水法, 拓扑排序) + 简单图最短路径问题
    什么时候应该使用BFS? (BFS 就是循环)
    - ① 图的遍历 Traversal in Graph
        层级遍历 Level Order Traversal (起点 → 一层一层遍历)
        由点及面 Connected Component (A&B能否联通)
        拓扑排序 Topological Sorting
    - ② 最短路径 Shortest Path in Simple Graph
        仅限简单图求最短路径 (简单图: 图中每条边长度都是1, 且没有方向 unweighted & undirected)
        BFS只能解决边长为1的最短问题, 还可以用动态规划DP
        求最长路径: DFS, DP
    **队列 Queue**
    支持操作: O(1) Push / O(1) Pop / O(1) Top
    BFS的主要数据结构, 多做做BFS的题就可以了

* 使用 DFS → 找所有的方案; 找最优的问题, 找最短/最长问题 (但很少)
    什么时候用 DFS? 求所有方案时 (90% DFS的题, 要么是排列, 要么是组合)
    怎么解决DFS? Recursion (不特别说明的话, DFS用recursion实现; 有几道题需要掌握non-recursion的方式)
    Note: DFS把结果放入results中, 一定要使用deep copy! (面试时脚本语言(Ruby, Python)更占便宜)
    **栈 Stack** 
    支持操作: O (1) Push / O(1) Pop / O(1) Top 
    非递归实现DFS的主要数据结构

难度 BFS < DFS < DP

## 2.1. 宽度优先搜索 Breadth First Search
什么时候应该使用BFS? (BFS 就是循环)
* ① 图的遍历 Traversal in Graph
   - 层级遍历 Level Order Traversal (起点 → 一层一层遍历)
   - 由点及面 Connected Component (A&B能否联通)
   - 拓扑排序 Topological Sorting
* ② 最短路径 Shortest Path in Simple Graph   
    仅限简单图求最短路径 (简单图: 图中每条边长度都是1, 且没有方向 unweighted & undirected)

如果题目问最短路径, 除了BFS还可能是什么算法? BFS只能解决边长为1的最短问题, 还可以用动态规划DP
如果问最长路径呢? DFS, DP

### 2.1.1. 二叉树上的宽度优先搜索 BFS in Binary Tree
创建一个队列, 把起始节点放进去 (第一层节点)
while队列不空, 处理队列中的节点, 并拓展出新的节点 (for 上一层节点, 拓展下一层节点 → 层级遍历)
level x → x+1

if root is None: return [ ]    # 而不是 return None !!!

Lintcode 69.[Binary Tree Level Order Traversal]() 图的遍历(层级遍历) 
树是图的一种特殊形态, 树属于图

#### 2.1.1.1. Soft and Deep Copy (深度拷贝)
A deep copy constructs a new compound object and then, recursively, inserts copies into it of the objects found in the original.
```java
import java.util.ArrayList;

public class HelloWorld{
    public static void main(String []args){
        ArrayList<Integer> list1 = new ArrayList<>();
        ArrayList<Integer> list2 = list1;    // soft copy, 只copy了reference
        list1.add(1);       		// list1, list2均为 [1]
        ArrayList<Integer> list3 = new ArrayList<>(list1);  // deep copy/clone, copy content
        list1.add(2);  			    // list3为[1], list1, list2为[1, 2]
    }
}
```

deep copy in BFS → 每次加进去的是相同的东西
no deep copy → 每次加进去的是新new出来的东西

宽搜BFS使用队列Queue作为主要的数据结构  (Queue可以用linked list实现, delete/add为O(1))
用栈(Stack)是否可行? BFS标配Queue, DFS标配Stack

#### 2.1.1.2. 层级遍历
需要分层的算法比不需要分层的算法多一个循环 size=queue.size()

如果直接 for (int i = 0; i < queue.size(); i++) 会怎么样?   for上一层节点, 拓展出新的节点
queue.size()在变化 → 所有的东西都挤在一层

### 1.6.1. Serialization 序列化
将内存中结构化的数据变成"字符串"的过程  (在传输中很重要)
序列化:object to string 反序列化:string to object

什么时候需要序列化?
* ①将内存中的数据持久化存储时
    内存中重要的数据不能只是呆在内存里, 这样断电就没有了, 所需需要用一种方式写入硬盘, 在需要的时候, 能否再从硬盘中读出来在内存中重新创建
* ②网络传输时, 机器与机器之间交换数据的时候, 不可能互相去读对方的内存。只能讲数据变成字符流数据(字符串)后, 通过网络传输过去。接受的一方再将字符串解析后到内存中。 

常用的一些序列化手段:
- XML 耗费空间, 但可读性高
- Json 和JS兼容
- Thrift (by Facebook)  可以序列化, 也可以做别的。
- ProtoBuf (by Google) 可以序列化, 也可以做别的。可以远程函数调用

例:
- 一个数组, 里面都是整数, 我们可以简单的序列化为"[1,2,3]"
- 一个整数链表, 我们可以序列化为 "1->2->3"
- 一个哈希表(HashMap), 我们可以序列化为 "{\"key\": \"value\"}"

序列化算法设计时需要考虑的因素:
* ①压缩率: 对于网络传输和磁盘存储而言, 当然希望更节省
  如 Thrift, ProtoBuf 都是为了更快的传输数据和节省存储空间而设计的
* ②可读性: 希望开发人员, 能够通过序列化后的数据直接看懂原始数据是什么。如 Json, LintCode 的输入数据

二叉树序列化 Binary Tree Serialization & 多叉树序列化
二叉树可以使用任何方法进行序列化, 只要保证能够解析回来即可。
LintCode采用的是BFS的方式对二叉树数据进行序列化, 好处是可以更为容易的自己画出整棵二叉树。

算法描述: http://www.lintcode.com/en/help/binary-tree-representation/  层级遍历

Lintcode 7.[Serialize and Deserialize Binary Tree]()

toString() 算序列化
Note: 现在配置文件流行用yaml, 以前用html, 后来用json

Lintcode 70.[Binary Tree Level Order Traversal II]()
Lintcode 71.[Binary Tree Zigzag Level Order Traversal]()
Lintcode 242.[Convert Binary Tree to Linked Lists by Depth]()

### 1.6.2. 图上的宽度优先搜索 BFS in Graph & 拓扑排序 Topological Sorting(必考)
和树上有什么区别? 树→父子关系; 图→双向关系, 可能存在地位平等(邻居关系)   directed/undirected graph
图是点和边组成的结构, 甚至可以不联通  G = < V, E > 

套用social network背景来考察图 (六度理论: 问A和B是几度关系? 用BFS, 从A开始层级遍历)
 
图中存在环(图和树的本质区别) --> 同一个节点可能重复进入队列
图中BFS时, 用hashmap/hashset记录是否完成任务

Lintcode 178.[Graph Valid Tree]()
图的遍历(由点及面) 图是树的 (条件1) N个点, N-1条边 (条件2) N个点连通 (从o出发可以联通所有点)
	BFS求连通性: 灌水法 flood fill. queue当前队列, hashset放入所有进入过队列的点 (看哈希表是不是n个数)

如何用基本数据结构表示一个图?  用hashmap {vertex, its neighbors} → {integer, hashset(int)} 

Lintcode 137.[Clone Graph]() = deep copy		
图的遍历(由点及面)  copy nodes, copy edges
训练code structure的好题, 所有程序实现在一个函数, 逻辑不清晰; 好程序其实不需要注释, 就能读懂

独孤九剑——破枪式
能用 BFS 解决的问题, 不要用 DFS! (除非面试官特别要求)
因为用 Recursion 实现的 DFS 可能造成 StackOverflow! (Non-Recursion 的 DFS你不会写, 面试官也看不懂)

Lintcode 618.[Search Graph Nodes]() 
图的遍历(由点及面) 为什么不需要做分层遍历?
如何找所有最近的value=target的点? 分层遍历

Lintcode 127.[Topological Sorting]()
拓扑排序可以用来检测循环依赖 (e.g 先修课程的问题), 拓扑排序排的是topo order (并不是一个排序算法)
几乎每个公司都有一道拓扑排序的面试题! 
indegree(入度): 有多少条边指向此点,   hashmap 点→点的入度   
入度为0的点为start node, 将入度0的放进队列进行BFS
可以使用 DFS 来做么? 可以 (但不用递归, 用stack)

Lintcode 615.[Course Schedule]()
Lintcode 616.[Course Schedule II]() 裸拓扑排序
Lintcode 605.[Sequence Reconstruction]()
判断是否只存在一个拓扑排序的序列, 只需要保证队列中一直最多只有1个元素即可

能不能被拓扑排序? 判断有没有入度为0的点

### 1.6.3. 棋盘上/矩阵中的宽度优先搜索 BFS in Matrix (格子图)
图 Graph: N个点, M条边, M最大是 O(N^2) 的级别 (两两连通), 图上BFS时间复杂度 O(N + M)   (点边之和)
    说O(M)问题也不大, 因为M一般都比N大 所以最坏情况可能是 O(N^2)
矩阵 Matrix: R行C列, R * C个点, R * C * 2 条边(每个点上下左右4条边, 每条边被2个点共享), 矩阵中BFS时间复杂度 O(R*C)

Lintcode 433.[Number of Islands]()
图的遍历(由点及面)

四个方向用四个if语句非常bad, 用坐标变换数组和if语句; inBound函数, 测在不在边界范围内
坐标变换数组 deltaX, deltaY = [1, 0, 0, -1], [0, 1, -1, 0]
如何写出八个方向的坐标变换数组?

Lintcode.[Zombie in Matrix]()
图的遍历(层级遍历)  分层遍历
大写variable name来定义常量, 甚至可以加static, 写在外面, 不要写在程序里!!
public int PEOPLE = 0;
public int ZOMBIE = 1;
public int WALL = 2;
// 千万别写 grid[?][?] == 1;    // bad coding style, 1是什么不直观

Lintcode.[Knight Shortest Path]()
简单图最短路径  八个方向 BFS
follow up: speed up?

无向图联通块
    http://www.lintcode.com/problem/connected-component-in-undirected-graph/   

覆盖黑点的最小矩阵(BFS无法AC但是可以作为BFS的练习题)
    http://www.lintcode.com/problem/smallest-rectangle-enclosing-black-pixels/

简单图最短路径
    单词阶梯    http://www.lintcode.com/problem/word-ladder/
    建邮局问题 Build Post Office II 简单图最短路径  http://www.lintcode.com/en/problem/build-post-office-ii/
    (方法一) 从空格出发
        循环枚举所有的office修建未知的可能性(空格)
        计算从这个位置出发到达所有房子的距离之和
        在所有方案中找到最小的距离和
    (方法二) 从房子出发
        循环枚举所有的房子位置
        从房子出发, 机选每个空格到达房子的距离之和
        累加某个空格到达其他所有房子距离之和
        在所有空格中, 找到最小距离和

## 1.7. 深度优先搜索 Depth First Search
什么时候用 DFS? 求所有方案时

怎么解决DFS? Recursion(不特别说明的话, DFS用recursion实现; 有几道题需要掌握non-recursion的方式)

Note: DFS把结果放入results中, 一定要使用deep copy!

面试时脚本语言(Ruby, Python)更占便宜

独孤九剑 —— 破鞭式   
找所有方案的题, 一定是DFS
90% DFS的题, 要么是排列, 要么是组合

### 1.7.1. 组合搜索问题 Combination 2**n
问题模型: 求出所有满足条件的"组合"
判断条件: 组合中的元素是顺序无关的
时间复杂度: 与 2^n 相关, 因为 C[0][n] + C[1][n] + .. C[n][n] = 2^n, C[i][n]=n个数中取i个

一般来说, 如果面试官不特别要求的话, DFS都可以使用递归(Recursion)的方式来实现
递归三要素是实现递归的重要步骤: 递归的定义; 递归的拆解; 递归的出口

我们在第一节课中讲过的全子集问题 Lintcode 17.[Subsets](Done)就是典型的组合搜索问题

Lintcode 135.[Combination Sum](Done)
和subsets的区别?
- Combination Sum 限制了组合中的数之和 → 加入一个新的参数(target)来限制
- Subsets 无重复元素, Combination Sum 有重复元素 → 需要先去重
- Subsets 一个数只能选一次, Combination Sum 一个数可以选很多次 → 搜索时从 index 开始而不是从 index + 1

Lintcode 153.[Combination Sum II](Done)
如何去重? (错误做法) 找到所有结果后再去重  (正确做法) 选代表

Lintcode 136.[Palindrome Partitioning](Done)
如何优化?
- 用hashmap存储回文串, 但这样没效果
    getkey不是 O(1), 是O(size of key), 取决于用作key的字符串有多长..
- 用二维数组

### 1.7.2. 排列搜索问题 Permutation
(相比组合问题少start index, 但同一个数不能重复的选, 所以多一个set放使用过的数或者使用过数的下标)
问题模型: 求出所有满足条件的"排列"
判断条件: 组合中的元素是顺序"相关"的
时间复杂度: 与 n! 相关

Lintcode 15.[Permutations](Done)
Lintcode 16.[Permutations II](Done)
如何去重?

Lintcode 33.[N-Queens]()

### 1.7.3. Search in a Graph 图中的搜索
Lintcode 120.[Word Ladder]()
http://www.lintcode.com/problem/word-ladder/

Lintcode.[Word Ladder II]()
http://www.lintcode.com/problem/word-ladder-ii/

### 1.7.4. Non Recursion
基本上都会用上栈(Stack)
必“背”程序

Tree Traversal
Preorder Lintcode .[]()  http://www.jiuzhang.com/solutions/binary-tree-preorder-traversal/
Inorder Lintcode .[]()  http://www.jiuzhang.com/solutions/binary-tree-inorder-traversal/ 
PostorderLintcode .[]()  http://www.jiuzhang.com/solutions/binary-tree-postorder-traversal/
Tree Iterator Lintcode .[]()  http://www.jiuzhang.com/solutions/binary-search-tree-iterator/ 

Combination Lintcode 17.[Subsets]
Permutation Lintcode 15.[Permutations]()

### 1.7.5. DFS时间复杂度
O(答案个数 * 构造每个答案的时间)
* 搜索的时间复杂度: O(答案总数 * 构造每个答案的时间)
    Subsets问题, 求所有的子集。子集个数一共2^n, 每个集合的平均长度是O(n)的, 所以时间复杂度为O(n * 2^n), 同理Permutations问题的时间复杂度为O(n * n!)
* 动态规划的时间复杂度: O(状态总数 * 计算每个状态的时间复杂度)
    triangle, 数字三角形的最短路径, 状态总数约O(n^2)个, 计算每个状态的时间复杂度O(1)——就是求min。所以总的时间复杂度为O(n^2)
* 用分治法解决二叉树问题的时间复杂度: O(二叉树节点个数 * 每个节点的计算时间)
    二叉树最大深度。二叉树节点个数为 N, 每个节点上的计算时间为 O(1)。总的时间复杂度为O(N)


## 1.8. dijkstra's algorithm

# 2. Sweep Line 扫描线算法 处理区间问题的扫描线
见到区间需要排序, 就可以考虑扫描线 (区间问题巧妙解法)
扫描问题的特点: 1.事件往往是以区间的形式存在  2.区间两端代表事件的开始和结束  3.按照区间起点排序, 起点相同的按照终点排序
扫描线要点: 将起点和终点打散排序 [[1, 3], [2, 4]] => [[1, start],[2, start],[3, end],[4, end]]

有5架飞机的起飞降落时间为[[1, 10], [2, 3], [5, 9], [4, 7], [6, 11]], 区间左端点代表飞机的起飞时间, 右端点为飞机的降落时间, 同时最多有多少架飞机在空中? 在时刻6, 共有第1345四架飞机在空中

LintCode 391: [Number of Airplanes in the Sky]() 扫描线经典入门题目
给定n架飞机的起飞降落时间, 求最多时天上有多少飞机; 如果一架飞机的降落时间恰好等于另一架飞机的起飞时间, 则认为先降落
输入: [[1, 10], [2, 3], [5, 8], [4, 7]]  输出: 3
* Soln 1: 事件event是关键点 (1 2 3 4 5 7 8 10)
    没有事件发生的空白区域, 飞机数目不变
    检查端点, n条线段, 2n端点, O(n^2)
* Soln 2:
    - 将每架飞机的起降时间作为区间左右端点, 建立两个事件
    - 对所有事件排序, 相同时间的事件降落排在起飞前面  排序O(nlogn)
    - 扫描: O(n)
        扫描线, 定义计数器 t=0时, C=0 (0飞机)
        遇到起飞事件(左端点, 加事件), C+=1; 遇到降落事件(右端点, 减事件), C-=1
        C的最大值即为答案
* Python使用HashHeap, Java用TreeSet/TreeMap, C++可以用Map/Multimap
* Follow-Up: 如果同时起降, 认为先起飞, 怎么修改算法? 相同时间起降, 起飞排在降落前

LintCode 131.[The Skyline Problem/Building Outline]()
给定n个矩形的坐标, 底边都在X轴, 求出所有矩形组成图形的外轮廓线/天际线  (覆盖这一点的矩形, 谁最高)
输入: [[2, 9, 10], [3, 7, 15], [5, 12, 12], [15, 20, 10], [19, 24, 8]]
输出: [[2, 10], [3, 15], [7, 12], [12, 0], [15, 10], [20, 8], [24, 0]]
* 将每个矩形的左边和右边建立两个事件, 记下对应高度
* 对所有事件按X坐标排序, 从小到大  TC=O(nlogn)
* 建立高度的最大堆 (动态维护, 添加/删除/求最大元素的操作, 用优先队列/堆)
* 扫描线:
    遇到左边事件, 堆中加入高度
    遇到右边事件, 堆中删除高度
    堆中最大值即为组合图形现在的高度
* 将同一个X坐标的事件全部处理完后, 如果新高度(新堆中最大值)≠原来的高度, 说明出现拐点, 记录下来
* Follow-Up: 形成的面积?
* Building Outline算法动图模拟 https://briangordon.github.io/2014/08/the-skyline-problem.html

哪种数据结构有快速的添加元素, 删除元素, 求最大元素值的操作? 堆/优先队列, 可以在O(logn)的时间复杂度中完成添加元素, 删除元素, 求最大元素值的操作。单调栈也可以, 但优先队列更方便

LintCode 919. [Meeting Rooms II]()

LintCode 821. [Time Intersection]() F家高频题 输出两组区间的交集


# 3. 两根指针 Two Pointers

## 3.1. 同向双指针
*** Lintcode 604-Window Sum
*** Lintcode 521-Move Zeroes 
*** Lintcode 521-Remove Duplicate Numbers in Array

## 3.2. 相向双指针
http://www.lintcode.com/problem/valid-palindrome/
http://www.lintcode.com/problem/rotate-string/ 
http://www.lintcode.com/en/problem/recover-rotated-sorted-array/

## 3.3. Two Sum & its variation
*** Lintcode 56-Two Sum
return 下标的话无论用hashmap还是sort+two pointers, 额外空间一定是O(n)
但是如果return的是满足条件的数值, 使用sort+two pointers, 额外空间是O(1)

只能用 HashMap: 
*** Lintcode 607-Two Sum III - Data structure design
http://www.lintcode.com/problem/two-sum-data-structure-design/ 

sorted array用 Two Pointers 会更快 (两个pointer一头一尾)
*** Lintcode 608-Two Sum II - Input array is sorted

*** Lintcode 587-Two Sum - Unique pairs
http://www.lintcode.com/en/problem/two-sum-unique-pairs/
是否可以先去重?

3Sum
http://www.lintcode.com/problem/3sum/
统计所有的和为 0 的三元组 (Triples)

Triangle Count
http://www.lintcode.com/problem/triangle-count/

独孤九剑 —— 破掌式 对于求 2 个变量如何组合的问题
可以循环其中一个变量, 然后研究另外一个变量如何变化

Two Sum 计数问题
统计所有和 <= target 的配对数 
http://www.lintcode.com/problem/two-sum-less-than-or-equal-to-target/ 

统计所有和 >= target 的配对数 
http://www.lintcode.com/en/problem/two-sum-greater-than-target/ 

Two Sum Closest
http://www.lintcode.com/problem/two-sum-closest-to-target/

Follow Up: 3Sum Closest
http://www.lintcode.com/problem/3sum-closest/

Related  Lintcodes
  4Sum
  http://www.lintcode.com/problem/4sum/
 
  Two Sum - difference equals to target (同向双指针)
  http://www.lintcode.com/problem/two-sum-difference-equals-to-target/

## 3.4. Partition Array 分割数组
Quick Select
分成两个部分
分成三个部分
一些你没听过的(但是面试会考的)排序算法

31. Partition Array
http://www.lintcode.com/problem/partition-array/


Quick Select
http://www.lintcode.com/problem/kth-smallest-numbers-in-unsorted-array/

小视频:http://www.jiuzhang.com/video/quick-select/

Related  Lintcodes
  Partition Array by Odd and Even
  http://www.lintcode.com/problem/partition-array-by-odd-and-even/
  http://www.jiuzhang.com/solutions/partition-array-by-odd-and-even/  
  Interleaving Positive and Negative Numbers
  http://www.lintcode.com/problem/interleaving-positive-and-negative-numbers/
  http://www.jiuzhang.com/solutions/interleaving-positive-and-negative-integers/  
  Sort Letters by Case
  http://www.lintcode.com/problem/sort-letters-by-case/
  http://www.jiuzhang.com/solutions/sort-letters-by-case/

Sort Colors
http://www.lintcode.com/problem/sort-colors/
分成两个部分 vs 分成三个部分

排序 Rainbow Sort
http://www.lintcode.com/en/problem/sort-colors-ii/
问:猜一猜最优的时间复杂度?

其他有趣的排序
烙饼排序 Pancake Sort(有可能会考哦) 
https://en.wikipedia.org/wiki/Pancake_sorting 
http://www.geeksforgeeks.org/pancake-sorting/
睡眠排序 Sleep Sort https://rosettacode.org/wiki/Sorting_algorithms/Sleep_sort
面条排序 Spaghetti Sort https://en.wikipedia.org/wiki/Spaghetti_sort
猴子排序 Bogo Sort https://en.wikipedia.org/wiki/Bogosort
  (还有前面学的拓扑排序)

unique pairs
closest to target
difference = target


# 4. 递归 Recursion
递归是一种程序设计方式
①递归的概念 	前置知识—函数 (定义&调用函数)     递归的三要素 (定义, 拆解, 出口)
②递归调用栈 内存的堆栈 (内存空间=堆 or 栈)  回溯
③值传递和引⽤传递 (参数传递方式) 
④递归综合训练   e.g. 汉诺塔, 排列组合

## 4.1. 递归的概念
我们生活过程中处理事情主要运用的是什么思想? 我们生活中主要运用迭代思想, 从已知推向未知

### 4.1.1. 递归的三要素
(递归, 函数的一种调用形式; 与普通函数类似)
* ①递归的定义: 接受什么参数(参数列表), 返回什么值, 代表什么意思 
    - 当函数直接或者间接调用⾃己时, 则发⽣了递归(函数内部出现对自己的调用)
    - 递归的定义: 参见"递归的定义"
    - 递归缩写: Bing - Bing Is Not Google; GNU - GNU's Not Unix; PHP - PHP: Hypertext Preprocessor
* ②递归的拆解: 每次递归都是为了让问题**规模变小**
* ③递归的出口: 必须有⼀个明确的结束条件(递归不会无限进行下去; 类似循环结构)
→ 得到⼀个可供其他函数调用的递归函数

```java
int func(int n){    // 1.递归函数的定义
// 3.递归的出口 (一般递归出口在函数体一开始)
    if (n == 1){ return 1; }
// 2.递归的拆解
    return func(n - 1) * 2 + 1; // (n - 1) 使得问题规模变小
}
```

LintCode 1807.[Fibonacci easy]() 斐波那契数列, 计算斐波那契数列的第n项
- 定义: 斐波那契数列指的是这样⼀个数列0,1,1,2,3,5,8,13,21,34.. 这个数列从第3项开始, 每⼀项都等于前两项之和 (第一项有时为0, 有时为1)
- 关系式: F[i]=F[i−1]+F[i−2]
- 递归函数:
    ```java
    int fib(int n){  // 函数的定义
        if (n <= 2) {  // n=1 or n=2 (第1, 2项)
            return n == 1 ? 0 : 1; // 函数的终止条件
        }
        return fib(n - 1) + fib(n - 2); // 拆解
    }
    ```
* 递归算法, 使用 functools.lru_cache 缓存结果

递归的执⾏过程/递归调用树
(图)
→ DFS顺序

LintCode 366.[Fibonacci]()
* Soln 1: 递归, 复杂度O(2^n), 空间复杂度为O(1), 会超时;
    - fibonacci[i] = fibonacci [i - 1] + fibonacci[i - 2], 故递归式为 thisFibonbacci = dfs(i) + dfs(i - 1)
    - 这么做的有很多被重复计算的数字, 时间复杂度难以接受
    - e.g 求解fib(10), 会找到fib(9)和fib(8)共两个, 然后下一层是fib(8)和fib(7), fib(7)和fib(6)共四个。这是一个呈指数增长的曲线, 其底数为2, 是稳定超时的代码

* Soln 2: 记忆化递归, 时间复杂度O(n), 空间复杂度为O(n)
    - 以空间换时间的优化算法
    - 将计算出的结果存储下来, 在计算到指定值的时候, 先判断这个值是否已经计算过, 若没有, 才进行计算, 否则读取已经存储下来的值。这样就把一个指数级复杂度变成了线性复杂度, 代价是空间复杂度从常数级上升至线性级

* Soln 3: 递推法/循环, 时间复杂度O(n)
    - 动态规划的滚动数组思想, 节省空间: 并不需要存储那么多的fibonacci数, 因为是返回第n项, 并且第n项只和前面的两个数字有关, 所以利用一个长度为2的空间记录前两个数字即可; 时间复杂度不变, 空间复杂度降为O(1)
    
* follow-up: 不超出Integer的斐波那契数很少, 仅有50个左右。 求下标很大的fibonacci数, 并取模数
* Soln 4: 矩阵快速幂 (Fibonacci II)

LintCode 949.[Fibonacci II]()
alternative formula for the Fibonacci sequence:
matrix [[F[n+1], F[n]], [F[n], F[n-1]]] = [[1, 1], [1, 0]] ^ n  = n times of matrix [[1, 1], [1, 0]]
* 矩阵快速幂 
    - LintCode 140.[Fast Power]()   
        Calculate the a^n % b where a, b and n are all 32bit non-negative integers.
    - 矩阵的乘法运算原理: 
    ```
    假设有一个2×2的矩阵 [[1,1],[1,0]] 和 一个2×1的矩阵[[2],[1]], 两个矩阵相乘会变成[[3],[2]], 
    再用[[1,1],[1,0]]和新的矩阵[[3],[2]]继续相乘又会变成[[5],[3]], 继续运算就是[[8],[5]], [[13],[8]]...
    神奇的事情出现了, 当不断地用[[1,1],[1,0]]乘上初始矩阵, 得到的新矩阵的上面一个元素就会变成的fibonacci数列中的一个数字, 
    下面的元素则是上面元素的前一项, 而且每多乘一次, 这个数字的下标就增加一。
    那么这个矩阵是怎么来的呢?

    推理中发现：某个矩阵A乘上[[fib(n+1)], [fib(n)]]会变成[[fib(n+2)], [fib(n+1)]]。
    现在设矩阵为[[a,b], [c,d]], 则可以列出下面的等式：
    a fib(n + 1) + b fib(n) = fib(n + 2)
    c fib(n + 1) + d fib(n) = fib(n + 1)
    很容易地, 我们得到：
    1 fib(n + 1) + 1 fib(n) = fib(n + 2)
    1 fib(n + 1) + 0 fib(n) = fib(n + 1)
    也就是说矩阵是[[1,1], [1,0]]

    原矩阵M连续多次乘上某个矩阵A会得到新的矩阵M', 并且M'的第一个元素就是我们想要的值。
    根据矩阵的运算法则, 中间的若干次相乘可以先乘起来, 但矩阵乘法的复杂度是O(n^3), 是不是一次一次的乘有点慢呢? 
    我们可以使用快速幂来优化矩阵乘法的速度, 这就是矩阵快速幂算法。

    值得注意的是, 在快速幂中, 我们有一步操作是：int result = 1。那么如何使用矩阵来实现这个单位1呢, 我们要借助单位矩阵。
    所谓的单位矩阵是一个从左上角到右下角对角线上都是1, 其余位置都是0的边长相等的矩阵（方阵）。
    比如[[1,0,0],[0,1,0],[0,0,1]]。单位矩阵E的特性在于满足矩阵乘法的任意矩阵AE一定等于A, EA一定等于A。

    将初始矩阵设置为[[1],[0]], 这样只需要将中间矩阵[[1,1],[1,0]]使用快速幂连乘n-2次, 再和[[1],[0]]相乘, 矩阵就变成了[[fib(n)],[fib(n-1)]]

    矩阵快速幂算法常常被应用在递推式的加速中, 可以很轻松的递推至下标相当大的位置, 而不用担心超时
    但是要注意以下两点：
    - 矩阵快速幂使用的过程中要注意是否应该取模, 因为C++和Java会有数值溢出, 如果题目要求递推式取模, 那么有很大概率是一道矩阵快速幂题目
    - 矩阵乘法是没有交换律的（AB ≠ BA）, 因此我们一定要注意乘法顺序

    矩阵乘法是矩阵大小L的三次方, 需要乘logn次。所占的空间一般只有矩阵的空间, 同样是L的三次方
    因此时间复杂度为O(L^3 * logn), 空间复杂度为O(L^3)
    ```

LintCode 771.[Double Factorial]() ⼆阶阶乘/双阶乘, 计算n!!
- 定义: 用符号!!表示, 正整数的双阶乘表示不超过这个正整数且与它有相同奇偶性的所有正整数乘积, 比如 5!! = 5 * 3 * 1 = 15, 6!! = 6 * 4 * 2 = 48   
- 关系式: F[i] = i * F[i−2]
- 递归函数:
    ```java
    int doubleFactorial(int n) {    //阶乘的增长非常快
        if (n <= 3) { // 1=1, 2=2, 3=3*1=3
            return n;
        }
        return n * doubleFactorial(n - 2);
    }
    ```
- 递归的执⾏过程	5!!  df(5) → df(3)		6!!  df(6) → df(4) → df(2)		7!!  df(7) → df(5) → df(3)

盗梦空间与递归 (略)

LintCode 1333.[Reverse Bits]()给⼀个 32 位⽆符号整数, 颠倒它的二进制位
Reverse bits of a given 32 bits unsigned integer
⽐如给 1, 即 00...01, 颠倒之后得到 100...00, 即 2147483648   (max int = 2147483648﹣1, int需要一位记录正负)
以 long 类型的形式进行输⼊输出

利用位运算可以获取⼀个整型的每一个二进制位, 相当于反转⼀个列表
- 递归的思路: 取出列表的最后一个; 递归调用, 反转列表的前n-1个; 把最后一个放到列表最前⾯
    ```java
    // 调用: 需要反转 [31, 0]
    // 终止条件: if(pos == 31) {return n;}
    // 拆解: 需要反转 [31, pos] 之间的位
    long last = n & 1; // 取最后一位
    long ret reverseBits(n >> 1, pos + 1); // 右移一位
    ret += last << (31 - pos);  // 左移(31-pos)位

    // 111..01  last=1
    // 111..0   ret=0..111
    // return 1(第31-pos位)111..0
    ```

### 4.1.2. 递归与非递归方法的比较
递归能做的很多, 不一定要像前⾯两个问题一样有严格的公式 —> 递归思路: 进行问题的拆解, 将问题的规模变小, 一步步趋近于直接可以得到答案的问题

LintCode 822.[Reverse Order Storage]() 
Give a linked list, and store the values of linked list in reverse order into an array.
反转链表: 给⼀个链表, 将这个链表反转之后的元素依次存⼊一个数组, 返回这个数组
- ⾮递归方法解决: 需要⽤栈或者是数组这样⼀个数据结构来辅助 (Stack先进后出, 元素依次入栈; 数组使用两根指针来翻转数组)
- 递归方法解决: 出口 head == null
递归⽅法的另⼀种写法 (使用一个重载的辅助函数)


## 4.2. 递归调用栈
内存中的堆和栈
* 递归深度太⼤容易 “爆栈” Stack Overflow, Segment Fault (桶满了..)
* 堆空间: heap
    - 存放 new 得到的对象(实例)
    - 无限制 (=剩余内存⼤⼩)
* 栈空间: stack
    - 存放对象的引用, 值类型变量(Java), 数组(C/C++), 以及函数调用信息(函数从谁调用的; 结束之后返回带哪里去执行)
    - 有限制, 一般很小, MB量级
对象在堆空间, 但是对象的引用在栈空间
Java的数组存在堆空间, 访问数组通过数组的引用, 在栈空间; C++把普通数组存在栈空间 int a[100];
   
想象一个 “桶” (栈空间), 调⽤的函数需要放到桶里, 第一个进入“桶”的是main()函数
每发生一次新的函数调用, 就会有一个新函数进入“桶”
正在执行的就是最上面的函数; 一个函数执行完毕, 就会被拿出来(一个函数占用“桶”的空间与参数、局部变量的数量有关)

### 4.2.1. 回溯法Backtracking
* 暴力搜索法的⼀种
* 试探着找问题的解, 如果到某一步发现上一次的选择不优或者达不到目标, 则退⼀步重新选择 
* 回溯是递归函数中经常发生的现象
经典问题: ⼋皇后     
Lintcode 33.[N-Queens]()                                         

LintCode 97.[Maximum Depth of Binary Tree]() 二叉树最⼤深度
二叉树中, 一个节点的深度是该节点到根节点的距离+1, 给定一棵二叉树, 问其中最大的节点的深度是多少
F[i] = max(F[i].left, F[i].right) + 1    F[null] = 0
递归层数与深度有关  

### 4.2.2. 二分查找/搜索 Binary Search 的递归写法 (二分)
在有序数组(假定升序) 中查找某一特定元素 X. 若有重复, 返回任意⼀个下标
1.若数组为空, 查找失败, 不存在 (边界判断)
2.若中间元素恰好是 X, 查找结束
3.若中间元素⼤大于 X, 则到左边的区间继续搜索, 转 1 
4.若中间元素⼩小于 X, 则到右边的区间继续搜索, 转 1
每次把区间长度减掉⼀半, 时间复杂度 O(logN)

LintCode 457.[Classical Binary Search]()
LintCode 14.[First Position of Target]()
LintCode 458.[Last Position of Target]()

## 4.3. 值传递和引⽤传递
函数调用的参数传递 (和返回值返回方式)
- Java 值传递, 引用传递
- C++ 值传递, 引用传递, 地址传递   
- Python 值传递, 引用传递

### 4.3.1. 值传递
"盗梦空间" 中, 下层梦境中的人的生死与上层梦境⽆关. 函数内部创建⼀个新的变量, 把值拷贝, 相当于⼀个副本
- Java基本数据类型 (byte, short, int, long, float, double, char, boolean)
- C++ 默认值传递
- Python 值类型 (类似于 Java)
- Java类成员中, 若有 final 修饰, 可以认为具有值传递的特性

### 4.3.2. 引⽤传递
引用, 可以理解为别名, 代号
⽐如我们可以用称号代指某个人 —— 李白: 诗仙, 青莲居士
传引用相当于起了一个新的称号, 代指原本的内容, 本质上是地址

- Java 类的实例     Java中类的实例本身就是引用  A x = new A();
- C++ 在参数列表中加 & 修饰
- Python 引⽤类型 (类似于 Java, ⽐如列表 (可以认为是list类的实例), 类的实例)   
- Java 类成员中, 若有 final 修饰, 可以认为是值传递

*想要知道 Java 的某个类呈现值传递的特性还是引用传递的特性?   查资料/试验!*

值传递和引⽤传递的主要区别: 内容是否复制; 空间占⽤ / 复制的时间消耗; 修改是否影响上⼀层
递归要在保证正确性的前提下, 尽可能提高效率. 需要考虑不仅参数传递, 还有返回值 (→尽量传引用)
   
LintCode 22.[Flatten List]() 列表扁平化
给⼀个列表, 每个元素可能是⼀个整数, 也可能是⼀个列表, 将其转化为⼀个只包含整数的简单列表
比如 [1, [2, 3], [4, [5]]] 应该被转化为 [1, 2, 3, 4, 5]
对于 Java / C++ 提供特定的接口: 判断⼀个元素是否整数; 返回这个整数 (仅在是整数的时候可调⽤用) ;  返回这个列表
- 递归的定义: flatten(nestedList) 传⼊列表, 返回扁平化的列表
- 递归的拆解: nestedList 中的每个列表元素都递归地调⽤ flatten() 进⾏扁平化 
- 递归的出⼝: 列表中的元素均为整数

⼆叉树的遍历 Binary Tree Preorder/Inorder/Postorder Traversal
LintCode 66.[Binary Tree Preorder Traversal]() 
LintCode 67.[Binary Tree Inorder Traversal]() 
LintCode 68.[Binary Tree Postorder Traversal]() 
使⽤递归可以访问⼀颗⼆叉树的所有节点
定义: traverse(node) 		拆解: traverse(node.left/right) 	  出⼝: node == null
⼆叉树的三种遍历顺序: 前/中/后序遍历   前序列:124356	中序列:421536	后序列:425631
* 前序遍历: 先访问当前节点, 再访问左右子树
* 中序遍历: 先访问左⼦树, 再访问当前节点, 最后访问右子树   
* 后序遍历: 先访问左右子树, 再访问当前节点

LintCode 72.[Construct Binary Tree from Inorder and Postorder Traversal]() 确定⼀棵⼆叉树
三种遍历序列, 其中⼀个相同, ⼆叉树不⼀定相同
* 中序列相同, 前序列相同, ⼆叉树相同
* 中序列相同, 后序列相同, ⼆叉树相同
由⼆叉树的中序列再加上前/后序列之⼀即可确定⼀棵⼆叉树 (必须⽆重复节点)

中序列:425136   后序列:452631

⼦树的序列是连续的
后序列的最后⼀个是当前序列对应的⼆叉树的根节点 
再由中序列可以确定左右子树的序列长度
递归的定义: buildTree(inorder, postorder)
递归的拆解: root.left = buildTree(leftInorder, leftPostorder)    	root.right = buildTree(rightInorder, rightPostorder) 
递归的出口: inorder == postorder == ""

## 4.4. 递归综合训练
LintCode 551.[Nested List Weight Sum]() 嵌套列表加权和
在 22. Flatten List 中提到了嵌套列表 (平化嵌套列表)
现在我们要求这样⼀一个列列表的元素的加权和, 每个元素的权重就是这个元素的深度  (元素×权重)
比如[1,[2,3]]的加权和就是1×1+2×2+3×2=11    [1,[2,[3]]]的加权和就是1×1+2×2+3×3=14 

相当于 22 的 follow up 
LintCode 22 的解决⽅法
- 递归的定义: flatten(nestedList) 传⼊入列表, 返回扁平化的列表
- 递归的拆解: nestedList 中的每个列表元素都递归地调用 flatten() 进⾏扁平化
- 递归的出口: 列表中的元素均为整数
在 22 的基础上思考
- 递归的定义: 增加⼀个参数, 表示当前的深度 (传入列表和当前列表(中整数的)深度, 返回列表的加权和)
- 递归的拆解: 递归调⽤时注意深度的改变 (调用时深度+1)
- 递归的出口: 不变

LintCode 1359.[Convert Sorted Array to Binary Search Tree]() 根据有序数组构造
Binary Search Tree ⼆叉搜索树, 一种特殊的⼆叉树(对于每个节点, 左子树的节点都⽐它⼩, 右子树的节点都⽐它大)
给⼀个有序的数组, 返回一棵合法的二叉搜索树  (中序遍历BST按顺序得到所有元素)

⽐如[1,2,3,4,5], 合法的构造: 

选定⼀个点作为根节点, 由它左边的元素构造左子树, 右边的元素构造右⼦树 (数组有序) 
递归三要素:
- 递归的定义: buildTree(arr) 返回由有序数组 arr 构造的 BST
- 递归的拆解: root.left = buildTree(subarr) 	root.right = buildTree(subarr)
- 递归的出⼝口: arr == null 

增加要求:
    ⼆叉树的深度最小 (LintCode 177)
    ⼆叉树的每⼀个节点的两个子树的最⼤深度相差不超过 1 (LintCode 1359) 
思考: 递归的哪⼀步影响⼆叉树的深度?

LintCode 1106.[Convert Sorted Array to Binary Search Tree]() 最⼤二叉树
给⼀个⽆重复元素的数组, 按照以下规则构造⼀棵二叉树	
根节点是当前数组中最⼤的元素	
使⽤用最⼤元素左侧的子数组构造左子树, 右侧的⼦数组构造右子树 
比如[3,2,1,6,0,5]  --> T(6, T(3, None, T(2, None, T(1)), T(5, T(0), None))

- 递归的定义: buildTree(arr) 返回由数组 arr 构造的⼆叉树 
- 递归的拆解: root.left = buildTree(subarr)	root.right = buildTree(subarr) 
- 递归的出口: arr == null

LintCode 469.[Same Tree]() 是否相同的二叉树 identical binary tree
给两棵⼆叉树, 判断它们的结构是否完全相同 (每一个节点权值相等, 并且左右子树也一样)
两棵⼆叉树相同, 当且仅当: 根节点的权值相同; 左⼦树相同; 右⼦树相同 

- 递归的定义: isIdentical(a, b)
- 递归的拆解: isIdentical(al, bl) && isIdentical(ar, br)
- 递归的出⼝口: a == null || b == null 

也可以用序列化解决 → 序列化相同才相同

LintCode 470.[Tweaked Identical Binary Tree]() 可扭转左右子树 Tweaked Identical Binary Tree 
Follow up 添加一个条件: ⼆叉树的左右子树可以扭转 
如果原本的 "递归的拆解" 得到了 false, 那么就扭转⼀下再 "拆解" 一次 
- 递归的拆解: (isIdentical(al, bl) && isIdentical(ar, br)) || (isIdentical(al, br) && isIdentical(ar, bl)) 

LintCode 169.[Tower of Hanoi]() 汉诺塔
有 A, B, C 三根柱⼦和 N 个⼤小互不相同的圆盘 
一开始所有的圆盘都在A柱上, 并且放在下⾯的圆盘都⽐上面的要大 
每次可以将某个柱子上顶端的圆盘移动到另一个柱子上 
在移动过程中也必须满⾜下⾯的圆盘要比上面的⼤大 
问把所有圆盘从A移动到C柱, 最少需要多少次操作, 操作序列是什么? 

一次尝试 A => C 	A => B 	C => B
如果再 A=>C 就完成了最大的盘的一次移动, 最大的盘移动到了目标柱 C! 接下来可以递归来做! 

将3个盘从A移动到C, 先把前2个盘从A移动到B然后把最大盘从A移动到C最后把2个盘从B移动到C 

即想要移动N个盘:
- 递归处理"移动N-1个盘" 
- 把最⼤盘移动一下
- 递归处理 "移动N-1个盘"

- 递归的定义: hanoi(n, c1, c2, c3) 	// c1: n, c2: 0, c3: 0, c1 => c3 
- 递归的拆解: 
    hanoi(n - 1, c1, c3, c2) 
    // move the biggest one from c1 to c3 
    hanoi(n - 1, c2, c1, c3) 
- 递归的出口: n == 1 

# 5. 贪心 Greedy Algorithms
https://www.geeksforgeeks.org/activity-selection-problem-greedy-algo-1/

# 6. 分治 Divide & Conquer

# Graph

## BFS & DFS


## Dijkstra, 

## Flloyd Warshall

## MST 

## flow

# 7. String问题
ACM带刷班 
* Question 54-String to Integer (atoi)
* Question 1510-Buddy Strings
* Question 415-Valid Palindrome
* Question 53-Reverse Words in a String
* Question 78-Longest Common Prefix
* Question 1263-Is Subsequence
* Question 384-Longest Substring Without Repeating Characters
* Question 213-String Compression
* Question 1352-Compare Version Numbers
* Question 1542-Next Time No Repeat
* Question 92-Wildcard Matching

## Rabin Karp

## KMP

## Aho-Crosaick


# [Number Theory](https://www.geeksforgeeks.org/tag/number-theory/)
