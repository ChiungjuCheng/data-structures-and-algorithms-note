# 144. Binary Tree Preorder Traversal
Given the root of a binary tree, return the preorder traversal of its nodes' values.

# Solution
time O(n) 
```java
class Solution {
    
    public List<Integer> preorderTraversal(TreeNode root) {
        
        List<Integer> result = new ArrayList<>();
                
        Stack<TreeNode> rightChildren = new Stack<>();
        
        // empty root
        if(root == null){
             return result;
        }
        
        TreeNode currentNode = root;
                
        while(!rightChildren.empty() || currentNode != null ){
            
            if(currentNode == null){
              currentNode = rightChildren.pop();
            }
            
            result.add(currentNode.val);
            
            if(currentNode.right != null){
                rightChildren.push(currentNode.right);
            }
            
            currentNode = currentNode.left;
        }
        
        return result;
    }
}
```
