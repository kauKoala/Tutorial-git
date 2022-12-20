# git fork, git clone

&#x20;실습은 아래 리포지토리를 토대로 연습하겠습니다.

{% embed url="https://github.com/koala-eat-eucalyptus/chrome-extensions-samples" %}



### 1. Fork

Fork는 다른 사람의 리포지토리를 그대로 복제해서 가져오는 기능입니다.

복제한 리포지토리는 이제 원본 리포지토리랑 분리가 됐기 때문에 Fork한 리포지토리에 코드 수정을 해도 원본 리포지토리에 영향을 주지 않습니다.

<figure><img src="../.gitbook/assets/image (1) (2).png" alt=""><figcaption></figcaption></figure>

링크에 들어가면 위와 같은 페이지가 나옵니다.

해당 페이지는 진짜 오픈소스 리포지토리에서 실습을 하는게 아니라 koala-eat-eucalyptus라는 조직에 fork를 한 리포지토리입니다. 그래서 여기에서 코드를 수정해도 전혀 문제가 없습니다.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

여기서 Fork 버튼을 누릅니다.

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Fork 버튼을 누르면 위 창이 나옵니다.

여기서 Owner만 자신의 아이디가 나오는지 확인하고, 제대로 나왔는지 확인했으면 초록색 Create fork 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

이후 왼쪽 위를 확인해보면 맨 처음과는 다르게 빨간 박스가 자신의 아이디가 되어 있는 것을 확인할 수 있습니다. 여기까지 들어왔다면 정상적으로 진행했다는 것입니다.



### 2. Clone

Clone은 로컬에 리포지토리 파일을 생성하는 것입니다.

개인 리포지토리는 Fork - Clone을 할 필요가 없지만, 다른 사람들이 만든 리포지토리에 기여를 하려면 Fork - Clone을 사용해야 합니다.

왜 굳이 이런 방식을 사용하냐면 다른 사람의 리포지토리에 접근할 권한이 없기 때문입니다.\
그래서 코드를 수정한 경우, 나중에 배우는 Pull Request라는 기능을 사용해서 원본 리포지토리에 ‘난 이렇게 코드를 수정했어’라는 신청서를 내면 된다고 생각하면 됩니다.

<figure><img src="../.gitbook/assets/image (1) (3).png" alt=""><figcaption></figcaption></figure>

이제 오른쪽 아래에 있는 초록색 Code 버튼을 클릭합니다.

주의할 점은 초록 버튼을 누를 때에도 오른쪽 위의 아이디가 자신의 아이디로 나와야 합니다.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

초록색 Code 버튼을 누르면 위와 같은 창이 나오는데, 여기서 복사 버튼을 누르면 됩니다.

해당 링크는 로컬에 리포지토리를 설치할 때 필요한 링크입니다.

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

이제 그러면 미리 실행해두었던 git을 실행하여 `git clone 복사한내용` 을 입력합니다.

<figure><img src="../.gitbook/assets/image (2) (2).png" alt=""><figcaption></figcaption></figure>

그러면 이렇게 자동적으로 폴더가 생성될 것입니다.
