
# Trees 
## 名詞定義
degree (分歧度): 一個node能指向幾個node

### 實現與結構
Tree的表現方式可以用LikedList來表示，但是會浪費太多的pointer的空間，例如有個degree為k，node數目為n的tree，會預先準備n*k個pointer，但是實際上只有每個node會被一個ponter指到，除了root以外，因此實際上浪費了n*k-(n-1)個pointer空間，為了解決這個問題，可用left-subing的方式或是binary tree來表示它

## binary tree
full binary tree: 擁有最大量node的二元樹，表示每個node都有指向兩個node。
complete binary tree: node沒有到達最大量數量，但每個node指向的node的數量為0或為2。

#### 使用array表示binary tree
![Foo](/Tree/picture/binaryTree_array.png)
但當遇到skew tree時，會浪費太多空間，雖然用array很容易做查詢。

#### 比較用LinkedList和array實現樹
![compare](/Tree/picture/comareTwoRepresentation.png)

### Binary Tree Traversals
* pre-, in-, post-是指parent node相對於child node的順序，每到一個subtree就跑一次規則，依序尋訪。
* left一定要先比right早拜訪
* V：Visiting，對當前所在的node進行print、assign或其他操作。
* L：移動到left child。
* R：移動到right child。

1. preorder(VLR) : 中-左-右。到達一個新的subtree時，先把root印出，接著往左邊走，並依照相同規則印出該節點後，若該節點沒有任何的子節點，則回到上一層，並且印出該層的右節點。
   [Q: binary-tree-preorder-traversal](https://leetcode.com/problems/binary-tree-preorder-traversal/)  

   可以使用Stack方法或是遞迴方法，使用Stack儲存每個還未走到的右節點。當左節點走完時，就需要走上一層的左節點，當該右節點的subtree全部走完後才會再走回更上一層的右節點，依照這個特性，每次都要先處理最後遇到的右節點，因此使用stack。

2. inorder traversal : 左-中-右。走到不能往左邊走，就把值(parent)印出來並且return，往右邊走。
可以用recusive的方式去實作，也可以用stack實現。
3. postrder: 最後才把值印出來。
4. Level-order : 把同一層的node都先印出來，可以用queue實現，將所有child node放入queue直到沒有child。

![tree traversal](/Tree/picture/tree_traversal.png)

# 參考
[Binary Tree: Traversal(尋訪)](http://alrightchiu.github.io/SecondRound/binary-tree-traversalxun-fang.html#pre)


