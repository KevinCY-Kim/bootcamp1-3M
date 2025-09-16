# 1. Python and Deeplearning Basic 폴더 안내

이 영역은 Python 기초 학습부터 데이터 수집/크롤링, 딥러닝 기초(PyTorch)까지 단계적으로 학습할 수 있도록 구성되어 있습니다. 아래 하위 폴더 설명과 빠른 링크를 참고하세요.

## 하위 폴더

- `01_Python/`
  - Python 문법 기초, 실습 자료, 문제풀이(ch1~ch6)로 구성
  - 빠른 링크: [01_Python/README.md](./01_Python/README.md)
  - 세부:
    - 기초추가자료(Numpy/Pandas/클래스/보험료 예측): [README](./01_Python/기초추가자료/README.md)
    - 실습자료(변수/문자열/자료구조/제어문/함수/클래스/모듈/파일/예외): [README](./01_Python/실습자료/README.md)
    - 문제풀이(ch1~ch6): [README](./01_Python/문제풀이/README.md)

- `02_Data Correction/`
  - 웹 크롤링/데이터 수집 실습 (requests/bs4/selenium, API 등)
  - 빠른 링크: [02_Data Correction/README.md](./02_Data Correction/README.md)

- `03_Deeplearning Basic/`
  - PyTorch 기초, MLP, 모델 학습/평가/예측 실습
  - 빠른 링크: [03_Deeplearning Basic/README.md](./03_Deeplearning Basic/README.md)

## 추천 학습 경로
1. Python 기초 실습: `01_Python/실습자료/README.md`
2. 데이터 처리 심화: `01_Python/기초추가자료/README.md`
3. 문제풀이로 개념 강화: `01_Python/문제풀이/README.md`
4. 크롤링/데이터 수집: `02_Data Correction/README.md`
5. 딥러닝 기초(PyTorch): `03_Deeplearning Basic/README.md`

## 실행 환경
- 루트 `requirements.txt` 설치 후 Jupyter Lab으로 열기
```bash
pip install -r requirements.txt
jupyter lab
```

필요 시, 상위 저장소 `README.md`에서 CUDA(Pytorch GPU) 설정 가이드를 참고하세요.
