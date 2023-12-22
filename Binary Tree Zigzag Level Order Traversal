/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
 import java.util.*;
class Solution {
    public List<List<Integer>> levelorder(TreeNode root,List<List<Integer>> ans,int level){
           if(root == null)
            return ans;
        
        if(ans.size() == level)
            ans.add(new ArrayList<>());
        
        ans.get(level).add(root.val);
        levelorder(root.left, ans,level+1);
        levelorder(root.right, ans,level+1);

        return ans;
    }
    public List<List<Integer>> zigzagLevelOrder(TreeNode root) {
        List<List<Integer>> ans = new ArrayList<>();
        levelorder(root,ans,0);
        for(int i =0;i<ans.size();i++){
            if(!(i%2 == 0)){
              Collections.reverse(ans.get(i));
            }
        }
        return ans;
    }
}
