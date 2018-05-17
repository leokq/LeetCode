### Two Sum

#### 题目：
Given an array of integers, return ==indices== of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

---

#### Example：
> Given nums = [2, 7, 11, 15], target = 9,
>
> Because nums[0] + nums[1] = 2 + 7 = 9,
>
>return [0, 1].

#### Solution：


```
class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        lookup = {}
        for i,num in enumerate(nums):
            if target-num in lookup:
                return [lookup[target-num],i]
            lookup[num] = i
        return []
```

#### ==笔记：==

##### enumerate()方法：
##### 描述：
`enumerate()`函数用于将一个可遍历的数据对象(如列表、元组或字符串)组合为一个索引序列，同时列出数据和数据下标，一般用在 for 循环当中。
##### 语法：

```
enumerate(sequence,[start = 0])
```
##### 参数：
- sequence -- 一个序列、迭代器或其他支持迭代对象。 
- start -- 下标起始位置。

##### 返回值：
返回enumerate(枚举)对象

### 实例

```
>>>seasons = ['Spring', 'Summer', 'Fall', 'Winter']
>>> list(enumerate(seasons))
[(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
>>> list(enumerate(seasons, start=1))       # 小标从 1 开始
[(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]
```
##### 普通for循环

```
>>>seq = ['one', 'two', 'three']
>>> for i, element in enumerate(seq):
...     print i, seq[i]
... 
>>>
0 one
1 two
2 three

```




