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
class Solution {
    public int countNodes(TreeNode root) {
        Queue<TreeNode> queue = new LinkedList<TreeNode>();
        if(root == null) return 0;
        queue.offer(root);
        int count = 0;
        while(!queue.isEmpty()){
            int queueSize = queue.size();
            count+=queueSize;
            System.out.println("count" +count);
            for(int i=queue.size(); i>0;i--){
              if(queue.peek().left != null) queue.offer(queue.peek().left);
              if(queue.peek().right != null) queue.offer(queue.peek().right);
              queue.poll();
            }
        }
        return count;
    }
}




