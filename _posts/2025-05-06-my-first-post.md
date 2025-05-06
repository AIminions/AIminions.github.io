---
layout: single
title: "Azure 우대 기업"
date: 2025-05-06
categories: [AI]
tags: [Azure 우대]
header:
  # ➜ overlay_image를 써야 page__hero--overlay가 찍힙니다
  overlay_image: /assets/images/Azure.png
  teaser: /assets/images/Azure.png
  caption: "Minimal Mistakes 샘플 썸네일"
  # ➜ 오버레이 영역에 excerpt(미리보기)가 나오지 않도록 끕니다
  show_overlay_excerpt: false
---

<!--───────────────────────────────────────────────────-->
<!-- 1. CSS: 썸네일 크기 & 테이블 스타일 조정               -->
<!--───────────────────────────────────────────────────-->
<style>
/* ─── 썸네일 크기 조절 ───────────────────────────── */
.page__hero--overlay {
  height: 200px !important;           /* 원하는 높이(px)로 조절 */
  background-size: contain !important;/* 이미지 비율 유지하면서 축소 */
  background-position: center center;
}

/* ─── 본문 테이블을 가로 스크롤 가능하게 래핑 ────────── */
.table-wrapper {
  overflow-x: auto;
  margin: 1.5rem 0;
}
.table-wrapper table {
  width: auto;            /* 내용에 맞춰 너비 결정 */
  min-width: 800px;       /* 최소 너비 지정 */
  border-collapse: collapse;
  font-size: 0.85rem;
  white-space: nowrap;    /* 칸 안에서 줄바꿈 방지 */
}
.table-wrapper th,
.table-wrapper td {
  padding: 10px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}
</style>

<!--───────────────────────────────────────────────────-->
<!-- 2. 본문: table-wrapper로 감싸서 넣기               -->
<!--───────────────────────────────────────────────────-->

| **기업명**   | **Azure 활용 분야**                    | **Azure 경력 인정 여부**     | **비고**                                   |
| ------------ | -------------------------------------- | ---------------------------- | ------------------------------------------ |
| 삼성SDS      | 멀티클라우드 기반 AI 플랫폼            | △ 클라우드 전환 경력 우대    | FabriX를 Azure에 탑재, MS와 협력           |
| LG CNS       | Azure 기반 생성형 AI 솔루션 및 컨설팅  | ◎ Azure 경력 적극 인정       | Azure AD 운영, MS Launch Center 운영       |
| SK텔레콤     | Azure Edge Zone 기반 5G 엣지 클라우드  | ○ 클라우드 역량 우대         | Azure 엣지 클라우드 출시 협업              |
| 롯데정보통신 | Azure 기반 e커머스 이미지/로그 처리    | ○ Azure 활용 경험 우대       | 롯데그룹 디지털 전환 사례 보유             |
| 웅진         | Azure 전환 및 라이선스 판매            | ◎ Azure 프로젝트 경력자 채용 | Azure 영업 경력직 채용, 다수 프로젝트 수행 |
| 클루커스     | Azure MSP, 데이터/AI/인프라            | ◎ Azure 전문가 상시 채용     | Azure Digital Twins 기반 배터리 예측 수행  |
| 패스트파이브 | Azure 기반 MSP 및 퍼블릭 클라우드 운영 | ◎ Azure 경력 우대 채용       | 멀티클라우드 엔지니어 채용 중 (Azure 포함) |

> ⚠️ 정확하지 않을 수 있음.  
> 출처: ChatGPT
