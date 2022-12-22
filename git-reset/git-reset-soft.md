# git reset --soft

<mark style="color:red;">`git reset`</mark> 의 경우 add한 폴더/파일을 취소하는 방법도 있지만, 특정 커밋 ID를 입력하면 해당 커밋 이후에 쌓은 코드를 모두 삭제하거나, 커밋 메시지만 삭제하는 방법이 존재합니다.

이번 장에서는 코드는 그대로 남기고 커밋 메시지만 삭제하는 방법을 알아봅시다.

이번에는 우리가 그동안 쌓아둔 커밋을 날려버리고, 그때 당시 가장 최근의 커밋만 존재하게 해봅시다.

<figure><img src="../.gitbook/assets/image (10) (2).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">`git log --oneline`</mark> 을 통해 확인해보면 제 커밋은 빨간 박스 안에 있는 fix: 코드 복구부터 새로운 커밋이 쌓였습니다.

그래서 빨간 박스에 있는 커밋 메시지를 모두 날려버리고, 새로운 커밋 메시지인 <mark style="color:red;">`feat: git reset --soft 실습`</mark> 으로 남기려고 합니다.

먼저 빨간 박스 밖에 있는 커밋 메시지를 전부 날려야하므로 마지막에 있을 커밋 메시지 ID인 8fb1656을 사용합니다. <mark style="color:red;">`git reset --soft 8fb1656`</mark> 을 입력합니다.

<figure><img src="../.gitbook/assets/image (7) (4).png" alt=""><figcaption></figcaption></figure>

터미널에 아무런 내용이 나타나지 않지만 <mark style="color:red;">`git log --oneline -3`</mark> 을 적용해보면 문제 없음을 알 수 있습니다.

<figure><img src="../.gitbook/assets/image (3) (4).png" alt=""><figcaption></figcaption></figure>

이후 <mark style="color:red;">`git status`</mark> 를 입력하면 위와 깉이 모두 Staging Area에 있는 것을 확인할 수 있습니다.

이제 모든 Staging Area에 있는 내용을 <mark style="color:red;">`feat: git reset --soft 실습`</mark> 이라는 커밋 메시지에 저장하게 만듭니다. (<mark style="color:red;">`git commit -m “feat: git reset —soft 실습`</mark>)

<figure><img src="../.gitbook/assets/image (1) (6).png" alt=""><figcaption></figcaption></figure>

빨간 박스처럼 forced update가 되었다는 것을 확인할 수 있습니다.

이제 커밋 메시지 목록을 확인해봅시다.

<figure><img src="../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>

제대로 된 것을 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (2) (1) (4).png" alt=""><figcaption></figcaption></figure>

각자 fork한 리포지토리를 확인해보면 저처럼 잘 덮어쓰기가 된 것을 확인할 수 있습니다.
