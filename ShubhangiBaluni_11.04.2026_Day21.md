class Solution {
    public String makeGood(String s) {
        StringBuilder stack = new StringBuilder();
        
        for (char currChar : s.toCharArray()) {
            int size = stack.length();
            
            if (size > 0) {
                char topChar = stack.charAt(size - 1);
                // Math.abs(topChar - currChar) == 32 checks for same letter, different case
                if (Math.abs(topChar - currChar) == 32) {
                    stack.deleteCharAt(size - 1);
                    continue;
                }
            }
            stack.append(currChar);
        }
        
        return stack.toString();
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/11-04-2026.png
