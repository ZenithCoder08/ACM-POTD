class Solution {
    public int maxProfit(int[] prices) {
       int minPrice = Integer.MAX_VALUE;
        int maxProfit = 0;
        
        for (int i = 0; i < prices.length; i++) {
            if (prices[i] < minPrice) {
                // Update the lowest price found so far
                minPrice = prices[i];
            } else if (prices[i] - minPrice > maxProfit) {
                // Update the maximum profit if selling today is better
                maxProfit = prices[i] - minPrice;
            }
        }
        
        return maxProfit; 
    }
}


URL: https://github.com/ZenithCoder08/ACM-POTD/blob/main/24-03-2026.png
