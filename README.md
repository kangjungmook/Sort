##1.삽입정렬(insertion sort)
자료 구조란 현실 세계 및 추상적 세계에서의 
Data들의 모임 또 이런 Data들의 관계 등 
Data들의 집합을 의미합니다.
자료구조는 더 효율적인 알고리즘을 사용할 수 있게 
하며 실행시간 및 메모리 용량과 같은 자원을 최소한으로 
사용하면서 연산을 수행하도록 해줍니다.
```java
public class Insertion_Sort {
 
	public static void insertion_sort(int[] a) {
		insertion_sort(a, a.length);
	}
	
	private static void insertion_sort(int[] a, int size) {
		
		
		for(int i = 1; i < size; i++) {

			int target = a[i];
			
			int j = i - 1;
	
			while(j >= 0 && target < a[j]) {
				a[j + 1] = a[j];
		   }
			a[j + 1] = target;	
		}
		
	}
}
```
#따라서 삽입정렬의 알고리즘은?
자료 배열의 모든 요소를 앞에서부터 차례대로 이미 정렬된 배열 부분과 비교하여, 
자신의 위치를 찾아 삽입함으로써 정렬을 완성하는 알고리즘
