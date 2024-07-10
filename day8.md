# day8
## 344.反转字符串
简简单单～

但是while update index 不要忘啊 要不还写comment吧

## 541. 反转字符串II
我的超长傻子code：不知道用function的？？pyhton builtin 太多了不熟

**Python里面的string也是不可改的，所以也是需要额外空间的。空间复杂度：O(n) s=list(s) s=''.join(s) **

还可以写helper function
   ```markdown
  def reverseStr(self, s, k):
        """
        :type s: str
        :type k: int
        :rtype: str
        """
        s=list(s)
        start=0
        last=2*k-1
        while last<len(s):
            left=start
            right=start+k-1
            while(left<right):
                tmp=s[left]
                s[left]=s[right]
                s[right]=tmp
                left+=1
                right-=1
            start=start+2*k
            last=last+2*k
        if len(s)-start >= k:
            left=start
            right=start+k-1
            while(left<right):
                tmp=s[left]
                s[left]=s[right]
                s[right]=tmp
                left+=1
                right-=1
            s=''.join(s)
            return s
        else:
            left=start
            right=len(s)-1
            while(left<right):
                tmp=s[left]
                s[left]=s[right]
                s[right]=tmp
                left+=1
                right-=1
            s=''.join(s)
            return s
   ```
在 Python 中，字符串切片（slicing）是一种非常强大的操作。你可以通过切片来获取字符串的子字符串。切片的基本语法是 `s[start:stop:step]`

在字符串 `s = 'abc'` 中，使用切片 `s[0:999]` 将返回字符串 `'abc'`。这是因为虽然 `stop` 索引超出了字符串的长度，但 Python 的切片操作会自动调整超出范围的索引，使其在有效范围内，这样就避免了边界条件的错误。

类似的特性在其他 Python 数据类型（如列表、元组等）中也存在。以下是一些例子和解释：

```python
tup = (1, 2, 3)
print(tup[0:999])  # 输出: (1, 2, 3)
lst = [1, 2, 3]
print(lst[0:999])  # 输出: [1, 2, 3]
s = 'abcdef'
print(s[-3:])     # 输出: 'def'（从倒数第三个字符到末尾）
print(s[::2])     # 输出: 'ace'（每隔一个字符切片）
print(s[::-1])    # 输出: 'fedcba'（字符串反转）
lst = [1, 2, 3, 4, 5]
print(lst[::-1])  # 输出: [5, 4, 3, 2, 1]（列表反转）
s = 'abc'
print(s[1:5])  # 输出: 'bc'（切片自动到字符串末尾）
lst = [1, 2, 3]
print(lst[1:5])  # 输出: [2, 3]
```
即使 `stop` 索引超出了列表的长度，Python 仍然会返回有效范围内的部分。
这种特性不仅简化了代码的编写，而且增强了代码的鲁棒性，使得我们在处理边界条件时不必担心超出索引范围引发错误。
## 卡码网：54.替换数字 
.isdigit() 好function
