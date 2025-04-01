# Top 75 Leet Code DSA Questions with Java

## Arrays (10 Questions)
    1. Two Sum
    2. 121. Best Time to Buy and Sell Stock
    3. 88. Merge Sorted Array
    4. 217. Contains Duplicate
    5. 238. Product of Array Except Self
    6. 53. Maximum Subarray
    7. 15. 3Sum
    8. 56. Merge Intervals
    9. 11. Container With Most Water
    10. 48. Rotate Image


## 1. Two Sum (LeetCode 1)
    Problem: Find two numbers in the array that add up to a specific target.
    Solution:


```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> map = new HashMap<>(); 
        for (int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            if (map.containsKey(complement)) {
                return new int[]{map.get(complement), i}; 
            }
            map.put(nums[i], i);
        }
        return new int[]{}; 
    }
}
