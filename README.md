# Stable Diffusion Wallpaper Generator

Stable Diffusion 기반으로 컴퓨터 및 핸드폰 배경화면 이미지를 생성해주는 서비스입니다.  
한국어 입력 시에는 Llama 모델을 이용해 영어 프롬프트로 변환 후 이미지를 생성하고, 영어 입력 시에는 프롬프트를 확장시켜 생성합니다.

---

## 🚀 목표
- **컴퓨터/핸드폰 배경화면 생성**: Stable Diffusion 모델을 활용하여 고해상도 배경화면 이미지 생성
- **한국어 입력 지원**: 한국어 프롬프트는 Llama 모델을 통해 영어로 번역 후 이미지 생성
- **영어 입력 지원**: 영어 프롬프트는 Llama 모델을 통해 자연스럽고 직관적인 스타일 프롬프트 생성후 이미지 생성

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
       └─ 영어 → Llama 확장 → 자연스럽고 직관적인 스타일의 영어 prompt → Stable Diffusion → 이미지 생성

```



**설명**

* 사용자가 입력한 문장이 한국어인 경우, **Llama 모델**이 영어로 번역해 Stable Diffusion에 전달합니다.
* 영어로 입력된 경우에는 **Llama 모델**이 프롬프트를 자연스럽고 상세하게 확장하여 더 높은 품질의 이미지를 생성합니다.
* 두 경로 모두 Stable Diffusion을 통해 배경화면 이미지를 생성한 뒤 사용자에게 결과를 반환합니다.

---

## 기술 스택

- Python 3.10+
-  FastAPI (웹 서버)
-  Stable Diffusion (Diffusers / Hugging Face)
-  Llama 모델 (한국어 → 영어 번역)
-  CUDA 지원 GPU (NVIDIA 권장)

## 버전

- meta-llama/Llama-3.2-3B-Instruct
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
<img width="951" height="502" alt="image" src="https://github.com/user-attachments/assets/11d8e890-e2b2-4a3f-8a0e-699e65e1c5cb" />
</br>
<img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/10af082a-4a95-4b23-813c-2d6f3edb874e" />
</br>
<img width="956" height="447" alt="image" src="https://github.com/user-attachments/assets/86d68806-59c0-4e97-9cd4-5b8a02375550" />
</br>
<img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/57d3c110-6680-4c90-ab2d-b88c0768bc5a" />
