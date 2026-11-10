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
| 3회차 | 11/10 (화) 18:30 · 투썸플레이스 | DS: Balanced Tree (AVL, Red-Black)<br>NW: TCP vs UDP / TCP Handshake, TCP 제어 기법 / 포트 포워딩 | 🔜 예정 |
| 4회차 | 11/12 (목) 점심시간 · SSAFY 건물 내 | DS: Heap & Priority Queue / Hash Table<br>NW: HTTP vs HTTPS / SSL 핸드셰이크 | ⬜ |

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

### 🔜 3회차 (11/10) 준비 사항

| 구분 | 대상 | 할 일 | 마감 |
| :---: | :---: | :--- | :---: |
| **DS 발표** | 최묘석, 김영웅 | **Balanced Tree (AVL, Red-Black)** 정리 후 `DataStructure/Day3(1110)/` 폴더에 PR | 모임 전날까지 |
| **NW 발표** | 조수연, 권혜강 | **TCP vs UDP / TCP Handshake / TCP 제어 기법 / 포트 포워딩** 정리 후 `Network/Day3(1110)/` 폴더에 PR | 모임 전날까지 |
| **청중** | 최나현, 최승우, 윤형섭 | 3회차 토픽 키워드 미리 공부, 발표 후 질문 및 보충 | 모임 당일 |
| **이슈란 작성** | 전원 | 아래 [이슈란 작성 안내](#-이슈란-작성-안내) 참고 | 3회차 시작 전 |
| **서기** | 미정 | 모임 기록 (권혜강이 NW 발표자라서 조정 필요) | 모임 당일 |

> 🗒️ 질문 Issue 템플릿: [Topics/expected-questions-issue-template.md](./Topics/expected-questions-issue-template.md)  
> 🗒️ 전체 스케줄과 역할 상세: [Topics/README.md](./Topics/README.md)

#### 📖 3회차 토픽 미리보기

**DS: Balanced Tree (AVL, Red-Black)**

- 왜 필요한가: BST가 편향되면 O(N)이 되므로, 균형을 유지해 높이를 O(log N)으로 지킵니다.
- AVL: 좌우 높이 차를 1 이하로 엄격히 유지하고, 회전 4종(LL, RR, LR, RL)으로 균형을 맞춥니다.
- Red-Black: 색과 5가지 규칙으로 가장 긴 경로가 가장 짧은 경로의 2배 이하가 되게 유지합니다. 삽입과 삭제 때 회전이 적습니다.
- 생각해볼 질문: AVL과 Red-Black은 언제 무엇을 쓰나?

**NW: TCP vs UDP / TCP Handshake / TCP 제어 기법 / 포트 포워딩**

- TCP vs UDP: 연결 지향과 신뢰성 vs 비연결과 속도. UDP가 지금도 많이 쓰이는 이유.
- TCP Handshake: 연결은 3-way(SYN, SYN+ACK, ACK), 종료는 4-way(FIN, ACK, FIN, ACK). 종료가 4-way인 이유와 TIME_WAIT.
- TCP 제어 기법: 흐름 제어(슬라이딩 윈도우), 혼잡 제어(Slow Start, AIMD), 오류 제어(재전송).
- 포트 포워딩: 사설 IP는 외부에서 바로 접속할 수 없고, 공유기에 "공인 IP:포트 → 내부 IP:포트" 규칙을 넣어 연결합니다(DNAT, SNAT). 여러 기기가 공인 IP 하나를 쓸 때는 포트까지 변환하는 NAPT와 변환 테이블이 쓰입니다. 포트는 전송 계층(TCP/UDP)의 주소라서 TCP vs UDP와 함께 보면 자연스럽습니다.
- 생각해볼 질문: ngrok은 공유기 설정 없이 어떻게 로컬 서버를 외부에 공개할까? 포트가 고갈되면 어떻게 될까?

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

> 💡 모인 벌금은 스터디 종료 후 카페 음료/디저트 회식비로 활용합니다!