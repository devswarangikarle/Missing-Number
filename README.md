# Missing-Number
Given an array nums containing n distinct numbers in the range [0, n], return the only number in the range that is missing from the array.

class Solution:
    def missingNumber(self, nums: List[int]) -> int:
        n = len(nums)
        v = [-1] * (n + 1)
        for num in nums:
            v[num] = num
        for i in range(len(v)):
            if v[i] == -1:
                return i
        return 0
        
