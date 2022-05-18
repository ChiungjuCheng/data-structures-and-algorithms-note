
# Trees 
一個undirected graph是connected且沒有cycle為Trees。G有n - 1個edges。 
# 名詞定義
* Degree (分歧度): 一個node能指向幾個node。  
* Height : 各節點的階層

# 實現與結構
Tree的表現方式可以用LikedList來表示，但是會浪費太多的pointer的空間，例如有個degree為k，node數目為n的tree，會預先準備n*k個pointer，但是實際上只有每個node會被一個ponter指到，除了root以外，因此實際上浪費了n*k-(n-1)個pointer空間，為了解決這個問題，可用left-subing的方式或是binary tree來表示它




