# git branch

Pull Request는 Merge 혹은 Closed가 되지 않는 한 새로운 커밋 메시지를 보내면 계속 반영이 된다는 특징을 가지고 있습니다.

이것은 장점이자 단점인데, 장점은 굳이 제가 PR에 어떤 커밋을 추가해야할지 고민할 필요 없이 기능 개발에 집중할 수 있다는 것입니다. 하지만 단점을 생각해보면 최신 버전으로 반영이 된다는 말은 우리는 기능 개발이 하나 끝났으면 해당 PR이 merge 혹은 closed가 될 때까지 새로운 기능을 만드는 것은 잠시 중단해야 합니다.

기록을 깔끔하게 관리하기 위해 GitHub를 사용하는데, 만약 해당 PR과 관련이 없는 기능을 개발하면 좋은 기록 관리가 되지 않겠죠

이때 우리는 기능 개발을 멈추는게 아닌 브랜치를 새로 하나 만들어서 개발을 할 수 있습니다.

브랜치는 팀원들이 fork를 하는 것과 비슷합니다. 나와 팀원들이 fork를 해도 내 리포지토리에서는 팀원들의 리포지토리와 서로 영향을 받지 않습니다. PR을 보낼 때도 오직 원본 리포지토리에만 영향을 받지, 팀원의 리포지토리와는 직접적인 영향을 받지는 않습니다.

브랜치도 똑같습니다. 각각의 브랜치는 서로 브랜치끼리 영향을 주고 받지 않습니다. 그래서 A라는 브랜치에 어떤 기능을 제작하고 PR을 보낸 상태라면 기다리지 말고, B라는 브랜치에서 또 다른 기능 개발을 진행하면 됩니다.

### 1. 브랜치 목록 확인하기

브랜치를 만들고, 변경하고, 삭제하는 방법은 간단합니다.

현재 제가 있는 branch를 확인하려면 <mark style="color:red;">`git branch`</mark> 를 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

현재는 main 브랜치 밖에 없으므로 main만 목록에 나오게 됩니다.

### 2. 브랜치 생성하기

이제 브랜치를 만들겠습니다. 브랜치를 생성하는 것은 <mark style="color:red;">`git branch <이름>`</mark> 을 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

이렇게 test라는 브랜치를 생성하고, 목록을 확인해보니 정상적으로 생성된 것을 알 수 있습니다.

### 3. 브랜치 이동하기

이제 main 브랜치에서 test 브랜치로 변경을 하겠습니다.

<mark style="color:red;">`git checkout <이동할 브랜치 이름>`</mark> 으로 변경을 할 수 있으므로 <mark style="color:red;">`git checkout test`</mark> 를 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

main 브랜치에서 test 브랜치로 바뀐 것을 확인할 수 있습니다.

### 4. 브랜치 삭제하기

다시 test 브랜치에서 main 브랜치로 이동해봅시다. `git checkout main` 을 입력하면 됩니다.

이제 test 브랜치를 삭제해봅시다.

<mark style="color:red;">`git branch -d <삭제할 브랜치 이름>`</mark> 으로 여기서는 <mark style="color:red;">`git branch -d test`</mark> 를 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### 5. 브랜치 생성하기 2

꼭 알아야 할 것은 현재 브랜치 코드를 가지고 새로운 브랜치를 만들기 때문에 현재 브랜치의 위치를 확인해야 합니다.

하지만 다른 브랜치에 있는 코드를 토대로 새로운 브랜치를 만든다면 아래와 같이 작성하면 됩니다.

<mark style="color:red;">`git branch <새로 만들 브랜치 이름> <가져올 브랜치 이름>`</mark> 을 입력하면 되는데, 이것도 실습을 진행해봅시다.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

먼저 다시 test 브랜치를 생성합니다. (<mark style="color:red;">`git branch test`</mark>)

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">`git branch new_test test`</mark> 를 입력해봅시다.

그러면 new\_test라는 브랜치가 만들어지게 됩니다.
