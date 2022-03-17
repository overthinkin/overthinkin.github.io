---
title: 2022년 1학기 컴퓨터 알고리즘 2주차 수업내용
categories: [알고리즘]
comments: true
---


# [22-2주차 수업] 알고리즘과 성능분석

#### 차례

1. #### 알고리즘의 의미와 특성  

2. #### 알고리즘의 분류

3. #### 알고리즘의 분석

4. #### 알고리즘의 효율성 표현: 시간 복잡도

   - O (Big-Oh) 표기
   - Ω (Big-Omega) 표기
   - θ (Theta) 표기





#### 1. 알고리즘의 의미와 특성

알고리즘은 문제를 해결하는 단계적 절차 또는 방법이다.

알고리즘의 일반적인 특성

- `정확성`: 알고리즘은 주어진 문제에 대해 올바른 해답을 도출해야 한다.
- `수행성`: 알고리즘은 컴퓨터에서 수행이 가능해야 한다.
- `유한성`: 알고리즘은 일정한 시간 내에 종료되어야 한다.
- `효율성`: 알고리즘은 효율적일수록 가치가 높아진다.



#### 2. 알고리즘의 분류

문제 해결의 방식에 따라 알고리즘을 분류할 수 있다 

- 분할 정복 알고리즘 (Divide and conquer algorithm)
- 그리디 알고리즘 (Greedy algorithm)
- 동적 계획 알고리즘 (Dynamic Programming, DP)
- 백트래킹 기법 (Backtracking)
- 근사 알고리즘 (Approximation algorithm)
- 랜덤 알고리즘 (Random)
- 병렬 알고리즘 (Parallel)
- 분산 알고리즘 (Distributed)
- 양자 알고리즘 (Quantum)
- 유전자 알고리즘 (Genetic)

이외에도 다양한 알고리즘이 있다.



#### 3. 알고리즘의 분석

알고리즘의 분석 관점은 두 가지 측면으로 분류할 수 있다. 


`시간복잡도`는 알고리즘이 수행하는 기본적인 연산 횟수를 입력 크기에 대한 함수로 표현한다. 


`공간복잡도`는 메모리, 비용 등 시간 외에 소요되는 자원을 말한다. 



#### 4. 알고리즘의 효율성 표현: 시간 복잡도

알고리즘의 효율성은 주로 시간복잡도가 사용된다.


`시간 복잡도`는 입력되는 크기를 단순한 함수로 표현하기 위해 **점근적 표기**를 사용한다.


**점근적 표기**에는 *빅오표기, 오메가표기, 세타표기* 가 있다.





- #### O (Big-Oh) 표기

Big-Oh notation은 점근적 상한을 나타낸다.


![식1](https://latex.codecogs.com/svg.image?O(g(n))=\{\&space;f(n)|\exists_c&space;>&space;0,&space;n_0&space;>&space;0&space;s.t.&space;{\forall}&space;n&space;>=&space;n{0},&space;f(n)&space;<=&space;cg(n)\})


> 0보다 큰 c와 0보다 큰 n제로가 있을 때 Eo n제로보다 크거나 같은 모든 n에 대해서 c g(n)보다 작거나 같은  f(n)은?

> **f(n)**: 성능을 확인해야할 알고리즘
> **g(n)**: Big-Oh notation으로 계산된 성능

![시간복잡도그래프](https://user-images.githubusercontent.com/80513292/158816914-4301902a-a668-4272-aa00-7bad9dcd17d3.png)

> c값을 9라고 가정했을 때, cg(n)은 9n이 되므로 n이 9일 때 O(n)이 f(n)=3n+54 를 포함하게 된다.


![식2](https://latex.codecogs.com/svg.image?O(n)&space;\in&space;f(n)=3n&plus;54)

따라서 g(n)과 f(n)의 차수가 같으면 Big-O 표기법으로 표현할 수 있다.


![식3](https://latex.codecogs.com/svg.image?\lim_{n&space;\to&space;\infty}&space;\left\lvert&space;\frac&space;{f(n)}{g(n)}&space;\right\rvert&space;<&space;\infty)


**점근적 상한**이란 쉽게 말해서 <u>알고리즘 f(n)이 빅오로 표기된 g(n) 이상의 성능을 낼 수 없다</u> 는 것을 말한다.







- #### Ω (Big-Omega) 표기

빅오메가 표기는 복잡도의 점근적 하한을 나타낸다.


![식4](https://latex.codecogs.com/svg.image?\Omega&space;(g(n))=\{\&space;f(n)|\exists_c&space;>&space;0,&space;n_0&space;>&space;0&space;s.t.&space;{\forall}&space;n&space;>=&space;n{0},&space;f(n)&space;>=&space;cg(n)\})

![식5](https://latex.codecogs.com/svg.image?\lim_{n&space;\to&space;\infty}&space;\left\lvert&space;\frac&space;{f(n)}{g(n)}&space;\right\rvert&space;>&space;0)



**점근적 하한**이란 쉽게 말해서 <u>알고리즘 f(n)이 빅오로 표기된 g(n) 보다는 더 나은 성능을 낼 수 있음</u>을 말한다.





- #### θ (Theta) 표기

세타 표기는 복잡도의 상한과 하한이 동시에 적용되는 경우를 표현한다.



세타 표기를 사용하면 **상한과 하한을 동시에 적용**했기 때문에 <u>성능을 더 자세하게 표현할 수 있다.</u>

$$ \theta (g(n)) = \{\ f(n)| \exist c_1 ,c_2 >0, n_0 > 0 s.t. \forall n >= n_0, c_1 g(n) <= f(n) <= c_2 g(n) \}\ $$

![식7](https://latex.codecogs.com/svg.image?0&space;<&space;\lim_{n&space;\to&space;\infty}&space;\left\lvert&space;\frac&space;{f(n)}{g(n)}&space;\right\rvert&space;<&space;\infty)




세타 표기를 사용하면 **상한과 하한을 동시에 적용**했기 때문에 <u>성능을 더 자세하게 표현할 수 있다.</u>

