# git config

★ 윈도우 기준으로 설명합니다. Git 명령어들은 맥, 윈도우 전부 똑같지만 맥은 세팅할 때 살짝 다를 수도 있습니다.



처음 준비할 것에 나와있는 대로 깃허브 계정 회원가입과 git을 설치했다면 이제 계정을 연결하면 됩니다.

윈도우는 빈 공간에 마우스 오른쪽을 클릭한 후 Git Bash Here를 클릭하면 됩니다.

### 1. 캐싱 데이터 삭제

먼저 이미 장비에 등록된 GitHub 계정을 삭제하는 것입니다.

그래서 아마 처음 Git을 사용하는 분들은 넘어가셔도 문제 없을 것 같습니다.

하지만 만약 아래 내용을 진행하다가 문제가 생긴 분들은 아래 명령어를 입력해주고, 다시 처음부터 시도해보세요.

```bash
git config --global --unset credential.helper
git config --system --unset credential.helper
```

### 2. Git 연결하기

이제 터미널에서 <mark style="color:red;">`git config --list`</mark>를 확인해봅시다.

<figure><img src="https://user-images.githubusercontent.com/79046106/208380255-7e851005-1b4a-475b-b851-eaf7f00bc69e.png" alt=""><figcaption></figcaption></figure>

그러면 위 사진과 같은 내용이 나오는데, 다른 내용은 다 필요 없고 아래 빨간 네모 박스만 수정할 것입니다.

```bash
git config --global user.name "자신 이름"
git config --global user.email 이메일
git config --global core.editor nano
```

첫 번째는 자신이 깃허브에 등록한 이름을 작성하면 됩니다.

```bash
ex. git config --global user.name "Dabeen Jeong"
```

두 번째는 자신의 깃허브 이메일을 작성하면 됩니다.

```bash
ex. git config --global hello70825@gmail.com
```

세 번째는 이번 스터디에서는 nano 에디터를 사용할 예정이라 nano로 설정해주면 됩니다. 그리고 네번째는 nano를 사용하기 위해 설치하는 것입니다.

```bash
ex. git config --global core.editor nano
```

에디터는 기본 설정인 vim으로 해도 상관 없지만, 단축키가 다르기 때문에 여기서는 nano로 진행하겠습니다.



이제 계정 연결 설정이 끝났으니 이제 실습을 진행하면서 병행하겠습니다.



