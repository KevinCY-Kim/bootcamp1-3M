# paper_implementation 폴더 안내

고전부터 현대까지 주요 컴퓨터 비전 모델들을 논문 기반으로 구현/실습한 자료 모음입니다. 각 노트북의 목적과 핵심 아이디어, 구현 범위를 정리했습니다. 모델 간 비교는 상위 폴더의 [클래식 CNN 참고서](../MODELS_CNN_CLASSICS.md)를 함께 보세요.

> 전이학습 실전 예시는 상위 폴더의 [02_Transfer_learning.ipynb](../02_Transfer_learning.ipynb) 참고

## 분류 모델 계열

- **01_(practice|solution)paper_implementation(AlexNet_modeling).ipynb**
  - 목적: AlexNet 구조 재현 및 학습 파이프라인 구현
  - 핵심 아이디어: 대규모 CNN, ReLU 활성화, 드롭아웃, 데이터 증강
  - 구현 범위: 모델 아키텍처 정의, 옵티마이저/손실 설정, 학습/검증 루프

- **02_(practice|solution)paper_implementation(AlexNet_Ensemble).ipynb**
  - 목적: 앙상블을 통한 성능 향상 실험
  - 핵심 아이디어: 서로 다른 초기화/증강으로 학습한 모델의 소프트/하드 보팅
  - 구현 범위: 다중 모델 학습, 예측 결합, 성능 비교

- ⚠️ **VGGNet 참고**: 이 폴더에는 VGG 구현 노트북이 없으며, 필요 시 torchvision의 `vgg16`/`vgg19`를 활용한 전이학습 예제를 [02_Transfer_learning.ipynb](../02_Transfer_learning.ipynb)에서 확인하세요.

- **03_(practice|solution)paper_implementation(GoogLeNet_modeling).ipynb**
  - 목적: GoogLeNet(Inception v1) 구조 구현
  - 핵심 아이디어: Inception 모듈(다중 커널 병렬), 보조 분류기(auxiliary classifiers)
  - 구현 범위: Inception 블록 설계, 전체 네트워크 구성, 학습/평가

- **04_(solution)paper_implementation(ResNet_modeling).ipynb / 03_(solution)paper_implementation(ResNet_modeling).ipynb**
  - 목적: ResNet 잔차학습(Residual Learning) 구조 구현
  - 핵심 아이디어: 스킵커넥션(Identity/Projection), 네트워크 깊이에 따른 성능 향상
  - 구현 범위: BasicBlock/Bottleneck 블록, 스테이지 구성, 학습/평가

## 객체탐지/세그멘테이션 계열

- **05_1_Yolo v1_architecture_implentation.ipynb**
  - 목적: YOLO v1 아키텍처 구성 이해 및 구현
  - 핵심 아이디어: 단일 CNN으로 박스와 클래스 동시 예측, 그리드 기반 예측
  - 구현 범위: Backbone-헤드 연결, 출력 텐서 구조 설계

- **05_2_yolo_v1_loss_implementation.ipynb**
  - 목적: YOLO v1 손실 함수 구현
  - 핵심 아이디어: 좌표/크기/객체성/클래스 손실의 결합, 책임 할당(responsibility)
  - 구현 범위: 손실 항목 계산, 람다 가중치 적용, 안정적 학습을 위한 트릭

- **07_(practice|solution)Yolo_v3_implementation.ipynb**
  - 목적: YOLO v3 멀티스케일 탐지 구현
  - 핵심 아이디어: FPN/3-스케일 예측, 앵커 박스, Darknet-53 백본
  - 구현 범위: 앵커 기반 디코딩, NMS 적용, 학습/추론 파이프라인

- **08_(solution)FCN_implementation.ipynb**
  - 목적: Fully Convolutional Network 기반 세그멘테이션
  - 핵심 아이디어: 완전 합성곱 구조, 업샘플링/스킵 연결로 픽셀단위 분류
  - 구현 범위: 인코더-디코더 구조, 업샘플링, 평가 메트릭(mIoU 등)

- **09_(solution)Unet_implementation.ipynb**
  - 목적: U-Net 세그멘테이션 모델 구현
  - 핵심 아이디어: 대칭형 U 구조, 컨캣 스킵 연결, 소량 데이터에서의 강점
  - 구현 범위: 인코더/디코더 블록, 스킵 연결, 학습/평가 루틴

---
실습(Practice) 노트북으로 스스로 구현에 도전한 뒤, Solution 노트북으로 정답 구현과 비교해 보세요. 모델 구조/손실/학습 루프의 연결관계를 이해하는 데 초점을 맞추었습니다.
