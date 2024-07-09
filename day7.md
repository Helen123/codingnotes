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

