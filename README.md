# 1.삽입정렬(insertion sort)

### 자료 구조란?
* 현실 세계 및 추상적 세계에서의 
Data들의 모임 또 이런 Data들의 관계 등 
Data들의 집합을 의미합니다.
### 목적 같은 경우엔?
* 자료구조는 더 효율적인 알고리즘을 사용할 수 있게<br>
하며 실행시간 및 메모리 용량과 같은 자원을 <br>최소한으로 
사용하면서 연산을 수행하도록 해줍니다.
## 따라서 삽입정렬의 알고리즘은?
* 자료 배열의 모든 요소를 앞에서부터 차례대로 이미 
정렬된 배열 부분과 비교하여, 
자신의 위치를 찾아 삽입함으로써 
정렬을 완성하는 알고리즘

### for문
```java
int [] arr = {10, 2, 6, 4, 3, 7, 5};
		for (int i = 1; i < arr.length; i++) {
			int standard = arr[i];  // 기준
			int aux = i - 1;   // 비교할 대상
			while (aux >= 0 && standard < arr[aux]) {
				arr[aux + 1] = arr[aux];   // 비교대상이 큰 경우 오른쪽으로 밀어냄
				aux--;
			}
			arr[aux + 1] = standard;  // 기준값 저장
		}
		printArr(arr);
	}
	public static void printArr(int[] arr) {
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
![image](https://user-images.githubusercontent.com/106642094/223327362-4994a1c7-687a-40a8-b73f-cd6d433b8717.png)


# 2. 버블정렬(bubble sort)

### 버블 구조란?
* 서로 인접한 두 원소를 검사하여 정렬하는 알고리즘
인접한 2개의 레코드를 비교하여 크기가 순서대로 되어 있지 않으면 서로 교환한다.
*선택 정렬과 기본 개념이 유사하다.

### 목적 같은 경우엔?
* 구현이 매우 간단하다.
## 따라서 버블정렬의 알고리즘은?
* 두 개의 인접한 원소를 비교하여 정렬하는 방식
### for문
```java
public static void main(String[] args) {
        int[] arr= {30,20,40,50,10};
        for(int i=0;i<arr.length-1;i++){
            for(int j=0;j<arr.length-1-i;j++) {
                if(arr[j]>arr[j+1]) {
                    int temp=arr[j];
                    arr[j]=arr[j+1];
                    arr[j+1]=temp;
                }
            }
        }
        for(int i:arr)
        {
            System.out.print(i+" ");
        }
    }
```

# 1.퀵 정렬(Quick sort)

### 퀵 정렬이란?
* 하나의 리스트를 피벗(pivot)을 기준으로 두 개의 
부분리스트로 나누어 하나는 피벗보다 작은 
값들의 부분리스트, 다른 하나는 피벗보다 큰 
값들의 부분리스트로 정렬한 다음, 각 부분리스트에 
대해 다시 위 처럼 재귀적으로 수행하여 정렬하는 방법이다
### 목적 같은 경우엔?
* 기준 데이터를 설정하고 그 기준보다 큰 
데이터와 작은 데이터의 위치를 바꾸는 것
## 따라서 퀵 정렬의 알고리즘은?
* 데이터 그룹에서 그룹을 나누는 기준인 피벗(pivot)을 
선택하고, 피벗을 기준으로 그룹을 나누는 것을 
반복하여 각 그룹이 1개가 되면 정렬을 마칩니다.


```java

import java.util.Arrays;

public class QuickSort {
    int[] array = new int[]{10, 2, 5, 6, 3, 73};

    public void sort() {
        quickSort(array, 0, array.length - 1);
        System.out.println(Arrays.toString(array));
    }

    private void quickSort(int[] array, int start, int end) {
        if (start >= end) return;

        int pivot = start;
        int left = start + 1;
        int right = end;
        int temp;

        while (left <= right) {
            while (array[pivot] >= array[left]) {
                left++;
            }
            while (array[pivot] <= array[right] && right > start) {
                right--;
            }

            if (left > right) {
                temp = array[right];
                array[right] = array[start];
                array[start] = temp;
            } else {
                temp = array[right];
                array[right] = array[left];
                array[left] = temp;
            }
        }

        quickSort(array, start, right - 1);
        quickSort(array, right + 1, end);
    }
}

```












