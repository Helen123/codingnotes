# day 9
##  151.翻转字符串里的单词
我不太擅长python builtin code：
所以练习
```python
words=s.split()
reverse=words[::-1]
result=' '.join(reverse)
return result
```



## 卡码网：55.右旋转字符串

python:

需要新内存  s不能改

c++ 思路： 整体反转 加两次反转substring


## 28. 实现 strStr()  
KMP: 作用快速找出string中substring 的start index

next数组就是一个前缀表（prefix table）

定义两个指针i和j，j指向前缀末尾位置，i指向后缀末尾位置

j>0 s[i] != s[j] 回退

s[i] == s[j] j++
##  459.重复的子字符串  （本题可以跳过）


## 字符串总结 
##  双指针回顾 
复习了一下之前的挺好
