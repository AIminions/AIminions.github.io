---
layout: single
title: "딥러닝, 파이토치 텐서 2편"
date: 2025-06-05
categories: [파이토치]
tags: [딥러닝, .tensor, 텐서]
header:
  overlay_image: /assets/images/pytorch.png
  teaser: /assets/images/pytorch.png
  caption: "pytorch"
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

```python
x = torch.tensor([3, 2.3])
print(x)
```

결과

```python
tensor([3.0000, 2.3000])
```

반면, torch.from_numpy(data)나 torch.as_tensor(data)는 가능하면 원본 데이터를 공유합니다.

> 이 경우 메모리 사용량, 속도, 데이터 변경 시 동기화 여부에 큰 영향을 줍니다

**예시**

```python
import numpy as np
a = np.array([1, 2, 3])
b = torch.tensor(a)
a[0] = 100
print(b)  # 여전히 tensor([1, 2, 3]) → 복사됨

c = torch.from_numpy(a)
a[1] = 200
print(c)  # tensor([100, 200,   3]) → numpy와 메모리 공유됨
```

---

## dtype 자동 추론의 위험

`torch.tensor([1.0, 2.0])`처럼 사용하면 float32가 아니라 float64로 초기화됩니다.

이는 `model.parameters()`처럼 float32로 초기화된 텐서와 함께 연산하면 dtype mismatch가 발생할 수 있습니다.

> 특히 `torch.tensor(..., dtype=torch.float32)`를 명시하지 않으면 예상치 못한 타입 에러 발생 가능

---

## requires_grad 설정과 그래프 연결 여부

`torch.tensor(data, requires_grad=True)`로 만들면, 기존 데이터를 베이스로 연산 그래프를 새로 생성해요.

반면, 연산을 통해 만들어진 텐서는 그래프에 연결됩니다 이는 역전파 구조를 설계할 때 혼동을 유발합니다.

---

## CPU/GPU 전송의 시작점이 될 수 있음

torch.tensor()는 항상 CPU에 텐서를 생성합니다. to(device)를 해줘야 GPU로 이동합니다.

실수로 .cuda()를 생략하면 GPU에서 동작하지 않으므로 성능이 저하 됩니다.

---

## 성능 이슈

torch.tensor()는 항상 복사가 발생하기 때문에, 큰 배열을 반복해서 처리할 경우 성능 병목의 원인이 됩니다.

이럴 땐 `as_tensor()`나 `from_numpy()`를 고려해야 함.

---

# 결론

torch.tensor()는 단순한 듯 보이지만, 메모리 관리, 성능, 자동 미묘한 타입 차이, 연산 그래프 연결 여부 등 실제 프로젝트에서는 실수하기 쉬운 지점이 많습니다.

내일은 `torch.from_numpy()` 에 관해 알아보겠습니다.
