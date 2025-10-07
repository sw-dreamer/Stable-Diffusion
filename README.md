# Stable Diffusion Wallpaper Generator

Stable Diffusion 기반으로 컴퓨터 및 핸드폰 배경화면 이미지를 생성해주는 서비스입니다.  
한국어 입력 시에는 Llama 모델을 이용해 영어 프롬프트로 변환 후 이미지를 생성하고, 영어 입력 시에는 바로 이미지를 생성합니다.

---

## 🚀 목표
- **컴퓨터/핸드폰 배경화면 생성**: Stable Diffusion 모델을 활용하여 고해상도 배경화면 이미지 생성
- **한국어 입력 지원**: 한국어 프롬프트는 Llama 모델을 통해 영어로 번역 후 이미지 생성
- **영어 입력 지원**: 영어 프롬프트는 바로 Stable Diffusion으로 이미지 생성

---

## 🛠️ 기능
**언어 기반 이미지 생성**
   - 한국어 입력 → Llama 번역 → 영어 prompt 생성 → Stable Diffusion
   - 영어 입력 → 바로 Stable Diffusion

---

## 처리 흐름
```
[사용자 입력]
       │
       ├─ 한국어 → Llama 번역 → 영어 prompt → Stable Diffusion → 이미지 생성
       │
       └─ 영어 → Stable Diffusion → 이미지 생성
```
## 기술 스택

- Python 3.10+
-  FastAPI (웹 서버)
-  Stable Diffusion (Diffusers / Hugging Face)
-  Llama 모델 (한국어 → 영어 번역)
-  CUDA 지원 GPU (NVIDIA 권장)

## 버전

- meta-llama/Meta-Llama-3-8B-Instruct
- runwayml/stable-diffusion-v1-5
- torch: 2.8.0+cu126
- torchvision: 0.23.0+cu126
- diffusers: 0.35.1
- transformers: 4.56.2
- Pillow: 11.3.0
- fastapi: 0.118.0
- uvicorn: 0.37.0

---

## 참고 
- Stable Diffusion 모델: https://huggingface.co/CompVis/stable-diffusion-v1-4

- [Llama 모델](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct)

---
## 결과 화면
<img width="375" height="267" alt="image" src="https://github.com/user-attachments/assets/90ce3049-eb47-4cba-b0e5-553e20901444" />


<img width="256" height="256" alt="image" src="https://github.com/user-attachments/assets/c5861ca1-0ab0-4380-bbd5-a23e2428af0c" />
