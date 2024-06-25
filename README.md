class Solution:
    def sumIndicesWithKSetBits(self, nums: List[int], k: int) -> int:
        x = 0
        for i in range(len(nums)):
            y = 0
            j = i
            while j:
                if (j & 1) == 1:
                    y += 1
                j = j >> 1
            if y == k:
                x += nums[i]
        return x
