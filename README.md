﻿합작맵 커밋할 때!
=
2명 이상의 인원이 함께 맵을 만드는 합작맵에서는 서로 만든 맵 사이의 충돌이 일어나지 않아야 합니다.
따라서 서로의 커밋이 충돌하지 않도록 하기 위해 **모든 커밋은 별도의 브랜치를 만들어 병합하는 것**을 원칙으로 합니다.

브랜치 만드는 법
-
새로운 브랜치를 만들 때에는 `git checkout -b <브랜치이름>` 명령을 사용하여 브랜치를 만듭니다.
브랜치 이름은 다음과 같이 만드세요.

    제작자-순번
   
   예를 들어, Tronix라는 제작자가 자신의 5번째 브랜치를 만든다고 가정하면, 브랜치 이름은 `tronix-5`이 될 것입니다.

단, 올라온 이슈를 바탕으로 브랜치를 만들 때는 다음과 같이 **이슈의 내용을 간략하게 적어주세요**. 예를 들어, Tronix라는 제작자가 자신의 5번째 브랜치를, 56번째 타일의 색을 변경해 달라는 이슈를 바탕으로 만든다면, 브랜치 이름은 `tronix-5_change-color-tile-59`이 될 것입니다.

커밋하는 법
-
커밋을 할 때는 반드시 **master 브랜치가 아닌 따로 만든 브랜치**에 해주세요. 커밋의 단위는 소규모여도 좋습니다. 브랜치 하나 당 커밋의 수도 중요하지 않습니다. 1개가 될 수도, 10개가 될 수도 있습니다.
커밋의 이름은 다음과 같이 해주세요.

맵의 새로운 부분이나 효과 등을 추가했을 때:

    add<종류>: 타일범위 (설명 - 선택)
  
맵에 이미 있던 부분이나 효과를 수정했을 때:

    fix<종류>: 타일범위 (설명 - 선택)


종류에 들어갈 단어는 다음과 같습니다.
`pattern`: 채보 관련 업데이트일 때
`effect`: 이펙트 관련 업데이트일 때
`deco`: 장식, 배경 등을 추가할 때 (이 경우에는 타일 범위를 입력하지 않아도 됩니다.)

타일 범위는 `1-10`과 같이 입력합니다.

괄호 안에 들어가는 설명은 웬만하면 쓰는 것을 권장하며, 쓰지 않아도 상관은 없습니다. 만약 쓰지 않을 경우, 괄호는 삭제하고 타일범위까지만 입력해 주세요.

그리고 커밋하기 전에 한 가지 주의사항이 있습니다.
만약 텍스트 에디팅을 통해 맵을 수정했을 경우, **반드시 얼불춤 게임 에디터 안에서 저장 버튼을 눌러주세요.** 게임 내에서 저장을 하지 않고 텍스트 에디터 내에서만 저장을 하게 되면, 코드가 정렬되지 않아 깃에서 변경 사항들이 꼬일 수 있습니다.

Pull Request 만들고 병합(Merge)하는 법
-
브랜치 내에서 커밋을 모두 마쳤다면, 풀 리퀘스트 (Pull Request)를 사용해 master 브랜치에 병합해야 합니다.
우선 풀 리퀘스트를 만들고, 오른쪽에서 알맞은 태그를 선택하세요. 풀 리퀘스트의 제목은 위에 설명한 **커밋의 제목과 같은 방식으로 짓습니다**. 커밋이 1개라면 해당 커밋의 제목을 그대로 가져오되, 커밋이 여러 개라면 그 **커밋들의 내용을 한번에 정리할 수 있는 제목**을 지어주세요.
최종적으로 아래에 있는 초록색 Merge 버튼을 눌러 master 브랜치에 병합하면 끝!

단, 브랜치 사이의 변경 사항에 충돌이 생겨 자동으로 병합이 되지 않을 때도 있습니다. 그럴 때는 어쩔 수 없이 수동으로 깃허브 내에서 변경 사항을 반영해 주어야 하는데, 어떻게 해야 할 지 모르겠다면 저에게 요청해 주세요.

### 그럼 맵 만들러 출발!
