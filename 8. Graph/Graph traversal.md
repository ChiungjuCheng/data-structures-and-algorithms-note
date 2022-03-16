# Depth-First Search 深度優先搜尋
從圖形中的某一節點開始走訪，並將拜訪過的節點標上記號，避免重複走訪後，開始拜訪該節點相鄰且未拜訪過的任一節點，並以該節點為起點繼續往下走訪。
![DFS](/8.%20Graph/picture/DFS.png)
[圖片來源](https://www.javatpoint.com/depth-first-search-algorithm)

### DFS使用Stack實現: 
1. 標示圖案中所有的節點為還未拜訪的節點，ex: 使用Map或array紀錄。
2. 將起點A放入Stack中
3. 重複4.5直到Stack為空。
4. pop stack並且對該節點運算
5. 將目前的節點中，還未拜訪的鄰節點放入Stack當中。

### 應用
1. 求得能夠與點S相連的所有點 - Connected component

# Breadth First Search 廣度優先搜尋
從圖形中任的某一節點開始走訪，並將該頂點設定為已拜訪後，接著依序走訪該節點的每個鄰近節點，標示走訪後，再從任一鄰近點擇一節點，開始進行下一輪的走訪。  
![BFS](/8.%20Graph/picture/BFS.png)
[圖片來源](https://dev.to/danimal92/difference-between-depth-first-search-and-breadth-first-search-6om)

### 應用
1. 求得最短距離
2. 求得能夠與點S相連的所有點 - Connected component
3. Bipartite graph

### BFS使用Queue實現: 
步驟和DFS一樣，只是換成Queue。