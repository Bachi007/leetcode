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

## Algorithm :
    1. Initialize a HashMap:

    Create a HashMap<Integer, Integer> to store numbers as keys and their indices as values.

    2. Iterate through the array:

    For each number nums[i], compute its complement:

    complement=target−nums[i]    
    Check if the complement already exists in the HashMap:
    If found, return the stored index and i as a new array.
    Otherwise, store nums[i] and its index i in the HashMap.

    3. Return an empty array if no solution is found (this case won’t happen as per problem constraints).
    

## Solution :
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
```
## 2. Best Time to Buy and Sell Stock (LeetCode 121)
    Problem: Maximize profit by choosing one day to buy and another to sell.
## Algorithm : 
    1. Initialize variables:

    minPrice = ∞ (Integer.MAX_VALUE): Keeps track of the lowest price encountered so far.
    maxProfit = 0: Stores the maximum profit found so far.

    2. Iterate through the prices array:

    For each price in prices[]:
    Update minPrice by comparing it with the current price:
    minPrice=min(minPrice,price)
   
    3. Calculate profit if the stock is sold at the current price:
    profit=price−minPrice
    
    4. Update maxProfit if the current profit is greater:
    maxProfit=max(maxProfit,profit)
    
    5. Return maxProfit at the end.

## Solution : 
```java
class Solution {
    public int maxProfit(int[] prices) {
        int minPrice = Integer.MAX_VALUE, maxProfit = 0;
        for (int price : prices) {
            minPrice = Math.min(minPrice, price);
            maxProfit = Math.max(maxProfit, price - minPrice);
        }
        return maxProfit;
    }
}
```

