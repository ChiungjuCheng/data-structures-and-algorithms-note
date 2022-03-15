
# Trees 
一個undirected graph是connected且沒有cycle為Trees。G有n - 1個edges。 
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




