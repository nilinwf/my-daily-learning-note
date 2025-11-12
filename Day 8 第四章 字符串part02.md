# 代码随想录算法训练营74期|第三章 哈希表part02 


| 题目     | Leetcode地址 |
| ----------- | ----------- |
|344.反转字符串 | [力扣题目链接](https://leetcode.cn/problems/4sum-ii/)      |
|541.反转字符串II | [力扣题目链接](https://leetcode.cn/problems/ransom-note/)      |
|卡码网：54.替换数字 | [力扣题目链接](https://programmercarl.com/kamacoder/0054.%E6%9B%BF%E6%8D%A2%E6%95%B0%E5%AD%97.html)      |


反转字符串:使用双指针，注意的是，python可以直接赋值而不需要temp临时存储；

反转字符串II：在反转字符串操作基础上
    -1. 使用range(start, end, step)来确定需要调换的初始位置
    -2. 对于字符串s = 'abc'，如果使用s[0:999] ===> 'abc'。字符串末尾如果超过最大长度，则会返回至字符串最后一个值，这个特性可以避免一些边界条件的处理。
    -3. 用切片整体替换，而不是一个个替换.
    
卡码网：54.替换数字:已打卡



