앞에서부터 차례대로 정렬된 배열 부분과 비교하여 삽입하는 정렬

[35, 25, 12, 22, 11] -> [25, 35, 12 , 22, 11] -> [12, 25, 35, 22, 11]

```python

def insertionSort(arr):
  for i in range(1, len(arr)):
    key = arr[i]
    j = i-1
    while key < arr[j] and j>=0:
      arr[j+1] = arr[j]
      j -= 1
    arr[j+1] = key
  return arr
```
```java

int[] insertionSort(int arr[]){
  for(int i=1;i<i.length;i++){
    arr[i] = key;
    j = i - 1;
    while(j>=0 $$ key < arr[j]){
      arr[j+1] = arr[j];
      j -=1;
      }
    arr[j+1] = key;
    }
    }
   ```
