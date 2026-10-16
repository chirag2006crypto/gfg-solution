## 01. Insertion Sort

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/insertion-sort/1)

### Problem Description

**Task:** Given an array arr[] of positive integers.The task is to complete the insertsort() function which is used to implement Insertion Sort. Examples:Input: arr[] = [4, 1, 3, 9, 7]

#### Examples

##### Example 1

- **Output:**
```text
[1, 4, 9]Explanation: The sorted array will be [1, 4, 9].
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (C++)

- **Submitted:** 2026-10-16 10:33:21
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    void insertionSort(vector<int>& arr) {
        // code here
        int n = arr.size();
          for (int i = 1; i < n; i++) {
            int j = i;
            while (j > 0 && arr[j] < arr[j - 1]) {
                swap(arr[j], arr[j - 1]);
                j--;
            }
        }
    }
};
```

#### Solution 2 (C++)

- **Submitted:** 2026-10-13 16:20:38
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    void insertionSort(vector<int>& arr) {
        // code here
        int n = arr.size();
        for (int i = 1; i < n; i++) {
           int j = i;
           while (j > 0 && arr[j] < arr[j - 1]) {
               swap(arr[j], arr[j - 1]);
               j--;
           }
       }

          

    }
};
```

#### Solution 3 (C++)

- **Submitted:** 2026-10-13 15:50:17
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    void insertionSort(vector<int>& arr) {
        // code here
        int n= arr.size();
        for(int i=0;i<n-1;i++) {
                bool flag = true;
                for(int j=0;j<n-1-i;j++){
                    if(arr[j]>arr[j+1]){
                        // int temp = arr[j];
                        // arr[j] =arr[j+1];
                        // arr[j+1]= temp ;
                        swap (arr[j], arr[j+1]);
                        flag = false;

                    }
                }
                if(flag == true){
                    break;
                }


            }
          

    }
};
```

*Generated on: 16/10/2026, 10:45:56*