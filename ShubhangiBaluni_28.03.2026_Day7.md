class Solution {
    public void rotate(int[] nums, int k) {
        int n = nums.length;
        // Step 1: Handle cases where k > n
        k %= n;
        if (k == 0) return;

        // Step 2: Reverse the whole array
        reverse(nums, 0, n - 1);
        // Step 3: Reverse the first k elements
        reverse(nums, 0, k - 1);
        // Step 4: Reverse the rest
        reverse(nums, k, n - 1);
    }

    private void reverse(int[] nums, int start, int end) {
        while (start < end) {
            int temp = nums[start];
            nums[start] = nums[end];
            nums[end] = temp;
            start++;
            end--;
        }
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD/blob/main/28-03-2026.png
