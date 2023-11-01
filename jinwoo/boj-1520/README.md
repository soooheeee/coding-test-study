# 내리막 길

## 문제

- [https://www.acmicpc.net/problem/1520](https://www.acmicpc.net/problem/1520)

## 난이도

- 골드 3

## 풀이

### 방법 1: DFS로 풀어보자

&nbsp; 가장 먼저 떠오른 방법은 DFS로 풀어보는 방법이였다. `DFS(Depth-First Search)`는 `깊이우선탐색`이라고도 하는데, 그래프에서 깊은 부분을 우선적으로 탐색하는 알고리즘이다. 순서를 살펴보자.<br>

```
1. 탐색 시작 노드를 스택에 삽입하고 방문 처리를 한다.
2. 스택의 최상단 노드에 방문하지 않은 인접 노드가 있으면 그 인접 노드를 스택에 넣고 방문 처리를 한다. 방문하지 않은 인접 노드가 없으면 스택에서 최상단 노드를 꺼낸다.
3. 2번 과정을 더 이상 수행할 수 없을 때까지 반복한다.
```

&nbsp; 이제 DFS를 이 문제에 적용시켜보자.

<img width="198" alt="image" src="https://user-images.githubusercontent.com/68031450/279544224-7d8b08b0-3465-43c1-867f-927c87eefd42.png">

&nbsp; 가장 먼저 왼쪽 위에서 시작을 하기 때문에 `50`이 스택에 들어가고 방문 처리를 한다. 그 후 `상, 하, 좌, 우`를 순서대로 살펴볼 것이다. 상에는 노드가 없으므로 하의 노드인 `35`를 스택에 넣고 방문 처리를 한다. 물론 방문 처리를 하기 이전에 이전 노드(스택의 top)보다 35가 작은 수 인지 확인해야 할 것이다. 이러한 과정을 반복하여 (5, 5) 좌표에 있는 10에 도달하게 되면 하나의 경로를 찾게 되는 것이다.