# fetch, merge, pull

이제 원격 저장소에 있는 코드를 로컬로 가져오는 방법을 알아봅시다.

{% hint style="info" %}
먼저 실습을 해보기 위해 <mark style="color:red;">`git reset --hard dcff87a`</mark> 와 <mark style="color:red;">`git push -f`</mark> 를 입력합니다.
{% endhint %}



### 1. fetch

fetch란 원격 저장소에서 가장 최신으로 저장된 데이터를 확인해보고, 원격 저장소에 데이터가 변경이 됐는지 안됐는지만 확인합니다.

이때 중요한 점은 fetch만 사용한다고 해서 바로 로컬에 있는 코드가 업데이트 되지 않습니다.

이제 fetch를 진행해봅시다.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

로컬에 저장된 리포지토리의 최신 커밋 목록을 확인해보면 이렇게 커밋 메시지가 되어 있습니다.

여기서 <mark style="color:red;">`git fetch <remote 이름>`</mark> 을 사용해봅시다. <mark style="color:red;">`git fetch upstream`</mark> 을 사용하면 됩니다.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

그러면 이렇게 새로운 브랜치를 찾은 것을 확인할 수 있습니다.

### 2. merge

Fetch를 했으면 이제 Merge를 해야 로컬에 반영을 할 수 있습니다.

이것은 <mark style="color:red;">`git merge <참조할 원격 저장소>/<업데이트를 할 브랜치명>`</mark>를 입력하면 됩니다.

여기서는 upstream과 main 브랜치이니 <mark style="color:red;">`git merge upstream/main`</mark> 으로 작성하면 됩니다. (브랜치는 다음 장에서 설명할 예정입니다.)

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

merge를 하면 최신 버전으로 저장할 수 있습니다.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

이제 GitHub를 살펴보면 아직 기록을 하지 않았기 때문에 옛날 버전 그대로 나오게 됩니다.

그래서 <mark style="color:red;">`git push`</mark> 를 통해 리포지토리에 반영을 합시다.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

가장 최신 커밋으로 바뀐 것을 확인할 수 있습니다.

### 3. pull

fetch and merge를 한 번에 하는 방법은 pull을 사용하는 방법입니다.

<mark style="color:red;">`git reset --hard dcff87a`</mark> 와 <mark style="color:red;">`git push -f`</mark> 를 다시 적용합시다.

이후 <mark style="color:red;">`git pull <원격 저장소 이름> <브랜치 이름>`</mark> 을 입력하면 됩니다.

여기서는 <mark style="color:red;">`git pull upstream main`</mark> 을 실행하면 됩니다.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

fetch와 merge가 한 번에 진행하는 것을 파악할 수 있습니다.

### 4. Fork한 리포지토리로 돌아가기

내가 Fork한 리포지토리와 현재 로컬의 기록이 서로 다른 상태일 때, 그리고 나는 GitHub에 기록된 Fork한 리포지토리로 돌아가고 싶을 때가 있을 겁니다.

이때에는 <mark style="color:red;">`git pull`</mark>을 사용하면 내가 Fork한 리포지토리의 GitHub 기록으로 다시 돌아가게 됩니다.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

이번엔 강제 push 없이 <mark style="color:red;">`git reset --hard dcff87a`</mark> 만 적용합니다. 그리고 현재 Fork한 리포지토리는 위 사진처럼 가장 최신 커밋으로 되어 있어야 합니다.

이후 <mark style="color:red;">`git pull`</mark> 을 적용해봅시다.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

이렇게 바로 GitHub에 기록된 내용으로 돌아갈 수 있게 됩니다.

