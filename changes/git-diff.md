# git diff

이제 파일의 수정/생성/삭제를 알았으니, 세부적으로 어떤 코드가 바뀌었는지 확인하는 방법을 알아봅시다.

이번에는 background.js에 있는 모든 ON 표시를 전부 OFF로 바꾸어 보겠습니다.

* Line 17 : ON → OFF
* Line 30 : ON → OFF
* Line 38 : ON → OFF
* Line 44 : ON → OFF

`git diff` 는 간단하게 설명하면 아직 add를 사용하지 않은 수정된 코드 중에 어떤 내용이 바뀌었는지 확인하는 기능입니다.

`git diff`를 사용해봅시다.

<figure><img src="../.gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>

이렇게 빨간색은 수정 이전의 내용, 초록색은 수정된 내용으로 확인할 수 있습니다.

참고로 git diff를 사용해 다양한 차이점을 확인할 수 있습니다.

* `git diff --cached` : add가 된 상태와 코드 수정 이전의 상태를 비교합니다.
* `git diff branch1 branch2` : 두 개의 브랜치가 서로 어떻게 다른지 비교합니다.
* `git diff commit1 commit2` : 두 개의 커밋이 서로 어떻게 다른지 비교합니다.



{% hint style="info" %}
해당 내용도 다음 실습을 위해 add - commit - push를 사용합시다.
{% endhint %}
