# classic88 合并两个有序数组
## easy way:
nums1[m:] = nums2

nums1.sort()

## my way: 
```python
class Solution(object):
    def merge(self, nums1, m, nums2, n):
        """
        :type nums1: List[int]
        :type m: int
        :type nums2: List[int]
        :type n: int
        :rtype: None Do not return anything, modify nums1 in-place instead.
        """
        #pionter for p1
        p1=m-1
        #pionter for p2
        p2=n-1
        #digit I am working on
        digit=m+n-1
        while (digit>=0):
            # normal case
            if p1>=0 and p2>=0:
                if nums1[p1]>= nums2[p2]:
                    nums1[digit]=nums1[p1]
                    p1-=1
                else:
                    nums1[digit]=nums2[p2]
                    p2-=1
            # edgee case(when one array finish first)
            else: 
                if p1>=0:
                    nums1[digit]=nums1[p1]
                    p1-=1
                else:
                    nums1[digit]=nums2[p2]
                    p2-=1
            digit-=1
```
