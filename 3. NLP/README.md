# 3. NLP (Natural Language Processing)

자연어 처리와 관련된 다양한 기법과 모델을 학습하는 프로젝트입니다.

## 📁 프로젝트 구조

### 0_dataset/
- **목적**: NLP 실습에 사용되는 다양한 데이터셋 저장
- **내용**: 
  - 대화체 데이터 (2_대화체.xlsx)
  - 시계열 데이터 (airline-passengers.csv, sbux.csv)
  - 영화 메타데이터 (movies_metadata.csv)
  - 교통 데이터 (서인천IC-부평IC 평균속도.csv)
  - 결함 데이터 (Faults.NNA)

### 1_텍스트_전처리/
- **목적**: 텍스트 데이터 전처리 기법 학습
- **주요 내용**:
  - `01_정규표현식.ipynb`: 정규표현식을 활용한 텍스트 패턴 매칭
  - `02_Text_Preprocessing.ipynb`: 텍스트 정제, 토큰화, 불용어 제거
  - `03_Text_Vectorization.ipynb`: 텍스트를 벡터로 변환하는 기법들

### 2_RNN/
- **목적**: 순환 신경망(RNN) 기반 자연어 처리 모델 학습
- **주요 내용**:
  - `01_RNN_basic.ipynb`: RNN 기본 구조와 동작 원리
  - `02_LSTM&GRU_basic.ipynb`: LSTM과 GRU 구조 이해
  - `03_RNN_분류(GRU).ipynb`: GRU를 활용한 텍스트 분류
  - `04_RNN_시계열_예측.ipynb`: RNN을 활용한 시계열 데이터 예측
  - `05_이상치_탐지.ipynb`: 시계열 데이터에서 이상치 탐지
  - `06_Seq2Seq_한영번역.ipynb`: Sequence-to-Sequence 모델을 활용한 번역
  - `[실습] 발화 상황 분류.ipynb`: 발화 상황 분류 실습 문제
  - `[실습] 발화 상황 분류 풀이.ipynb`: 발화 상황 분류 해답

### 3_Attention_Transformer/
- **목적**: 어텐션 메커니즘과 Transformer 모델 학습
- **주요 내용**:
  - `01.Seq2Seq with attention.ipynb`: 어텐션을 적용한 Seq2Seq 모델
  - `02_텍스트_분류_att_with_rnn.ipynb`: RNN에 어텐션을 적용한 텍스트 분류
  - `03_텍스트_분류_full_att.ipynb`: 완전한 어텐션 기반 텍스트 분류
  - `04_Keras_Transformer_전체 구현 코드.ipynb`: Keras로 Transformer 구현
  - `04_2_Transformer(chatbot).ipynb`: Transformer 기반 챗봇 구현
  - `05_Transformer를 사용한 시계열 예측.ipynb`: Transformer를 활용한 시계열 예측
  - `06_transformer_텍스트분류_full_attention.ipynb`: Transformer 기반 텍스트 분류
  - `07_Vision_In_Transformer.ipynb`: Vision Transformer (ViT) 구현

### 4_오디오_전처리/
- **목적**: 오디오 데이터 전처리 기법 학습
- **주요 내용**:
  - `1_오디오_전처리.ipynb`: 오디오 신호 처리 및 특성 추출

### 5_LLM/
- **목적**: 대규모 언어 모델(Large Language Model) 학습
- **주요 내용**:
  - GPT, BERT 등 최신 LLM 모델들
  - 파인튜닝 및 프롬프트 엔지니어링
  - 생성형 AI 활용법

## 🚀 추천 학습 경로

### 초급자
1. **텍스트 전처리**: `1_텍스트_전처리/` 폴더부터 시작
2. **RNN 기초**: `2_RNN/01_RNN_basic.ipynb` → `02_LSTM&GRU_basic.ipynb`
3. **실습**: `2_RNN/[실습] 발화 상황 분류.ipynb`

### 중급자
1. **어텐션 메커니즘**: `3_Attention_Transformer/01.Seq2Seq with attention.ipynb`
2. **Transformer 구현**: `3_Attention_Transformer/04_Keras_Transformer_전체 구현 코드.ipynb`
3. **시계열 예측**: `2_RNN/04_RNN_시계열_예측.ipynb`

### 고급자
1. **Vision Transformer**: `3_Attention_Transformer/07_Vision_In_Transformer.ipynb`
2. **LLM 활용**: `5_LLM/` 폴더의 최신 모델들
3. **오디오 처리**: `4_오디오_전처리/1_오디오_전처리.ipynb`

## 📚 주요 기술 스택

- **프레임워크**: TensorFlow/Keras, PyTorch
- **전처리**: NLTK, spaCy, scikit-learn
- **시각화**: Matplotlib, Seaborn
- **데이터 처리**: Pandas, NumPy
- **오디오 처리**: librosa, soundfile

## 🔗 참고 자료

- [Natural Language Processing with Python](https://www.nltk.org/book/)
- [Attention Is All You Need (Transformer 논문)](https://arxiv.org/abs/1706.03762)
- [BERT: Pre-training of Deep Bidirectional Transformers](https://arxiv.org/abs/1810.04805)
- [TensorFlow NLP 가이드](https://www.tensorflow.org/text)
- [PyTorch NLP 튜토리얼](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html)

## ⚠️ 주의사항

- 일부 노트북은 대용량 데이터셋을 사용하므로 충분한 메모리와 저장공간이 필요합니다
- GPU 환경에서 실행 시 더 빠른 학습이 가능합니다
- 텍스트 전처리 과정에서 언어별 특성을 고려해야 합니다
- 시계열 데이터는 시간 순서를 유지하는 것이 중요합니다
