---
title: 리팩터링 2판 - 리팩터링 원칙
date: 2020-11-20 20:10:02
author: Hyunseok Jeong
tags:
  - Hyunseok Jeong
  - Martin Fowler
  - Refactoring
  - Principles
---

![Photo by Marc Edgar Chaparro on Unsplash](./principles-in-refactoring/edgar-chaparro-r6mBXuHnxBk-unsplash.jpg)

리팩터링(2판)의 구성은 1-5장의 개론과 설명, 6-12장의 실제 기법 설명으로 이루어져 있다.
그 중 4장은 테스트에 관한 내용인데, 물론 리팩터링과 밀접한 주제이긴 하지만 여기서는 연관성과 간략한 소개만 있으며, 5장은 6장부터 12장을 보는 방법에 대한 안내이다.
리팩터링의 전반적 개요를 다룬 2장 리팩터링 원칙을 정리하여 공유한다.

## 리팩터링이란

리팩터링은 외부에서 보이는 `겉보기 동작(observable behavior)`은 그대로 유지하되,
코드를 이해하고 수정하기 쉽게 내부의 구조를 변경하는 것이다. 즉, 설계 변경이다.

새 집으로 이사를 와서 가구와 전자제품을 적당히 편리하다 싶은 곳에 두고 살아가면서
점차 가장 적합하다 싶은 위치로 재배치를 한다고 할까? 아무리 고심해서 결정한다 하여도
살아보기 전에는 최적의 배치를 알 수 없는 것이다. 심지어는 그때는 맞았는데 시간이 흐르며 바뀌는 것도 있다.

특정한 방식으로 코드를 정리하는 것만이 리팩터링이다. 겉보기 동작에 변화가 없는 작은 단계들을 거쳐서 완성하는데,
그렇기에 언제든 중간 단계에서 멈출 수 있다.

코드 정리 및 구조 변경은 `재구성(restructuring)` 이며, 리팩터링은 재구성의 특수한 한 형태이다.
사실 이 책을 읽기 전에는 재구성을 리팩터링이라 오해하고 있었다.

겉보기 동작에 변화가 없다는 점에 리팩터링과 성능 최적화는 같다고 볼 수 있지만 그 목표는 다르다.

- 리팩터링: 겉보기 동작 변화없음. 목표는 이해와 수정이 쉬운 코드
- 성능 최적화; 겉보기 동작 변화없음. 목표는 속도 개선

## 두 개의 모자

켄트 벡의 비유인데 기능을 추가하는 것과 리팩터링을 하는 것은 엄격히 구분하라는 것이다. 둘을 섞어서 하다가는 탈이 나고 만다.
기능 추가할 때는 기능 추가 모자를 쓰고, 기능 추가만 한다. 리팩터링을 할 때는 리팩터링 모자를 쓰고, 리팩터링만 한다.

## 리팩터링을 왜 하나요?

```text
"난 뛰어난 프로그래머가 아니에요. 단지 뛰어난 습관을 지닌 괜찮은 프로그래머일 뿐이에요." 83p, 켄트 벡
```

1. 소프트웨어 아키텍처가 좋아진다
2. 소프트웨어를 이해하기 쉬워진다.
3. 버그를 쉽게 찾을 수 있다.

이와 같은 이유로, 프로그래밍 속도가 빨라진다.

마틴 파울러는 `설계 지구력 가설(Design Stamina Hypothesis)` 이라는 표현을 썼는데
리팩터링을 잘 해두어서 `설계가 잘 되어 있고`, `이해하기 쉬우며`, `버그도 찾기 쉬운 코드`에서는
코드에 기능을 추가하거나, 유지 보수하는 속도가 결코 느려지지 않는다는 것이다.

![design stamina hypothesis](./principles-in-refactoring/designStaminaGraph.png)

프로젝트 초기에 아무리 세심하고 치밀하게 설계를 해도 코딩을 시작하면 그때부터 디자인은 점차 망가지게 마련이다.
리팩터링을 한다는 것은 설계를 지속적으로 개선한다는 것이다. 그 덕분에 시간이 지나도 생산성이 떨어지지 않게 되는 것이다.

## 리팩터링은 언제 해야 할까?

책에서는 다양한 기준으로 리팩터링의 시점을 이야기하고 있다.

### 세 번 반복하면 리팩터링 - 돈 로버츠(Don Roberts)

1. 그냥 코딩하다가
2. 중복 작업을 인식하면 일단은 그냥 코딩한다.
3. 하지만, 비슷한 작업을 세 번째 하게 되면 리팩터링을 할 때이다.

### 준비를 위한 리팩터링(Preparatory Refactoring) - 기능을 쉽게 추가할 수 있다.

현재 구조를 살펴보고 구조를 다듬어서 새로운 기능을 적용하기 좋게 만들어주자.
버그를 잡을때도 좋다. 버그를 한 군데로 모아서 리팩터링하는 것이다.

### 이해를 위한 리팩터링(Comprehension Refactoring)

수정을 하려면 이해를 해야한다.
이해를 한 다음 간단하게 변수, 함수의 이름을 바꾸는 것 만으로도 전체 설계가 눈에 들어오기 시작한다.
이해한 것을 코드 속에 녹여내야 한다. 그래야 다음에 코드를 들여다 볼때 또다시 이해를 해야하는 과정을 뛰어넘을 수 있다.

### 쓰레기 줍기 리팩터링(Litter-Pickup Refactoring)

코드 분석중 원래 하려던 일과 다른 문제들, 비유하자면 쓰레기들을 발견하였다면?
당장 할 수 있는 것들을 조금이라도 해두고, 나머지는 메모를 해둔 다음에 하던 일로 돌아간다.
리팩터링은 작은 단계들로 이루어지고, 각각의 단계는 전체 코드를 깨뜨리지 않는다는 것을 기억하자.
작은 단계라도 할 수 있는 단계만큼 해두는 것이다.

### 계획된 리팩터링과 수시로 하는 리팩터링

```text
"보기 싫은 코드를 발견하면 리팩터링하자. 그런데 잘 작성된 코드 역시 수많은 리팩터링을 거쳐야 한다." 88p
"무언가 수정하려 할 때는 먼저 수정하기 쉽게 정돈하고(단, 만만치 않을 수 있다) 그런 다음 수정하자." - 켄트 벡. 88p
"리팩터링 작업 대부분은 드러나지 않게, 기회가 될 때마다 해야 한다." 89p
```

앞서 언급한 준비를 위한, 이해를 위한, 쓰레기 줍기 리팩터링은 기회가 될때에 하는 것이다.
(때로는 필요할 수 있지만) 리팩터링이란 계획적으로 하는게 아니다.

### 오래 걸리는 리팩터링

```text
"팀 전체가 리팩터링에 매달리는 데는 회의적이다." 89p, 마틴 파울러
```

일부러 시간을 내서 하지 말고, 리팩터링 해야할 코드를 만날 때 마다, 리팩터링 하자.

### 코드 리뷰에 리팩터링 활용하기

코드를 보고 떠오르는 걸 개선안을 제시하지 말고 리팩터링을 하면 어떻게 될까 생각하거나, 실제로 해보자
작성자 없이 pull request 하는 것은 효과적이지 않다. 작성자와 함께 앉아 코드를 훑어가면서 리팩터링 하자(pair programming)

### 관리자에게는 뭐라고 말해야 할까?

필요성을 아는 관리자라면 리팩터링을 권장할 것이며, 팀원의 리팩터링 역량이 충분한지 수시로 살펴볼 것이다.
필요성을 모르는 관리자라면 말하지 말자. 내가 필요성을 알고, 그 덕분에 더 빠르게 개발할 수 있다는 것을 알면 `책임있게`, `프로답게`, 리팩터링을 하는 것이다.

### 리팩터링하지 말아야 할 때

굳이 수정할 필요 없다면 하지 말자. 외부 API 또는 그와 유사하게 호출하여 쓰는 코드라면 그냥 두자. 충분히 내부동작을 이해해야 할 시점에 리팩터링을 하면 된다.

## 리팩터링 시 고려할 문제

발생할 수 있는 문제에 대한 고려도 해야 한다.

### 새 기능 개발 속도가 저하된다고?

```text
"리팩터링의 궁극적인 목적은 개발 속도를 높여서, 더 적은 노력으로 더 많은 가치를 창출하는 것이다." 92p
```

당장 보아서는 속도가 느려지는 것 같지만, 애초에 리팩터링의 목표중 하나는 개발 속도를 높이는 것이다.
리팩터링은 `도덕적`, `미학적` 이유로 하는 것이 아니다. `경제적`인 이유로 하는 것이다.

### 코드 소유권

다른 팀원, 또는 나아가 외부로 공개된 코드는 변경하기가 쉽지 않다.
그래도 최소한 팀 단위의 소유권을 가지도록 하여(=좀 더 자유롭고 넓은 코드 수정권한을 주어서) 관리의 책임은 나누되 수정은 자유롭게 해주자. 단, 이것은 마틴 파울러의 의견이다.

### 브랜치

브랜치로 나누어서 작업하는 경우 머지(브랜치를 master로 합치기), 또는 통합(수시로 master를 브랜치로 합치기)을 할 수 있다.
마틴 파울러는 매우 짧게 통합하기를 주장한다. 2-3일 보다도 짧게 CI(Continuous Integration) 또는 TBD(Truck-Based Development) 하자고 한다. 다만 master 브랜치를 건강하게 유지하려면, 개발중인 기능은 flag를 이용하여 disable 을 시켜두도록 한다.

무엇보다 CI와 리팩터링은 궁합이 좋다. 켄트 백이 `익스트림 프로그래밍(eXtreme Programming)`을 만든 이유이다.

### 테스팅

리팩터링의 대표적 특징은 겉보기 동작이 똑같이 유지된다는 것이다.
절차에 따라서 하면 단계별 변경이 작다. 테스트를 그 단계별로 매번 하면 된다. 테스트 코드가 필요한 이유이다.
믿을 수 있는 `자동 리팩터링`만 쓰자는 사람들도 있으니 참고하자.

### 레거시 코드

어마무시한, 손도 대기 싫은 레거시 코드를 만져야 한다면?

1. 테스트를 보강한다.
2. 조금씩이라도 더 개선하려고 노력한다.
3. 자주보는 곳을 더 개선한다. 더 잘 이해하게 되는 곳이고, 더 중요한 곳일 가능성이 높다.

### 데이터베이스

데이터베이스도 리팩터링 할 수 있다.
변환 수행토드 작성후, VCS에 저장한 다음 마이그레이션 스크립트를 실행한다.
가능한 여러단계로 나누어서 한다. 프로덕션 환경에서 문제 생겼을때 되돌리기 쉽기 때문이다.

## 리팩터링, 아키텍처, 애그니(YAGNI)

먼저 충분히 고려하는 것과, 나중에 개선하는 것 중에서 어느게 나을까?

```text
"나는 나중에 문제를 더 깊이 이해하게 됐을 때 처리하는 쪽이 훨씬 낫다고 생각하는 편이다." 101p, 마틴 파울러
```

이 부분은 현업에서 느끼고는 했었는데 많은 공감이 되었다.

당장 필요한 기능만 구현하자. 대신 제대로, 멋지게, 정성스럽게 구현하자.
불확실한 미래에 대한 대비보다는 당장 눈앞의 기능을 잘 구현하자는 것이다.  
개발을 해나가며 요구사항을 더 잘 이해하게 되면 리팩터링을 하면서 더 개선하자.

```text
- You Aren't Going to Need It.
- Simple design
- Incremental design
```

## 리팩터링과 소프트웨어 개발 프로세스

```text
"자가 테스트 코드, 지속적 통합, 리팩터링이라는 세 기법은 서로 강력한 상승효과를 발휘한다." 102p
```

Test-Driven Development = 자가 테스트 코드(self-testing code) + 리팩터링
단계별로 리팩터링을 하면서, 사이사이마다 테스트를 통해 겉보기 동작이 변함 없는지 확인하는 것이다.

## 리팩터링과 성능

```text
"나는 실제로 소프트웨어를 이해하기 쉽게 만들기 위해 속도가 느려지는 방향으로 수정하는 경우가 많다." 103p
"하드 리얼타임(hard real-time) 시스템을 제외한 소프트웨어를 빠르게 만드는 비결은, 먼저 튜닝하기 쉽게 만들고 나서 원하는 속도가 나게끔 튜닝하는 것이다." 103p
```

성능 개선의 세 방법은 다음과 같은데 3번으로 가자.

1. 시간예산 분배(time budgeting): 하드 리얼타임 시스템에서 많이 사용. 자원을 최적으로 할당함
2. 끊임없이 관심 기울이기: 성능 개선에만 신경쓰면 코드가 점점더 알아먹기 어렵게 되고, 컴파일러, 런타임, 하드웨어 동작을 충분히 이해하지 못한 코드가 된다.
3. 일단은 코드를 다루기 쉽게 만드는데 집중하자. 때가 되면 각을 잡고 성능 최적화를 하는 것이다.

- 프로파일러로 분석하여 시간, 공간을 잡아먹는 지점을 알아낸다. 짬밥과 직관으로 하는 것이 아니다.
- 알아낸, 개선할 수 있는 작은 부분들을 개선한다. 적은 노력으로 큰 효과를 얻을 수 있다.

```text
"시스템에 대해 잘 알더라도 섣불리 추측하지 말고 성능을 측정해봐야 한다.(profiling)" 105p
"성능에 대한 흥미로운 사실은, 대부분 프로그램은 전체 코드 중 극히 일부에서 대부분의 시간을 소비한다는 것이다." 105p
```

이와 같이 하면

- 성능 개선에 투입하는 시간 최적화
- 리팩터링 잘 되어 있으니 세밀하게 분석하기 쉽고, 프로파일러가 지적하는 성능문제 범위가 좁아진다.
- 당장의 리팩터링은 성능을 저하시키지만, 나중에 튜닝하기 훨씬 좋아진다
