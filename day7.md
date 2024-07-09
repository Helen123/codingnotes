# day7
## 454.四数相加II 
注意在dict中的增加和修改：

修改：showed[num1+num2] += 1

增加：  showed[num1+num2] = 1

if num1+num2 in showed:

showed[num1+num2] += 1

else:

showed[num1+num2] = 1

在遍历nums1 nums2 时可能有多组num 加到该key

## 383. 赎金信  
again: if represent: table[i]+=1

if not table[i]=1

##  15. 三数之和 
满足条件且不重复的三元组

例如：给定数组 nums = [-1, 0, 1, 2, -1, -4]，

满足要求的三元组集合为： [ [-1, 0, 1], [-1, -1, 2] ]

难点在于去重

**剪枝**重要

sort():nums.sort()

##  18. 四数之和  

for k in range(len(nums)):

            if nums[k]>0 and nums[k]>target:
            
                return result
                
            if(k>0 and nums[k]==nums[k-1]):
            
                continue
                
            for i in range(k+1,len(nums)):
            
                if nums[k]+nums[i]>target and nums[i]>0:
                
                    **continue**#剪枝之前错了，不应该是return
                    
                if (i>k+1 and nums[i]==nums[i-1]):
                
                    continue



