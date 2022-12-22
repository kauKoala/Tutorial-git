# 커밋 메시지 본문 작성하기

우리는 그동안 <mark style="color:red;">`git commit -m "메시지 제목"`</mark> 을 사용해왔습니다. 하지만 좀 더 자세한 내용을 작성하고 싶으면 <mark style="color:red;">`git commit`</mark> 을 사용해서 작성을 할 수 있습니다.

일단 코드를 아무렇게 수정하고 <mark style="color:red;">`git add .`</mark> 을 입력합니다. 이후 git commit을 입력합니다.

<figure><img src="../.gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>

그러면 위와 같은 사진이 나온다는 것을 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (5) (3).png" alt=""><figcaption></figcaption></figure>

첫 번째 줄은 무조건 커밋 메시지 제목이 됩니다.

이후 줄바꿈을 하고 다음 줄부터는 본문에 나오는 메시지가 됩니다.

파이썬의 주석 처리(#)처럼 커밋 메시지가 GitHub에 나오고 싶지 않으면 주석 처리를 할 수 있습니다.

다 작성했으면 nano 에디터 기준으로 Ctrl + O, Ctrl + X를 하면 커밋 메시지를 저장하게 됩니다.

이후 Push를 해서 GitHub의 리포지토리에 들어가면 이렇게 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (1) (5).png" alt=""><figcaption></figcaption></figure>
