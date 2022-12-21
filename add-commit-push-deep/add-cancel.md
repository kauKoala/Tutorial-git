# 특정 파일/폴더만 add 취소하기

이전 장에 있던 상태 그대로 진행합니다.

이제 특정 파일을 add를 하는 방법을 알았으니 반대로 add를 취소하는 방법을 알아보겠습니다.

add를 취소하는 방법은 `git reset 파일/폴더` 입니다.

바로 연습을 해보겠습니다. 이것도 특정 파일과 폴더로 취소를 해보겠습니다.

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

`git reset tutorials/focus-mode/background.js` 와 `git reset tutorials/focus-mode/focus-mode.css` 를 입력합니다. 그리고 `git status` 를 확인해보면 취소가 된 것을 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

이번엔 hello-world 폴더 안에 add가 된 변경된 파일을 전부 취소해보겠습니다.

`git reset tutorials/hello-world` 를 하고 `git status` 를 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

보통 작은 단위로 커밋을 보내기 때문에 add - commit - push를 하기 전에 git status를 실행하여 필요한 파일 경로만 복사하면 편하게 add를 할 수 있게 됩니다.
