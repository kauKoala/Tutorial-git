# git remote

{% hint style="info" %}
이 글을 읽기 전에 Pull Request에 대해 기억이 나지 않는 분들은 그 부분만 다시 읽고 오시길 바랍니다.
{% endhint %}



한 프로젝트를 여러 명에서 협업을 한다고 하면 팀원들은 원본 리포지토리를 fork하여 기능을 제작한 뒤에 pull request를 보낼 것입니다.

이 과정에서 원본 리포지토리에 반영이 되어 코드가 바뀌는 경우가 존재하는데요. 이때 다른 팀원들은 자신도 pull request를 보낼 때, 충돌을 회피하기 위해 원본 리포지토리의 변경 사항에 맞게 업데이트를 하는 경우가 존재합니다.

참고로원본 리포지토리와 우리가 fork한 리포지토리는 원격 저장소(Remote Repostory)라고 부릅니다.



fork만 한 상태에서는 fork한 리포지토리를 원본 리포지토리에 맞게 업데이트를 할 수가 없습니다.

일단 현재 git에 저장된 원격 저장소의 목록을 확인하기 위해 `git remote -v` 를 입력해봅시다.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

origin은 현재 우리가 fork한 리포지토리를 뜻합니다.

URL 주소만 보아도 원본 리포지토리는 없다는 것을 알 수 있습니다.

그래서 원본 리포지토리가 있는 원격 저장소를 git에 등록해야 합니다.



보통 원본 리포지토리의 이름으로는 upstream을 사용합니다.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

원본 리포지토리의 git 주소는 우리가 처음에 clone을 했던 것처럼 koala-eat-eucalyptus의 chrome-extensions-samples에 들어가서 다시 주소를 복사하면 됩니다.

이후 <mark style="color:red;">`git add upstream <git주소>`</mark> 를 프로젝트에서 작성을 하면 됩니다.

<figure><img src="../.gitbook/assets/image (1) (7).png" alt=""><figcaption></figcaption></figure>

그리고 다시 <mark style="color:red;">`git remote -v`</mark>로 확인해보면 위처럼 upstream이라는 이름으로 두 개가 만들어질 겁니다.



이제 여기서 다음 장에 배울 fetch and merge를 하여 현재 프로젝트를 원본 리포지토리에 맞게 반영할 수 있습니다.

{% hint style="warning" %}
주의할 점은 원본 리포지토리에 맞게 업데이트를 진행할 때, 원본 리포지토리에서 변경된 파일에서는 수정한 코드가 없어야 합니다.

만약 수정이 되어 있으면 충돌이 일어나 업데이트를 하지 못하게 됩니다.
{% endhint %}

물론 원격 저장소를 삭제하는 기능도 존재합니다.

<mark style="color:red;">`git remote remove upstream`</mark> 을 입력하고 <mark style="color:red;">`git remote -v`</mark> 를 통해 upstream이 사라졌는지 확인해봅시다.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

정상적으로 삭제된 것을 확인할 수 있습니다.

다음 장으로 넘어가기 전에 다시 한 번 <mark style="color:red;">`git remote add upstream https://github.com/koala-eat-eucalyptus/chrome-extensions-samples.git`</mark> 를 입력합시다.
