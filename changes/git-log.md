# git log

이번엔 그동안 우리가 보낸 커밋 목록을 확인하는 방법을 알아봅시다.

모든 내용은 중간에 나가고 싶으면 터미널에 q를 입력하면 됩니다.

### 1. git log

가장 기초가 되는 커밋 메시지 목록 확인 방법입니다.

<figure><img src="../.gitbook/assets/image (8) (2).png" alt=""><figcaption></figcaption></figure>

git log만 입력해보면 위와 같이 커밋 내역을 확인할 수 있습니다.

노란색 줄은 커밋의 해시 아이디인데, 이 값은 하나의 커밋에 대응하는 유일한 값으로 특정 커밋을 조작할 때 유용하게 사용합니다.

하지만 이 방법은 하나의 커밋에 자세한 설명이 나와있기 때문에 많은 양의 커밋 메시지를 확인할 때에는 비효율적인 방법입니다.

참고로 숫자 옵션을 붙이면 확인하는 커밋의 최대 개수를 설정할 수 있습니다.

3개의 커밋을 확인한다고 가정하면 `git log -3`을 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

이렇게 3개가 나오는 것을 확인할 수 있습니다.





### 2. git log —oneline

<figure><img src="../.gitbook/assets/image (2) (1) (2).png" alt=""><figcaption></figcaption></figure>

커밋 아이디와 커밋 메시지 제목만 확인하는 방법입니다.

보통 커밋 메시지 제목은 어떤 코드를 수정했는지 요약한 내용이 담겨있기 때문에 빠르게 확인할 수 있습니다.

여기서도 5개의 커밋만 확인한다고 해봅시다.

`git log --oneline -5` 를 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>





### 3. git log 옵션 1 - 커밋 메시지 검색

자주 사용할만한 옵션에 대해서 알아보겠습니다.

우리는 커밋 메시지에 tutorial이 들어간 커밋 메시지를 찾아보려고 합니다. 이때 검색하는 기능은 grep이라는 옵션을 사용합니다.

`git log --oneline --grep "tutorial"`을 입력해봅시다.

oneline 옵션의 경우엔 제가 임의로 설정을 한 것이지 oneline이 없어도 상관은 없습니다.

<figure><img src="../.gitbook/assets/image (6) (2).png" alt=""><figcaption></figcaption></figure>

이렇게 tutorial을 입력한 내용만 나오게 됩니다.

참고로 대소문자를 구분합니다. 그러면 이번엔 Tutorial을 검색해봅시다.

<figure><img src="../.gitbook/assets/image (7) (2).png" alt=""><figcaption></figcaption></figure>

대소문자를 구분하기 때문에 서로 다른 결과물이 나온다는 것을 알 수 있습니다.





### 4. git log 옵션 2 - 파일 변경 요약

특정 커밋에 어느정도의 변경 사항이 있는지 확인하는 기능을 사용해봅시다.

`git log --oneline --shortstat` 을 입력해봅시다.

<figure><img src="../.gitbook/assets/image (1) (3) (2).png" alt=""><figcaption></figcaption></figure>

이렇게 몇 개의 파일이 변경됐는지, 몇 개의 코드가 생성/삭제가 됐는지 확인할 수 있습니다.





### 5. git log 옵션 3 - merge 메시지 삭제

Pull Request를 해서 merge를 하게 되면 merge를 했다는 기록을 남기기 위해 커밋 메시지에 아무 의미 없는 메시지가 남게 됩니다.

<figure><img src="../.gitbook/assets/image (1) (1) (3).png" alt=""><figcaption></figcaption></figure>

보통 리포지토리 기록을 깔끔하게 관리한다면 squash and merge를 통해 pull request에 있는 모든 커밋을 하나의 커밋으로 관리하게 됩니다. 여기에 나온 #61이 Pull Request의 번호입니다.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

하지만 일반적인 merge가 될 경우, 모든 커밋이 리포지토리에 저장이 되는데, 위 사진과 같이 머지가 됐다는 것만 기록하는 아무런 내용이 없는 커밋 메시지가 들어가게 됩니다.

그래서 이 메시지를 삭제하고 커밋 메시지 목록을 확인할 경우 `git log --oneline --no-merges` 를 사용하면 됩니다.
