# git reset --hard

이번에는 특정 커밋 이후에 나온 모든 커밋 메시지와 코드를 삭제하는 방법을 알아봅시다.

이 방법을 사용하면 삭제된 커밋과 코드를 복구하기가 힘드므로 조심히 사용하시길 바랍니다.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

저는 일단 테스트용으로 커밋 메시지를 여러 개 채웠습니다.

우리는 커밋 ID가 8fb1656인 fix: 의도와 다른 코드를 추가의 커밋 다음에 있는 모든 커밋과 코드를 삭제하려고 합니다.

제 커밋 ID는 8fb1656이므로 `git reset --hard 8fb1656` 을 입력합니다.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

이후 `git status`와 `git log --oneline` 을 통해 확인을 해봅시다.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

git status에서는 IDE에서 기본 제공되는 파일을 제외하고는 다 없어진 상태입니다.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

git log —oneline 에서도 커밋 메시지가 삭제된 상태입니다.



여기까지는 git pull을 사용하여 복구를 할 수 있습니다.

하지만 지금은 복구하는 것이 연습이 아니므로 강제 push를 진행합니다.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

이제 GitHub를 확인해봅시다.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

이렇게 처음으로 되돌아간 것을 확인할 수 있습니다.
