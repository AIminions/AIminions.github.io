---
layout: single
title: "AI-102 자격증"
date: 2025-05-06
categories: [AI]
tags: [Azure 자격증]
header:
  overlay_image: /assets/images/ai-102.png
  teaser: /assets/images/ai-102.png
  caption: "Minimal Mistakes 샘플 썸네일"
---

<style>
/* ─── 썸네일 크기 조절 ───────────────────────────── */
.page__hero--overlay {
  height: 200px !important;           /* 원하는 높이(px)로 조절 */
  background-size: contain !important;/* 이미지 비율 유지하면서 축소 */
  background-position: center center;
}
<style>
# AI-102 로드맵 (실전형 학습 경로)

### 1단계: 기본기 다지기 (필수 기초)

Azure 기초

Azure 포털 사용법

리소스 그룹, 스토리지, App Service 기본

[AZ-900 학습 내용 참조]

AI 개요

인공지능과 머신러닝 차이

AI 서비스와 Azure AI 서비스의 구분

### 2단계: Azure AI 서비스 이해 및 실습

이 단계가 AI-102의 핵심 영역입니다.

영역 내용 주요 서비스
NLP (자연어 처리) 텍스트 분석, 언어 감지, 개체 인식, 문서 요약 등 Azure Language Service (Text Analytics, Translator 등)
음성 처리 음성 인식, 음성 합성, 텍스트-음성 변환 Speech Service
컴퓨터 비전 이미지 분석, OCR, 얼굴 인식 Computer Vision, Face API
지식 마이닝 Azure Cognitive Search 활용 Azure Cognitive Search
Bot Azure Bot Service, QnA Maker → Language Studio로 통합됨 Azure Bot Service
맞춤형 AI Custom Vision, Custom Translator, LUIS → Language Studio로 통합됨 Language Studio, Custom AI 모델

실습 팁:

Azure Portal + Azure AI Studio에서 샘플 프로젝트 해보기

GitHub 예제: [링크텍스트](https://github.com/MicrosoftLearning/AI-102-AIEngineer)

### 3단계: 통합 및 배포 능력

Azure Functions와 Logic Apps로 AI 서비스 연결

AI 서비스 인증 및 보안: Key, Endpoint, RBAC, Managed Identity

컨테이너 배포: Cognitive Services를 Docker로 배포

### 4단계: 실전 프로젝트 구축

케이스 스터디 기반 프로젝트 만들기 (예: 음성 챗봇, 자동 리뷰 분석기 등)

아래 요소를 모두 통합한 엔드-투-엔드 프로젝트 구성

데이터 수집 → AI 처리 → 결과 시각화/응답 → 배포

### 5단계: 시험 준비

Microsoft 공식 학습 경로:

https://learn.microsoft.com/en-us/training/courses/ai-102t00?wt.mc_id=studentamb_433861

MeasureUp 모의고사 또는 Whizlabs 등 실전 대비 퀴즈

시험 구성:

케이스 기반 문항 35개 + 단답형/객관식 혼합 (총 4060문항)

시험 시간: 100~120분

합격 기준: 700점 (1000점 만점)

### 학습 타임라인 (예시)

주차 목표
1주차 Azure 기초 + AI 서비스 개요 학습
2~3주차 NLP / Computer Vision / Speech 핵심 서비스 실습
4주차 Bot Service, Azure Search, Custom 모델 실습
5주차 인증/보안/통합 구성 학습
6주차 실전 프로젝트 구성 및 복습
7주차 모의고사 + 부족한 부분 반복 학습
8주차 시험 응시
