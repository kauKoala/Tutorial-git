# git status

통합 개발 환경(IDE)에서는 어떤 파일을 수정했는지 색깔 별로 구분하여 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

제가 자주 사용하는 IntelliJ에서는 파란색은 코드가 수정된 파일이고, 빨간색은 파일을 새로 만들게 됐는데, 아직 git에 기록이 되지 않은 파일입니다.

소규모의 프로젝트의 경우에는 디렉토리 목록만 확인해도 어느 정도는 가늠할 수 있지만, 그 외에는 확인하기가 어려운 편입니다. (ex. 대규모 프로젝트라 파일이 너무 많거나, 목록에서 일일이 확인하기 귀찮거나, …)

이것을 git에서 확인하는 방법은 git status입니다.

먼저 위 사진처럼 나올 수 있도록 아래와 같은 작업을 실행합니다.

* background.js에서 ON을 전부 OFF로 수정합니다.
* test.js 파일을 새로 생성합니다.

이제 git status를 통해 확인하면 됩니다.

<figure><img src="../.gitbook/assets/image (2) (5).png" alt=""><figcaption></figcaption></figure>

* background.js는 수정이 됐지만 Staging Area 상태가 아니라서 빨간색으로 나오고 있습니다.
* test.js는 새로 만들어진 파일이라 아직 기록이 되지 않았습니다.

일단 git add .을 사용하여 파일을 둘 다 Staging Area 상태로 이동해주고, 다시 git status를 사용해서 확인을 해보겠습니다.

<figure><img src="../.gitbook/assets/image (1) (5).png" alt=""><figcaption></figcaption></figure>

이렇게 초록색의 글자로 바뀌게 된 것을 확인할 수 있습니다.

이처럼 git status를 통해 한 번에 파일이 수정/생성/삭제가 됐는지 확인할 수 있습니다.

그래서 저는 add - commit - push를 하기 전에 어떤 파일이 변경되어 있는지 git status로 확인하는 편입니다.

{% hint style="info" %}
다음 실습은 background.js에서 진행할 예정이니 add - commit - push를 진행하시길 바랍니다. 커밋 메시지는 연습용이니 아무 내용이나 적어서 보내도 상관 없습니다.
{% endhint %}
