# add, commit, push 동작 과정

저번 장에서 add - commit - push에 대해 배웠으니, add - commit - push가 정확히 어떤 역할을 하는지 알아봅시다.

### 1. Working Directory, Staging Area, Repository

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

우리가 코드를 수정하고, 커밋을 보내 GitHub에 기록을 할 때까지 총 3가지 영역을 거치게 됩니다.

* Working Directory : 우리가 코드를 수정하고 있는 곳
* Staging Area : add 명령어를 사용하면 등록되는 곳
* Repository : push 명령어를 사용하면 업로드 되는 GitHub

add 명령어를 사용하면 Working Directory와 Repository가 아닌 Staging Area에 일단 저장이 됩니다.

이후 Commit 메시지를 작성한다면 Staging Area에 들어간 모든 파일을 묶어서 해당 메시지에 저장합니다.

마지막으로 Push를 해서 GitHub에 등록이 됩니다.

#### Staging Area?

Working Directory에서 코드를 수정하고, 바로 Repository로 보내도 되지 안될까요? 굳이 Staging Area를 거쳐서 보내야 하는지 궁금한 사람들도 있을 것 입니다.

실제로 Git만 다른 형상 관리 툴과 다르게 Staging Area를 가지고 있습니다. 왜 Git만 Staging Area가 존재하냐면 다른 형상 관리 툴은 Git과 다르게 남들에게 코드를 공개한다는 목적이 더 크기 때문입니다. 참고로 Staging Area가 없으면 add도 존재하지 않아 commit - push만 할 수 있게 됩니다.

Staging Area가 존재할 경우 아래의 장점이 존재합니다.

* 수정한 코드 중에서 일부분만 add 하여 커밋 메시지를 작성할 수 있다.
* 충돌(Conflict)이 일어날 경우, 파일 단위로 어디에서 충돌이 일어났는지 알 수 있다.
* 이미 커밋 메시지를 작성한 상태에서 해당 커밋 메시지에 있는 파일 변경 내용을 수정할 경우 빠르게 수정할 수 있다.

{% hint style="warning" %}
충돌 (Conflict)

만약 제가 어떤 리포지토리를 Fork 했을 때, 원본 리포지토리의 가장 최근 커밋이 A라고 가정해봅시다. 그리고제가 Fork한 리포지토리에 어떤 파일을 수정해서 B라는 커밋 메시지를 보냈다고 해봅시다.

Fork한 리포지토리의 커밋 메시지는 A → B의 순서로 기록이 되어 있을 것 입니다.

하지만 누군가가 원본 리포지토리에 제가 수정한 파일과 똑같은 파일의 코드를 수정하여 C와 D라는 커밋 메시지를 보냈다고 해봅시다. 그러면 원본 리포지토리의 커밋 메시지는 A → C → D로 기록이 되어 있을 것입니다.

이때 제가 수정한 B를 원본 리포지토리에 반영을 하려고 합니다. 그런데 제가 Fork한 저장소는 A → B 순서의 커밋 메시지만 존재하지만, 원본 리포지토리는 A → C → D가 되어 있으므로 서로다른 내용이 기록 되어 있습니다. 이 경우 제 코드를 원본 리포지토리에 바로 반영을 할 수 없게 되므로 Conflict 상태가 일어나게 됩니다.
{% endhint %}





### 2. 커밋 메시지는 시간 순서대로 저장

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

위 사진처럼 push를 하지 않고, 여러 번 add와 commit을 반복한 후에 push를 해도 됩니다.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

만약 push를 하기 전에 GitHub에 init이라는 커밋 메시지가 가장 최근 메시지라면 커밋 메시지를 만든 순서대로 push를 하게 되어 init → python → java 순서대로 커밋 메시지가 쌓이게 됩니다.
