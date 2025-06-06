---
layout: single
title: "앞으로 적어야 할 파이토치 함수들"
date: 2025-06-05
categories: [파이토치]
tags: [딥러닝]
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

> 이 파일은 블로그 포스팅 시 내부 작동 원리까지 이해해야 하는 핵심 함수 목록입니다.  
> ✔️: 이미 작성한 항목 / ❌: 아직 작성하지 않은 항목

## 텐서 생성 관련

- ✔️ `torch.empty()`
- ❌ `torch.tensor()`
- ❌ `torch.from_numpy()`
- ❌ `torch.clone()` vs `detach()`
- ❌ `torch.as_tensor()`

## Autograd / 역전파

- ❌ `torch.autograd` 모듈 전반
- ❌ `requires_grad`, `no_grad`, `detach`, `retain_graph`
- ❌ `backward()` 호출 구조
- ❌ `.grad` 필드의 초기화 타이밍

## Optimizer / 파라미터 업데이트

- ❌ `torch.optim.SGD`, `Adam`, `zero_grad()` 호출 이유
- ❌ 파라미터 업데이트 순서
- ❌ 학습률 스케줄러 (`lr_scheduler`)

## 모델 정의 관련

- ❌ `torch.nn.Module` 동작 원리 (forward override, hooks)
- ❌ `model.eval()` vs `model.train()` 내부 상태 변화
- ❌ `state_dict()` / `load_state_dict()`

## CUDA 관련

- ❌ `.to(device)`의 작동 방식
- ❌ `.cuda()`와 `.to()` 차이
- ❌ CPU ↔ GPU 간 연산 병목

## DataLoader

- ❌ `num_workers`, `pin_memory` 의미
- ❌ `collate_fn` 커스터마이징
- ❌ `shuffle=True`가 학습에 미치는 영향

## Random

- ❌ `torch.manual_seed()`가 통제하는 범위
- ❌ GPU 연산 시 seed가 재현되지 않는 경우

## 기타

- ❌ `torch.jit` (TorchScript)
- ❌ `torch.nn.functional`과 `nn.Module`의 차이
- ❌ `forward()` 함수 내에서 `register_buffer()`가 쓰이는 이유
  """

## 역량

| 역량                    | 설명                                                                          |
| ----------------------- | ----------------------------------------------------------------------------- |
| **텐서 차원 이해**      | `view`, `permute`, `unsqueeze`, `expand` 등 자유자재로 조작 가능해야 함       |
| **모델 정의 능력**      | `nn.Module`로 네트워크를 정의하고 forward 함수 작성                           |
| **학습 루프 작성 능력** | `optimizer.zero_grad() → loss.backward() → optimizer.step()` 루틴 이해        |
| **디버깅**              | 에러가 났을 때 `shape mismatch`, `nan`, `cuda error` 등 원인 파악 가능해야 함 |
| **프로젝트 구조화**     | 모델, 데이터셋, 훈련 루프, 실험 추적 등을 모듈화할 수 있어야 함               |

## 실제 외우는 범위

| 범위                                                          | 숙련도                            |
| ------------------------------------------------------------- | --------------------------------- |
| 텐서 연산 (`tensor`, `reshape`, `permute`, `unsqueeze`)       | ✅ 잘 익혀 있음                   |
| `nn.Module`, `forward`, `optimizer`, `loss` 등 기본 학습 루프 | ✅ 능숙                           |
| Autograd를 직접 구현 (`torch.autograd.Function`)              | ❌ 거의 사용 안 함                |
| Low-level 함수 (`as_strided`, `einsum`, custom backward 등)   | ⚠️ 고급 유저나 연구자만 일부 사용 |
| 모든 dtype, 모든 device 간 동작                               | ❌ 문서 보면서 사용함             |
| GPU 분산 학습 (`DDP`, `NCCL`, `FSDP`)                         | ⚠️ 필요할 때만 익힘               |
| TorchScript, ONNX, Quantization, AMP                          | ⚠️ 필요하면 익히고, 모르면 검색함 |

---
