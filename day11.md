# day11
##  150. 逆波兰表达式求值
细节处比较困难

The division between two integers always truncates toward zero

function divi is difficult

minus and divi 后pop除以先pop

divi只出int

## 239. 滑动窗口最大值
用deque

维护可能成为max的num

什么时候pop？，加入元素，size要大于k，deq[0]还是之前应该pop的值。

## 347.前 K 个高频元素

python: 

import heapq

min priority queue

invert the value we can implement min heap

functions:

myheap=[]

heapq.heappush(myheap,(fre,key))

heapq.heappop(myheap)

先hash出freq
再minheap 前k

