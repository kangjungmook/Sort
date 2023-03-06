# 1.삽입정렬(insertion sort)
자료 구조란 현실 세계 및 추상적 세계에서의 
Data들의 모임 또 이런 Data들의 관계 등 
Data들의 집합을 의미합니다.
자료구조는 더 효율적인 알고리즘을 사용할 수 있게 
하며 실행시간 및 메모리 용량과 같은 자원을 최소한으로 
사용하면서 연산을 수행하도록 해줍니다.
```java
package sort;

import java.util.Arrays;

public class InsertionSort {
	static int[] nums;

	public static void main(String[] args) {
		nums = new int[10];
		for (int i = 0; i < 10; i++) {
			nums[i] = (int) (Math.random() * 10);
		}
		System.out.println("<정렬 전>");
		System.out.println(Arrays.toString(nums));
		
		for(int i = 1; i < nums.length; i++) {
			// 현재 선택된 원소의 값을 임시 변수에 저장해준다.
			int temp = nums[i];
			// 현재 원소를 기준으로 이전 원소를 탐색하기 위한 index 변수.
			int prev = i - 1;
			// 현재 선택된 원소가 이전 원소보다 작은 경우까지만 반복. 단, 0번째 원소까지만 비교한다.
			while(prev >= 0 && nums[prev] > temp) {
				// 현재 선택된 원소가 현재 탐색중인 원소보다 작다면, 해당 원소는 다음 인덱스로 미뤄버린다.
				nums[prev + 1] = nums[prev];
				// 다음 대상 원소를 탐색한다.
				prev--;
			}
			// 탐색이 종료된 지점에 현재 선택되었던 변수의 값을 삽입해준다.
			nums[prev + 1] = temp;
		}
		
		System.out.println("<정렬 후>");
		System.out.println(Arrays.toString(nums));
	}
}
```
## 따라서 삽입정렬의 알고리즘은?
자료 배열의 모든 요소를 앞에서부터 차례대로 이미 
정렬된 배열 부분과 비교하여, 
자신의 위치를 찾아 삽입함으로써 
정렬을 완성하는 알고리즘
