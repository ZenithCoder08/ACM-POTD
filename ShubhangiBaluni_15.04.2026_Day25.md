class Solution {
    public int maxDepth(TreeNode root) {
        // Base case: if node is null, depth is 0
        if (root == null) {
            return 0;
        }
        
        // Recursively find the depth of left and right subtrees
        int leftHeight = maxDepth(root.left);
        int rightHeight = maxDepth(root.right);
        
        // The current depth is 1 + the max of the two subtrees
        return Math.max(leftHeight, rightHeight) + 1;
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/15-04-2026.png
