# 클래식 CNN 모델 빠른 참고서 (AlexNet, VGGNet, GoogLeNet, ResNet)

현대 CV의 기반이 되는 네 가지 대표 CNN을 한눈에 비교/이해할 수 있도록 정리했습니다. 각 모델의 개요, 핵심 아이디어, 대표 구성, 장단점, 활용 포인트, 본 저장소 내 연계 노트북을 제공합니다.

---

## AlexNet (2012)
- **개요**: ImageNet 대회에서 딥러닝의 우월성을 입증한 초기 대규모 CNN
- **핵심 아이디어**
  - ReLU 활성화로 학습 가속화, 드롭아웃으로 과적합 완화
  - 데이터 증강(랜덤 크롭/플립), Local Response Normalization(LRN)
  - 대형 커널과 깊어진 계층 구조의 효과 검증
- **대표 구성(단순화)**: 5×Conv + 3×FC, ReLU, MaxPool, Dropout
- **장점**: 당시 기준 높은 성능, ReLU/Dropout/증강의 효과 검증
- **단점**: 매개변수 수가 많고 무겁다, LRN은 현재 거의 사용 안 함
- **언제 쓰나**: 역사적/교육적 참고, 소형 실험 벤치마크
- **연계 노트북**: `paper_implementation/01_(practice|solution)paper_implementation(AlexNet_modeling).ipynb`, `...AlexNet_Ensemble.ipynb`

## VGGNet (2014)
- **개요**: 작은 3×3 필터를 깊게 쌓아 성능을 높이는 단순/규칙적 아키텍처
- **핵심 아이디어**
  - 3×3 Conv를 연속 사용해 수용영역을 늘리면서 매개변수 효율 개선
  - 통일된 블록 구조(Conv-Conv-Pool)로 구현 단순성/이식성 향상
- **대표 구성(VGG-16)**: [Conv3×3×2 + MaxPool] × 5 → FC(4096-4096-1000)
- **장점**: 구조적 일관성, 구현 용이, 전이학습 백본으로 널리 활용
- **단점**: 계산량/메모리 사용량 큼, 최신 비교 시 비효율적
- **언제 쓰나**: 특징 추출기 백본, 실험용 기준선(baseline)
- **연계 노트북**: 전이학습 예제 `02_Transfer_learning.ipynb` (torchvision VGG 가용)

## GoogLeNet / Inception v1 (2014)
- **개요**: Inception 모듈로 멀티 스케일 특징을 병렬 추출하는 효율적 네트워크
- **핵심 아이디어**
  - 1×1 Conv로 차원 축소 후 3×3/5×5 경로 병렬 처리(멀티 스케일)
  - 보조 분류기(auxiliary classifiers)로 그래디언트 흐름 안정화
- **대표 구성**: Inception 모듈을 여러 스테이지로 스택, GlobalAvgPool 후 FC
- **장점**: 매개변수/계산 효율적, 높은 성능-효율 균형
- **단점**: 모듈 설계가 비교적 복잡, 구현 난이도↑
- **언제 쓰나**: 제한된 자원에서 성능-효율 균형 필요 시
- **연계 노트북**: `paper_implementation/03_(practice|solution)paper_implementation(GoogLeNet_modeling).ipynb`

## ResNet (2015)
- **개요**: 잔차 학습(Residual Learning)으로 초심도 네트워크 학습을 가능하게 함
- **핵심 아이디어**
  - `F(x) + x` 스킵 연결로 기울기 소실/폭주 완화, 깊이 확장 용이
  - BasicBlock(ResNet-18/34) vs Bottleneck(50/101/152)
- **대표 구성(ResNet-50)**: Conv stem → [Bottleneck ×3, ×4, ×6, ×3] → GAP → FC
- **장점**: 매우 깊은 네트워크 학습 가능, 전이학습 백본으로 표준
- **단점**: 블록/스테이지 설계 이해 필요, 계산량 존재
- **언제 쓰나**: 범용 백본, 전이학습/파인튜닝에 강력한 기본 선택지
- **연계 노트북**: `paper_implementation/04_(solution)paper_implementation(ResNet_modeling).ipynb`, 전이학습 `02_Transfer_learning.ipynb`

---

## 빠른 비교 표(요약)
- **매개변수 효율**: GoogLeNet ≥ ResNet > VGG > AlexNet
- **구현 용이성**: VGG ≥ AlexNet > ResNet > GoogLeNet
- **전이학습 백본 적합성**: ResNet ≥ VGG > GoogLeNet > AlexNet
- **현업 선호도(최근)**: ResNet 계열이 기본값, 경량/효율은 MobileNet/EfficientNet 고려

## 이 저장소에서의 시작 경로
- 간단 구조/실습: AlexNet → VGGNet → GoogLeNet → ResNet 순으로
- 전이학습 바로 실전: `02_Transfer_learning.ipynb`에서 ResNet/VGG 선택
- 구조 심화 이해: `paper_implementation/` 내 해당 모델 노트북 참조
