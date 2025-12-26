

# Time Complexity

  

Describes the amount of time necessary to execute the program

  

# Space Complesity

Descibes amount of memory or space utilized by an algorithm/ program required![[Pasted image 20251222060614.png]]


![[Pasted image 20251222060627.png]]



To loop through the entire list of N
numbers, and make sure that 2 is or is
not in the list, it would take N time. We
need to check every number in the list
once. Making this solution O(N) - linear
time. The longer the list, (the bigger N
is), the longer it would take.

![[Pasted image 20251222060741.png]]

![[Pasted image 20251222063601.png]]




![[Pasted image 20251222060759.png]]

![[Pasted image 20251222061121.png]]


![[Pasted image 20251222063732.png]]
Hashmap has same time complexity O(1) for each operation
as these operation work on the hash function 



##COnstant time always may not mean fast , it can be slow also 

![[Pasted image 20251222063912.png]]


![[Pasted image 20251222064011.png]]


![[Pasted image 20251222064043.png]]



![[Pasted image 20251222064121.png]]


![[Pasted image 20251222064327.png]]

![[Pasted image 20251222064424.png]]


## Problem Solving 


- Read the problem twice to understand it (ask clarifying questions)
- Try think basically of different ways to solve the problem 
- Think end to end of the best solution based on complexity 
- Write the algorithm from patterns in drawing 
- code it out 
- Try and improve it once you think you are finished 
- go through other solutions (even if you answer correctly )

# Array

DUPLICATE VALUES

### 217 Contains Duplicate

Q. Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if 
every element is distinct.


**Example 1:**

**Input:** nums = [1,2,3,1]

**Output:** true

**Explanation:**

The element 1 occurs at the indices 0 and 3.

**Example 2:**

**Input:** nums = [1,2,3,4]

**Output:** false

**Explanation:**

All elements are distinct.

**Example 3:**

**Input:** nums = [1,1,1,3,3,4,3,2,4,2]

**Output:** true







```python 

# first approach will be related to nested loops but that will be more time complexity
# bruteforce approach

# by nesting loops but what it will do it will have more itme complexity


# Sorting Approach 

# we can sort out the array first then compare the adjacent value of the array element so that it is easy to compute the answer
# complexity == > O(nLogn)


# if we secrificce the memory then we can achieve better time complexity

# by using hashmap
# Time = O(n)
# Space = O(n)

# hashset in python by using set 

hashset = set()
for n in nums:
	if n in hashset:
		return True
	hashset.add(n)
return False


# so for thiss question we will be taking the help of python Sets , a set is one of the 4 built in data type in python used to store collection of data the other 3 are list tupple and dictionary  , all with different quantities and usage

# Sets are unorederd , unchangablem hetrogeneous , unique
if len(set(nums)) == len(nums):
	return False
else:
	return True

```



### 268 Missing Number

Given an array `nums` containing `n` distinct numbers in the range `[0, n]`, return _the only number in the range that is missing from the array._

**Example 1:**

**Input:** nums = [3,0,1]

**Output:** 2

**Explanation:**

`n = 3` since there are 3 numbers, so all numbers are in the range `[0,3]`. 2 is the missing number in the range since it does not appear in `nums`.

**Example 2:**

**Input:** nums = [0,1]

**Output:** 2

**Explanation:**

`n = 2` since there are 2 numbers, so all numbers are in the range `[0,2]`. 2 is the missing number in the range since it does not appear in `nums`.

**Example 3:**

**Input:** nums = [9,6,4,2,3,5,7,0,1]

**Output:** 8

**Explanation:**

`n = 9` since there are 9 numbers, so all numbers are in the range `[0,9]`. 8 is the missing number in the range since it does not appear in `nums`.

```python

#### we do have to find the missing number from the list 
# if we do have

# **Input:** nums = [0,1]
#   **Output:** 2


# for index 0 we have the value 0 
# for index 1 we do have the value index 1
# if we do have same length of nums as the index in the list then 
nums.sort()
for i, v in enumerate(nums):
	if (i!=v):
		return v-1
	if v==len(nums)-1:
		return v+1
		
		
		
		
		
		
# o to n but in this range we do have n+ 1 number in this list 
# o(1) extra space and O(n) time complexity

# Input: nums = [3,0,1]

# Output: 2

# we can use hash map and cross out the one that is in the list already
# it will take O(n) extra memory


# for O(1) we need binary memory or XOR property

# XOR  - 2 ^ 3
# if diffenent then output will be one only

# how do we use xor in this case
# XOR - 5^5 = 0
# XOR - 5^5^3 = 3
# order does not matter here 
# XOR - 5^3^5 = 3

# how we gonna use this face in out benifit 

# we take the complete array and xor it with out given array so we will able to find the missing number as output of xor

# [0,1,2,3] ^ [0,1,3] = 2
# and 2 was our missing number 

#memory used O(1)
#Time Complexity = O(2n)



###### another SOlution############################

# SUm of this range and then substract it from the sum of input array
# we will be left with missing number


# for sum we will take O(n)
# for sum  2 we will take O(n)


# Time complexity


# another solution 
return sum(range(len(nums)+1)) - sum(nums)


```

![[Pasted image 20251222071501.png]]

![[Pasted image 20251222071528.png]]



![[Pasted image 20251222071541.png]]


![[Pasted image 20251222071552.png]]


## 448 Find All Numbers Disappeared in an Array


![[Pasted image 20251222072706.png]]


![[Pasted image 20251222071717.png]]

Given an array `nums` of `n` integers where `nums[i]` is in the range `[1, n]`, return _an array of all the integers in the range_ `[1, n]` _that do not appear in_ `nums`.

**Example 1:**

**Input:** nums = [4,3,2,7,8,2,3,1]
**Output:** [5,6]

**Example 2:**

**Input:** nums = [1,1]
**Output:** [2]

**Constraints:**

- `n == nums.length`
- `1 <= n <= 105`
- `1 <= nums[i] <= n`


```python 



## 448 Find All Numbers Disappeared in an Array
# sets in python are unordered also 
## [4,3,2,7,8,2,3,1]
ret =[]
set_nums = set(nums)
set_nums = (4,3,2,7,8,3,1)
for i in range(1,len(nums)+1): # as this list was starting from 1 
	if i not in set_nums:
		ret.append(i)
	
return ret
	
# we are using o(n) space and O(n) time
	
# this one was also good but what we can also do here 

# mark existing 
 for n in nums:
	 i = abs(n) -1
	 nums [i] = -1 * abs(nums[i])
	 
	 res = []
	 for i, n in enumerate(nums):
		if n>0:
		res.append(i+1)
		
	 
	 

```



## Two Sum

![[Pasted image 20251223232431.png]]

bruteforce approach is to take the first number and then add it to every other number and check f those numbers are equal to the target

for this we will take two loops one outer and one inner 


Time complexity will eb around
O(n^2)

```python 
class Solution:

    def twoSum(self, nums: List[int], target: int) -> List[int]:

        hash = {}

  

        for i,v in enumerate (nums):

            diff = target-v

            if diff in hash:

                return [i,hash[diff]]

            hash[v] = i
```

##   1365. How Many Numbers Are Smaller Than the Current Number


How Many Numbers Are Smaller Than the Current Number(https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)


Given the array `nums`, for each `nums[i]` find out how many numbers in the array are smaller than it. That is, for each `nums[i]` you have to count the number of valid `j's` such that `j != i` **and** `nums[j] < nums[i]`.

Return the answer in an array.

![[Pasted image 20251223234525.png]]
