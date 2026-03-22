class Solution {
    public int removeDuplicates(int[] nums) {
        if (nums.length == 0) {
            return 0;
        }

        // 'i' is the index of the last known unique element
        int i = 0;

        // 'j' scans through the array starting from the second element
        for (int j = 1; j < nums.length; j++) {
            // If we find a value different from the current unique element
            if (nums[j] != nums[i]) {
                i++; // Move to the next slot for a unique element
                nums[i] = nums[j]; // Update the slot with the new unique value
            }
        }

        // The number of unique elements is the index + 1
        return i + 1;
    }
}


Refrence:https://github.com/ZenithCoder08/ACM-POTD/blob/main/a.png
