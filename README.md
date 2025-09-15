# Bootcamp Repository 안내

이 저장소는 두 축으로 구성됩니다:

- [1.Python and Deeplearning Basic/](./1.Python%20and%20Deeplearning%20Basic/): Python 기초, 데이터 처리, 크롤링, 딥러닝 기초(PyTorch)
- [2. CV and Object detection/](./2.%20CV%20and%20Object%20detection/): 분류/전이학습, 평가 지표, 전처리/증강, 생성모델, 객체탐지(YOLO), 논문 구현

## 📦 프로젝트 환경 설치 가이드 (분리된 requirements)

본 프로젝트는 폴더별 작업 목적에 따라 requirements를 분리했습니다. 필요한 환경만 선택적으로 설치하면 됩니다.

### 1) 기본(Core) 환경
```bash
pip install -r requirements_core.txt
```

### 2) Torch (기본 CPU)
```bash
pip install -r requirements_torch.txt
```
GPU 환경(CUDA)에서는 공식 PyTorch 페이지에서 wheel 선택 후 설치하세요:
👉 https://pytorch.org/get-started/locally/

### 3) Computer Vision / Detection
```bash
pip install -r requirements_cv.txt
```

### 4) 데이터 수집 / 크롤링
```bash
pip install -r requirements_data.txt
```

### 5) Notebook & 실험 환경
```bash
pip install -r requirements_notebook.txt
```

✅ 권장 설치 순서
```bash
pip install -r requirements_core.txt
pip install -r requirements_torch.txt
# 이후 필요한 작업 폴더에 맞게 cv, data, notebook을 추가 설치
```

## Jupyter 환경 실행
```bash
jupyter lab
```

## 폴더별 빠른 링크

### 1. Python and Deeplearning Basic
- 개요: [01_Python/README.md](./1.Python%20and%20Deeplearning%20Basic/01_Python/README.md)
- 데이터 수집/크롤링: [02_Data Correction/README.md](./1.Python%20and%20Deeplearning%20Basic/02_Data%20Correction/README.md)
- 딥러닝 기초(PyTorch): [03_Deeplearning Basic/README.md](./1.Python%20and%20Deeplearning%20Basic/03_Deeplearning%20Basic/README.md)
- 문제풀이 모음: [문제풀이/README.md](./1.Python%20and%20Deeplearning%20Basic/01_Python/%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4/README.md)

추천 시작 경로
- Python 기초 실습: [실습자료/README.md](./1.Python%20and%20Deeplearning%20Basic/01_Python/%EC%8B%A4%EC%8A%B5%EC%9E%90%EB%A3%8C/README.md)
- Pandas/Numpy 추가자료: [기초추가자료/README.md](./1.Python%20and%20Deeplearning%20Basic/01_Python/%EA%B8%B0%EC%B4%88%EC%B6%94%EA%B0%80%EC%9E%90%EB%A3%8C/README.md)

### 2. CV and Object detection
- 개요: [README.md](./2.%20CV%20and%20Object%20detection/README.md)
- 클래식 CNN 빠른 참고서(AlexNet/VGG/GoogLeNet/ResNet): [MODELS_CNN_CLASSICS.md](./2.%20CV%20and%20Object%20detection/MODELS_CNN_CLASSICS.md)
- 논문 구현 모음: [paper_implementation/README.md](./2.%20CV%20and%20Object%20detection/paper_implementation/README.md)

추천 시작 경로
- 전이학습 실전: [02_Transfer_learning.ipynb](./2.%20CV%20and%20Object%20detection/02_Transfer_learning.ipynb)
- 평가 지표: [03_model_evaluation_metrics.ipynb](./2.%20CV%20and%20Object%20detection/03_model_evaluation_metrics.ipynb)
- 객체탐지 YOLOv8: [12_ObjectDetection_with_YOLOv8s.ipynb](./2.%20CV%20and%20Object%20detection/12_ObjectDetection_with_YOLOv8s.ipynb)

## 주의 및 팁
- 일부 노트북(예: YOLOv5)은 노트북 내부에서 별도 패키지를 설치합니다.
- 크롤링 노트북은 웹 페이지 구조 변경에 따라 수정이 필요할 수 있습니다.
- 대용량 연산 시 GPU/VRAM 한도를 고려해 배치 크기와 이미지 크기를 조절하세요.
