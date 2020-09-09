리스트 [6,5,3,2,1,7,4]를 정렬하고 싶다. 우리는 보통 어떻게 정렬을 할까??
일단 눈으로 가장 작은걸 왼쪽으로 보내고 그 다음 작은 것을 그다음 작은 것을 그렇게 쭉 가다보면 정렬이 완료된다.
이게 바로 직관적으로 우리가 생각해낼 수 있는 정렬법이다.
이를 선택정렬이라고 하는데 리스트에서 가장 작은 원소를 찾고 그것을 초기인덱스 원소와 뒤바꾸고 그런식으로 똑같이 반복하면 된다.
어떤 원소가 가장 작음을 알기위해서는 리스트 모든 원소를 꺼내보아야 하므로 한 시행당 n-1번 ..... 1번 으로 1+ ``` +n-1 = n(n-1)/2 
시간 복잡도 상에서는 o(n2)이다. 

특징은 어떻든간에 리스트 원소를 모두 보는것이므로 C(avg), C(min), C(max) 모두 같다는 것이다.
선택정렬은 불안정한 정렬이다. 즉, 동일한 값에 대하여 기존의 순서가 유지되지 않는다.
ex)

<b>, <B>, <A>, <c>
이러면 정렬 후
<A>, <B>, <b>, <c> 가 되므로 selection sort is not stable.

http://stackoverflow.com/questions/4601057/why-is-selection-sort-not-stable

출처: https://mygumi.tistory.com/94 [마이구미의 HelloWorld]




```python
def selectionSort(x):
  length = len(x)
  for i in range(length-1):
    indexMin = i
    for j in range(i+1, length):
      if x[indexMin] > x[j]:
        indexMin = j
        
    x[indexMin], x[i] = x[i], x[indexMin]
  return x
```

```java
void selectionSort(int [] list){
    for(int i=0;i<list.length-1;i++){
      indexMin = i;
      for(int j=i+1;j<length;j++){
        if(list[indexMin] > list[j]){
          indexMin = j;
          }
      temp = list[indexMin];
      list[indexMin] = list[i];
      list[i] = temp;
      }
    return list;
    }
    }
      
          ```
