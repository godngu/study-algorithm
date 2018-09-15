# Cycle ã��
n ���� node�� �̷���� ������ directed graph�� �־����� ��, ���̰� m�� cycle�� ã�� ����ϴ� ���α׷��� �ۼ��Ͻÿ�. cycle�� ���� �� �ִ� ���, �� �߿��� �ƹ��ų� ����ص� ����. * Directed graph ��, � node A���� �ٸ� node B�� �̵��� �� �ִ� edge�� �����Ѵٰ� �ؼ�, B���� �ٽ� A�� �̵��� �� �ִ� edge�� �׻� ���������� �ʴ� graph�̴�. * �� ���������� cycle�� ���� ������ ��� �����ϴ� sequence�� �����Ѵ�. * 0 �� i < m-1 �� �ش��ϴ� i�� ����, i��° node���� i+1��° node�� �̵��ϴ� edge�� �����ؾ� �Ѵ�. * ������ node���� ù��° node�� �̵��ϴ� edge�� �����ؾ� �Ѵ�. * ������ node�� ������ sequence�� ������ �� �ִ�

�����ؾ� �ϴ� method�� signature�� ������ ����.

```java
void findCycle(boolean[][] graph, int m) {
    // assume graph is NXN adjacency matrix
    // TODO: Implement
}
```

graph[x][y]�� ���� true�� ���, x���� y�� ���� edge�� �����ϰ�, false�� ���, edge�� �������� �ʴ� ��.

�Է� ������ ������ ����.

```java
boolean[][] graph = {{false,true,false,true},{true,false,false,false},
{true,false,false,false}, {false,false,true,false}};
findCycle(graph, 3);
```

����� stdout�� ������ ���� ����Ѵ�.

cycle�� �ִ� ��� : ù �ٿ� 1�� ����ϰ�, ���� �ٿ� cycle�� �����ϴ� m���� node ��ȣ�� ������� ��
���Ѵ�.
```
1 
0 3 2
```

�� �Է� ��������, graph[0][3], graph[3][2], graph[2][0]�� ��� true�̹Ƿ�. 0,3,2�� ���� 3�� cycle�� ������ �����Ѵ�.

cycle�� ���� ���
```
0
```