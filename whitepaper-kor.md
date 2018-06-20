# Commitground

개발활동으로부터 인센티브를 얻을 수 있는 Gerritium 토큰 경제 기반의, 소스코드 기여와 보상이 투명하게 연결된 프로젝트 개발 플랫폼.



## 초록

블록체인의 탈중앙화 운동은 자본가에게 유리하게 짜여진 기존의 경제구조를 벗어나, 참가자들 모두가 고르게 가치 창출에 대한 대가를 보상받을 수 있도록 도와줍니다. 이것은 다수의 시민이 참가하여 믿을 수 있는 공동의 장부를 운영함으로 "신뢰"의 가치를 창출하는 생산 수단을 사회화했기 때문에 가능해졌습니다. 따라서 블록체인의 탈중앙화 운동은 일종의 마르크스주의로, 블록체인 커뮤니즘이라 부를만 합니다.

더불어, 오픈소스 운동은 값비싼 부가가치를 지니고 있는 "소스코드"를 인류 공동의 자산으로 만듦으로써 가장 중요한 생산수단 중 하나를 사회화하고 있으며, 이것은 블록체인 커뮤니즘에서 아주 중요한 역할을 합니다. 하지만 오픈소스운동이 블록체인 생태계에서 이처럼 중요한 역할을 하고 있음에도 불구하고, 지금까지 오픈소스에 기여한 것을 보상받을 수 있는 시스템은 잘 갖추어져있지 않았습니다.

그래서 **우리는 소스코드 컨트리뷰션을 가치로 전환할 수 있는 시스템을 통해 소스코드 컨트리뷰션에 대한 보상을 적절하게 받을 수 있도록 하고, 오픈소스 운동을 더욱 활성화시켜  블록체인 커뮤니즘을 고도화시키고 블록체인 생태계가 성장하는 것에 기여하고자**합니다.



[TOC]

## 기여에 대한 가치평가

기여에 대한 가치평가는 두 가지로 나뉘어집니다. 그것은 그 기여를 원하는 사람이 누구냐에 따라서 달라집니다. 

첫 번째는 **커뮤니티에 의한 가치평가** 입니다. 예를 들어, 웹사이트를 개발하는 개발자가 있습니다. 이러한 개발자에게 컨텐츠를 작성하면 자동으로 아름다운 웹사이트로 변환해주는 Jekyll과 같은 오픈소스 라이브러리는 축복과도 같습니다. 만약에 웹 어플리케이션으로서의 기능이 필요할 때에는 ReactJS라는 축복이 존재합니다. 여기서 이미 "축복"이라는 단어에 두 라이브러리들에 대한 가치 평가를 엿볼 수 있습니다. 이처럼 오픈소스 프로젝트들은 프로젝트 자체 뿐 아니라 세부적인 기여 행위들에 대해서도 오픈소스 커뮤니티의 구성원들로부터 평가와 피드백을 받습니다.

두 번째는 **시장에 의한 가치평가**입니다. 예를 들어, 지금 당장 웹사이트를 만들고 싶은 **의뢰자**에게는 "주어진 컨텐츠로 웹사이트를 제작하여 인터넷에서 접속가능하도록 배포하기"라는 기여행위를 필요로 합니다. 따라서 의뢰자는 위 기여행위를 제공한 **기여자**에게 해당 기여행위가 의뢰자 본인에게 얼마나 필요한지 (수요)에 따라 보상을 지불할 의사가 있을 것입니다. 

그래서 우리는, **커뮤니티에 의한 가치평가**를 구현하기 위하여 Gerritium 화폐와 그 채굴시스템인 Plant System을 제공합니다. 이것은 인센티브가 존재하는 오픈소스 커뮤니티이며, 이를 통해 다양한 구성원들로부터 좋은 평가를 많이 받을수록 큰 가치를 인정받을 수 있습니다. '이 때 어뷰징을 통한 평가는 가치로서 인정받지 못합니다.'

**시장에 의한 가치평가**는 이슈를 생성하고 해당 이슈의 해결에 보상을 제공하거나 요구하는 기능을 통해서, 다양한 방식으로 프로젝트가 발전하고 새로운 가치가 생성될 수 있도록 돕습니다. 이러한 기능이 시스템상에서 유기적으로 동작할 수 있도록 Gerrit Code Review 시스템으로부터 영감을 받은 프로젝트 개발 플랫폼 commitground를 핵심 어플리케이션으로 제공합니다. commitground플랫폼에서는 기여행위와 보상의 연결이 투명하게 진행되며, 지속적인 개발이 지속적인 투자로 이루어질 수 있는 Gerritium Project Token기반의 dapp 프로젝트를 런칭할 수 있습니다.



## Commitground

Commitground는 프로젝트 개발 플랫폼입니다. Commitground 플랫폼에서는 앞서 이야기한 두 가지 가치평가 시스템을 통해 기여한 것에 따라 보상을 받을 수 있습니다. 이 때 보상으로 주어지는 것은 Gerritium이라고 불리는 화폐입니다. 다음 과정을 통해 어떻게 프로젝트를 시작하고 보상을 받게 되는지 살펴보겠습니다.



### How to use commitground

#### 프로젝트 시작하기

```javascript
const {client} = require('commitground')
client.startPorject({
    type: "General" | "GPT",
    name: "ProjectName",
    repoistory: "Project repository's hosting information" // e.g. "https://commitground.com/projects/my-project"
})
```

##### type

프로젝트를 시작할 때 크게 두 가지 유형으로 나눌 수 있습니다.

1. General SW Project
2. GPT App

General SW Project는 우리가 흔히 github 등의 개발플랫폼에서 볼 수 있는 모든 종류의 소프트웨어를 의미합니다. GPT App이란  GPT(Gerritium Project Token)기반의 토큰을 만들어 자체적인 토큰 이코노미를 구현하는 dapp(decentralized application)을 의미합니다. GPT App에 대해서는 [다음항목](#Gerritium Project Token)에서  자세하게 다룹니다.

##### name

프로젝트 이름은 영문, 숫자 그리고 '-', '_', '.'에 해당하는 문자를 사용할 수 있습니다. 

##### repository

Commitground 프로젝트는 두 곳에 데이터를 저장하는데, 첫 번째는 바로 이더리움네트워크이고 두 번째는 별도의 저장소입니다. 이 때 이더리움네트워크에는 프로젝트의 커밋트리 해쉬값들이 저장되는데, 이 값은 별도 저장소에서 서비스되는 소스코드가 원본이 맞는지 확인합니다. 별도의 저장소는 사용자가 자유롭게 지정할 수 있습니다. 

>**Git 프로젝트의 데이터 구성.**
>
>일반적인 Git 프로젝트는 다음과 같은 파일 구성을 지니고 있습니다.
>
>```bash
>.git
>├── HEAD
>├── config
>├── description
>├── hooks
>├── index
>├── info
>├── modules
>├── objects
>└── refs
>```
>
>이 중, objects폴더에는 커밋 별로 hash값을 기준으로 소스코드 파일이 분할 저장되어 있습니다. 여기에서 블록체인에는 objects폴더를 제외한 파일들이 기록되는데, 그 이유는 다음과 같습니다. 첫 째, 소스코드의 내용을 전부 블록체인에 기록할 경우 비용 낭비가 심합니다. 그리고 Git system은 각 commit마다 변경사항의 hash값, 그리고 이전 commit의 hash값, 작성자 정보와 작성일자를 토대로 hash되어 그 값을 저장하기 때문에 commit tree를 저장하는 것만으로도 외부 저장소에 별도로 저장된 소스코드가 실제 blockchain에 기록된 기여 내용과 일치하는 지 확인할 수 있습니다. 마지막으로 모두에게 공개된 오픈소스의 경우 사람들이 소스코드의 원본을 각각의 저장소에 clone하여 보관하는 경우가 많아 위변조를 탐지하는 것이 쉽고, 비공개 소스코드의 경우에는 위변조 위협을 소스코드 저장소 관리 차원에서 방어할 수 있습니다. 

소스코드를 서비스할 저장소는 다음과 같은 방식 중에서 선택할 수 있습니다.

1. Self hosted server

   사용자가 직접 저장소를 서비스하는 방식입니다. 정의된 Git protocol을 따르면 사용할 수 있습니다. 서비스를 위한 [docker 이미지를 제공]()(링크 업데이트 필요)합니다.

2. Commitground Repository Service

   Commitground에서 직접 서비스하는 관리형 Git 저장소입니다. 오픈소스 프로젝트의 경우에는 무료로 사용할 수 있습니다. 기여에 의한 보상을 직접적으로 받기 위해서는 이 방식을 이용해야 합니다.

3. 3rd Parties

   Github나 Gitlab 등의 3rd party 어플리케이션을 사용해 소스코드를 서빙할 수 있습니다. 이 경우 기여에 의한 보상을 받기 위해서는 플러그인과 확장 프로그램을 설치하는 작업이 필요합니다. 

   [github와 연동하기 바로가기]()(링크 업데이트 필요)

   [gitlab과 연동하기 바로가기]()(링크 업데이트 필요)



#### 이슈 등록하기

프로젝트를 생성한 뒤, 프로젝트를 다른 사람들과 협업하여 발전시키기 위해 Issue를 생성할 수 있습니다.

```javascript
client.registerIssue({
    registrar: "Address of registrar's account", // e.g) 0xh1298h
    project: "Address of project", // e.g) 0xjjjp12
    contents: "String or Object"
})
```

##### registrar

이슈를 제안한 사람의 계정 주소입니다.

##### project

이슈를 제안할 프로젝트의 계정 주소입니다.

##### contents

String 혹은 JSON형태로, UI에서 표현되는 컨텐츠 내용을 담고 있습니다.



#### 이슈 해결에 보상 제공하기 

우리는, 이슈가 정말 중요할 경우, 해당 이슈에 보상을 제공하여 보다 빨리 해결되도록 촉진할 수 있습니다.

```javascript
client.offerReward({
    targetIssue: "Address of target issue",
    gerritiums: "Amount of gerritiums to offer", // default: 0
    gerritrons: "Amount of gerritrons to offer", // default: 0    
    provider: "Address of offer provider's account",
    contents: "Critical bug during registration process",
    type: "Soft" | "Hard" // default: Soft
})
```

##### targetIssue

보상을 제공하고자 하는 이슈의 주소값입니다.

##### gerritiums

보상으로 주고자 하는 Gerritium의 양을 의미합니다. 

##### gerritrons

보상으로 주고자 하는 Gerritron의 양을 의미합니다. 

>Gerritium vs Gerritron?
>
>[Gerritron](#Gerritron)이란, Github에서의 Star와 같은 역할을 하는 것으로, Gerritium에서 추출할 수 있습니다. 단, Gerritium에서 Gerritron을 추출했을 때 해당 Gerritium은 한동안 거래할 수 없는 잠김 상태가 됩니다. 수신한 Gerritron을 모아서 Gerritium으로 교환할 수 있는데, 이 때 교환가능한 Gerritium은 모은 Gerritron들 발신자들의 명성에 영향을 받습니다. 
>
>Gerritium의 생태계에 따르면 Gerritron을 주고 받는 행위는 **구성원들에 의한 가치평가**에 속하는 것으로, Gerritium의 발행량을 결정하는 중요 메커니즘입니다. 이는 주로 오픈소스 프로젝트에 필요한 보상 생태계를 구성합니다.
>
>이에 반해 Gerritium을 직접 보상으로 사용하는 것은 **시장에 의한 가치평가**행위에 속하며 생태계가 필요에 의해 효율적으로 움직일 수 있도록 합니다. 이 방식은 자본에 의해 빠르게 가속되어 진행되는 프로젝트들에 어울리는 방식입니다.

##### provider

보상을 지불하기 위한 출금지갑의 주소입니다. 트랜잭션이 만들어지면, 해당 지갑에서 지정된 Gerritium 혹은 Gerritron이 출금되어 Issue에 보관됩니다.

##### contents

보상을 제시할 때, 메세지를 입력할 수 있습니다.

##### type

이슈를 종결할 때, 이슈를 해결하는 다양한 솔루션이 있을 수 있는데 어떤 제공자에게 예약한 보상이 돌아가게 할지 결정하는 방법입니다. "Soft" 타입의 경우 이슈 등록자가 결정하는 방식을 그대로 따라서 사용자가 예약한 보상금액이 지불되는 방식입니다. "Hard" 타입의 경우는 이슈 등록자의 결정과 상관없이 Issue가 종결되었을 때, 직접 보상 지불 대상을 선택할 수 있습니다.



#### 이슈에 테스트 케이스 작성하기

견고한 프로그램을 만들기 위해 Issue가 제대로 해결되었는지 확인하는 테스트 케이스를 작성하고 등록하는 것이 가능합니다. 작성된 스크립트는 컨테이너 상에서 테스트 케이스를 실행할 수 있도록 되어있습니다. 이는 오픈소스 프로젝트의 경우 Commitground 플랫폼에서 제공하는 빌드/테스트 도구를 무료로 사용할 수 있습니다.

```javascript
client.registerTestCase({
    targetIssue: "Address of target issue",
    branch: "Branch name"
    testScript: "test/issue1.yml",
})
```

##### targetIssue

테스트를 등록하고자 하는 이슈의 주소값입니다.

##### branch

테스트 케이스가 포함되어있는 브랜치의 이름입니다.

##### testScript

프로젝트 내 테스트 스트립트의 경로입니다. yml 형식으로 작성되어 있습니다. 

[How to write test script 바로가기]()(링크업데이트필)



#### 이슈 해결 선언하기

이슈를 해결하고자 하면, 기존에 이미 이슈해결을 시작한 사람과 협업해서 이어갈 것인지 혹은 독자적인 솔루션을 제안할 것인지 결정해야 합니다. 

```javascript
client.resolveIssue({
    targetIssue: "Address of target issue",
    baseSolution: "Base solution's branch name" | null,
    description: "Simple description here"
})
```

##### targetIssue

해결하고자 하는 이슈의 주소값입니다.

##### baseSolution

이미 이슈해결을 시작한 사용자가 있었고, 이 사용자의 이슈 해결에 기여하고 싶다면 baseSolution을 해당 사용자의 이슈 해결 브랜치로 지정할 수 있습니다. 만약 이것을 `null`로 설정할 경우에는 이슈 해결을 위한 브랜치가 `issue-13/sol-2`와 같은 이름으로 생성됩니다. 만약 `issue-13/sol-1`을 baseSolution으로 지정했다면 `issue-13/sol-1/sub-1`과 같은 브랜치가 생성됩니다.

##### description

이슈 해결을 시작할 때, 다른 사람들에게 어떠한 방식으로 이슈를 해결할 것인지 설명할 수 있습니다. 설명을 자세하게 적는 것은 중복된 개발을 방지하고 협업을 촉진할 수 있습니다.



#### Pull Request 작성하기

이슈 해결을 선언하여 브랜치를 만들고 나면, 해당 브랜치에는 쓰기 권한이 있습니다. 개발을 진행하여 브랜치가 이슈를 해결하는 상태가 되었다면 이슈 해결을 완료했다는 의미로, 혹은 중간 완료나 소규모 변경을 위하여 Pull Request를 작성하게 됩니다. 이 Pull Request를 이슈 생성자가 승인할 경우 `issue-13/solution` branch에 병합되게 됩니다. 

```javascript
client.pullRequest({
    registrar: "Address of registrar",
    target: "targetIssueId" | "targetSolutionBranch" | "baseBranch",
    compare: "repository/branch",    
    levelOfContribution: 0.3 | null,
    description: "Simple description here"
})
```

##### registrar

Pull Request를 작성한 계정의 주소값입니다.

##### target

Pull request의 target에는 3가지 종류가 있습니다. 

1. Issue

   target으로 Issue Id를 지정할 경우에는, `compare`브랜치로부터 checkout된 solution 브랜치가 자동으로 생성되어 Issue를 해결하는 Pull Request임을 알리게 됩니다.

2. Solution

   targeting하는 Solution Branch가 있다면, `compare`브랜치로부터 checkout된 sub-solution 브랜치가 자동으로 생성되고 Solution 협업을 위한 Pull Request임을 알리게 됩니다.

3. Etc

   이슈 해결을 위한 Pull Request가 아닌 경우의 Pull Request는 Target branch를 직접 입력하게 됩니다.

##### compare

Merge를 요청할 커밋헤드를 의미합니다.

##### levelOfContribution

이것은 *target*이 issue이거나 solution일 경우에 보상을 분배받기 위해 지정하는 값입니다. 0에서 1사이의 숫자를 통해 본인의 기여가 프로젝트에서 얼만큼인지를 주장할 수 있습니다. 이슈가 종결될 때는 이 값들의 합을 제수(divisor)로 하고 각 levelOfContribution을 피제수(dividend)로 한 비율만큼 보상을 지급받게 됩니다. null을 입력하여 자선봉사의 성격으로 Pull Request를 만들 수도 있습니다.



#### Solution 선택하기

다양한 사람들이 Solution을 제안하여 충분하게 이슈가 해결된 경우에는, 이슈를 등록한 사람이 솔루션을 선택하고 이슈를 종결할 수 있습니다. 

```javascript
client.closeIssue({
    solution: "solutionBranch",
    description: "Simple description here"
})
```

##### solution

선택할 솔루션의 브랜치 이름입니다. 종결시 `issue-{number}/solution`에 지정한 solution이 머지되고 해당 solution branch에 기여한 사람들에게 등록된 보상이 자동으로 지급됩니다.

##### description

이슈를 종결하면서 간단한 설명을 추가할 수 있습니다.



#### Comment 추가하기

지금까지 위에서 `client`를 사용하여 이루어진 transaction은 모두 activity로 취급됩니다. Activity에는 comment를 추가하는 것이 가능합니다. Comment또한 Activity이기 때문에 Comment에도 Comment를 추가하는 것이 가능합니다.

```javascript
client.comment({
    at: "activityId",
    contents: "comment"
})
```

##### at

모든 activity는 Transaction이 일어날 때, Activity Id를 발급받습니다. Comment를 어느 Activity에 추가할 것인지 지정하는 변수입니다.

##### contents

코멘트 내용을 포함합니다.



#### Activity에 대해 Gerritron을 주기

지금까지 Issue의 생성 및 솔루션 선언, Pull Request의 생성 및 이슈의 종결과 comment등에 해당하는 Activity들이 있음을 확인하였습니다. 우리가 확인한 모든 Activity는 가치를 생성하는 것에 일조한 것들이므로 Vote를 통해 그 행동들이 얼마나 가치있었는지 평가할 수 있습니다. 구성원들은 특정 Activity의 기여가 충분하다면 Upvote와 함께 본인이 만들어낼 수 있는 Gerritron을 선물함으로 그 기여를 인정해줄 수 있습니다.

```javascript
client.upvote({
    activity: "activityId",
    gerritrons: 10 | null
})
```

##### activity

Upvote할 Activity의 Id입니다.

##### gerritrons

지정한 만큼의 Gerritron이 Activity를 만든 사람에게 전달됩니다.



#### 수신한 Gerritron을 화폐로 교환하기

커뮤니티 기여를 통해 수취한 Gerritron들은 교환소를 통해 Gerritium으로 교환할 수 있습니다. 이 때 교환가치의 단위는 GQ로 표시하는데, 다양한 사람들에게 Gerritron을 받을수록 교환 가치는 높아집니다. 또한 이미 다양한 사람들에게 Gerritron을 수신한 경험이 있는 사람들로부터 Gerritron을 수신했을 때 교환가치가 더욱 높아집니다. 예를 들어 한 사람에게 100개의 Gerritron을 수신했을 때 100 GQ의 교환가치가 있다면, 두 사람으로부터 각각 50씩 받아 100개의 Gerritron을 수신했을 때는 150 GQ의 교환가치가 될 수 있습니다. 1 GQ 당 몇 개의 Gerritium을 받을 수 있는지는 교환소에서 Plant(채굴자)와의 거래 시세에 따라 달라집니다. 



## GPT App(Gerritium Project Token Application)

GPT(Gerritium Project Token)란 ERC20에서 확장된 토큰 형태로, DApp을 Commitground를 사용하여 개발할 때 해당 DApp에서 사용할 토큰을 GPT로 발행할 수 있습니다. GPT로 토큰을 발행할 경우 commitground 내에서의 ICO를 거쳐 프로젝트에 펀드를 유치할 수 있습니다. 또한 기여에 대한 가치평가 시스템에 따라서 기여자들은 프로젝트가 유치한 펀드로부터 보상을 받아 급여처럼 활용할 수 있으며, 프로젝트가 발급할 GPT형태의 토큰 또한 보상받아 스톡옵션처럼 보유할 수 있습니다. 이 시스템은 Gerrit Code Review로부터 영감을 받았으며 TDD(Test Driven Development)에 충실한 애자일 프로젝트 개발 기법을 활용하는 것을 바탕으로 만들어졌습니다.

이 시스템은 통해 우리는 

1. 지속적 개발과 지속적 펀딩: CD-CF (Continuous Development and Continuous Funding)
2. 사기(Scam)위험성의 감소
3. ICO 과정의 간소화
4. 유망 프로젝트에 대한 투자 편의성 증대
5. 원격 근무의 활성화

등의 효과를 기대할 수 있습니다.



### GPT App의 생명주기

1. 한 사람이 우버를 대체하는 DApp을 만들겠다고 하였습니다. 그리고, 그 앱에서 사용될 화폐는 XBer Token(XTO)이라고 명명하였습니다.
2. 한 투자자가 해당 아이디어와 계획을 검토한 결과 유망하다고 판단하여, 보유한 Gerritium을 사용해서 XTO를 새로 발급해갔습니다. 이 때 투자자는 ICO에 가장 먼저 참여하였으므로 가장 큰 수익을 기대할 수 있습니다.
3. 투자자가 펀딩한 것을 전 세계의 여러 개발자들이 확인하였습니다. 이제 보상을 받을 수 있기 때문에 많은 개발자들이 프로젝트에 기여한 뒤 보상을 획득해 갑니다. 개발자들은 보상으로 Gerritium과 XTO를 모두 받아가게 되는데, Gerritium은 바로 월급처럼 사용하여 생활을 유지하는 것에 사용할 수 있습니다. 하지만 XTO는 아직 거래가 불가능하므로(프로젝트가 Unlock 되어야 거래 가능), 스톡옵션처럼 가치를 올리는 것에 집중합니다.
4. 프로젝트가 활발하게 개발되는 것을 확인한 투자자들은 추가적인 투자를 진행하고, 펀드와 개발이 지속적으로 이루어지는 것을 확인한 개발자들은 프로젝트에 지속적으로 참가하여 기여한 뒤 보상을 받아갑니다.
5. 개발이 완료되자 프로젝트 위원회는 프로젝트를 배포하여 잠김상태를 해제하였습니다. 이에 따라 XTO가 거래가능한 상태가 되고 Xber를 사용하겠다는 사람들이 기존의 토큰보유자들에게 토큰을 구매해갑니다. 
6. Uber를 블록체인으로 대체하여 더 저렴한 서비스를 제공하는 XBer가 성공적으로 마무리되고 이에 기여한 개발자들과 투자자들은 충분한 보상을 받아갑니다.

![](https://s3.ap-northeast-2.amazonaws.com/my-publics/how-it-works.png)



### Development Process

우리는 위 과정을 매끄럽게 진행하는 것을 돕기 위하여 다음과 같은 프로세스를 제공합니다.

1. 마일스톤의 제안
2. 세부 액션의 설정
3. 테스트 케이스 작성
4. 개발
5. 테스트 진행 및 PR
6. 코드 리뷰 및 피드백
7. 코드 수정 및 PR
8. 코드 리뷰 및 승인
9. 버그 발견 및 이슈 등록
10. 버그 수정 및 PR

![](https://s3.ap-northeast-2.amazonaws.com/my-publics/process-of-oss-development.png)

위 흐름에 따라서 프로젝트 개발과정을 살펴보도록 하겠습니다.



### How to make a GPT App

#### Project 시작 후 Governance 설정하기

GPT App project를 시작하기 위해서는 Project를 어떤 방법으로 관리할 것인지 설정해야 합니다. Project 관리체계에는 다음 세 가지가 있습니다. 

1. 위원회 시스템

   위원회 시스템은 위원회를 설립하고 위원회에서의 의결절차를 거쳐 안건을 처리하는 방식입니다. 프로젝트의 규모가 커질 경우 일부 안건 처리 권한을 위임할 수 있도록 부속위원회(sub-committee)를 설립하여 프로젝트 관리를 유연하게 할 수 있습니다. 투자를 필요로 하는 DApp을 개발할 때 가장 이상적인 형태의 프로젝트 관리 시스템입니다.

2. 슈퍼 어드민 시스템

   슈퍼 어드민 시스템은 등록된 슈퍼 어드민이 모든 권한을 행사할 수 있는 시스템입니다. 우리가 현재 프로젝트를 개발할 때 주로 사용하는 Github, Gitlab 등에서의 프로젝트 관리 방법과 유사합니다. 의사결정이 가장 빠르지만 그 과정이 독단적으로 이루어지므로 소규모의 작은 프로젝트에서 유용한 방식입니다.

3. 주주 시스템

   주주 시스템은 위원회 시스템 및 슈퍼 어드민 시스템과 혼용할 수 있는 관리 시스템입니다. 이는 해당 프로젝트 토큰 보유자들의 결정에 따라 의사결정을 할 수 있는 방법을 제공합니다. 의사결정의 모든 부분 혹은 일부에 대해 토큰 보유자들이 내리는 결정을 따르도록 합니다. 이는 각각 보유한 토큰을 토대로 권리를 행사할 수 있도록 도와줍니다. 이것을 적절하게 사용할 경우 투자자들을 보호하는 유용한 수단이 될 수 있으나, 잘못 사용되었을 경우에는 소수의 대주주에게 이익이 집중되어 생태계가 악화될 수 있습니다.

```javascript
const {Project, Governance} = require('commitground')
const {Committee, SuperAdmin, Stakeholder} = require('commitground')
const project = new Project('project-address')
const myGovernance = Governance.Committee({
    president: "Address of user account"
})
project.setGovernance(myGovernance.getAddress())
```



#### 마일스톤 설정하기

프로젝트 위원회는 프로젝트 마일스톤을 설정합니다. 마일스톤은 큰 줄기들로 이루어져 있으며 각 마일스톤 개발에 필요한 예산을 설정합니다. 이것은 ICO에 필요한 자금 조달 지표로 투자자들에게는 적정 투자금액을 가늠할 수 있도록 하고, 개발자들에게는 얼마의 보상을 획득할 수 있을지 가늠할 수 있도록 합니다.

예를 들어, 우버 대체 프로젝트에서는 다음 7개의 마일스톤을 제안하고 각각의 마일스톤에 예산을 책정합니다. 각 예산은 프로젝트 위원회(혹은 슈퍼어드민)가 변경할 수 있습니다.

1. 스마트 컨트랙트 개발

   1. 운전자/승객 등록 (10,000 Gerritium)
   2. 운전자/승객 매칭 (10,000 Gerritium)
   3. 운전자/승객 피드백 (10,000 Gerritium)

2. UI/UX 디자인

   1. UI/UX 스토리보드 (10,000 Gerritium)
   2. 테스트케이스 작성 (10,000 Gerritium)

3. 클라이언트 개발

   1. Driver 용 Client (10,000 Gerritium)
   2. Passenger 용 Client (10,000 Gerritium)

   

#### Raising Funds(ICO)

commitground에서 GPT App을 개발할 경우, 간편한 ICO를 지원합니다. ICO의 기본 계약으로 총 발행량과 판매량 및 목표 금액을 설정하면 자동으로 토큰 발행 및 세일을 진행할 수 있습니다.

ICO를 진행할 목표 금액을 프로젝트 위원회가 마일스톤과 예산을 어떻게 책정하는지에 따라 달라집니다. 투자자들은 해당 마일스톤과 예산이 적절하게 책정되었는지를 확인하고 신뢰성 있는 계획일 경우 투자를 집행할 것입니다.

ICO 과정에서는 Gerritium이 기본화폐로 사용되므로 투자자들을 Gerritium을 프로젝트에 지불하고 해당 프로젝트의 GPT를 발급받아 보유하게 됩니다. 여기에서 프로젝트가 유치한 Gerritium은 프로젝트 개발과정에 따라 투명한 과정을 통해 프로젝트 개발에 기여한 사람들에게 적절하게 분배됩니다.

 투자자가 Gerritium을 지불하고 확보한 GPT는 프로젝트의 개발이 완료되어 프로젝트를 Unlock하기 전까지는 소유권의 이전이 불가능합니다. 즉, 거래 불가능 상태입니다. 이것은 일반적인 스타트업에서 스톡옵션, 주식이 동작하는 방식과 유사합니다. 이 프로젝트에 참가한 투자자와 구성원들은 보유하고 있는 GPT가 더욱 큰 가치를 지니도록 하기 위해, 그리고 실제 거래가 가능하도록 만들어 Exit과 같은 성공을 실현하기 위해 프로젝트에 더욱 몰두하고 기여하게 됩니다.

```javascript
project.setICOPlan({
    tokenName: "XBer Token",
    symbol: "XTO",
    model: "linear" | "exponential" | "other contract address"
})
```

##### tokenName

토큰의 이름입니다.

##### symbol

토큰의 심볼입니다.

##### model

1. Linear

   토큰 가격이 발행시마다 선형적으로 증가하도록 설정하는 방법입니다.

2. Exponential

   토큰 가격이 발행시마다 Exponential하게 증가하도록 설정하는 방법입니다.

3. Other contract's address

   토큰 발행에 따른 가격을 특정한 계약에 따라서 변경되도록 설정하는 방법입니다.



#### 액션아이템 만들기

GPT Project에서의 액션 아이템은 Issue와 본질적으로 동일합니다. 하지만, Action Item과 Issue가 다른 점은 Issue 수행 보상을 제공하는 것이 프로젝트 펀드라는 것입니다. Action Item은 누구나 만들 수 있으며 이 Action Item이 등록되기 위해서는 프로젝트 위원회(혹은 슈퍼어드민)의 승인이 필요합니다.

```javascript
project.createActionItem({
    issue: "registering a driver",
    reward: {
        Gerritium: 10,
        GPT: 10
    },
    test: "test/register.yml"
})
```

##### issue

액션 아이템이 해결하고자 하는 이슈입니다.

##### reward

이슈의 해결 보상으로 프로젝트 위원회로부터 요구하는 보상 금액입니다.

##### test

액션아이템이 적절하게 완료되었는지를 확인하는 테스트 케이스입니다. 테스트 케이스가 잘 작성되어 있을수록 프로젝트는 견고하게 진행될 수 있습니다.



#### 액션아이템의 평가 및 리뷰

액션 아이템은 Public Review와 Contributor Review를 받을 수 있습니다. 이것은 액션 아이템을 심사하는 것에 영향을 줄 수 있습니다.

```javascript
actionItem.registerReview({
    contents: "Contents",
    scores: {
        importance: 3.3,
        urgency: 4.5,
        reward: 1.9,
        test: 2.9
    }
})
```

##### importance

액션 아이템이 얼마나 중요한 내용인지에 대한 평가입니다.

##### urgency

얼마나 빠르게 수행되어야 하는지에 대한 평가입니다.

##### reward

액션 아이템에 책정된 보상 요구가 적절하게 책정된 것인지에 대한 것입니다.

##### test

테스트 케이스가 적절하게 작성되었는지에 대한 평가입니다.



#### Pull request 만들고 Code Review 진행하기

액션 아이템이 승인되었으므로 개발자들은 액션 아이템을 수행하기 위해 솔루션을 제안합니다. Issue에 대해 Pull Request를 생성하는 과정과 동일하게 진행됩니다. 다만 GPT에서는 Code Review를 강제하고 있습니다. 여기에서 Code Review는 지정된 Reviewer와 Public Reviewer 모두가 해당됩니다. 해당 Pull Request가 일정 Code Review 점수 이상을 획득해야 해당 액션 아이템을 성공적으로 수행한 것으로 평가받고 그 보상을 얻을 수 있습니다. 이 때 Code Review를 촉진시키기 위해 Pull Request 생성자는 Code Reviewer를 위해 본인이 획득할 보상의 일부를 Reviewer와 나눌 수 있습니다.

```javascript
pullRequest.registerReview({
    contents: "",
    details: [
        {
            file: "detail/path/of/file/to/review",
            lineNumber: 32,
            review: "Do not change any global variable inside a function"
        }
    ],
    scores: {
        "solution": 5.0,
        "quality": 5.0
    }
})
```

##### contents

Pull Request 코드리뷰에 대한 커멘트입니다.

##### details

코드 라인별로 자세한 커멘트를 남길 수 있습니다. 

##### scores

- solution: Pull Request가 이슈를 정확하게 해결 하는지에 대한 평가입니다.
- quality: 코드 퀄리티가 얼마나 좋은지에 대한 리뷰입니다.

특정 기준을 넘을 경우 자동으로 Merge가 될 수 있고, 그렇지 않을 경우에는 프로젝트 위원회의 의결을 거쳐 Merge 될 수 있습니다. 이 때 코드 개발과정에 참여한 사람들에게 보상이 적절하게 분배됩니다.



#### Build/Test/Deploy

 commitground는 TDD와 dev-ops를 유연하게 지원하는 것에 초점을 두고 있습니다. 따라서 Pull Request를 머지하는 과정에서 빌드-테스트-배포가 자동으로 이루어지도록 합니다. Commitground 플랫폼은 저장소 서비스와 마찬가지로 오픈소스의 경우에는 무료로 서비스를 제공하며 Private Project의 경우에는 유상으로 서비스를 제공합니다. 



#### AaaS(Audit as a Service)

블록체인 어플리케이션의 경우에는 블록체인 특성상 배포를 되돌리는 것이 어렵습니다. 따라서 배포과정에 전문적인 코드 리뷰가 필요합니다. 따라서 commitground 플랫폼에서는 코드 배포전 Audit 과정을 추가할 수 있습니다. 실력있는 개발자들은 Audit 팀을 구성하고, 다른 프로젝트들의 Audit 요청을 처리하고 보상을 획득할 수있습니다.



#### 3rd Party Integration 

commitground에서의 변경사항을 Webhook을 추가하는 것을 통해, 3rd party 어플리케이션과 통합할 수 있습니다. 

```javascript
project.addWebhook({
    topic: "pull-request" | "issue-registration" | "etc...",
    url: "https://your-thirdpary-application-url"
})
```

##### topic

webhook을 보내기 위한 topic입니다. 지원되는 topic은 

- pull-request
- issue-registration 
- 추가 요망

등이 있습니다.

##### url

POST 형태의 HTTP Request를 전송하기 위한 목적지입니다.



### 펀드 낭비 방지하기

1. 평판

   기여한만큼 돈을 벌 수 있으므로, 코드리뷰, 이슈, 액션, PR을 무의미하게 생성하는 사람들이 생겨날 수 있습니다. 모든 기여행위에는 Upvote와 Downvote가 존재하고 이것은 기여자들의 평판을 결정합니다. 이 평판에 따라서 지급되는 보상금액이 달라지게 됩니다.

2. 부도덕에 대처하기

   펀드가 많이 모일 경우, 특정 세력이 위원회를 장악한 뒤 과도한 보상을 액션 아이템에 책정하고 해결하는 등의 악의적인 방법으로 펀드를 탈취하려는 시도를 할 수 있습니다. 이 때 주주시스템은 보상이 확정되기 전 계류기간동안 챌린지를 할 수 있도록 하고, 악의적인 공격이라 판단될 경우 액션 아이템의 등록과 수행을 무효화시킬 수 있습니다. 이를 위해서는 챌린지에 참여한 총 토큰이 전체 발행량의 특정 비율을 넘어야 합니다. 혹은 프로젝트의 진행 자체를 취소시킬 수 있는 챌린지도 가능합니다.



#### 시장 공개(Going to public)

프로젝트가 정상궤도를 달려 제시한 마일스톤을 모두 달성하였을 경우 프로젝트를 런칭하고 Unlock할 수 있습니다. 이 결정에는 프로젝트 위원회의 2/3이상이 참여해야하고 2/3 이상의 득표가 필요합니다. 프로젝트가 공개되고 나면, 이제 프로젝트를 통해 개발된 GPT 토큰은 시장에서 자유롭게 거래될 수 있습니다. 그동안 이 순간을 위해 기다려온 기여자들과 투자자들은 투자 이익을 환수할 수 있게 됩니다.



## Gerritium

Gerritium은 Plant System을 통해 생산 및 데이터의 기록이 이루어집니다. Gerritium을 생산하기 위해선 Plant 노드를 운영해야 합니다. Gerritium 경제 시스템은 인센티브와 인플레이션이 가치평가와 적절하게 맞물릴 수 있는 정교한 물리시스템으로 설계되었습니다. 하지만 채굴을 하거나 플랫폼을 사용할 때 물리 시스템의 동작을 모두 이해할 필요는 없습니다.



### Physics & Token Economy

Gerritium은 기본 화폐로 쓰이는 물질입니다. 그리고 기여를 인정해주기 위해서는 Gerritium에서 추출한 Gerritron을 사용합니다. 한 번 Gerritron을 추출하면 Gerritium은 Light Gerritium으로 전환되어 화폐로 사용하지 못하지만, 시간이 지나면 다시 Gerritium으로 복원됩니다. 사람들이 보내준 Gerritron을 모으면 거래소에 Gerritium을 받고 판매할 수 있습니다. 

#### 핵심 명제

1. 개발 활동에 기여한 것은 가치를 생성한 것입니다.

2. 화폐가 발행되기 위해서는 프로젝트 기여를 통한 가치의 생성과 블록체인에 대한 기여가 필요합니다.

3. 기여활동이 얼마나 가치를 만들었는지는 커뮤니티 구성원의 평가에 좌우되며, 다양한 구성원으로부터 평가받을 경우 더욱 그 가치를 인정받습니다.

4. 다양한 구성원으로부터 평가를 받아왔을 경우, 영향력이 강화됩니다.

   


#### 물질

다음 물질[^1]들은 commitground의 경제시스템을 이루는 기본 요소로 활용됩니다.

1. Gerritron

   commitground 물리세계에서의 기본입자입니다. 보유하고 있는 Gerritium을 분열시키면 획득할 수 있습니다. 개발에 대한 기여를 인정할 때, 본인의 Gerritium에서 추출한 Gerritron을 전송함으로 그 기여를 인정해줄 수 있습니다. 수신한 Gerritron은 Gerritium을 생성하는 핵융합의 원료인 Gerritite를 만드는 것에 사용할 수 있습니다. 각 Gerritron은 어떤 Material Manager가 생성했는지에 따라 고유회전각을 가지게 됩니다.

2. Gerritite

   Gerritron을 모아 응축시킨 형태의 원재료로 Rietveldium 핵융합 과정에 연료로 사용됩니다. 다양한 출처의 Gerritron으로 구성된 Gerritite일 수록 품질이 좋아 에너지 생산효율이 높아지고 더 많은 양의 Gerritium을 만들어낼 수 있습니다. Gerritite-Gerritium Market을 통해 Plant에게 판매할 수 있습니다.

3. Rietveldium

   7개의 Gerritron으로 이루어져 있는 물질로, Commitground에서 화폐로 사용됩니다. Gerritium은 Rietveldium을 핵융합하여 얻을 수 있고 이 때 재료로 Gerritite가 사용됩니다. 핵융합과정에서 잉여의 Gerritron이 강력한 운동에너지를 가지고 공간으로 퍼져나는데, 이를 Hyper Gerritron이라 합니다.

4. Light Gerritium

   6개의 Gerritron으로 이루어진 물질입니다. Gerritium에 간단한 충격을 가하면, Light Gerritium과 Gerritron으로 쪼개어지는 Gerritium 분열의 산출물입니다. Light Gerritium은 공기 중 Hyper Gerritron과 반응하여 서서히 Gerritium으로 재전환됩니다. 이 때의 전환 속도는 pHG(potential of Hyper Gerritron)에 비례합니다.

#### Plant system: DPoT(Delegated Proof of Transaction)

Plant system은 DPoT(Delegated Proof of Transcation)에 따라서 보상을 지급합니다. 이 시스템에서 Client는 발생시키고자 하는 Transaction을 Plant에게 전달합니다. 그리고 Plant는 직접 Gas를 소모하여 이더리움 네트워크에 Transaction을 발생시킵니다. Transaction이 성공적으로 수행되었으면 Plant는 그 보상으로 화폐를 만들 수 있는 재료를 얻을 수 있습니다. DPoT는 클라이언트가 직접 블록체인 노드를 가지고 있을 필요가 없도록 만들며, 직접 메인네트워크를 운영하지 않고도 이더리움 네트워크 위에서 보상화된 화폐 경제를 구현할 수 있도록 합니다. 다음을 통해 Gerritium Token Economy의 DPoT인 Plant System이 어떻게 동작하는지 자세하게 살펴보겠습니다.

![physical-laws-for-gerritium](https://s3.ap-northeast-2.amazonaws.com/my-publics/physical-laws-for-gerritium.png)

[① 계정 생성](#1. 계정-생성)

[② 트랜잭션의 기록과 보상체계](#트랜잭션의-기록과-보상체계)

[③ 광물(Rietveldium)의 채굴 공식](#③-광물(Rietveldium)의-채굴-공식)

[④ 핵융합 재료(Gerritite)의 거래](#④-핵융합-재료(Gerritite)의-거래)

[⑤ 핵융합과 부산물(Gerritium & Hyper Gerritron)](#⑤-핵융합과 부산물(Gerritium & Hyper Gerritron))

[⑥ 핵분열과 부산물(Light Gerritium & Gerritron)](#⑥-핵분열과 부산물(Light Gerritium & Gerritron))

[⑦ 가치 평가](#⑦-가치-평가)

[⑧ 핵융합 재료(Gerritite)의 제조와 품질](#⑧-핵융합-재료(Gerritite)의-제조와-품질)

[⑨ 고에너지 입자에 의한 자연 핵융합과 Gerritium 복원](#⑨-고에너지 입자에 의한 자연 핵융합과 Gerritium 복원)



##### ① 계정 생성

Gerritium 커뮤니티에 새로 가입한 구성원은 Material Manager와 비대칭 암호화 키 쌍을 지급받습니다. 그리고 각 Material Manager는 고유의 주소를 가지고 있으며, 발급 받은 키 중 Public Key는 블록체인 상에 Material Manager의 고유 주소와 함께 기록됩니다.

사용자가 지급받은 Material Manager는 다음 역할을 수행합니다.

1. 화폐인 Gerritium을 보관, 전송, 수신하기
2. 커뮤니티 내에서 다른 구성원의 기여를 인정하는 것에 사용하는 [Gerritron을 추출](#핵분열과 부산물(Light Gerritium & Gerritron))하기
3. 커뮤니티 내에서 다른 구성원의 기여를 [Gerritron을 전송](#가치-평가)하여 인정해주기
4. 커뮤니티에서의 기여를 인정받아 다른 구성원들로부터 Gerritron을 수신하고, 수신한 [Gerritron을 화폐로 교환](#핵융합-재료(Gerritite)의-거래)하기




##### ② 트랜잭션의 기록과 보상체계

Plant 시스템을 사용할 경우, dapp client는 이더리움 노드일 필요가 없어집니다. dapp client가 커뮤니티에서 활동을 하였고 그 내역이 블록체인에 기록되기 위해서는 Plant 노드와 http 프로토콜로 통신할 수만 있으면 됩니다.

예를 들어, User A가 commitground 프로젝트에 이슈를 등록했다는 활동을 이더리움 상에 기록해보도록 하겠습니다. 

1. 해당 활동을 기록하기 위한 트랜잭션을 json abi에 의거하여 생성합니다. (예시로 작성된 것이므로, 디테일한 프로그램 설계시 업데이트 필요)

   ```json
   {
       "method": "register_issue",
       "params": ["0xAddressOfUser", "0xAddressOfProject", "0xAddressOfIssue"]
   }
   ```

2. 그리고 위 Transaction 데이터를 보유하고 있는 Private Key로 암호화한 뒤, 다음과 같은 데이터를 Plant node에게 HTTP 프로토콜로 전송합니다.

   ```json
   {
       "from": "0xAddressOfUser",
       "transaction": "bytesArrayEncrypteByUsersPrivateKey"
   }
   ```

3. Plant node는 HTTP 프로토콜로 수신한 json data를 input data로 삼아 다음 Transaction을 발생시킵니다.

   ```json
   {
       "jsonrpc": "2.0",
       "method": "mineRietveldium",
       "params": [
           "0xAddressOfPlant",
           "0xAddressOfUser",
           "bytesArrayEncryptedByUsersPrivateKey"
       ]
   }
   ```

4. 위 트랜잭션 실행되면 다음과 같은 과정을 진행합니다.

   1. Parameter로 받은 User의 주소를 보고, 이더리움상에 등록된 User의 Public Key를 불러옵니다.
   2. 불러온 User의 Public Key를 사용하여 암호화된 데이터를 복호화합니다.
   3. 복호화된 데이터를 토대로 internal transaction 확인합니다.
   4. internel transaction이 실행시킬 계약이 Gerritium 시스템에 등록된 것인지 확인 후 실행시킵니다.
   5. Plant가 해당 트랜잭션을 대신하여 실행하느라 얼만큼의 Gas를 소모했는지를 기록합니다.
   6. Plant는 모든 Plant가 소모한 총 Gas량 중 얼마나 기여했는지에 따라 Rietveldium을 분할 지급받으며 그 계산은 1일 기준으로 이루어집니다.




##### ③ 광물(Rietveldium)의 채굴 공식

(수식 추가 필요)

위의 트랜잭션처리과정에서 얻을 수 있는 광물인 Rietveldium은 화폐인 Gerritium을 만드는 재료로 사용됩니다. 따라서 Rietveldium의 수급이 전체 화폐 발행에 영향을 미칩니다.

- 총 가스 소모량이 기존 기록과 비교하여 많아졌다면 Rietveldium 채굴량 감소
- 총 가스 소모량이 기존 기록과 비교하여 적어졌다면 Rietveldium 채굴량 증가

[Plant Economy 참조](#Plant-Economy)



##### ④ 핵융합 재료(Gerritite)의 거래

커뮤니티의 구성원들로부터 기여에 대한 가치 평가의 보상으로 Gerritron을 수신했을 때, 이 Gerritron을 응축시키면 Gerritite라고 불리우는 고체 물질을 얻을 수 있습니다. 이 고체 물질은 Gerritium을 만드는 핵융합과정에서 재료로 사용되므로 Plant가 구매해갑니다.

$ price\ of\ gerritite = k \times  quality \times mass $

위 수식에서 Gerritite를 판매하는 기본 단위는 $quality \cdot mass$가 입니다. $k$는 Plant를 운영하는 사람이 정하는 가격에 해당하는 수치로 $Gerritium / quality \cdot mass$ 의 단위를 가지고 있습니다. 이에 따라 Gerritite 거래소에서는 Plant의 수요와 구성원들의 공급이 만나는 곳에서 $k$가 조절되며 시장가격을 형성하게 됩니다. 



##### ⑤ 핵융합 그리고 부산물

Plant 운영자는 Gerritium을 생산하는 핵융합을 진행할 수 있습니다. 다만, 이를 위해서는 

1. Rietveldium
2. Gerritite

![rietveldium fusion](https://s3.ap-northeast-2.amazonaws.com/my-publics/rietveldium+fusion.png)

두 가지가 필요합니다. 여기에서 Rietveldium은 Plant를 운영할 경우 Gas를 사용해 트랜잭션을 대신 처리해주고 얻게되는 보상입니다. 그리고 Gerritite는 Gerritite-Gerritium 마켓에서 구매할 수 있습니다.  

핵융합을 통해 발생한 산출물인 Gerritium은 Plant를 운영한 사람의 소유가 됩니다. 핵융합과정에서는 고에너지를 지닌 Gerritron입자가 튀어나가는데, 이것은 공간을 떠돌며 Light Gerritium을 다시 Gerritium으로 전환시키는 역할을 합니다.



##### ⑥ 핵분열과 부산물(Light Gerritium & Gerritron)

Gerritium을 보유하고 있다면, 간단하게 Gerritium을 핵분열시켜 Gerritron 입자를 얻어낼 수 있습니다.이 과정을 Gerritium Fission이라고 합니다. 

![Gerritium Fission](https://s3.ap-northeast-2.amazonaws.com/my-publics/gerritium+fission.png)

Gerritium Fission을 진행하면 Gerritium이 Light Gerritium 그리고 Gerritron으로 분열되는데, 산출물인 Light Gerritium 후술되는 Hyper Gerritron에 의한 자연핵융합으로 인해 시간이 지나면 다시 Gerritium으로 복원됩니다. Light Gerritium의 경우 따로 거래가 불가능하니 자산관점에서 보았을 때, Gerritium은 유동성을 잃었다 그 유동성을 시간에 따라 회복하는 과정을 거치게 됩니다.

Gerritron을 얻는 과정에서 맨 처음에는 Material Manager가 단 한개의 고유한 회전축으로 밖에 Gerritron을 추출하지 못합니다.  하지만 Material Manager가 다른 구성원으로부터 Gerritron을 수신한다면, 수신한 Gerritron의 회전축으로도 Gerritron을 추출할 수 있는 확률이 발생하게 됩니다. 따라서 다양한 회전축의 Gerritron을 많이 수신할 수록 수신한 Gerritron의 회전축의 Gerritron을 생성하는 확률이 점점 증가합니다. 



##### ⑦ 가치 평가

커뮤니티 구성원에게 Gerritron입자를 선물하는 것을 통해 기여에 대한 노고를 치하해줄 수 있습니다. Gerritron의 송 수신은 정해진 계약에 따라 진행됩니다. 예를 들어, User B가 프로젝트에서 문제를 발견하고 Issue를 등록했습니다. 그리고 커뮤니티의 구성원인 User A는 B가 발견한 Issue가 너무 중요하기 때문에, B에게 중요한 이슈를 발견해줘서 고맙다는 표시로 Gerritron을 3개를 송신하고, 해당 이슈에는 Gerritron 10개를 송신하였습니다. 그리고 User C는 해당 이슈를 풀어내는 Pull Request를 작성하여 User A가 예약을 걸어둔 10개의 Gerritron을 수신하였습니다.

위 사례는 가장 기본적인 가치평가 방법입니다. [코드 기여에 대한 보상](#코드-기여에-대한-보상의-설정)을 Gerritron 이외에도 설정할 수 있는데 이것에 대해서는 뒤에서 자세하게 다루도록 합니다.



##### ⑧ 핵융합 재료(Gerritite)의 제조와 품질

수신한 Gerritron을 사용하여 간단하게 '응축' 과정을 거치면 Gerritite를 만들어낼 수 있습니다. 다양한 회전축을 가진 Gerritron으로 Gerritite를 만들경우 그 퀄리티가 높아집니다.

Gerritite는 Gerritite를 구성하는 Gerritron들이 얼마나 다양한 회전축을 가지고 있는지에 따라 그 품질이 달라집니다. Gerritium으로부터 Gerritron을 추출할 때, Gerritron은 각각 고유한 회전축을 가지고 추출됩니다. 이것은 Material Manager마다 고유한 값을 가지고 있기 때문입니다. Gerritite를 구성하고 있는 Gerritron 입자들이 다양한 회전축을 가지고 있을 수록 핵융합 반응의 효율이 좋습니다. 그리하여 퀄리티는 다음과 같이 계산됩니다.

$quality = put\ a\ proper\ equation\ here$

Gerritium Fission 과정을 통해 Gerritron을 추출할 때 Gerritron의 회전각은 Material Manager의 고유 회전각과 그동안 수신한 Gerritron들의 회전각에 영향을 받는다고 하였습니다. 이것은 동일한 인물과 지속적으로 Gerritron을 이동시키는 행위를 할 경우 Gerritite의 품질이 감소하여 커뮤니티 기여를 어뷰징하는 것을 방지할 수 있도록 합니다. 또한 실제로 영향력 있는 사람의 경우 그동안 다양한 사람들에게 Gerritron을 받아왔으므로, Gerritron을 추출할 때 다양한 회전축으로 추출됩니다. 즉, 구성원의 기여를 영향력 있는 사람이 인정해주었을 경우 같은 양의 Gerritron이라도 그 가치가 더욱 상승하게 됩니다.



##### ⑨ 고에너지 입자에 의한 자연 핵융합과 Gerritium 복원

핵융합 부산물로 공간 중 떠도는 Hyper Gerritron은 다음과 같이 Light Gerritium들과 만나서 Gerritium으로 융합되고 이를 Light Gerritium Fusion이라고 합니다. 

![light gerritium fusion by hyper gerritron](https://s3.ap-northeast-2.amazonaws.com/my-publics/light+gerritium+fusion+by+hyper+gerritron.png)

Light Gerritium Fusion은 자연스럽게 이뤄지는 현상이며, 공간 내 Hyper Gerrition 농도인 pHG(potential of Hyper Gerritron)에 그 속도가 영향을 받습니다. 

$fusion\ rate\ per\ minute \propto pHG$



### Economy

Rietveldium 채굴 공식에 의하여 커뮤니티가 활성화될수록 Rietveldium 공급이 줄어듭니다.

- RIetveldium 공급이 줄어들면, 핵융합에 쌍으로 필요한 Gerritite에 대한 수요가 줄고 Gerritite 가격이 내려간다.
- Rietveldium 양이 줄었으므로 핵융합 반응 총량이 줄어들고 HyperGerritron 농도가 줄어든다.
- HyperGerritron 농도가 줄어들었으므로 LightGerritium->Gerritium 재 전환이 느려지고 이로 인해 Gerritron 추출 비용(Gerritium을 Light Gerritium으로 묶어놔야 하는 기회비용)이 높아진다.
- Gerritron 추출 비용이 높아지고 또 Gerritium 발행량이 줄어들었으므로 Gerritium의 유동성이 줄어든다.
- Gerritium의 유동성이 줄어듦으로 인해, 커뮤니티에 기여하는 충성도 높은 유저가 남고 충성도 낮은 유저는 떠난다. 이를 통해 커뮤니티의 질이 향상된다.
- Gerritium 유동성이 줄어들어 Gerritite 공급이 줄어들고, 다시 Gerritite 가격이 회복된다.

즉, Gerritite 가격이 안정되면서 커뮤니티의 퀄리티가 올라가게 됩니다.



또한 커뮤니티가 비활성화될수록 Rietveldium 공급이 늘어나는데, 

- Rietveldium 공급이 늘어나므로 Gerritite 수요가 많아지고 Gerritite 가격이 올라간다.
- Rietveldium 공급량이 늘었으므로 핵융합 반응 총량이 늘어나고 HyperGerritron 농도가 높아진다.
- HyperGerritron 농도가 높아졌으므로 LightGerritium->Gerritium 재전환이 빨라지고 이로 인해 Gerritron 추출 비용(Gerritium을 Light Gerritium으로 묶어놔야 하는 기회비용)이 낮아진다.
- Gerritron 추출 비용이 낮아지고 Gerritium 발행량이 늘었으므로 Gerritium의 유동성이 증가한다. (양적완화)
- Gerritium의 유동성이 증가하므로 커뮤니티에 신규유입되는 자본이 많아진다.
- Gerritite 가격이 비싸졌으므로 커뮤니티에서 활동하려는 사람이 늘어나고 Gerritron 추출비용이 낮아졌으므로 더 활발한 활동이 이루어진다. 
- 커뮤니티의 활동이 다시 활발해짐에 따라 Gerritite의 공급은 다시금 늘어나고 Gerritite의 가격은 안정세에 접어든다.

즉, 커뮤니티가 비활성화되었을 때에는 양적완화를 통해 커뮤니티를 활력있게 만들게 됩니다.



### Plant system의 기대효과

Plant 시스템을 사용하면, 다음과 같은 효과를 얻을 수 있습니다.

1. dapp을 구동할 때, 이더리움 노드를 지닐 필요가 없으며, HTTP 통신만 필요합니다.
2. 채굴을 통해 새로운 화폐를 발행하고 인센티브로 제공하는 시스템을 별도의 메인넷을 운영하지 않고도 구현할 수 있습니다. 따라서 이더리움 등의 견고한 블록체인 네트워크를 활용하는 것을 통해 블록체인 컨센서스 알고리즘에 대한 걱정을 덜 수 있습니다. 또한 멀티 플랫폼으로 확장하는 것이 가능합니다.
3. 새로운 화폐(Gerritium)가 발행되기 위해서는 이더리움 네트워크에 기여해야 하며 또한 커뮤니티에서의 가치평가가 접목되어야만 합니다. 따라서 이더리움 네트워크에 건전한 노드를 많이 참여할 수 있도록 독려하므로 이더리움 전체 생태계에 좋은 영향을 끼칩니다.



## Business Plan

### Entities

Commitground플랫폼은 Commitground Foundation이 참가자들과 함께 만들어나가는 모두의 것입니다. 여기에 Commitplay, inc.는 Commitground platform의 개발을 주도하고 기술적인 지원을 하는 회사입니다. Commitground Foundation과 Commitplay, inc.가 앞으로 어떻게 운영될 것인지는 다음과 같습니다.



#### Commitground Foundation

##### 역할

1. 기술 개발 방향에 대한 의결
2. dapp 투자
   - 재단이 보유한 Gerritium을 사용하여 dapp에 투자하고 투자금 회수
   - 회수한 투자 이익은 플랫폼 운영에 재투입

##### 구성

1. 기술위원회
2. 자문위원회
3. 기술 사용 지원 및 홍보팀
4. 투자팀

##### 토큰 발행 계획

1. 토큰 발행 구성

![Token allocation](https://s3.ap-northeast-2.amazonaws.com/my-publics/gerritium-token-allocation.png)

2. 향후 예측

   향후 예측은 1. 얼마나 많은 IT industry가 블록체인 기반의 서비스로 대체될 것인가, 그리고 2. 그 중 얼마나 많은 프로젝트가 우리 플랫폼을 사용하여 개발될 것인가에 따라 달라집니다. 전체 Gerritium Project Token들의 시가총액이 Gerritium의 총 가치를 나타낸다는 가정 하에 다음과 같은 시나리오를 예상해볼 수 있습니다(2016, 2017년 [자료](https://en.wikipedia.org/wiki/List_of_largest_Internet_companies)에 의하면, 전세계 인터넷 회사들의 상위 25개 기업의 총 시가 총액의 합은 약 3813조 원이었습니다.)

   - 기대하는 시나리오

     1. 블록체인 생태계가 현재 인터넷 기업의 10%를 대체하는 경우

     2. 블록체인 생태계에서 개발되는 프로젝트의 10%가 커밋그라운드 플랫폼을 사용해 개발되는 경우

        기대 시가 총액: 약 38조 원

   - 최상의 시나리오

     1. 블록체인 생태계가 현재 인터넷 기업의 20%를 대체하는 경우

     2. 블록체인 생태계에서 개발되는 프로젝트의 50%가 커밋그라운드 플랫폼을 사용해 개발되는 경우

        기대 시가 총액: 약 381조 원

   - 최악의 시나리오

     1. 블록체인 생태계가 현재 인터넷 기업의 1%를 대체하는 경우

     2. 블록체인 생태계에서 개발되는 프로젝트의 1%가 커밋그라운드 플랫폼을 사용해 개발되는 경우

        기대 시가 총액: 약 3813 억 원

3. 토큰 세일 전략

   1. 토큰의 최대 발행량: 1,000,000,000 개 (mining을 통해 모두 발행될 경우 재단에서 재조정)
   2. 초기 토큰 발행 모델: Exponential 
   3. 가격 증가 비율: 1.0000000206
   4. 시작 Valuation: $10M
   5. 종료 Valuation: $3.8 B

   ![Token Pricing](https://s3.ap-northeast-2.amazonaws.com/my-publics/commitground-token-pricing.png)

#### Commitplay, inc.

##### 역할

1. 기술개발 주도(Seed)
   - Gerritium, GPT 개발
   - 기술개발 주도 대가로 Gerritium ICO에서 pre-allocation을 받는다.
2. 서비스 비즈니스(Series A)
   - commitground platform을 개발,서비스한다.
   - commitground는 다음을 유료로 제공한다 (오픈소스는 무료 제공)
     - 저장소 서비스
     - 빌드/테스트/배포 툴 서비스
     - Audit as a Service
3. dapp company builder(Series B)
  - commitground는 dapp project를 개발할 수 있는 플랫폼이므로 우리 플랫폼을 사용하여 dapp을 개발할 수 있도록 dapp company builder로 사업을 확장한다. 이 경우 dapp 개발 투자 수익과 더불어 플랫폼을 활성화 시킬 수 있는 효과를 가지게 된다.
  - pre allocation 받은 Gerritium ICO를 사용하여 다음과 같이 운영한다
    - 엔지니어 고용
    - GPT project를 진행하도록 하여 프로젝트를 완성. 필요할 경우 Gerritium도 투자.
    - ICO를 진행시키고 투자 자금을 회수한다.
  - 블록체인 엔지니어 교육 선도
4. dapp 기술 개발 선도
   - dapp 개발에 필요한 주요 라이브러리들을 오픈소스로 개발할 수 있도록 연구팀을 확보하고 개발하도록 하여 오픈소스 생태계가 commitground 상에서 더욱 커질 수 있도록 한다.

##### 구성

1. 연구팀 (기술 개발 주도 팀)
2. 서비스팀 (비즈니스하는 팀)
   - 개발팀
   - 지원팀
   - 세일즈팀
3. company building 팀

##### 투자 유치 계획

1. 시드 펀딩
   - 규모: 약 \$300k ~\$500k  (한/미 VC)
   - 목적: 코어 기술 개발 및 SF 팀 세팅
2. Series A
   - 규모: 시드 이후 결정
   - 목적: commitground 플랫폼 개발 비용 조달 및 서비스 런칭
   - 기타: SF+Seoul(혹은 대전) 운영 / Commitground Foundation에서 ICO 이후 지분 투자에 직접 참여
3. Series B
   - 규모: Series A 및 서비스 런칭 이후 결정
   - 목적:
     - dapp company building 사업(dapp 팀 1년에 10~20개 배출하는 것 등을 목표로)
     - 연구소 설립 및 운영



### Business Timeline

|         | Foundation's Milestones               | Company's Milestones                    |
| ------- | ------------------------------------- | --------------------------------------- |
| ~ 18.6  |                                       | 팀 빌딩 & 시드 펀딩                     |
|         | 설립 및 주요 인사 구성                | 코어 기술 개발                          |
| ~ 18.9  | 토큰 발행 & ICO                       | Pre-allocation 할당                     |
| ~ 18.12 |                                       | Series A 유치                           |
| ~ 19.03 |                                       | commitground와 dappground 베타 런칭     |
| ~ 19.06 | 재단 실무팀(기술 지원팀, 투자 팀)구성 | commitground와 dappground 정식 런칭     |
|         | 재단 본격 운영                        | Series B 유치(foundation에서 leading)   |
| ~ 19.09 |                                       | 연구소 & dapp company builder 본격 가동 |
|         |                                       |                                         |
|         |                                       |                                         |



[^1]: Commitground에서 기여활동을 가치로 측정하는 주요 방법은 Gerrit Code Review에서 크게 영감을 얻었다. Gerrit Code Review는 Rietveld 프로젝트의 fork 프로젝트로, Commitground에 등장하는 주요 명칭인 Gerritron, Gerritium, Rietveldium은 이에 대한 오마주로 작성되었다.

