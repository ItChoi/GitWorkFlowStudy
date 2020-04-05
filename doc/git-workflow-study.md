## Git WorkFlow 연습

### Git-Flow 전략
- 정적 브랜치
  - master
  - develop
- 동적 브랜치 (일정 기간동안 유지되는 보조 브랜치)
  - feature
  - release
  - hotfix
- 간단 설명
  - Branches
    - master: 제품으로 출시될 수 있는 브랜치
    - develop: 다음 출시 버전을 위한 브랜치
    - feature: 기능 개발을 위한 브랜치
    - release: 이번 출시 버전을 위한 브랜치
    - hotfix: 출시 버전에서 발생한 버그를 수정하는 브랜치
  - Work Flow 
    - master -> develop: develop은 master에서 시작된 브랜치다.
    - develop은 상시로 버그 수정한 커밋들이 추가된다.
    - develop -> feature: 새로운 기능 작업, feature는 develop에서 시작된 브랜치다.
    - feature에서 새로운 기능 작업 완료 시 develop 브랜치로 merge
    - develop은 이번 버전에 포함되는 모든 기능이 merge되면 QA를 하기 위해 dev -> release 브랜치를 생성한다.
    - QA에서 발생한 버그들은 release 브랜치에 수정된다.
    - QA가 완료되면, release 브랜치를 -> master / develop 브랜치로 merge
    - 출시된 master 브랜치에 버전 태그를 추가! 
  

### 참조
1. [2017 우아한 형제들 깃 워크 플로우](https://woowabros.github.io/experience/2017/10/30/baemin-mobile-git-branch-strategy.html)

