# Daily-Leetcode-problem-solution15
PROBLEM

You are given a 0-indexed integer array nums. A pair of indices (i, j) is a bad pair if i < j and j - i != nums[j] - nums[i].
Return the total number of bad pairs in nums.

Intuition

Rearranging the Condition: nums[j]−nums[i]−(j−i)≠0
Rewriting: nums[j]−j≠nums[i]−i
Define diff[i]=nums[i]−i, then the condition simplifies to:
diff[j]≠diff[i]

This means that two indices
(i,j) form a bad pair if diff[j]≠diff[i].

Approach

Efficient Approach Using HashMap:
Instead of checking all pairs
O(n^2), we use a frequency map to count how many times each value of diff[i] appears.

Steps:
1. Total pairs in the array: n(n−1)/2
2. Good pairs: Pairs where diff[j]=diff[i], counted using a hash map.
3. Bad pairs: Subtract the number of good pairs from the total.

Complexity

Time complexity:
O(n)

Space complexity:
O(n)
