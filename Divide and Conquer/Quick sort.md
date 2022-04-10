# Quick sort
取得一個pivot元素，將array拆成兩個部分，所有比pivot元素大的置於pivot右邊array，小的則置於左邊array，接著以遞迴的方式重複上個步驟。

```java
	// Function to sort an array using quick sort algorithm.
	static void quickSort(int arr[], int low, int high) {

		if (low > high) {
			return;
		}
		int middle = partition(arr, low, high); // 將array整理成兩部分

		quickSort(arr, low, middle - 1); // left part
		quickSort(arr, middle + 1, high); // right part

	}

	static int partition(int arr[], int low, int high) {
		int pivot = arr[low];

		int highIndex = high;

		int lowIndex = low + 1;

		while (lowIndex < highIndex) {

			// 找大於pivot
			while (lowIndex < high) {
				if (arr[lowIndex] > pivot) {
					break;
				}
				lowIndex++;
			}

			// 找小於pivot

			while (highIndex > low) {
				if (arr[highIndex] < pivot) {
					break;
				}

				highIndex--;
			}

			if (lowIndex < highIndex) {
				swap(arr, lowIndex, highIndex);
			} else {
				break;
			}

		}

		if (arr[low] > arr[highIndex])
			swap(arr, low, highIndex);

		return highIndex;

	}

	static void swap(int arr[], int a, int b) {
		int tem = arr[a];
		arr[a] = arr[b];
		arr[b] = tem;
	}
```
### 測試
[geeksforgeeks](https://practice.geeksforgeeks.org/problems/quick-sort/1)
[LeetCode](https://leetcode.com/problems/sort-an-array/)

# 分析
Time O(n log(n)) average, O(n^2) worst case, Space O(log(n))
![big-O-of-quick-sort](/Divide%20and%20Conquer/pic/big-O-of-quick-sort.png)
[來源](https://stackoverflow.com/questions/10425506/intuitive-explanation-for-why-quicksort-is-n-log-n)