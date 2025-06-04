---
layout: single
title: "딥러닝 첫 시작"
date: 2025-06-04
categories: [프로젝트]
tags: [딥러닝, MS AI School]
header:
  overlay_image: /assets/images/aischool.jpg
  teaser: /assets/images/aischool.jpg
  caption: "AI school 로고"
---

<style>
/* ─── 썸네일 크기 조절 ───────────────────────────── */
.page__hero--overlay {
  height: 200px !important;           /* 원하는 높이(px)로 조절 */
  background-size: contain !important;/* 이미지 비율 유지하면서 축소 */
  background-position: center center;
}
</style>

---

# 백엔드 마무리, 딥러닝 모델 개발

백엔드 작업이 드디어 마무리 됐습니다. 제가 급하게 맡았던 작업은 Azure에 모델을 배포한 후 엔드포인트를 코드와 연결하는 작업을 맡았어요.
그리고 그 코드에서 자동으로 DB 컬럼들과 매핑해서 DB에 모델 출력값을 저장하는 파이프라인 로직을 작성했어요. 전적으로 GPT한테 의지를 많이 했지만요..
생각해보니 GPT가 없었다면 과연 수작업으로 코딩을 할 수 있었을지 감이 안잡힙니다.

자 아무튼 오늘부터는 백엔드 작업은 마무리단계이니 담당 팀원분들께 맡기고 딥러닝 개발과 틈나면 모델 파라미터 수정으로 성능개선 작업을 하려고 해요.

---

# 포트폴리오에서 AI엔지니어/연구원의 느낌의 어필을 하려면.

AI 엔지니어나 AI 연구원 포지션을 지향한다면, 다음과 같은 작업이 함께 들어가야 더 자연스럽다고 해요.

> 범주 대표 요소는 대충 이렇습니다.

**_DNN 설계 CNN, RNN, Transformer 구조 정의
딥러닝 프레임워크 PyTorch, TensorFlow(실제 현장에선 사용 잘 안함) 직접 사용
실험 코드화 학습 loop, loss function, optimizer 구성 직접 구현
MLOps 모델 저장, 배포, API화 (FastAPI, Azure ML 등)
RAG 등 응용 GPT + 벡터 DB 조합, 대화형 응답 생성
학습 구조의 이유 설명 왜 이 아키텍처를 썼는지 이론적 근거 제시_**

이 중 저는 DNN 설계와 PyTorch 전문가 수준까지 가는 게 현재 목표입니다.

---

# 마무리

프로젝트 진행시간동안 pytorch 입문자 수준만 공부 했습니다. 이제 나머지 공부하고 자러 가야겠어요.
다음 글에서 또 뵙겠습니다.
