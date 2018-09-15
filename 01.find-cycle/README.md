# Cycle 찾기
n 개의 node로 이루어진 임의의 directed graph가 주어졌을 때, 길이가 m인 cycle을 찾아 출력하는 프로그램을 작성하시오. cycle이 여러 개 있는 경우, 그 중에서 아무거나 출력해도 좋다. * Directed graph 란, 어떤 node A에서 다른 node B로 이동할 수 있는 edge가 존재한다고 해서, B에서 다시 A로 이동할 수 있는 edge가 항상 존재하지는 않는 graph이다. * 이 문제에서의 cycle은 다음 조건을 모두 만족하는 sequence로 정의한다. * 0 ≤ i < m-1 에 해당하는 i에 대해, i번째 node에서 i+1번째 node로 이동하는 edge가 존재해야 한다. * 마지막 node에서 첫번째 node로 이동하는 edge가 존재해야 한다. * 동일한 node가 여러번 sequence에 등장할 수 있다

구현해야 하는 method의 signature는 다음과 같다.

```java
void findCycle(boolean[][] graph, int m) {
    // assume graph is NXN adjacency matrix
    // TODO: Implement
}
```

graph[x][y]의 값이 true인 경우, x에서 y로 가는 edge가 존재하고, false인 경우, edge가 존재하지 않는 다.

입력 예제는 다음과 같다.

```java
boolean[][] graph = {{false,true,false,true},{true,false,false,false},
{true,false,false,false}, {false,false,true,false}};
findCycle(graph, 3);
```

출력은 stdout에 다음과 같이 출력한다.

cycle이 있는 경우 : 첫 줄에 1을 출력하고, 다음 줄에 cycle을 구성하는 m개의 node 번호를 순서대로 출
력한다.
```
1 
0 3 2
```

위 입력 예제에서, graph[0][3], graph[3][2], graph[2][0]이 모두 true이므로. 0,3,2는 길이 3인 cycle의 조건을 만족한다.

cycle이 없는 경우
```
0
```