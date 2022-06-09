# **Mighter Fighters Blog**
1788005 게임공학과 김민창
## 목차 <a name='0'></a>
- 클릭하면 이동합니다.<br>
**1. [게임 소개](#1)**<br>
**2. [컨셉](#2)**<br>
**3. [모티브](#3)**<br>
**4. [컨셉 설명 이미지](#4)**<br>
**5. [구성 요소](#5)**<br>
**6. [개발 요구사항](#6)**<br>
**7. [개발 작업](#7)**<br>
**8. [참고](#8)**<br>
**9. [리소스 출처](#9)**<br>
<br>

# [게임 소개](#0) <a name='1'></a>

![1](https://user-images.githubusercontent.com/49381621/172955197-ab901f34-02f6-4429-b16b-4bc48b522a40.PNG)
<br>
- 작품명: **Mighter Fighters** (누가 더 강한(Mightier) 파이터(Fighter)인지 겨룬다는 의미.) 
- 제작 동기: 평소 격투 게임을 좋아해서 주변 사람들에게도 권했는데, 대부분 게임을 어려워했다. 격투 게임 속 심리전의 재미를 느끼기 전에 그만두는 경우가 많았다.
  그래서 이를 보고 격투 게임을 조작과 룰을 단순화해서 만들면 초보자도 어려워 하지 않고 즐길 수 있지 않을까 생각해서 이 작품을 만들게 되었다.
- 특징 : 단순한 조작, 자동 가드 (행동을 하면 가드가 불가능), 점프 없음, 한 매치에서 단 3번만 필살기 사용 가능, 고전 게임 스타일의 디자인, 어두운 배경 설정
- 장르: 단순한 조작의 2d 격투 게임
- 플랫폼: PC
- 개발: Unity 3D

<br>

# [컨셉](#0) <a name='2'></a>

### 메인 컨셉 : 심리전(Mind Games)

- 마치 가위바위보와 같이 서로 어떤 행동을 할지 예측하여 플레이하고, 상대의 행동을 잘 캐치한 유저가 유리해진다.
- 일부러 기술을 헛쳐 상대의 실수를 유도하거나 상대의 공격을 피하는 기술을 이용해 반격하는 등 타이밍적 감각도 중요하다.
- Footsies(풋시즈): 격투 게임 유저들의 은어로 공격하기 유리한 위치를 잡거나 상대의 기술을 읽기 위해 긴장감있는 거리 재기 싸움을 유도하는 행동이다.
- Whiff Punish(윕 퍼니시): 상대가 헛휘두른 공격(whiff)을 보고 반응하여 그 빈틈을 공격(punish)하는 것
- Zoning(조닝): 자신의 리치가 긴 기술을 깔아두어 상대를 압박하는 행동이다. 이런 기술은 상대를 압박하고 견제하는데 효과적이지만 그만큼 리스크도 크다.

### 서브 컨셉 : Easy to learn

- 메인 컨셉인 "심리전"을 초보자들도 쉽게 익히려면 게임의 룰과 조작이 단순해야 한다고 생각했다.
- 플레이에 금방 적응할 수 있도록 조작법을 단순화
- 체력바, 필살기 게이지등의 표시를 직관적이게 했다.(칸의 갯수로 표시)

<br>

# [모티브](#0) <a name='3'></a>

- 단순하면서도 격투 게임 특유의 심리전 싸움의 재미가 있는 작품이라는 같은 목적의 다른 격투 게임들을 참고했다. 

### Fantasy Strike 

[![](https://user-images.githubusercontent.com/49381621/135260825-3d24b0db-fcc6-44e3-b570-e30bfa5c4b8f.png)](https://www.youtube.com/watch?v=vBT7ZyJOU4A&t=1713s)

- 위 이미지를 클릭하면 해당 게임의 플레이 영상 링크(유튜브)로 이동합니다.
(11분 부터 경기 시작)

[판타지 스트라이크 공식 홈페이지](https://www.fantasystrike.com/)

단순한 체력바와 게이지 시스템을 갖고 있다. 체력이 칸으로 되어 있는게 특징. 앉기가 없으며 공격 버튼도 3개 뿐이다.

특이한 점은 잡기 기술에 상대가 아무 행동도 하지 않는다면, 잡히지 않으며 오히려 자동으로 카운터 당하게 된다.

따라서 항상 가위바위보를 하는 느낌으로 심리전을 펼침과 동시에 상대 공격 타이밍을 읽는 피지컬적 플레이도 매력인 게임이다.

### Divekick

[![](https://user-images.githubusercontent.com/49381621/135261167-7ecabfd1-dd6c-49d6-b60d-5efd48f2a6ac.jpg)](https://www.youtube.com/watch?v=S5UV17aotac)

- 위 이미지를 클릭하면 해당 게임의 플레이 영상 링크(유튜브)로 이동합니다.
(1분 10초 부터 경기 시작)

[다이브킥 스팀 페이지](https://store.steampowered.com/app/244730/Divekick/?l=koreana)
 
점프 버튼, 다이브킥 버튼만 존재하는 극단적으로 단순한 조작이 특징. 체력 게이지가 의미 없어서 다이브킥에 맞으면 반드시 한방에 패배한다.

가드를 할 수 없고 관련 시스템도 없기 때문에 오로지 거리 조절과 타이밍 싸움으로 승부한다.

이처럼 매우 단순한 룰의 게임이지만 캐릭터가 다양하다. 각 캐릭터 마다 점프와 다이브킥의 성능이 달라서 각자의 개성이 있다.

### Footsies

[![](https://user-images.githubusercontent.com/49381621/135261210-86fc9b96-59b5-4b78-838f-737dc0cdda70.PNG)](https://www.youtube.com/watch?v=dcMrn71t8Rs)

- 위 이미지를 클릭하면 해당 게임의 플레이 영상 링크(유튜브)로 이동합니다.
(40초 부터 경기 시작)

[개발자 트위터](https://twitter.com/hifightth)

이 게임은 스트리트 파이터의 패러디 작품으로, 현대 2D 격투게임들이 갖고 있는 여러가지 문제점을 해소해 보자는 아이디어로 만들어 졌다.

초보자를 위한 튜토리얼 부재, 어려운 격투 게임 용어 사용, 온라인 환경, 밸런스 문제 등을 극복하고자

극히 단순한 조작법과 룰을 적용하여 개발 리소스를 최소화 시켰다.

일정 횟수 이상 가드를 할 수 없어서 상대의 공격을 피하거나 상대 움직임의 빈틈을 이용하는 플레이가 주가 된다.

<br>

# [컨셉 설명 이미지](#0) <a name='4'></a>

![메인1](https://user-images.githubusercontent.com/49381621/135263482-d1e514eb-ebb3-4958-82b8-2a79775796c8.jpg)

![메인2](https://user-images.githubusercontent.com/49381621/135262981-e5d08e15-72e4-4034-b531-e5b3efe88813.jpg)

![메인3](https://user-images.githubusercontent.com/49381621/135262984-244d549d-f183-4f0d-8d42-627b86bf3897.jpg)

![메인4](https://user-images.githubusercontent.com/49381621/135262985-f15bfbb7-b0d8-4de5-88c2-aa5fd1bab808.jpg)

![메인5](https://user-images.githubusercontent.com/49381621/135262987-6b2b44ad-5417-41ee-b669-f4d07138d6f3.jpg)

![메인6](https://user-images.githubusercontent.com/49381621/135262988-43e1e3d6-bed4-4e15-a4f1-eed3ab6b45e4.jpg)

![메인7](https://user-images.githubusercontent.com/49381621/135262989-120bc4eb-233b-4abe-94be-69c6e995d0cf.jpg)

![메인8](https://user-images.githubusercontent.com/49381621/135262991-958f4a6f-c2f3-4450-bd91-e7d7a66a2733.jpg)

![메인9](https://user-images.githubusercontent.com/49381621/135262992-d5bd1526-18a5-4ead-8f28-cc90c32ca446.jpg)

![메인10](https://user-images.githubusercontent.com/49381621/135262994-b1b786e8-fee6-4bbb-95bb-ef713cc47fa8.jpg)

![메인11](https://user-images.githubusercontent.com/49381621/135262996-d5932b57-aa0f-471e-a24b-46247f30f588.jpg)

<br>
# [구성 요소](#0) <a name='5'></a>

- Mighter Fighters의 구성 요소로 게임 메커니즘, 시나리오, 외적 디자인에 대해서 설명한다.

<br>

## 1. 게임 메커니즘

### 조작법

![키보드](https://user-images.githubusercontent.com/49381621/172907087-6e949974-8297-49c7-9af9-93ad71dc7fb8.jpg)

```
1p (좌)
←, ↓, → 방향 입력 (a, s, d)
P(unch) = j
K(ick) = k
S(pecial) = l

2p (우)
←, ↓, → 방향입력 (방향키 ←, ↓, →)
P(unch) = numpad4
K(ick) = numpad5
S(pecial) = numpad6
```
### 게임 룰

유저는 좌측 플레이어 (1P), 우측 플레이어 (2P)로 구성된다.
한 쪽 플레이어의 체력이 0이 되거나 타이머가 0이 되면 라운드가 종료되고, 승리 판정을 실시한다.
타임 아웃 시에 서로 체력이 같으면 마지막에 공격을 상대에게 적중(가드시키거나 타격)한 플레이어가 승리한다.

자동 가드 시스템이 있다. 이는 특정 버튼 입력이 없이 상대의 공격 가드를 자동으로 하는 것으로 이 게임의 진입 장벽을 낮추는 요소이다.
아무 행동도 하지 않아야만 가드가 된다.
시간 종료시 마지막에 공격한 플레이어가 이긴다.
10초간 조작을 하지 않은 플레이어의 체력을 1칸씩 감소 시킨다. "아무 행동도 하지 않고 자동 가드만 하는 플레이"를 한다면 이 페널티에 의해 손해를 본다.

S키에 대응하는 버튼으로 기술 사용 가능. (캐릭터마다 성능이 다르고 게이지의 디자인도 다르다)
한 라운드가 아닌 한 매치(전체 경기) 동안 단 3개가 유지되므로 상당히 신중해서 S 기술을 사용해야 한다. S 기술의 성능은 게임의 역전을 이뤄낼 수도 있을 정도의 강력한 판정을 가졌다.

실제 게임시에 육안으로 보이지 않는 '피격 판정'박스와 '공격 판정'박스가 있다. 피격 판정 박스에 공격 판정 박스가 닿으면, 피격 판정 박스의 플레이어가 피해를 받는다.
(캐릭터가 공격 모션을 취할 시 기술마다 공격 범위나 맞는 몸의 판정이 다르므로 양 플레이어 기술 간에 상성관계가 성립될 수 있다.)

### 재미 요소

캐릭터들의 기술을 익혀 어떤 기술을 어떤 상황에 사용하는지 배워가며 실력을 올리는 재미
긴장감 있는 심리전, 반응 속도 싸움이 재미 요소이다. 때로는 리스크가 큰 기술을 질러서 이기거나 매우 불리한 상황에서 기술 하나 차이로 역전하는 등 다양하고 흥미진진한 전투가 연출된다.
또한 캐릭터 마다 고유한 스타일의 기술이 있으므로 다양한 전략으로 여러 캐릭터를 즐겨볼 수 있다.

### 참신한 요소

이 게임의 참신함은 다른 격투게임에서 찾아보기 힘든 가드 방식이다. "아무 행동도 하지 않으면 가드"라는 점은 가드가 쉽다는 이점이 있어서 진입장벽을 낮춰준다.
하지만 위에서 설명 했듯이 자동 가드에 너무 의존하면 타임 아웃과 페널티 룰로 인해 게임을 이기기 어려워 질 수 있다.
공격과 방어를 동시에 할 수 없는 게임이기에 상대의 기술을 예측하고 이기는 기술을 사용해 보거나 침착하게 기다리는 플레이가 도움이 될 것이다.

## 2. 시나리오 
- 배경 설정<br>
어느날 이계에서 강력한 흑마법사 **섕 쑹**이 지구에 방문했다.<br>
그는 자신의 주인이 벌이는 이계에서의 정복 전쟁을 돕기 위해, 그 힘에 필적할 만한 파이터를 찾아온 것이다.<br>
이를 위해 격투 대회를 연 섕 쑹은 **우승자에게 자신과 주인의 마법을 이용해 원하는 소원**을 들어주겠다고 한다.<br>
어쩌면 지구의 운명을 뒤흔들지도 모를 거대한 이벤트가 열린 것이다.<br>
이에, 각자의 사연을 가진 파이터들이 각각의 목적을 갖고 대회에 참여했다.<br>
**지금 전 세계의 파이터들이 모였다. 최고를 겨루는 싸움이 지금 시작된다!**
<br><br>
- 캐릭터 설정 <br>
**스콜피온(노란 닌자)**: 본명은 하사시 한조. 시라이류 닌자 가문의 수장. 과격파 린 쿠에이 리더인 비 한에 의해 가족과 조직을 잃었다. 복수로 서브-제로를 처단하고자 대회에 참여했다.<br>
**서브-제로(푸른 닌자)**: 본명은 콰이 량. 중국 자객 집단인 린 쿠에이의 리더이다. 형의 잘못으로 스콜피온의 오해를 사버린 그는, 잘못되어 버린 과거를 고치고자 대회에 참여했다.<br> 
**케이노(애꾸눈)**: 형의권과 합기도의 대가인 그는 범죄 조직 흑룡회의 수장이다. 그의 대회 참여 목적은 불분명하나 탐욕에 가득찬 그의 성격을 보아 부와 권력이 목적인 것 같다.<br>
**소냐 블레이드(여성 격투가)**: 미국 특수부대원. 흑룡회가 과거 소냐의 부대원들을 전멸시키는 사건으로 케이노가 동료들의 원수이자 주 타겟이 되었다. 케이노의 우승을 막으려 한다.<br>
<br>

## 3. 디자인
- 4가지 캐릭터가 있다. 각자 고유의 스프라이트와 모션을 애니메이션으로 제작하여 개성이 넘친다.<br>
- 4가지 맵(배경)을 선택할 수 있으며 각자 어울리는 테마가 전투중에 재생된다.<br>
- 양 플레이어 화면 하단부에 스페셜 게이지가 있다. 스페셜 게이지는 아이콘으로 표시되며 사용 시마다 하나씩 줄어든다. 캐릭터마다 기술과 본인의 테마를 상징하는 아이콘이 표현된다.
<br>

# [개발 요구사항](#0) <a name='6'></a>
1. 캐릭터 조작 : 1P기준 a, s, d(←,↓,→), j, k, l(P, K, S) 2p기준 ←, ↓, →, numpad4, numpad5, numpad6(P, K, S) 
2. 화면: 메뉴, 캐릭터 선택, 맵 선택, 전투 화면 화면 총 4개의 화면
3. 메뉴(시작) 화면: Multiplayer(로컬 매치), Exit(종료) 총 3개의 버튼
4. 캐릭터 선택 화면: 화면 중앙에 선택할 캐릭터들의 얼굴 아이콘(클릭시 선택되어 각 좌우 1p 2p자리의 공간에 캐릭터 보이기), 마우스 커서를 움직여 캐릭터 아이콘 클릭
6. 맵 선택 화면: 화면 중앙 하단부에 선택할 맵들의 아이콘, 마우스 커서를 움직여 맵 아이콘 클릭하게 하기
7. 전투 화면: 화면 상단부 좌우에 각 캐릭터들의 체력바 (10칸), 체력바 사이에는 타이머가 있음. 화면 하단부 양 옆에 캐릭터별 고유 디자인의 스페셜 게이지.
8. 전투: 아무런 행동을 하지 않을 시 자동 가드(피격 박스 대신 가드 판정의 박스가 캐릭터를 덮음), 행동 시(이동, 앉기, 공격, 스페셜) 피격 가능. 상대의 공격에 피격 시 정해져 있는 데미지 만큼 체력 게이지 감소. 스페셜 기술 사용 시 스페셜 게이지 소모. 한쪽의 체력이 0이 되거나 타이머가 0이 되면 승부 판정을 내리고 서로 체력만 Full이 된 채로 다음 라운드 개시. 라운드가 반복되어 최종 승리 조건 승수를 한쪽이 달성 하면 전투가 완전히 종료.
9. 승부 판정: 한쪽의 체력이 0이 되면 체력이 남아있는 플레이어 승리. 만약 타이머가 0이 될때 까지 결판이 나지 않았다면 타임아웃. 이때 체력이 더 많은 쪽이 승리. 만약 타임아웃 시에 서로 체력이 같으면 마지막에 공격을 적중(피격, 가드) 시킨 플레이어가 승리하도록 함. 이 점을 계속 체크 하기 위해 1p 혹은 2p가 자신의 공격을 상대에게 피격 or 가드 시킬때 마다 해당 상황을 확인하는 변수에 계속 갱신한다. 
10. 편법 견제 룰: 아무 행동도 하지않고 10초가 지나면 해당 플레이어 페널티로 체력 감소.
<br>

# [개발 작업](#0) <a name='7'></a>
[겜프2 작업 내용(내용보기)](gameprogress.md)
<br>



# [참고](#0) <a name='8'></a>
- 게임 플레이 시나리오 개요 <br>
각 개발자와 유저의 관점으로 게임을 플레이 할때 어떤 모습이 전개되는지 구상한 내용 (초기 기획 단계) <br>
[내용보기(개발자 관점)](gameplayscenario1.md)<br>
[내용보기(유저 관점)](gameplayscenario2.md)
<br>

# [리소스 출처](#0) <a name='9'></a>

- 원작 : Mortal Kombat 1~3 (NetherRealm Studios)

- 스프라이트:
[스콜피온](https://www.mortalkombatwarehouse.com/mk1/scorpion/sprites/), [서브-제로](https://www.mortalkombatwarehouse.com/mk1/subzero/sprites/), 
[케이노](https://www.mortalkombatwarehouse.com/mk1/kano/sprites/), 
[소냐 블레이드](https://www.mortalkombatwarehouse.com/mk1/sonya/)<br>

- 배경 : <br>
[맵1 (동양풍 배경)](https://www.mortalkombatwarehouse.com/mk1/arenas/throneroom/)<br>
[맵2 (아포칼립틱 현대 도시)](https://www.mortalkombatwarehouse.com/mk3/arenas/thebridge/)<br>
[맵3 (어두운 숲 속)](https://www.mortalkombatwarehouse.com/mk2/arenas/livingforest/)<br>
[맵4 (음침한 배경)](https://www.mortalkombatwarehouse.com/mk1/arenas/thepit/)<br>

- 사운드 : <br>
메인 메뉴 음악: [Mortal Kombat 1 Arcade OST Original Music Soundtrack Victory and Ending](https://www.youtube.com/watch?v=RF7DjGziHZg)<br>
캐릭터/맵 선택 음악: [Mortal Kombat 1 Arcade - OST Music Soundtrack - In The Beginning - Character Select](https://www.youtube.com/watch?v=omvdFcr0z08)<br>
맵 1 배경음악: [Mortal Kombat 1 Arcade OST Original Music Soundtrack Throne Room](https://www.youtube.com/watch?v=O-_jZchKYaQ&list=PLNJZ_2XtY314QB9yr7ABNETJn6Bo42f3p&index=7)<br>
맵 2 배경음악: [Mortal Kombat 3 - The Bridge - Remake](https://www.youtube.com/watch?v=lppU2bCl7V8)<br>
맵 3 배경음악: [Mortal Kombat 2 MusicThe Living Forest](https://www.youtube.com/watch?v=jMJJ47lO25M)<br>
맵 4 배경음악: [Mortal Kombat 1 Arcade OST - Original Music Soundtrack - The Bridge (The Pit)](https://www.youtube.com/watch?v=tgWtxnyggOQ&list=PLNJZ_2XtY314QB9yr7ABNETJn6Bo42f3p&index=6)<br>
[UI, 기합 소리 및 기술 사운드](https://www.mortalkombatwarehouse.com/mk1/sounds/)<br>


<br>

<br>

<br>

<br>

<br>


