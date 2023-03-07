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
public void insertion_sort(int[] arr) {
    int temp = 0, prev = 0;
    for(int i=1; i<arr.length; i++) {
    	temp = arr[i];
        prev = i - 1;
        while(prev >= 0 && arr[prev] > temp) {
            arr[prev + 1] = arr[prev];
            prev--;
        }
        arr[prev + 1] = temp;	
    }
}
```


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
import java.util.Arrays;

public class BubbleSort {
	static int[] nums;

	public static void main(String[] args) {
		nums = new int[10];
		for (int i = 0; i < 10; i++) {
			nums[i] = (int) (Math.random() * 10);
		}
				for(int i = nums.length - 1; i > 0; i--) {
			for(int j = 0; j < i; j++) {
				if(nums[j] > nums[j + 1]) {
					int temp = nums[j];
					nums[j] = nums[j + 1];
					nums[j + 1] = temp;
				}
			}
		}
		System.out.println(Arrays.toString(nums));
	}
}
```












