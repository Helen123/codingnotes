# day11
##  150. 逆波兰表达式求值
## 239. 滑动窗口最大值

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

