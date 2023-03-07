# 1.삽입정렬(insertion sort)

### 자료 구조란?
* 현실 세계 및 추상적 세계에서의 
Data들의 모임 또 이런 Data들의 관계 등 
Data들의 집합을 의미합니다.
### 목적 같은 경우엔?
* 자료구조는 더 효율적인 알고리즘을 사용할 수 있게 
하며 실행시간 및 메모리 용량과 같은 자원을 최소한으로 
사용하면서 연산을 수행하도록 해줍니다.

### 따라서 삽입정렬의 알고리즘은?
* 자료 배열의 모든 요소를 앞에서부터 차례대로 이미 
정렬된 배열 부분과 비교하여, 
자신의 위치를 찾아 삽입함으로써 
정렬을 완성하는 알고리즘
### for문
```java
package sort;      
for (int end = 1; end < arr.length; end++) {
            for (int i = end; i > 0; i--) {
                if (arr[i - 1] > arr[i])
                    swap(arr, i - 1, i);
            }
        }
    }

    private static void swap(int[] arr, int a, int b) {
        int tmp = arr[a];
        arr[a] = arr[b];
        arr[b] = tmp;
    }
}
```


<br>
<br>
<br>
<br>
<br>
<br>


# 버블정렬(bubble sort)
* 서로 인접한 두 원소를 검사하여 정렬하는 알고리즘
인접한 2개의 레코드를 비교하여 크기가 순서대로 되어 있지 않으면 서로 교환한다.
* 선택 정렬과 기본 개념이 유사하다
### 목적 같은 경우엔?
* 정렬을 하는 방법이 매우 다양하고, 
이를 비교하여 알고리즘의 효율성 차이를 잘 나타내 줄 수 있기 때문입니다.

### 따라서 삽입정렬의 알고리즘은?
* 두 개의 인접한 원소를 비교하여 정렬하는 방식

### for문
```java
 for (int i = 0; i < arr.length; i++) {
	            for (int j = 0; j < arr.length - i - 1; j++) {
	                if (arr[j] > arr[j + 1]) {
	                    int temp = arr[j];
	                    arr[j] = arr[j + 1];
	                    arr[j + 1] = temp;
	                }
	            }
	        }

	        //1 4 5 8 10 13 19 21 25 30
	        for (int i = 0; i < arr.length; i++) {
	            System.out.printf("%d ", arr[i]);
	        }
```







