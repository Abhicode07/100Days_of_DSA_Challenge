class Solution {
    int K; 
    public int kthSmallest(TreeNode root, int k) {
        K = k; 
        return util(root);
    }

    private Integer util(TreeNode root){
        if(root == null) return null;
        Integer left = util(root.left);
        if(left == null){
            if(--K == 0) return root.val;
            return util(root.right);
        }
        return left; 
    }
}
