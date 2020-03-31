# [1. 两数之和](https://leetcode-cn.com/problems/two-sum)

## 题目描述
<!-- 这里写题目描述 -->
<p>给定一个整数数组 <code>nums</code>&nbsp;和一个目标值 <code>target</code>，请你在该数组中找出和为目标值的那&nbsp;<strong>两个</strong>&nbsp;整数，并返回他们的数组下标。</p>

<p>你可以假设每种输入只会对应一个答案。但是，你不能重复利用这个数组中同样的元素。</p>

<p><strong>示例:</strong></p>

<pre>给定 nums = [2, 7, 11, 15], target = 9

因为 nums[<strong>0</strong>] + nums[<strong>1</strong>] = 2 + 7 = 9
所以返回 [<strong>0, 1</strong>]
</pre>



## 解法
<!-- 这里可写通用的实现逻辑 -->


### Python3
<!-- 这里可写当前语言的特殊实现逻辑 -->

```python

#!/usr/local/bin/python3
# -*- coding: UTF-8 -*-
def find(arr, target, start):
	one=two=i1=i2= None
	print('start=', start)
	for i in range(len(arr)):
		if(i > start and  one is None and arr[i] < target):
			one = arr[i]
			two = target -one
			i1= i
		elif(two == arr[i]):
			i2 = i

	if(i2 is None):
		return find(arr,target,i1)
	else:
		return (one,two,i1,i2)

nums = [9,8,7,6,5,3,2,1]
target =9

res = find(nums,target,-1)

print("----")
for i in res:
	print(i)

```

### Java
<!-- 这里可写当前语言的特殊实现逻辑 -->

```java

```

### ...
```

```
