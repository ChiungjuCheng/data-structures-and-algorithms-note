# 144. Binary Tree Preorder Traversal
Given the root of a binary tree, return the preorder traversal of its nodes' values.

# Solution
1. iterative way time O(n) 
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
                
        while(currentNode != null){
            
            result.add(currentNode.val);
            
            if(currentNode.right != null){
                rightChildren.push(currentNode.right);
            }
            
            currentNode = currentNode.left;
            
            if(currentNode == null && (!rightChildren.empty())){
              currentNode = rightChildren.pop();
            }
        }
        
        return result;
    }
}
```
2.  Recursive solution
```java
class Solution {
    
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();
        addToResultByRecursive(root, result);
        return result;
    }
    
    private void addToResultByRecursive(TreeNode current, List<Integer> result){
        if(current == null){
            return;
        }
        result.add(current.val);
        
        addToResultByRecursive(current.left, result);
        addToResultByRecursive(current.right, result);
        
    }
}
```