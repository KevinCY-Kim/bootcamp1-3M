# 2. CV and Object detection 폴더 안내

컴퓨터 비전 기본 분류부터 전이학습, 평가 지표, 전처리/증강, 콜백 고급학습, 종합 실습, 생성모델(AE/VAE/GAN), 객체탐지 데이터셋/증강, YOLO(v5/v8)까지 단계별로 학습할 수 있는 자료 모음입니다. 각 노트북의 목적과 핵심 학습 포인트를 정리했습니다.

- 고전 CNN 한눈에 보기: [클래식 CNN 모델 빠른 참고서 (AlexNet/VGG/GoogLeNet/ResNet)](./MODELS_CNN_CLASSICS.md)

## 분류 기본 및 전이학습

- **01_pytorch_MNIST.ipynb / 01_pytorch_MNIST_test.ipynb**
  - 목적: CNN 기본 구성요소(Conv2d, MaxPool 등)와 입력 텐서 구조(B×C×H×W) 이해, MNIST 기초 실습
  - 핵심: 텐서 생성/형태, 합성곱/풀링 계층, 간단한 분류 파이프라인
- **02_Transfer_learning.ipynb**
  - 목적: 사전학습 모델(ResNet, GoogLeNet) 기반 전이학습 파이프라인 구축
  - 핵심: 입력 크기 리사이즈(224), 데이터 증강, 파라미터 고정/해제, 최적화 설정
- **03_model_evaluation_metrics.ipynb**
  - 목적: 분류 성능 평가 지표 전반 적용
  - 핵심: 혼동행렬, Precision/Recall/F1, ROC-AUC, 멀티클래스 원-핫 라벨링, 시각화(Seaborn)

## 전처리/증강/학습 고급

- **04_basic_preprocessing.ipynb**
  - 목적: 기본 전처리 파이프라인 설계(정규화/리사이즈 등)
  - 핵심: torchvision.transforms 조합, 학습/검증 파이프라인 차별화
- **05_basic_augmentation.ipynb**
  - 목적: 이미지 증강 기법 적용으로 일반화 성능 향상
  - 핵심: RandomCrop, HorizontalFlip, ColorJitter 등 주요 증강 조합
- **06_[Callbacks]advanced_learning.ipynb**
  - 목적: 고급 학습 전략과 콜백(유사 기능) 활용
  - 핵심: 학습률 스케줄러, Early Stopping, Checkpoint 저장/로깅

## 종합 실습

- **07_1_종합_(practice|solution)advanced_preprocessing.ipynb**
  - 목적: 고급 전처리/증강 전략 종합 적용 실습 및 해설
  - 핵심: 데이터 파이프라인 설계, 실험 설정 비교
- **07_2_종합_(practice|solution)model_training.ipynb**
  - 목적: 모델 학습 파이프라인 종합 구현 실습 및 해설
  - 핵심: 학습 루프, 검증 루프, 메트릭 로깅/시각화, 체크포인트 관리

## 생성 모델

- **08_1_Autoencoder.ipynb**
  - 목적: 오토인코더 기본 구조와 재구성 학습
  - 핵심: 인코더/디코더, 재구성 손실, 잠재공간 이해
- **08_2_Variational_Autoencoder.ipynb**
  - 목적: 변분 오토인코더(VAE)로 확률적 잠재공간 모델링
  - 핵심: 재매개변수화 기법, KL 발산, 샘플링 기반 생성
- **08_3_GAN.ipynb**
  - 목적: GAN 기본 구조 학습 및 이미지 생성
  - 핵심: 생성자/판별자, 적대적 학습, 학습 안정화 팁

## 객체 탐지 실습

- **09_(practice|solution)Dataset_for_ObjectDetection.ipynb**
  - 목적: 객체탐지용 데이터셋 구성 실습
  - 핵심: 어노테이션 구조, 바운딩박스 형식, 커스텀 Dataset/Dataloader
- **10_Augmentation_for_ObjectDetection.ipynb**
  - 목적: 객체탐지에 특화된 증강 적용
  - 핵심: 박스 보존 증강, 좌표 변환, 시각화 검증
- **11_ObjectDetection_with_YOLOv5s.ipynb**
  - 목적: YOLOv5s로 객체탐지 파이프라인 실행
  - 핵심: 레포 클론/요구사항 설치, 데이터 구성, 학습/추론/평가 워크플로우
- **12_ObjectDetection_with_YOLOv8s.ipynb**
  - 목적: YOLOv8s로 최신 탐지 파이프라인 체험
  - 핵심: 모델 로딩, 학습/검증/추론, 결과 시각화

## 논문 구현 모음

- `paper_implementation/` 폴더에 고전/현대 CV 모델 구현 및 실습이 정리되어 있습니다. 아래 하위 README를 참고하세요.
- 클래식 CNN 심화 참고: [MODELS_CNN_CLASSICS.md](./MODELS_CNN_CLASSICS.md)

### 빠른 링크
- 분류/전이학습/평가: [02_Transfer_learning.ipynb](./02_Transfer_learning.ipynb), [03_model_evaluation_metrics.ipynb](./03_model_evaluation_metrics.ipynb)
- 전처리/증강: [04_basic_preprocessing.ipynb](./04_basic_preprocessing.ipynb), [05_basic_augmentation.ipynb](./05_basic_augmentation.ipynb)
- 종합 실습: [07_1_종합_(practice)advanced_preprocessing.ipynb](./07_1_종합_(practice)advanced_preprocessing.ipynb), [07_2_종합_(practice)model_training.ipynb](./07_2_종합_(practice)model_training.ipynb)
- 생성 모델: [08_1_Autoencoder.ipynb](./08_1_Autoencoder.ipynb), [08_2_Variational_Autoencoder.ipynb](./08_2_Variational_Autoencoder.ipynb), [08_3_GAN.ipynb](./08_3_GAN.ipynb)
- 객체탐지: [09_(solution)Dataset_for_ObjectDetection.ipynb](./09_(solution)Dataset_for_ObjectDetection.ipynb), [10_Augmentation_for_ObjectDetection.ipynb](./10_Augmentation_for_ObjectDetection.ipynb), [11_ObjectDetection_with_YOLOv5s.ipynb](./11_ObjectDetection_with_YOLOv5s.ipynb), [12_ObjectDetection_with_YOLOv8s.ipynb](./12_ObjectDetection_with_YOLOv8s.ipynb)
- 논문 구현: [paper_implementation/README.md](./paper_implementation/README.md)
