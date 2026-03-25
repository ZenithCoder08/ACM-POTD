class Solution {
    public int missingNumber(int[] nums) {
        int n = nums.length;
        
        // Sum of numbers from 0 to n: n * (n + 1) / 2
        int expectedSum = n * (n + 1) / 2;
        int actualSum = 0;
        
        // Calculate the sum of elements in the array
        for (int num : nums) {
            actualSum += num;
        }
        
        // The difference is the missing number
        return expectedSum - actualSum;
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD/blob/main/25-03-2026.png
