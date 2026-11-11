# ☕ CS-Study (Computer Science 기술 면접 스터디)

> **"지식을 나누며 함께 성장하는 주 2회 CS 기술 면접 아카이빙 스터디"**  
> SSAFY 일과 후 카페에 모여 준비한 주제를 짧게 발표하고 질의응답을 나눈 뒤, GitHub에 기록하여 취업 준비를 위한 우리만의 레퍼런스를 구축합니다.

---

## 👥 스터디원 (총 7명)

<table>
  <tr>
    <td align="center" width="120px">
      <a href="https://github.com/strongsun806">
        <img src="https://github.com/strongsun806.png" width="80px" alt="권혜강 프로필" style="border-radius: 50%;" /><br />
        <sub><b>권혜강</b></sub>
      </a><br />
      <a href="https://github.com/strongsun806">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
      </a>
    </td>
    <td align="center" width="120px">
      <a href="https://github.com/GrayBoxTool">
        <img src="https://github.com/GrayBoxTool.png" width="80px" alt="최묘석 프로필" style="border-radius: 50%;" /><br />
        <sub><b>최묘석</b></sub>
      </a><br />
      <a href="https://github.com/GrayBoxTool">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
      </a>
    </td>
    <td align="center" width="120px">
      <a href="https://github.com/aaaaef">
        <img src="https://github.com/aaaaef.png" width="80px" alt="최승우 프로필" style="border-radius: 50%;" /><br />
        <sub><b>최승우</b></sub>
      </a><br />
      <a href="https://github.com/aaaaef">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
      </a>
    </td>
    <td align="center" width="120px">
      <a href="https://github.com/gudtjq32450">
        <img src="https://github.com/gudtjq32450.png" width="80px" alt="윤형섭 프로필" style="border-radius: 50%;" /><br />
        <sub><b>윤형섭</b></sub>
      </a><br />
      <a href="https://github.com/gudtjq32450">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
      </a>
    </td>
    <td align="center" width="120px">
      <a href="https://github.com/peanut-cherry">
        <img src="https://github.com/peanut-cherry.png" width="80px" alt="최나현 프로필" style="border-radius: 50%;" /><br />
        <sub><b>최나현</b></sub>
      </a><br />
      <a href="https://github.com/peanut-cherry">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
      </a>
    </td>
    <td align="center" width="120px">
      <a href="https://github.com/xodrndishfwk-crypto">
        <img src="https://github.com/xodrndishfwk-crypto.png" width="80px" alt="김영웅 프로필" style="border-radius: 50%;" /><br />
        <sub><b>김영웅</b></sub>
      </a><br />
      <a href="https://github.com/xodrndishfwk-crypto">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
      </a>
    </td>
    <td align="center" width="120px">
      <a href="https://github.com/sue9585">
        <img src="https://github.com/sue9585.png" width="80px" alt="조수연 프로필" style="border-radius: 50%;" /><br />
        <sub><b>조수연</b></sub>
      </a><br />
      <a href="https://github.com/sue9585">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
      </a>
    </td>
  </tr>
</table>

---

## 📅 진행 현황 & 다음 일정

| 회차 | 날짜 | 주제 | 상태 |
| :---: | :---: | :--- | :---: |
| 1회차 | 11/4 (수) | DS: Array vs LinkedList / Stack & Queue<br>NW: OSI 7 계층 & TCP/IP 4 계층 | ✅ 완료 |
| 2회차 | 11/6 (금) | DS: Tree 기초 & BST (예상 질문 Q&A)<br>NW: 네트워크 전체 흐름 개요 | ✅ 완료 |
| 3회차 | 11/10 (화) 18:30 · 투썸플레이스 | DS: Balanced Tree (AVL, Red-Black)<br>NW: TCP vs UDP / TCP Handshake, TCP 제어 기법 / 포트 포워딩 | ✅ 완료 |
| 4회차 | 11/12 (목) | DS: Heap & Priority Queue / Hash Table<br>NW: HTTP vs HTTPS / SSL 핸드셰이크 | 🔜 예정 |

### ✅ 2회차 (11/6) 요약

<details>
<summary>펼쳐서 보기</summary>

**DS: Tree 기초 & BST**

- 트리는 연결되고 사이클이 없는 그래프라서, 노드가 N개면 간선은 항상 N-1개입니다.
- 이진 트리는 모양 규칙, BST는 값의 정렬 규칙까지 포함합니다. BST 판별은 직속 자식만 비교하면 오답이고, 범위 전달이나 중위 순회로 확인합니다.
- BST는 정렬된 순서로 넣으면 편향 트리가 되어 O(N)으로 퇴화하고, 이를 막는 것이 자가 균형 트리(AVL, Red-Black)입니다.
- 자식이 둘인 노드를 삭제할 땐 중위 선행자나 후속자로 대체합니다.

**NW: 네트워크 전체 흐름 개요**

- 구성: 노드와 간선, 호스트, 네트워크 장비, 통신 매체, 메시지. 서버와 클라이언트는 기계가 아니라 역할입니다.
- 범위: LAN, CAN, MAN, WAN. 인터넷은 WAN의 대표 예시일 뿐입니다.
- 교환 방식: 회선 교환(길 예약)과 패킷 교환(쪼개서 전송). 오늘날 인터넷은 대부분 패킷 교환입니다.
- 요청 흐름: DNS로 IP 획득, TCP 연결, TLS, HTTP 요청, 응답, 렌더링.
- 캡슐화: TCP, IP, 링크 헤더를 차례로 붙이고, 라우터는 구간마다 링크 포장(MAC)을 새로 씌웁니다.
- 이슈에서 나온 추가 주제(포트 포워딩, NAPT)는 3회차에서 이어서 다룹니다.

</details>

### ✅ 3회차 (11/10) 요약

<details>
<summary>펼쳐서 보기</summary>

**📂 발표 자료**

| 파트 | 발표자 | 자료 |
| :---: | :---: | :--- |
| DS | 최묘석, 김영웅 | [Balanced Tree (AVL, Red-Black)_최묘석.md](./DataStructure/Day3/Balanced%20Tree%20(AVL,%20Red-Black)_최묘석.md)<br>[AVL_RedBlack_발표자료_22페이지.pdf](./DataStructure/Day3/AVL_RedBlack_발표자료_22페이지.pdf) |
| NW | 조수연, 권혜강 | [TCP_Handshake_조수연_발표자료.pdf](./Network/Day3/TCP_Handshake_조수연_발표자료.pdf) ([pptx](./Network/Day3/TCP_Handshake_조수연_발표용.pptx))<br>[3회차_NW_TCP_UDP_포트포워딩_권혜강.pdf](./Network/Day3/3회차_NW_TCP_UDP_포트포워딩_권혜강.pdf) |

---

#### 🌳 DS: Balanced Tree (AVL, Red-Black)

**왜 필요한가**

- BST는 정렬된 값을 순서대로 넣으면 한쪽으로 치우쳐 탐색이 O(N)이 됩니다.
- 균형 트리는 높이를 O(log N)으로 묶어 탐색·삽입·삭제의 최악 시간을 O(log N)으로 보장합니다.

**AVL 트리**

- 균형 인수 `BF = 왼쪽 높이 - 오른쪽 높이`가 모든 노드에서 -1, 0, +1이어야 합니다.
- 균형이 깨지면 회전합니다. 회전은 값을 바꾸지 않고 부모·자식 연결만 바꾸며, BST 대소 관계는 그대로 유지됩니다.

| 유형 | 발생 위치 | 해결 |
| :---: | :--- | :--- |
| LL | 왼쪽 자식의 왼쪽 | 오른쪽 회전 |
| RR | 오른쪽 자식의 오른쪽 | 왼쪽 회전 |
| LR | 왼쪽 자식의 오른쪽 | 왼쪽 회전 → 오른쪽 회전 |
| RL | 오른쪽 자식의 왼쪽 | 오른쪽 회전 → 왼쪽 회전 |

- **삽입**: 회전 한 번(단일 또는 이중)이면 위쪽까지 균형이 맞춰집니다.
- **삭제**: 회전 후 서브트리 높이가 줄 수 있어 루트까지 올라가며 반복합니다. 회전이 최대 O(log N)번 일어날 수 있습니다.

**Red-Black 트리**

1. 모든 노드는 빨강 또는 검정
2. 루트는 검정
3. 모든 NIL 노드는 검정
4. 빨강 노드의 자식은 검정 (빨강 연속 불가)
5. 어떤 노드에서 NIL까지 가는 모든 경로의 검정 노드 수는 같음

→ 가장 긴 경로가 가장 짧은 경로의 2배를 넘지 않는 **느슨한 균형**입니다.

- **삽입**: 새 노드는 빨강으로 넣고, 부모도 빨강이면 **삼촌**의 색을 봅니다.
  - 삼촌이 빨강 → **Recoloring**: 부모·삼촌을 검정, 조부모를 빨강으로 바꾸고 위로 반복
  - 삼촌이 검정 → **Restructuring**: 회전 후 종료 (최대 2번)
- **삭제**: 검정 노드를 지우면 그 경로의 검정이 1개 모자란 **Double Black**이 생기고, **형제**를 보고 해결합니다.

| 상황 | 처리 |
| :--- | :--- |
| 형제 검정 + 먼 조카 빨강 | 부모 기준 회전 + 색 정리 → 끝 |
| 형제 검정 + 가까운 조카만 빨강 | 형제 기준 회전 → 위 경우로 |
| 형제 검정 + 조카 모두 검정 | 형제를 빨강으로 바꾸고 부족분을 부모로 넘김 |
| 형제 빨강 | 부모·형제 색 교환 후 회전 → 형제가 검정인 경우로 |

> 💡 **"형제에게 빌릴 빨강이 있으면 회전, 없으면 위로 넘긴다."** 삭제 회전은 최대 3번입니다.

**자식이 2개인 노드 삭제 (AVL·RB 공통)**

- 바로 지우지 않고 **중위 후속자**(오른쪽 서브트리의 최솟값)로 값을 교체한 뒤, 후속자 노드를 대신 지웁니다.
- 후속자는 왼쪽 자식이 없어서 항상 자식이 0~1개입니다. 그래서 균형 복구는 실제로 지워진 후속자 자리에서 시작합니다.

**AVL vs Red-Black**

| 구분 | AVL | Red-Black |
| :---: | :--- | :--- |
| 균형 기준 | 서브트리 높이 차 | 색 규칙 |
| 균형 정도 | 엄격 | 느슨 |
| 탐색 | 더 빠른 편 | 약간 느릴 수 있음 |
| 삽입 회전 | 최대 1번 (이중 포함) | 최대 2번 |
| 삭제 회전 | 최대 O(log N)번 | 최대 3번 |
| 추가 정보 | 높이(BF) | 색 1비트 |
| 시간 복잡도 | 탐색·삽입·삭제 O(log N) | 탐색·삽입·삭제 O(log N) |

**실무 연결**

- **Java TreeMap**: Red-Black 트리입니다. `deleteEntry()`가 후속자 교체 → 실제 삭제 → `fixAfterDeletion()` 순서로 동작하고, `ceilingKey()`도 후속자 찾기와 같은 원리입니다.
- **DB 인덱스(B+트리)**: 페이지가 비면 형제에게서 빌리거나 병합 후 부모로 넘깁니다. RB 삭제와 비슷한 발상이고, 대량 DELETE를 나눠 실행하거나 소프트 삭제(`deleted_at`)를 쓰는 이유 중 하나입니다.
- **리눅스 CPU 스케줄러**: 가장 왼쪽(가장 덜 실행된) 프로세스를 꺼내 실행합니다. 삽입·삭제가 매우 잦아 회전이 적은 RB가 유리합니다.

---

#### 🌐 NW: TCP vs UDP / Handshake / TCP 제어 / 포트 포워딩

**TCP vs UDP**

- IP는 "어느 컴퓨터로", 포트는 "그 컴퓨터의 어느 프로그램으로"를 정합니다. 연결 하나는 (출발지 IP, 출발지 포트, 목적지 IP, 목적지 포트, 프로토콜) 5개 값으로 구분합니다.

| 구분 | TCP | UDP |
| :---: | :--- | :--- |
| 연결 | 연결 지향 (3-way handshake 후 전송) | 비연결 |
| 신뢰성 | 재전송·순서 보장·중복 제거 | 보장 안 함 |
| 제어 | 흐름·혼잡·오류 제어 | 없음 |
| 데이터 경계 | 바이트 스트림 | 데이터그램 단위 |
| 헤더 | 20~60바이트 | 8바이트 |
| 사용처 | 웹(HTTP/1.1·2), SSH, 이메일, DB | DNS, 게임, 음성·영상 통화, DHCP, QUIC |

**3-way Handshake (연결)**

- `SYN(seq=x)` → `SYN+ACK(seq=y, ack=x+1)` → `ACK(ack=y+1)`
- 서로의 준비 상태와 초기 순서 번호(ISN)를 확인합니다. ISN은 이전 연결 패킷과 섞이거나 예측당하지 않도록 무작위로 정합니다.
- **2번이 아닌 이유**: 서버는 자기 번호가 클라이언트에 닿았는지 확신할 수 없고, 늦게 도착한 옛 SYN에 속아 연결을 열 수 있습니다.
- 전화 비유: "연결할래요?" → "좋아요, 저도 준비됐어요" → "확인했어요!"

**4-way Handshake (종료)**

- `FIN` → `ACK` → (남은 데이터 전송) → `FIN` → `ACK`
- TCP는 양방향을 각각 닫습니다. FIN을 받은 쪽은 아직 보낼 데이터가 있을 수 있어 ACK와 FIN을 합치지 못합니다(Half-Close).
- **CLOSE_WAIT**가 서버에 잔뜩 쌓였다면 코드에서 소켓을 안 닫은 버그일 가능성이 큽니다.
- **TIME_WAIT**: 먼저 끊은 쪽이 2MSL 동안 기다립니다. ① 마지막 ACK가 유실되면 상대가 FIN을 다시 보내기 때문이고, ② 늦게 온 옛 패킷이 새 연결에 섞이는 것을 막기 위해서입니다.
- 실무: 짧은 연결을 대량으로 맺고 끊으면 TIME_WAIT 소켓이 쌓여 포트가 부족해집니다 → Keep-Alive, 커넥션 풀로 재사용합니다.

**TCP 제어 기법**

| 제어 | 지키는 대상 | 방법 |
| :---: | :---: | :--- |
| 흐름 제어 | 수신자 | 슬라이딩 윈도우, rwnd(수신 윈도우). rwnd = 0이면 전송 중단 후 Zero Window Probe |
| 혼잡 제어 | 네트워크 | cwnd(혼잡 윈도우). Slow Start(지수 증가) → 임계치 이후 AIMD(선형 증가, 손실 시 절반). 3 Duplicate ACK → Fast Retransmit/Recovery |
| 오류 제어 | 데이터 | 체크섬, ACK, 타임아웃·중복 ACK 시 재전송 |

> 💡 송신자가 한 번에 보낼 수 있는 양은 `min(rwnd, cwnd)`입니다.

**포트 포워딩**

- **공유기(라우터)의 NAT**에서 일어납니다. 외부에서 `공인 IP:포트`로 들어온 요청을 미리 정한 규칙에 따라 `내부 사설 IP:포트`로 바꿔 전달합니다(DNAT).
- IP(3계층)와 포트(4계층)를 함께 다루므로 **L3~L4 동작**입니다.
- 여러 기기가 공인 IP 하나를 쓸 때는 포트까지 변환하는 **NAPT**와 변환 테이블을 씁니다.

```plaintext
[외부 사용자] → 203.0.113.5:8080
      ↓
[공유기 NAT] 규칙: 외부 8080 → 192.168.0.10:80
      ↓
[내부 서버 192.168.0.10:80]
```

| 구분 | 일반 NAT (NAPT) | 포트 포워딩 |
| :---: | :--- | :--- |
| 방향 | 내부 → 외부 | 외부 → 내부 |
| 규칙 | 나갈 때 자동 생성 | 관리자가 미리 설정 |
| 예시 | 집 PC로 웹 서핑 | 집 서버를 외부에 공개 |

- 생각해볼 질문: ngrok은 공유기 설정 없이 어떻게 로컬 서버를 외부에 공개할까? 포트가 고갈되면 어떻게 될까?

</details>

### 🔜 4회차 준비 사항

| 구분 | 대상 | 할 일 | 마감 |
| :---: | :---: | :--- | :---: |
| **DS 발표** | 조수연, 윤형섭, 권혜강 | **Heap & Priority Queue / Hash Table** 정리 후 `DataStructure/Day4/` 폴더에 PR | 모임 전날까지 |
| **NW 발표** | 최묘석, 최나현, 김영웅, 최승우 | **HTTP vs HTTPS / SSL 핸드셰이크** 정리 후 `Network/Day4/` 폴더에 PR | 모임 전날까지 |
| **이슈란 작성** | 전원 | 3회차 질문 답변 채우기. 아래 [이슈란 작성 안내](#-이슈란-작성-안내) 참고 | 4회차 시작 전 |
| **서기** | 미정 | 모임 기록 (전원 발표라서 조정 필요) | 모임 당일 |

> 🗒️ 질문 Issue 템플릿: [Topics/expected-questions-issue-template.md](./Topics/expected-questions-issue-template.md)  
> 🗒️ 전체 스케줄과 역할 상세: [Topics/README.md](./Topics/README.md)

#### 📖 4회차 토픽 미리보기

**DS: Heap & Priority Queue / Hash Table**

- Heap: 부모가 자식보다 항상 크거나(최대 힙) 작은(최소 힙) 완전 이진 트리. 삽입·삭제 O(log N), 최댓값/최솟값 조회 O(1).
- Priority Queue: 우선순위가 높은 것부터 꺼내는 추상 자료형이고, 보통 Heap으로 구현합니다.
- Hash Table: 해시 함수로 키를 인덱스로 바꿔 평균 O(1)에 접근합니다. 충돌 해결은 체이닝과 개방 주소법(선형·제곱 탐사, 이중 해싱).
- 생각해볼 질문: Java HashMap은 왜 충돌이 많아지면 버킷을 Red-Black 트리로 바꿀까? (3회차와 연결)

**NW: HTTP vs HTTPS / SSL 핸드셰이크**

- HTTP는 평문이라 도청·변조에 취약하고, HTTPS는 TLS로 암호화·무결성·인증을 더합니다.
- TLS 핸드셰이크: 인증서로 서버를 확인하고, 비대칭키로 세션키를 안전하게 나눈 뒤 대칭키로 통신합니다.
- 2회차 흐름(DNS → TCP 연결 → TLS → HTTP)에서 3회차가 "TCP 연결"이었다면, 4회차는 그다음 단계인 "TLS"입니다.
- 생각해볼 질문: 왜 처음부터 끝까지 비대칭키로 암호화하지 않을까? 인증서는 누가 어떻게 믿을 수 있게 만들까?

### 📝 이슈란 작성 안내

지금 이슈에는 질문만 있고 **답변이 비어 있습니다.** 아래 순서로 각자 채워 주세요.

1. **내가 올린 질문의 답변 채우기**
2. **함께 보면 좋을 것들**: 도움이 된 블로그, 영상, 문서 링크 등
3. **질문에 대해 내가 생각하고 답해본 것들**: 모범 답안이 아니어도 괜찮고, 틀린 부분은 같이 고치면 공부가 됩니다.
4. 다른 사람의 질문에 의견을 남겨도 좋습니다.

> 길이나 형식은 자유롭게 적어 주세요.

---

## 🎯 스터디 운영 방식

### 1. 모임 일정 및 장소
- **주기**: 주 2회 
- **시간**: 일과 종료 후 (18:30 \~ 19:30 투표로 세부 조정 가능)
- **장소**: 근처 카페 (오프라인 모임) / 점심 시간 이용해 회의실 이용
- **진행 방식**:
  1. **사전 준비**: 모임 전날까지 본인 담당 주제 정리 마크다운 작성 후 PR 제출
     - 회차별 마감이 따로 공지되면 공지된 시간(예: 2회차 11/6 18:00)을 따릅니다.
     - 발표 외 주제는 **Issue**로 예상 질문을 모읍니다 (회차별 공지, 1인 2개).
  2. **오프라인 발표 (약 50\~60분)**:
     - 1인당 약 5\~10분 발표 + 5분 질의응답 (회당 3\~4명씩 순환 발표)
     - 다른 스터디원은 적극적으로 꼬리 질문 및 피드백 제시
  3. **회고 및 피드백 (약 10분)**:
     - 다음 회차 주제 확인 및 발표자 선정
     - PR 상호 코드 리뷰 및 승인(Approve) 후 Merge
  4. **역할**: 발표자 / 청중(질문·보충) / **서기**(모임 기록, 회차별 공지에 따라 조정)

### 2. 학습 로드맵
- **1단계**: [자료구조 (Data Structure)](./DataStructure/) & [네트워크 (Network)](./Network/) 병행 학습
- **참고 자료**:
  - [gyoogle 기술 면접 인터뷰 가이드](https://github.com/gyoogle/tech-interview-for-developer)
  - [Topics/ 주제 가이드 및 커리큘럼](./Topics/)

---

## 📂 저장소 디렉토리 구조

```plaintext
CS-Study/
├── .github/
│   ├── workflows/
│   │   └── auto-merge.yml            # 🤖 PR 자동 머지 GitHub Actions 봇
│   ├── ISSUE_TEMPLATE/
│   │   └── expected-questions.md     # 회차별 DS 예상 질문 Issue 템플릿
│   └── pull_request_template.md      # PR 생성 템플릿
├── DataStructure/                    # 자료구조 발표 아카이빙
│   ├── README.md                     # 자료구조 커리큘럼 및 체크리스트
│   └── Day[N](MMDD)/                 # 회차별 폴더 (예: Day1(1104))
│       └── [주제명]_[이름].md          # 개인별 정리 문서
├── Network/                          # 네트워킹 발표 아카이빙
│   ├── README.md                     # 네트워크 커리큘럼 및 체크리스트
│   └── Day[N](MMDD)/                 # 회차별 폴더 (예: Day2(1106))
│       └── [주제명]_[이름].md          # 개인별 정리 문서
├── Topics/                           # 전체 학습 주제 요약 및 발표 템플릿
│   ├── README.md                     # 토픽 한눈에 보기
│   ├── DataStructure-Curriculum.md   # 자료구조 핵심 키워드/질문 리스트
│   ├── Network-Curriculum.md         # 네트워크 핵심 키워드/질문 리스트
│   └── template.md                   # 스터디 발표 정리 마크다운 템플릿
└── README.md                         # 스터디 소개 및 룰북
```

---

## 🚀 Git & GitHub 협업 규칙 (Fork & PR 방식)

### 1. 작업 및 브랜치 흐름 (Fork Workflow)
1. 본 메인 저장소(`upstream`)를 각자의 GitHub 계정으로 **Fork**합니다.
2. Fork한 저장소를 로컬 PC로 `git clone` 합니다.
3. 새로운 브랜치를 생성하여 작업합니다.
   - 브랜치 네이밍: `[카테고리]/[주제명]-[이름]`
   - 예시: `network/tcp-udp-hong`, `datastructure/hash-table-kim`
4. 발표 자료 작성 후 Fork 저장소의 해당 브랜치로 `push` 합니다.
5. 원본 저장소(`upstream`)의 `main` 브랜치로 **Pull Request(PR)**를 생성합니다.

### 2. 파일 명명 규칙
- 각 카테고리 폴더 하위의 **회차 폴더(`Day[N](MMDD)`)** 안에 아래 형식으로 `.md` 파일을 생성합니다.
- `[주제영문or한글]_[이름].md`
  - 예: `Network/Day2(1106)/네트워크_전체_흐름_홍길동.md`
  - 예: `DataStructure/Day1(1104)/Array_LinkedList_이순신.md`

### 3. Commit Message 규칙
Angular / Gitmoji 컨벤션을 따릅니다.

| 태그 | 설명 | 예시 |
| :---: | :--- | :--- |
| `docs` | 문서 작성 및 수정 | `docs: Network TCP/UDP 핸드셰이크 정리 - 홍길동` |
| `feat` | 새로운 기능/구조 추가 | `feat: PR 템플릿 추가` |
| `refactor` | 기존 정리 내용 보완/수정 | `refactor: B-Tree 설명 보완 - 김철수` |
| `fix` | 오탈자 또는 잘못된 지식 수정 | `fix: OSI 7계층 오탈자 수정` |

### 4. Pull Request & 자동 머지 봇 (Auto-Merge Bot 🤖)
1. **PR 제목**: `[카테고리] 주제명 - 발표자 이름`
   - 예: `[Network] TCP 3-way & 4-way Handshake - 홍길동`
2. **PR 내용**: [PR 템플릿](./.github/pull_request_template.md) 양식을 준수하여 작성
3. **자동 머지(Auto-Merge)**:
   - PR이 열리면 GitHub Actions **Auto Merge Bot**이 안내 댓글을 남기고 충돌이 없을 시 `main` 브랜치로 **자동 머지**를 수행합니다.
   - 발표 후 오프라인 카페 모임에서 나눈 질문/답변이나 피드백은 머지된 후에도 자유롭게 추가 커밋 및 코멘트로 남길 수 있습니다.

---

## ⚖️ 스터디 페널티 (벌금 / 리워드)

스터디의 지속성과 책임감을 위해 가벼운 패널티 제도를 권장합니다 (투표로 금액 확정 가능).

| 구분 | 조건 | 패널티 |
| :---: | :--- | :---: |
| **지각** | 모임 시작 시간 기준 10분 이상 지각 시 | 1,000원 |
| **당일 노쇼** | 사전 연락 없이 불참 시 | 3,000원 |
| **PR 미제출** | 모임 당일 시작 전까지 PR 미작성 시 | 2,000원 |

> 💡 모인 벌금은 스터디 종료 후 회식비로 활용합니다!