class Solution {
    public boolean checkIfExist(int[] arr) {
        Set<Integer> seen = new HashSet<>();
        
        for (int n : arr) {
            // Check if double the current number exists
            // OR if half the current number exists (must be even)
            if (seen.contains(2 * n) || (n % 2 == 0 && seen.contains(n / 2))) {
                return true;
            }
            // Add current number to the set for future comparisons
            seen.add(n);
        }
        
        return false;
    }
}

URL: https://github.com/ZenithCoder08/ACM-POTD/blob/main/27-03-2026.png
