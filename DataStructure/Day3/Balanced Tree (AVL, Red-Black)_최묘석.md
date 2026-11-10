
# 📑 Balanced Tree (AVL, Red-Black) 정리

> **발표자**: 최묘석  
> **날짜**: 2026-11-10  
> **카테고리**: Data Structure  
> **참고 링크**: 

---

## 1. 개요 및 정의

> 이진 탐색 트리(BST)의 한계를 알아보고, AVL Tree와 Red-Black Tree가 균형을 유지하는 원리를 정리.

### 이진 탐색 트리(BST)

**이진 탐색 트리(Binary Search Tree, BST)**는 각 노드의 왼쪽 서브트리에는 작은 값을, 오른쪽 서브트리에는 큰 값을 저장하는 이진 트리이다.

```text
        50
       /  \
     30    70
    / \    / \
   20 40  60 80
```

예를 들어 40을 찾는다면 `50 → 30 → 40` 순서로 탐색한다.

BST는 이러한 규칙을 이용해 모든 노드를 확인하지 않고도 원하는 값을 찾을 수 있다.

### 일반 BST의 문제점

BST는 삽입 순서에 따라 한쪽으로 치우칠 수 있다.

**균형이 잡힌 경우**

```text
        30
       /  \
     20    40
    /        \
   10         50
```

**한쪽으로 치우친 경우**

```text
    10
      \
       20
         \
          30
            \
             40
               \
                50
```

두 트리는 같은 데이터를 저장하지만, 50을 찾을 때 확인해야 하는 노드 수가 다르다.

- 균형 잡힌 BST: `30 → 40 → 50` (3개)
- 한쪽으로 치우친 BST: `10 → 20 → 30 → 40 → 50` (5개)

일반 BST는 트리의 높이가 커지면 최악의 경우 탐색에 **O(N)** 시간이 걸린다.

이를 해결하기 위해 등장한 것이 **균형 이진 탐색 트리(Self-Balancing BST)**이다.

대표적인 종류로 AVL Tree와 Red-Black Tree가 있다.

---

## 2. 핵심 동작 원리 및 특징

### 2-1. 트리의 높이와 균형

트리의 **높이(Height)**는 특정 노드에서 가장 멀리 있는 리프 노드까지의 거리이다.

여기서는 노드 수를 기준으로 높이를 계산한다.

- 빈 트리의 높이: 0
- 리프 노드의 높이: 1

```text
          30         높이 3
         /  \
       20    40      높이 2
      /
     10              높이 1
```

균형 트리는 삽입과 삭제가 발생하더라도 높이가 지나치게 커지지 않도록 관리한다.

다만 AVL과 Red-Black Tree는 균형을 판단하는 기준이 다르다.

### 2-2. AVL Tree

**AVL Tree**는 모든 노드에서 왼쪽과 오른쪽 서브트리의 높이 차이가 1 이하가 되도록 유지하는 BST이다.

이를 확인하기 위해 **균형 인수(Balance Factor, BF)**를 사용한다.

```text
BF = 왼쪽 서브트리 높이 - 오른쪽 서브트리 높이
```

예를 들어 다음 트리를 살펴보면,

```text
          30
         /  \
       20    40
      /
     10
```

루트 노드 30의 왼쪽 서브트리 높이는 2이고, 오른쪽 서브트리 높이는 1이다.

따라서 `BF = 2 - 1 = 1`이므로 균형이 유지된다.

AVL Tree에서는 모든 노드의 BF가 `-1`, `0`, `1` 중 하나여야 한다.

### 2-3. AVL Tree의 회전(Rotation)

새로운 노드가 삽입되어 균형이 깨지면 **회전(Rotation)**을 수행한다.

회전은 노드의 값을 변경하는 것이 아니라, 부모와 자식의 연결 관계를 바꾸는 연산이다.

대표적으로 네 가지 불균형 유형이 있다.

#### LL 유형 - 오른쪽 회전

30 → 20 → 10 순서로 삽입한 경우이다.

**회전 전**

```text
        30
       /
      20
     /
    10
```

**오른쪽 회전 후**

```text
        20
       /  \
      10   30
```

왼쪽으로 치우친 트리를 오른쪽으로 회전하여 균형을 복구한다.

#### RR 유형 - 왼쪽 회전

10 → 20 → 30 순서로 삽입한 경우이다.

**회전 전**

```text
    10
      \
       20
         \
          30
```

**왼쪽 회전 후**

```text
        20
       /  \
      10   30
```

오른쪽으로 치우친 트리를 왼쪽으로 회전한다.

#### LR 유형 - 왼쪽 회전 후 오른쪽 회전

30 → 10 → 20 순서로 삽입한 경우이다.

```text
[회전 전]

        30
       /
      10
        \
         20

[10을 기준으로 왼쪽 회전]

        30
       /
      20
     /
    10

[30을 기준으로 오른쪽 회전]

        20
       /  \
      10   30
```

#### RL 유형 - 오른쪽 회전 후 왼쪽 회전

10 → 30 → 20 순서로 삽입한 경우이다.

```text
[회전 전]

    10
      \
       30
      /
     20

[30을 기준으로 오른쪽 회전]

    10
      \
       20
         \
          30

[10을 기준으로 왼쪽 회전]

        20
       /  \
      10   30
```

**AVL 회전 유형 정리**

| 불균형 유형 | 발생 위치 | 해결 방법 |
| :--- | :--- | :--- |
| LL | 왼쪽 자식의 왼쪽 | 오른쪽 회전 |
| RR | 오른쪽 자식의 오른쪽 | 왼쪽 회전 |
| LR | 왼쪽 자식의 오른쪽 | 왼쪽 회전 → 오른쪽 회전 |
| RL | 오른쪽 자식의 왼쪽 | 오른쪽 회전 → 왼쪽 회전 |

### 2-4. Red-Black Tree

**Red-Black Tree**는 노드에 빨간색(Red)과 검정색(Black)을 부여하고, 색상 규칙을 이용해 균형을 유지하는 BST이다.

AVL Tree가 높이 차이를 엄격하게 관리한다면, Red-Black Tree는 색상 규칙을 통해 트리의 높이가 지나치게 커지는 것을 방지한다.

**Red-Black Tree의 주요 규칙**

1. 모든 노드는 빨간색 또는 검정색이다.
2. 루트 노드는 검정색이다.
3. 모든 NIL 노드는 검정색이다.
4. 빨간색 노드의 자식은 반드시 검정색이다.
5. 특정 노드에서 모든 하위 NIL 노드까지의 경로에 포함되는 검정색 노드 수는 같다.

여기서 **NIL 노드**는 실제 데이터가 없는 빈 자식 위치를 의미한다.

**Red-Black Tree 예시**

```text
           20(B)
          /     \
       10(B)    30(B)
                /   \
             25(R)  40(R)
```

- `(B)`: Black
- `(R)`: Red

빨간색 노드인 25와 40의 자식은 NIL 노드이므로 검정색으로 취급한다.

또한 루트에서 각 NIL 노드까지 내려가는 경로의 검정색 노드 수가 동일하다.

### 2-5. Red-Black Tree의 삽입 과정

Red-Black Tree는 새로운 노드를 일반적으로 빨간색으로 삽입한다.

삽입 후 규칙이 깨지면 **색상 변경(Recoloring)** 또는 **회전(Rotation)**으로 복구한다.

10 → 20 → 30 순서로 삽입하는 경우를 살펴봤다.

**1단계 - 10 삽입**

```text
       10(B)
```

루트 노드이므로 검정색으로 설정한다.

**2단계 - 20 삽입**

```text
       10(B)
           \
           20(R)
```

부모가 검정색이므로 규칙을 위반하지 않는다.

**3단계 - 30 삽입**

```text
       10(B)
           \
           20(R)
               \
               30(R)
```

빨간색 노드 20의 자식인 30도 빨간색이므로 규칙을 위반한다.

**4단계 - 회전 및 색상 변경**

```text
       20(B)
      /     \
   10(R)   30(R)
```

왼쪽 회전과 색상 변경을 통해 규칙을 복구한다.

Red-Black Tree에서는 부모뿐 아니라 **삼촌(Uncle) 노드**의 색상도 확인한다.

삼촌 노드는 부모 노드의 형제 노드를 의미한다.

예를 들어 다음 구조에서 15의 삼촌은 30이다.

```text
          20(B)
         /     \
      10(B)    30(B)
         \
         15(R)
```

삽입 후 부모와 삼촌의 색상에 따라 색상 변경만 수행하거나 회전을 함께 수행한다.

### 2-6. AVL Tree와 Red-Black Tree 비교

| 구분 | AVL Tree | Red-Black Tree |
| :--- | :--- | :--- |
| 균형 판단 기준 | 서브트리 높이 차이 | 노드의 색상 규칙 |
| 균형 유지 | 상대적으로 엄격함 | 상대적으로 유연함 |
| 균형 복구 | 회전 | 색상 변경 및 회전 |
| 탐색 성능 | 높이가 더 낮게 유지되는 경향 | 효율적인 탐색 가능 |
| 삽입·삭제 | 재균형 부담이 클 수 있음 | 일반적으로 변경 작업에 유리 |
| 탐색 | O(log N) | O(log N) |
| 삽입 | O(log N) | O(log N) |
| 삭제 | O(log N) | O(log N) |

두 자료구조 모두 트리의 높이를 O(log N) 수준으로 유지한다.

따라서 일반 BST와 달리 삽입 순서가 한쪽으로 치우쳐도 탐색 성능이 O(N)까지 악화되는 것을 방지한다.

### 2-7. Python으로 AVL Tree 구현

AVL Tree는 BST의 삽입 기능에 높이 계산과 회전 기능을 추가하여 구현할 수 있다.

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None
        self.height = 1


def height(node):
    if node is None:
        return 0
    return node.height


def update_height(node):
    node.height = 1 + max(
        height(node.left),
        height(node.right)
    )


def balance(node):
    return height(node.left) - height(node.right)


def rotate_left(x):
    y = x.right
    middle = y.left

    y.left = x
    x.right = middle

    update_height(x)
    update_height(y)

    return y


def rotate_right(y):
    x = y.left
    middle = x.right

    x.right = y
    y.left = middle

    update_height(y)
    update_height(x)

    return x


def insert(root, value):
    if root is None:
        return Node(value)

    if value < root.value:
        root.left = insert(root.left, value)
    elif value > root.value:
        root.right = insert(root.right, value)
    else:
        return root

    update_height(root)
    bf = balance(root)

    if bf > 1:
        if value > root.left.value:
            root.left = rotate_left(root.left)
        return rotate_right(root)

    if bf < -1:
        if value < root.right.value:
            root.right = rotate_right(root.right)
        return rotate_left(root)

    return root


root = None

for value in [10, 20, 30]:
    root = insert(root, value)

print(root.value)
print(root.left.value)
print(root.right.value)
```

**실행 결과**

```text
20
10
30
```

일반 BST에서는 10 → 20 → 30 형태로 한쪽으로 치우치지만, AVL Tree는 왼쪽 회전을 통해 20을 루트로 변경한다.

코드에서 중요한 부분은 삽입 후 `update_height()`로 높이를 갱신하고, `balance()`로 균형 인수를 확인하는 과정이다.

회전 이후에는 서브트리의 루트가 변경될 수 있으므로 새로운 루트를 반환하여 부모 노드와 연결해야 한다.

### 2-8. Python에서 Red-Black Tree의 구조 이해

Red-Black Tree는 AVL과 달리 높이 대신 색상 정보를 관리한다.

```python
class Node:
    def __init__(self, value, color="RED"):
        self.value = value
        self.color = color
        self.left = None
        self.right = None
        self.parent = None
```

AVL Tree와 비교하면 `height` 대신 `color`를 사용하고, 부모 노드를 추적하기 위한 `parent`가 추가되어 있다.

삽입 후에는 부모와 삼촌 노드의 색상을 확인하고, 필요한 경우 회전과 색상 변경을 수행한다.

전체 삽입 알고리즘은 AVL보다 복잡하지만, **BST의 기본 삽입 → 색상 규칙 확인 → 색상 변경 또는 회전**이라는 흐름으로 이해할 수 있다.

---

## 3. 실무 / 면접 핵심 포인트

### Q1. 일반 BST와 Balanced Tree의 차이점을 설명하시오.

- **A**: 일반 BST는 삽입 순서에 따라 한쪽으로 치우칠 수 있으며, 이 경우 탐색 시간복잡도가 최악의 경우 O(N)이 됩니다.

  반면 Balanced Tree는 삽입과 삭제 이후에도 트리의 균형을 유지하여 높이가 지나치게 커지는 것을 방지합니다.

  대표적인 AVL Tree와 Red-Black Tree는 탐색, 삽입, 삭제를 O(log N)에 수행할 수 있습니다.

### Q2. AVL Tree와 Red-Black Tree의 차이점을 설명하시오.

- **A**: AVL Tree는 모든 노드에서 왼쪽과 오른쪽 서브트리의 높이 차이를 1 이하로 유지합니다. 균형이 깨지면 회전을 통해 복구합니다.

  Red-Black Tree는 노드의 색상 규칙을 이용해 균형을 유지하며, 색상 변경과 회전을 사용합니다.

  AVL Tree는 상대적으로 엄격하게 균형을 유지하므로 탐색에 유리한 경향이 있고, Red-Black Tree는 균형 조건이 상대적으로 유연하여 삽입과 삭제가 빈번한 상황에서 유리할 수 있습니다.

### Q3. AVL Tree에서 회전이 필요한 이유를 설명하시오.

- **A**: 새로운 노드를 삽입하거나 기존 노드를 삭제한 뒤 트리의 높이가 한쪽으로 치우칠 수 있기 때문입니다.

  AVL Tree는 균형 인수가 -1, 0, 1 범위를 벗어나면 회전을 수행합니다.

  회전은 노드의 연결 관계를 변경하면서 BST의 정렬 규칙을 유지하고, 트리의 균형을 복구하는 연산입니다.

### 균형 트리의 활용과 선택 기준

AVL Tree와 Red-Black Tree의 특징을 비교하면서 어떤 상황에서 각각의 구조가 적합한지 정리했다.

AVL Tree는 높이를 엄격하게 관리하므로 **탐색이 빈번하고 데이터 변경이 상대적으로 적은 상황**에서 고려할 수 있다.

반면 Red-Black Tree는 삽입과 삭제 과정에서 색상 변경으로 균형을 복구할 수 있어 **탐색뿐 아니라 데이터 변경도 자주 발생하는 상황**에 적합하다.

대표적인 예시로 Java의 `TreeMap`과 `TreeSet`은 Red-Black Tree 기반으로 구현되어 있다.

다만 실제 성능은 데이터의 특성이나 구현 방식에 따라 달라지므로, 특정 자료구조가 모든 상황에서 더 빠르다고 단정할 수는 없다.

### 학습하며 느낀 점

기존에는 BST가 왼쪽에 작은 값, 오른쪽에 큰 값을 저장하기 때문에 항상 빠르게 탐색할 수 있다고 생각했다. 하지만 삽입 순서에 따라 트리가 한쪽으로 치우치면 연결 리스트와 비슷한 구조가 되어 탐색 성능이 떨어질 수 있다는 점을 알게 되었다.

AVL Tree의 회전 과정을 직접 따라가면서 노드의 값은 그대로 유지한 채 연결 관계만 변경해 균형을 복구할 수 있다는 점을 이해했다.

또한 Red-Black Tree는 AVL처럼 높이를 직접 비교하지 않고 색상 규칙을 이용한다는 점이 흥미로웠다.

두 자료구조 모두 탐색 성능을 유지하기 위한 균형 트리이지만, 균형을 얼마나 엄격하게 관리하느냐에 따라 삽입과 삭제 과정의 특징이 달라진다는 점을 정리할 수 있었다.

---

## 4. 오프라인 모임 Q&A 기록 (발표 후 작성)

> 스터디원들과 나눈 질문이나 토론 내용을 발표 후 작성.

- **Q (스터디원 A)**:
- **A (발표자)**:
- **느낀 점 / 보충할 점**:
