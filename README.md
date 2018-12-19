### 문제 1

프린터기기는 인쇄하고자 하는 문서를 인쇄 명령을 받은 '순서대로', 즉 먼저 요청된 것을 먼저 인쇄한다. 여러개의 문서가 쌓인다면 Queue 자료 구조에 쌓여서 FIFO - First In First Out - 에 따라 인쇄가 되게 된다. 하지만 새로운 프린터 내부 소프트웨어를 발 하였는데, 이 프린터기는 다음과 같은 조건에 따라 인쇄를 하게 된다.

1. 현재 Queue의 가장 앞에 있는 문서의 '중요도'를 확인 한다.
2. 나머지 문서들 중 현재 문서보다 중요도가 높은 문서가 하나라도 있다면, 이 문서를 인쇄하지 않고 Queue의 가장 뒤에 재배치 한다. 그렇지 않다면 바로 인쇄를 한다.

예를 들어 Queue에 4개의 문서 (A, B, C, D)  가 있고, 중요도가 2 1 4 3 라면 C 를 인쇄하고, 다음으로 D 를 인쇄하고 A, B를 인쇄하게 된다. 

현재 Queue에 있는 문서의 수와 중요도가 주어졌을 때, 어떤 한 문서가 몇 번째로 인쇄되는지 알아내는 것이다.

예를 들어 위의 예에서 C문서는 1번째로, A 문서는 3번째로 인쇄되게 된다.



### 입력

첫줄에 test case 의 수가 주어진다. 각 test case에 대해서 문서의 수 N와 몇 번째로 인쇄되었는지 궁금한 문서가 현재 Queue의 어떤 위치에 있는지를 알려주는 M이 주어진다. 다음줄에는 N개의 문서 중요도가 주어진다. 중요도가 같은 문서가 여러개 있을 수도 있다.

N <= 100

0 <= M < N



위의 예로 A 문서가 몇번째로 인쇄되는지 궁금하다면

N = 4, M = 0 

2 1 4 3 이 된다.



### 출력

각 test case에 대해 문서가 몇 번째로 인쇄되는지 출력한다.



##### 예제 입력

```
3			// 테스트 케이스
1 0			// N, M
5			// 문서 중요도
4 2			// N, M
1 2 3 4		// 문서 중요도
6 0
1 1 9 1 1 1
```

##### 예제 출력

```
1
2
5
```





### 문제 2

괄호 문자열은 두개의 괄호 기호인 '(' 와 ')' 만으로 구성되어 있는 문자열이다. 그 중에서 괄호의 모양이 바르게 구성된 문자열을 올바른 괄호 문자열이라고 부른다. 한 쌍의 괄호 기호로 된 "()" 문자열은 기본 VPS 이라 부른다. 만일 x가 VPS라면 이것을 하나의 괄호에 넣은 새로운 문자열 "(x)"도 VPS가 된다. 그리도 두 VPS x 와 y 를 접합 시킨 새로운 문자열 xy도 VPS가 된다. 예를 들어 "(())()" 와 "((()))"는 VPS 이지만 "(()(", "(())()))"는 VPS가 아니다.

입력으로 주어진 괄호 문자열이 VPS인지 아닌지를 판단해서 그 결과를 YES와 NO로 나타내어야 한다.

### 입력

입력 첫번째 줄에는 test case의 수가 주어지고 그 수만큼 괄호 문자열이 주어진다.

하나의 괄호 문자열 길이는 2 이상 50 이하이다.

### 출력

만약 입력 괄호 문자열이 올바른 VPS이면 YES 아니면  NO를 한줄에 하나씩 출력한다.



##### 예제 입력

```
6
(())())
(((()())()
(()())((()))
((()()(()))(((())))()
()()()()(()()())()
(()((())()(
```



##### 예제 출력

```
NO
NO
YES
NO
YES
NO
```





### 문제 3

난이도 조절을 위해 게임 실패율을 구하는 코드완성

- 실패율은 다음과 같이 정의한다.
  - 스테이지에 도달했으나 아직 클리어하지 못한 플레이어의 수 / 스테이지에 도달한 플레이어 수

전체 스테이지의 개수 N, 게임을 이용하는 사용자가 현재 멈춰있는 스테이지의 번호가 담긴 배열 stages가 매개변수로 주어질 때, 실패율이 높은 스테이지부터 내림차순으로 스테이지의 번호가 담겨있는 배열을 return 하도록 solution 함수를 완성하라.



##### 제한사항

- 스테이지의 개수 N은 1 이상 500 이하의 자연수이다.
- stages의 길이는 1 이상 200,000 이하이다.
- stages에는 1이상 N+1 이하의 자연수가 담겨있다.
  - 각 자연수는 사용자가 현재 도전중인 스테이지의 번호를 나타낸다.
  - 단,  N+1은 마지막 스테이지(N 번째 스테이지)까지 클리어한 사용자를 나타낸다.
- 만약 실패율이 같은 스테이지가 있다면 작은 번호의 스테이지가 먼저 오도록 하면 된다.
- 스테이지에 도달한 유저가 없는 경우 해당 스테이지의 실패율은 0으로 정의한다.

##### 입출력 예

| N    | stages                   | result          |
| ---- | ------------------------ | --------------- |
| 5    | [2, 1, 2, 6, 2, 4, 3, 3] | [3, 4, 2, 1, 5] |
| 4    | [4, 4, 4, 4, 4]          | [4, 1, 2, 3]    |

##### 입출력 예 설명

###### 입출력 예 #1

1번 스테이지는 총 8명의 사용자가 도전 했으며, 이 중 1명의 사용자가 아직 클리어 하지 못했다. 따라서 1번 스테이지의 실패율은 다음과 같다.

- 1번 스테이지 실패율 : 1/8

2번 스테이지에는 총 7명의 사용자가 도전했으며, 이 중 3명의 사용자가 아직 클리어하지 못했다. 따라서 2번 스테이지의 실패율은 다음과 같다.

- 2번 스테이지 실패율 : 3/7

마찬가지로 나머지 스테이지의 실패율은 다음과 같다.

- 3번 스테이지 실패율 : 2/4
- 4번 스테이지 실패율 : 1/2
- 5번 스테이지 실패율 : 0/1

각 스테이지의 번호를 실패율의 내림차순으로 정렬하면 다음과 같다.

- [3, 4, 2, 1, 5]

###### 입출력 예 #2

모든 사용자가 마지막 스테이지에 있으므로 4번 스테이지의 실패율은 1이며 나머지 스테이지의 실패율은 0이다.

- [4, 1, 2, 3]



### 답안 코드 작성 방식 예

##### python

```python
def solution(N, stages):
    answer = []
    return answer
```

##### java

```java
class Solution {
    public int[] solution(int N, int[] stages) {
        int[] answer = {};
        return answer;
    }
}
```

##### javascript

```javascript
function solution(N, stages) {
    var answer = [];
    return answer;
}
```

> 이외 다른 언어로 작성해도 됩니다.