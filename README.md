
질문 텍스트를 분류하기 위한 RoBERTa 기반 세분화 카테고리(subcategory) 분류 모델입니다.
모델은 양자화(ONNX format)되어 CPU 환경에서도 실행 가능하며, 추론용 스크립트인 `main.py`와 함께 사용됩니다.

## 파일 구성

- `main.py`: ONNX 모델을 사용하여 입력 텍스트에 대해 예측을 수행하는 추론 스크립트
- `subcat_model_quant.onnx`: 양자화된 ONNX 분류 모델
- `subcategory_label_encoder.pkl`: 세분화 카테고리 라벨 인코더 파일 (scikit-learn의 LabelEncoder 사용)


양자화 모델: https://drive.google.com/file/d/1F6jHyW6GI6oesbwW1O0Guatxa64tymhM/view?usp=drive_link

## ⚙️ 설치 및 실행 방법

### 1. 의존성 설치

```bash
pip install transformers onnxruntime scikit-learn fastapi pydantic uvicorn
