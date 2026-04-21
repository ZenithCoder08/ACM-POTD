class Solution {
    public int climbStairs(int n) {
        // Base cases
        if (n <= 2) return n;
        
        int first = 1;  // Ways to reach step 1
        int second = 2; // Ways to reach step 2
        
        for (int i = 3; i <= n; i++) {
            int current = first + second;
            first = second;
            second = current;
        }
        
        return second;
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/21-04-2026.png
