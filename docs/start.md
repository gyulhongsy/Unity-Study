# 유니티 시작
### 1. 유니티 다운로드
- [다운로드 링크](https://unity.com/kr/download)를 방문하여 다운로드
<br>

### 2. 새 프로젝트 생성
<img width="1000" alt="unityHub" src="../imgs/01/01_unityHub.png">

- 우측 상단의 `New project` 클릭
<img width="1000" alt="makeProject" src="../imgs/01/02_makeProject.png">

- 탬플릿, 버전 선택 후 프로젝트 이름 입력 (협업 시 다른 팀원과 동일하게 맞춰야 합니다!)
- 우측 하단의 `Create project` 클릭
<br>

### 3. 인터페이스 간단히 살펴보기
<img width="1000" alt="unityScene" src="../imgs/01/03_unityScene.png">

- 1: **씬 뷰**
  - 게임의 화면을 만드는 부분
  - 게임 오브젝트를 배치하는 곳
  - 흰색 테두리 안이 화면에 표시되는 부분
    
- 2: **게임 뷰**
  - 게임 플레이 시 확인하는 화면
  - 씬 뷰와 겹쳐있기 때문에 위쪽의 탭을 눌러 전환
    
- 3: **하이어라키 창**
  - 씬에 등장하는 것의 리스트
  - 게임 오브젝트는 겹쳐져서 보이지 않아도 이름으로 찾을 수 있기 때문에 해당 리스트에서 선택 가능
    
- 4: **인스펙터 창**
  - 선택한 것에 대한 자세한 정보
  - 선택한 것에 따라 표시가 바뀜
    
- 5: **프로젝트 창**
  - 게임에 필요한 것을 넣어두는 창고
  - 이미지, 스크립트, 애니메이션, 씬 등
<br>

### 4. 비주얼 스튜디오에 유니티 개발 환경 추가하기
<img width="500" alt="vsSetting" src="../imgs/01/04_VSSetting_1.png">

- 비주얼 스튜디오에서 `도구 > 도구 및 기능 가져오기` 클릭
<img width="1000" alt="vsSetting" src="../imgs/01/04_VSSetting_2.png">

- `Unity를 사용한 게임 개발` 체크박스 선택 후 오른쪽의 선택 사항도 모두 체크
  - (`C++를 사용한 게임 개발`은 선택하지 않으셔도 됩니다!)
- 우측 하단의 `수정` 클릭 &rarr; 설치 진행
<br>

### 5. 유니티 프로젝트에서 비주얼 스튜디오 연동하기
<img width="500" alt="addVS" src="../imgs/01/05_addVS_1.png">

- 생성된 프로젝트에서 `Edit > Preferences` 선택
<img width="800" alt="addVS" src="../imgs/01/05_addVS_2.png">

- External Tools의 `External Script Editor`를 비주얼 스튜디오로 선택
  - 설치된 버전에 맞게 선택하시면 됩니다!
  - 이후 유니티에서 스크립트 파일 작성 시 비주얼 스튜디오로 연결됩니다.
