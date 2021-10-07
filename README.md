# DSA-Practice

## Day 1

- [X] [Sort an array of 0’s 1’s 2’s without using extra space or sorting algo](https://www.geeksforgeeks.org/sort-an-array-of-0s-1s-and-2s/)
  **Similar Questions**
  - [Sort Colors](https://leetcode.com/problems/sort-colors/) 
- [X] Repeat and Missing Number
  **Similar Questions**
  - [Missing Number](https://leetcode.com/problems/missing-number/)
  - [Repeating Number](https://leetcode.com/problems/find-the-duplicate-number/)
  - [Find all the Duplicates in an array](https://leetcode.com/problems/find-all-duplicates-in-an-array/)
- [X] Merge two sorted Arrays without extra space
  **Optimal Method** - Gap Method
  ```C++
  // Merging two sorted arrays with O(1) extra space
  // Function to find next gap.
  
  int nextGap(int gap) {
    if (gap <= 1)
      return 0;
    return (gap / 2) + (gap % 2);
  }

  void merge(int* arr1, int* arr2, int n, int m) {
    int i, j, gap = n + m;
    for (gap = nextGap(gap); gap > 0; gap = nextGap(gap)) {
      // comparing elements in the first array.
      for (i = 0; i + gap < n; i++)
        if (arr1[i] > arr1[i + gap])
          swap(arr1[i], arr1[i + gap]);

      // comparing elements in both arrays.
      for (j = gap > n ? gap - n : 0; i < n && j < m; i++, j++)
        if (arr1[i] > arr2[j])
          swap(arr1[i], arr2[j]);

      if (j < m) {
        // comparing elements in the second array.
        for (j = 0; j + gap < m; j++)
          if (arr2[j] > arr2[j + gap])
            swap(arr2[j], arr2[j + gap]);
      }
    }
  }

  // Driver code
  int main() {
    int a1[] = {10, 27, 38, 43, 82};
    int a2[] = {3, 9};
    int n = sizeof(a1) / sizeof(int);
    int m = sizeof(a2) / sizeof(int);

    // Function Call
    merge(a1, a2, n, m);

    printf("First Array: ");
    for (int i = 0; i < n; i++)
      printf("%d ", a1[i]);

    printf("\nSecond Array: ");
    for (int i = 0; i < m; i++)
      printf("%d ", a2[i]);
    printf("\n");
    return 0;
  } ```
- [X] Kadane’s Algorithm
- [X] Merge Overlapping Subintervals
- [X] Find the duplicate in an array of N+1 integers. 




## Day 2

- [X] Set Matrix Zeros
- [ ] Pascal Triangle
- [ ] Next Permutation
- [ ] Inversion of Array (Using Merge Sort) 
- [ ] Stock Buy and Sell 
- [ ] Rotate Matrix 
