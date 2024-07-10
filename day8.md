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
## 卡码网：54.替换数字 
.isdigit() 好function
