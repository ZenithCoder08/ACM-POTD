class Solution {
    public void moveZeroes(int[] nums) {
        // 'lastNonZeroFoundAt' points to the position where the next 
        // non-zero element should be moved.
        int lastNonZeroFoundAt = 0;
        
        for (int cur = 0; cur < nums.length; cur++) {
            if (nums[cur] != 0) {
                // Swap the current non-zero element with the 
                // element at lastNonZeroFoundAt
                int temp = nums[lastNonZeroFoundAt];
                nums[lastNonZeroFoundAt] = nums[cur];
                nums[cur] = temp;
                
                lastNonZeroFoundAt++;
            }
        }
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD/blob/main/26-03-2026.png
