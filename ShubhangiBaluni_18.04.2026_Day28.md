class Solution {
    public boolean isSubtree(TreeNode root, TreeNode subRoot) {
        if (root == null) return false;
        
        if (isSameTree(root, subRoot)) return true;
        
        return isSubtree(root.left, subRoot) || isSubtree(root.right, subRoot);
    }
      private boolean isSameTree(TreeNode s, TreeNode t) {
        if (s == null && t == null) return true;
        
        if (s == null || t == null || s.val != t.val) return false;
        
        return isSameTree(s.left, t.left) && isSameTree(s.right, t.right);
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/18-04-2026.png
