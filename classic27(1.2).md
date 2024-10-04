# classic 27 Remove Element
## mycode
```python
class Solution(object):
    def removeElement(self, nums, val):
        """
        :type nums: List[int]
        :type val: int
        :rtype: int
        """
        # val: need to be removed
        # return len(left array)
        fast=0
        slow=0
        length=len(nums)
        while (fast<length):
            # we delete that 
            if nums[fast]==val:
                fast+=1
            # nums[fast]!=val(we need to keep this)
            else:
                nums[slow]=nums[fast]
                slow+=1
                fast+=1
        return slow
```
## 
