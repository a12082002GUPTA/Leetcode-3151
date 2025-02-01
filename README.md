# Leetcode-3151

# C++

class Solution {
public:
    bool isArraySpecial(vector<int>& nums) {
        for(int i=1;i<nums.size();i++)
        {
            int a=nums[i]^nums[i-1];
            if(!(a&1))return false;
        }
        return true;
    }
};

# Java

class Solution {
    public boolean isArraySpecial(int[] nums) { // Use int[] instead of List<Integer>
        for (int i = 1; i < nums.length; i++) { // Use .length for arrays
            int a = nums[i] ^ nums[i - 1];
            if ((a & 1) == 0) return false;
        }
        return true;
    }
}

# Python

class Solution:
    def isArraySpecial(self, nums):
        for i in range(1, len(nums)):
            a = nums[i] ^ nums[i - 1]
            if (a & 1) == 0:
                return False
        return True
