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
