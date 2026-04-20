class Solution {
    public boolean isPowerOfTwo(int n) {
        // A power of two must be positive.
        // n & (n - 1) removes the only set bit. If it becomes 0, it was a power of two.
        return n > 0 && (n & (n - 1)) == 0;
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/20-04-2026.png
