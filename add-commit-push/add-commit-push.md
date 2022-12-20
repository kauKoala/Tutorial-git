# add, commit, push

### 1. add - commit - push

GitHub에 기록을 남기는 방법은 add - commit - push입니다.

* add : 기록할 파일을 추가하다.
* commit : 추가한 파일에 저장할 메시지를 작성하다.
* push : GitHub에 기록을 하다.

엄밀히 말하면 add - commit - push의 의미는 위와 살짝 다르지만, 처음부터 제대로 된 역할을 설명하면 어렵기 때문에 일단은 이렇게 생각하면 됩니다.

이제 직접 코드를 수정을 해보겠습니다.

IDE를 통해 이전에 Fork - Clone한 리포지토리인 chrome-extensions-samples 폴더에서 `tutorials > focus-mode > background.js` 로 들어가면 됩니다.

<figure><img src="../.gitbook/assets/image (5) (2).png" alt=""><figcaption></figcaption></figure>

저는 Javascript를 사용 안해서 Java IDE인 IntelliJ를 사용하여 실행을 했는데, 해당 경로에 들어가면 이런 파일이 나오게 됩니다. 일단은 한 줄만 수정하면 됩니다.

* line 17 : ON → OFF

이후 수정한 내용을 깃허브에 기록을 해두고 싶습니다.

터미널을 사용하는 방법은 여러가지가 있습니다.

* \[윈도우] chrome-extensions-samples 폴더 안에 들어가 빈 공간에 오른쪽 마우스 클릭 후 Git Bash Here를 클릭하여 Git Command 창을 실행
* \[맥] 터미널을 chrome-extensions-samples 폴더 안까지 이동
* \[IDE] Terminal을 실행

이후 아래 코드를 작성하면 됩니다.

```bash
git add .
git commit -m "fix: 코드 복구"
git push
```

* `git add .` : 온점(.)은 수정/생성/삭제된 모든 파일을 추가
* `git commit -m "fix: 코드 복구"` : add한 파일들은 fix: 코드 복구라는 내용으로 기록
* `git push` : 내가 기록한 내용을 GitHub에 저장

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

이제 아래에 메시지가 추가된 것을 확인할 수 있습니다.

해당 메시지를 클릭해서 들어가 봅시다.

<figure><img src="../.gitbook/assets/image (2) (3).png" alt=""><figcaption></figcaption></figure>

저는 분명 파일을 하나만 수정했는데, 여러가지 파일이 추가되었다고 나옵니다.

수정된 내용만 나오는 분들도 있겠지만, 여러 개의 파일이 등록되어도 문제가 없습니다.

일단 중요한 점은 add - commit - push 방식으로 GitHub에 기록한다고 생각하면 됩니다.



### 2. 연습

나머지 아래 내용도 수정해서 add - commit - push를 해봅시다.

커밋 메시지는 아무 내용이나 적어도 상관 없습니다.

* line 38 : OFF → ON
* line 44 : ON → OFF
