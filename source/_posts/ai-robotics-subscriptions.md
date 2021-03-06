---
title: 내가 최신 딥러닝 / 로보틱스 뉴스를 따라잡는 방법
date: 2020-08-30 14:17:44
author: Hyunggi Chang
tags:
  - Hyunggi Chang
  - AI
  - 딥러닝
  - 로보틱스
  - YouTube
  - News
---

## 0. 커뮤니티에 기대서 뉴스를 보던 때는...

AI 와 Robotics 뉴스는 매일같이 쏟아져 나온다. 나는 내가 뉴스를 받아보기 위해 종종 내가 관심있는 연구 그룹의 블로그에 들어가서 뉴스를 확인하곤 했다.

그런데 어떤 때는 내가 직접 찾아보기 전에 페이스북 TensorFlow KR이나 AI Korea 등의 커뮤니티를 통해 뉴스를 접하기도 한다. 이 두 커뮤니티에는 빠르게 뉴스를 전달해서 인지도를 높이시는 분들도 계시고, 심지어 관리자가 만든 뉴스 봇도 있다 (추정). 페이스북을 통해서 뉴스를 받아보는것에 익숙해지다보니, 점차 뉴스를 보기 위해 페이스북에 접속하게 되었다.

그러다가 느낀 것이 있다. 커뮤니티를 통해서 새로운 정보를 빠르게 접하는 것은 좋았다. 하지만 남들이 골라주는 뉴스만 보다보니, 내가 정말로 보고싶은 나의 취향의 뉴스와 소식을 받을 수 없게 된 것이다. 페이스북에서 SLAM에 대한 뉴스는 잘 나오지도 않는다. 한창 컴퓨터 비전과 SLAM에 관심을 가지고 있었는데, AI 정보에 치우쳐진 페이스북 뉴스를 통해서 파이썬도 배우지 않은 상태로 CNN과 RNN의 기초를 이해하게 되었고, YOLO와 Faster-RCNN의 차이도 알게 되었다. AI 분야의 뉴스를 아는게 잘못된건 아니지만, 내가 당시 집중해야할 것은 기존의 컴퓨터 비전과 SLAM 이였다.

이렇게 자꾸 물들어 갈 수는 없었다. 내가 보고싶은 뉴스는 내가 골라서 봐야했다.

이번 주제로 2개의 글을 쓸 것 같다. 하나는 AI 뉴스를 보는 방법, 하나는 SLAM 뉴스를 보는 방법이 될 것 같다. 이번 글은 우선 AI 뉴스를 보는 방법에 대해 설명하고, 다음 글에서 SLAM 뉴스를 보는 방법을 적을 것이다.

[내가 최신 SLAM 뉴스를 따라잡는 방법 글 링크](https://cv-learn.com/SLAM-cadf848aa80f4a3bbd291247fb44c209)

## 1. 첫번째 방법: Feedly 앱

첫번째 방법은 아이패드에서 사용하는 Feedly 앱이다. 이 앱을 통해 여러 뉴스 웹사이트와 블로그 RSS 피드를 가져와서 한 앱에서 한눈에 쉽게 볼 수 있다. 이러한 방식의 장점은, 구글에서 내가 기억하는 랩실의 이름을을 하나씩 기억하고 찾는 것 보다, 아이패드에서 앱을 한번 누르는 것만으로 쉽게 많은 정보를 빠르게 접할 수 있기 때문이다 (정보를 얻는데에 들어가는 수고를 덜어준다).

또 다른 좋은 점은 기사 / 블로그 글의 썸네일까지 함께 제공하기 때문에, 시각적으로도 좀 더 끌리는 것 같다.

![Feedly-AI-subscriptions 1](./ai-robotics-subscriptions/feedly1.png)
![Feedly-AI-subscriptions 2](./ai-robotics-subscriptions/feedly2.png)

Arxiv는 끊었다. 너무 논문 업데이트가 많다.
내가 보고싶어하는 저자의 논문만 보는 방법은 없을까?

AI 관련으로는 가장 SOTA를 많이 뽑아내는 Google AI Blog, OpenAI, BAIR, Nvidia, FAIR, DeepMind, Microsoft Research, Fast.ai와 몇가지 상업적인 AI 뉴스를 구독했다. 아직 AI 분야는 내가 핸즈온으로 도전하고 있지 않았기 때문에, 논문보다는 기사 제목만 훑는 것 만으로 어느정도 연구 트렌드 변화와 산업 변화를 확인할 수 있다.

최신 논문을 빨리 훑어보려고 Arxiv 피드도 구독했었다. 그러나 지금은 구독 취소를 했는데, 매일 내 분야도 아닌 논문이 300개씩 추가가 되서이다.

Robotics 분야의 뉴스는 사실 특정 기술의 내용보다는 제품군이 좀 더 많이 나오는 것 같다. 그나마 조금 깊게 들어가는 IEEE Spectrum을 보는게 조금 좋은 것 같다. 단순히 로보틱스 뿐만이 아니라 주변 기술 (automation, energy) 등등 피드도 구독해놨다.

기본적으로 나는 이런 피드들을 읽을 때 모든 글을 읽겠다는 생각은 하고있지 않다. 나는 내가 구독한 소스의 수가 많다고 생각하고 있고, 또 너무 많은 정보를 소화하려고 하다보면 정보의 바다에 휩쓸리기 쉽고, 개인 스케줄 등으로 혹시나 딜레이가 생기게 될 경우 스트레스를 받는 편이다.

실제로 사용할 때는 아래처럼 보인다. 썸네일이 안보이는 이유는 아마 로딩중이라서 그런 것 같다. 아침에 출근하면서 지하철에서 글 하나, 점심시간에 하나, 퇴근하면서 하나 정도 보면 딱 괜찮은 것 같다.

![Feedly 메인 화면](./ai-robotics-subscriptions/feedly3.png)

## 2. Paperswithcode

![Papers with code](./ai-robotics-subscriptions/papers_with_code.png)

딥러닝을 업으로 삼으신 지인으로부터, SOTA 랭킹에 대해 알고싶다면 Paperswithcode를 보라고 추천을 받았다.

종종 논문 검색을 위해 이 페이지를 이용했지만, 아직 딥러닝에 대한 지식이 부족해서 애용하는 정도는 아니다. 그래도 가끔 들어가서 현재 SOTA가 무엇인지 확인하고, 딥러닝을 업으로 삼으시는 분들과 이야기 할 때 도움이 된다.

최근에는 task의 범위가 넓어지면서, 은근히 non-딥러닝 방식도 올라온 것 같다. 하지만 non-딥러닝 방식의 연구자 분들은 이 웹사이트를 잘 안 쓰시는 것 같다.

한동안 Detection 분야에서 TridentNet 아키텍처를 사용한 기술이 SOTA 였을 때, Detection task로 어려워하시는 분께 아무것도 모르고 'TridentNet이 SOTA래요~ 성능이 제일 좋대요~' 라고 말했다가 괜히 그분만 TridentNet 구현을 위해 고생하신 것도 기억난다 ㅋㅋ 그 후로는 함부로 랭킹만 믿지 않게 되었다.

[Papers With Code : the latest in machine learning 링크](https://paperswithcode.com)

## 3. YouTube

Paperswithcode는 어떤 기술이 가장 좋은 벤치마크를 내는지 알 수 있지만, 사실 이러한 벤치마크 정보는 이미 해당 분야를 업으로 삼으신 분들께 도움이 되는 것 같다.

아직 나처럼 딥러닝 꼬꼬마는 YouTube 영상들을 통해서 눈으로 보고 흥미를 느끼는게 좀 더 도움이 될 것이라고 생각한다.

### 3.1 Two Minute Paper

Two Minute Paper는 딥러닝이 적용되는 다양한 분야의 기술들을 짧게 설명해준다. 오전에 지하철 타고 출근하면서 보기 딱 좋은 채널이다. 다루는 분야가 상당히 많은데, 기존의 detection / segmentation과 같은 컴퓨터 비전, BERT, GPT-3 같은 NLP 분야, 강화학습 분야...를 넘어서 종종 물리학 시뮬레이션과 그래픽스, 모션 추정 등 다양한 분야를 섭렵하는게 넓고 얕은 지식을 쌓기에 좋다.

![Two Minute Paper 채널 화면](./ai-robotics-subscriptions/two_minutes_paper.png)

### 3.2 Karol Majek

Karol Majek 채널은 실제로 컴퓨터 비전 분야의 detection / segmentation / feature extraction 코드를 돌리면서 나오는 결과를 보여준다. 이런 영상이 좋은 이유는, 논문들의 홍보 영상들을 보다보면 항상 좋은 결과만 나오기 때문이다. 이런 영상들 중, 어떤 기술이 실제로 좋고 어떤 영상이 cherry pick인지 알 수 없는데, Majek의 영상들을 보면 각각의 딥러닝 모델들의 실제 퍼포먼스가 어느정도 되는지 알 수 있다.

![Karol Majek 채널 화면](./ai-robotics-subscriptions/karol_majek.png)

### 3.3 Lex Fridman

기술 자체를 파고들기보다 여러 기술분야의 전문가들을 데려와서 팟캐스트 인터뷰를 진행한다. 이전에 Elon Musk가 나왔을 때 부터 봤는데, 얼마 지나지 않아 George Hotz가 나오는 것을 보고 완전 팬이 되었다. 이 둘은 사이도 좋지 않고 기술적으로도 경쟁하는 관계라고 들었는데, 그만큼 Lex는 중립을 지키면서 팟캐스트를 운영한다는 것을 보여주는 것 같다.

자주 나오는 질문 중에 '우리가 지금 살아가는 이 세상이, 사실 시뮬레이션 일 것 같은가?' 라는 질문이 있다. 처음엔 이게 무슨 공상과학 질문인가 싶었는데, 은근히 여러 전문가들마다 색다른 견해를 보여주는게 재밌다.

단점이라면 너무 길어서 일주일동안 한 영상을 쪼개봐야한다.

그리고 Lex가 생각보다 기타를 잘 친다.

![Lex Fridman 채널 화면](./ai-robotics-subscriptions/lex_fridman.png)

### 3.4 Yannic Kilcher

내가 제일 약한 NLP 분야의 기술과 메타러닝 분야를 잘 설명해주는 유투버이다. 설명하는데에 도가 튼 것 같다. 사실 아직 딥러닝의 기초도 탄탄히 잡은 편도 아니고, NLP에는 아직 흥미가 가지 않기 때문에 자주 찾아보지는 않는다. 다만, DETR이라던지, DELF 와 같이 Attention이 컴퓨터 비전에 적용이 되는 것을 보고 Attention을 이해하기 위해 이 채널을 찾게 되었는데, 기술에 대한 설명을 정말로 깔끔하게 하는 것을 보고 이 채널에 대해 좋은 인상을 가지고 있다.

![Yannic Kilcher 채널 화면](./ai-robotics-subscriptions/yannic_kilcher.png)

### 3.5 Henry AI Labs

Two Minute Paper와 비슷한 느낌의 채널이다. 채널의 OpenAI와 Facebook의 연구를 특히 좋아하는 것 같은데, 평소에 나오는 영상들은 사실 내 취향은 아니다. 하지만 학회가 진행될 때 마다 특정 기업의 연구 결과와 트렌드를 한번에 정리해주는게 굉장히 도움이 많이 된다.

![Henry AI Labs 화면](./ai-robotics-subscriptions/henry_ai_lab.png)

### 3.7 Gadget Seoul

드디어 처음으로 나오는 한국인 채널 ㅋㅋ

가젯서울 채널은 정확히 이야기하면 딥러닝 채널은 아니다. 반도체, 배터리, 데이터센터 관련된 뉴스가 주를 이루는데, 지난 1년간 엔비디아가 만들어내는 뉴스, 인텔의 자율주행 뉴스 등등으로 인해 딥러닝 프로세서 기업들의 트렌드를 알기 굉장히 좋다. 종종 가젯서울 채널주의 의견과 인사이트가 영상을 통해 공유되는데, 반도체 시장에 대한 굉장히 깊은 이해를 통해 오는 인사이트라고 느껴지고, 개인적으로 이정도 급의 인사이트를 무료로 들을 수 있다는 것에 대해 감사하게 생각한다.

이 채널을 통해 최근 ARM 인수에 대해 Nvidia의 행보에 대해서 지속적으로 보고 있는 편.

![Gadget Seoul 채널 화면](./ai-robotics-subscriptions/gadget_seoul.png)

### 3.8 ML Explained - AI Socrates

이 아래부터는 아직 보고 있지 않은 채널들에 대해 소개한다.

최근 웨비나를 진행하고 녹화를 하는 채널인 것 같은데, 제목들이 심상치 않다.

![ML Explained - AI Socrates 채널 화면](./ai-robotics-subscriptions/ml_explained.png)

### 3.9 FAIR Vision

갓 3-4일전 만들어진 FAIR Vision의 유투브 채널.

![FAIR Vision 채널 화면](./ai-robotics-subscriptions/fair_vision.png)

### 3.10 딥러닝 논문읽기 모임 + PR12

그리고 국내에서 유명한 두 딥러닝 논문 읽기 채널들이다. PR12는 워낙 유명해서 말할 것도 없고, 딥러닝 논문 읽기 모임도 업로드한 영상이 많이 쌓이면서 인지도가 많이 쌓이고 있다.

![딥러닝 논문 읽기 모음 채널 화면](./ai-robotics-subscriptions/dl_reading.png)
![PR12 재생목록 화면](./ai-robotics-subscriptions/pr12.png)
