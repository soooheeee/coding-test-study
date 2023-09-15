# [Bronze I] 소가 길을 건너간 이유 1 - 14467 

[문제 링크](https://www.acmicpc.net/problem/14467) 

### 성능 요약

메모리: 31256 KB, 시간: 40 ms

### 분류

구현

### 문제 설명

<p>닭이 길을 건너간 이유는 과학적으로 깊게 연구가 되어 있지만, 의외로 소가 길을 건너간 이유는 거의 연구된 적이 없다. 이 주제에 관심을 가지고 있었던 농부 존은 한 대학으로부터 소가 길을 건너는 이유에 대한 연구 제의를 받게 되었다.</p>

<p>존이 할 일은 소가 길을 건너는 것을 관찰하는 것이다. 존은 소의 위치를 N번 관찰하는데, 각 관찰은 소의 번호와 소의 위치 하나씩으로 이루어져 있다. 존은 소를 10마리 가지고 있으므로 소의 번호는 1 이상 10 이하의 정수고, 소의 위치는 길의 왼쪽과 오른쪽을 의미하는 0과 1 중 하나다.</p>

<p>이 관찰 기록을 가지고 소가 최소 몇 번 길을 건넜는지 알아보자. 즉 같은 번호의 소가 위치를 바꾼 것이 몇 번인지 세면 된다.</p>

### 입력 

 <p>첫 줄에 관찰 횟수 N이 주어진다. N은 100 이하의 양의 정수이다. 다음 N줄에는 한 줄에 하나씩 관찰 결과가 주어진다. 관찰 결과는 소의 번호와 위치(0 또는 1)로 이루어져 있다.</p>

### 출력 

 <p>첫 줄에 소가 길을 건너간 최소 횟수를 출력한다.</p>
 
-----

입력
8    ->관찰 횟수
3 1  -> 3은 소의 번호, 1는 오른쪽 (소의 위치)
3 0  -> 6은 소의 번호, 0은 왼쪽
6 0
2 1
4 1
3 0
4 0
3 1

3번 소는 총 2번 길을 건넘
4번 소는 총 1번 길을 건넘
따라서 총 소들은 3번 길을 건넘

출력
3


1->0 오른쪽에서 왼쪽으로 바뀌었으니, 길을 한 번 건넘 (반대로, 0->1도 똑같은 원리임)

-----
1. 관찰 횟수를 입력 받은 만큼 반복하는 반복문을 사용한다.
2. 소의 번호와 소의 위치를 입력 받는다.
3. 만약 딕셔너리에서 키들의 값에 소의 번호가 이미 존재한다면,
4. 만약 딕셔너리의 value값이 소의 현재 위치와 동일하다면 패스
5. 현재 위치와 동일한 조건이 아니라면 딕셔너리의 vlaue값이 현재 위치와 동일하게 해주고 카운트+1
6. 딕셔너리에서 키들의 값에 소의 번호가 존재하지 않는다면, key와 value추가
7. 총 몇 번 건넜는지 출력하기