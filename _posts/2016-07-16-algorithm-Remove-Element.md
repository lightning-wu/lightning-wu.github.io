---
layout: post
title: Remove Element
categories: blog
tag: algorithm, array
markdown: redcarpet
---

# Remove Element

## [问题](https://leetcode.com/problems/remove-element/)

> Given an array and a value, remove all instances of that value in place and return the new length.Do not allocate extra space for another array, you must do this in place with constant memory.The order of elements can be changed. It doesn't matter what you leave beyond the new length.

> Example:
Given input array nums = [3,2,2,3], val = 3.Your function should return length = 2, with the first two elements of nums being 2

## 问题描述
> 给定一个数组nums, 值val, 在nums中去掉值等于val的元素，返回nums中剩余元素的长度。要求空间复杂度O(1)。

## 解题直觉
> 使用两个指针i,j 一前一后；j遍历数组nums，i指向最新的有效元素

## 算法
```
分析nums[j] 与 val的关系
case：nums[j] = val
 　　跳过nums[j], j后移
case: nums[j] != val
 　　nums[i] <= nums[j]
      i, j同时后移
```


## 示例代码
```
public int removeElement(int[] nums, int val) {
		int i = 0, j = 0;
		int len = nums.length;
		while(j < len){
			if(nums[j] == val){
				j ++;
			}else{
				nums[i++] = nums[j++];
			}		
		}
		return i;
    }
```

## 算法分析
> 时间复杂度：O(n),空间复杂度：O(1)

## 进阶问题
> 如果nums中只存在少数val？

　　思考中。。。



