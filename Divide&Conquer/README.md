# Divide and Conquer

## 분할 정복법이란?

### 1. 엄청나게 크고 방대한 문제를 작은 문제로 '분할'하고, 분할된 문제들을 '조합'하면서 정복하는 방법이다.

### 2. 분할 / 정복/ 조합 의 단계로 구성된다.
  - 분할 : 문제를 동일 유형의 여러 하위 문제로 나눈다.
  - 정복 : 가장 작은 하위 문제를 해결하여 정복한다.
  - 조합 : 정복된 하위 단계를 원래 문제에 대한 결과로 조합한다.

## 예시

### 1. Merge sort
  - 시간 복잡도는 O(nlogn)이지만, 다른 정렬방식에 비해 메모리를 많이 사용한다.

```cpp

```

### 2. a^b 구하기
  - O(b)의 시간복잡도를 O(logb)의 시간복잡도로 단축시킬 수 있다.

```cpp
int powAB(int a, int b) {
	if (b == 0) return 1;
	else if (b == 1) return a;
	else if (b % 2 == 0) {
		int t = powAB(a, b / 2);
		return t * t;
	}
	else {
		return a * powAB(a, b - 1);
	}
}
```

### 3. 대수 연산과 분할 정복
  - **거듭 제곱 연산에 대한 mod 연산** : 분할 정복의 방법 (O(logN)의 복잡도로 구현 가능)
  - **곱셈 연산에 대한 mod 연산** : (a * b) % n == ( (a % n) * (b % n) ) % n
  - **나눗셈 연산에 대한 mod 연산** : 페르마의 소정리를 통한 연산 구현
