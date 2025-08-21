# Two-Sum
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]
Example 3:

Input: nums = [3,3], target = 6
Output: [0,1]
 
Constraints:
* 2 <= nums.length <= 104
* -109 <= nums[i] <= 109
* -109 <= target <= 109
* Only one valid answer exists.

## Original Algorithm
Add an index of the array with every other index after it, then move to the next index and repeat. So every repetition the size of additions that need to be done gets smaller.

It runs (n-1) + (n-2) + (n-3) + ... + 1 which is O(n^2) time complexity

## Optimized Algorithm
Use hashmap to check if a number has a compliment that adds up to the target. It does this in one pass through the array so the time complexity is O(1).

A hash map/hash table retrieves ke-value pairs using a hash function that takes a key and computes an index (hash code) where the key-value pair should be stored in the array. It stores data in pairs where each key is unique and maps to a specific value. The array in a hash map is divided into buckets, where each bucket can hold multiple key-value pairs in case of collisions
