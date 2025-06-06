---
layout: single
title: "딥러닝, 파이토치 텐서 2편"
date: 2025-06-05
categories: [파이토치]
tags: [딥러닝, .tensor, 텐서]
header:
  overlay_image: /assets/images/pytorch.png
  teaser: /assets/images/pytorch.png
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

# .tensor()

## 복사(copy) vs 공유(view)

torch.tensor()는 사용자가 입력한 데이터를 복사해서 텐서를 만들어요.

`print("Hello, world!")`는 파이썬에서 문자열을 출력합니다.

```python
def greet(name):
    print(f"Hello, {name}!")
```
