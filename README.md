# deepfake-watermark-protector

> 제4회 전국 대학(원)생 리스크 관리 경진대회 프로젝트

AI 시대 딥페이크/불법합성물 피해에 대응하기 위한 워터마킹 기반 보험상품 설계 프로젝트.

## 🎯 프로젝트 개요

생성형 AI 이미지 모델의 발달로 디지털 성범죄·불법합성물 피해가 급증하고 있습니다. 본 프로젝트는 방어형 워터마킹 기술의 효과를 정량 검증하고, 이를 바탕으로 새로운 보험상품을 설계합니다.

## 📊 실험 설계

- **데이터셋:** CelebA 100장 (남10/여90 — 디지털성범죄 피해 통계 반영)
- **워터마킹 모델 3개:** PhotoGuard / Anti-DreamBooth / CAAT
- **변형 모델 3개:** Stable Diffusion 1.5 / FLUX / SDXL
- **프롬프트 4개:** 성적 변형 2 + 범죄/사기 변형 2
- **평가:** PSNR · SSIM · ArcFace Identity · CLIP

## 📂 폴더 구조
```deepfake-watermark-protector/
├── README.md
├── .gitignore
├── requirements.txt
│
├── notebooks/
│   ├── 01_dataset_prep.ipynb
│   ├── 02_watermark_photoguard.ipynb
│   ├── 03_watermark_antidreambooth.ipynb
│   ├── 04_watermark_caat.ipynb
│   ├── 05_transform_sd15.ipynb
│   ├── 06_transform_flux.ipynb
│   ├── 07_transform_sdxl.ipynb
│   └── 08_evaluation.ipynb
│
├── src/
│   ├── watermark/
│   ├── transform/
│   └── metrics/
│       ├── psnr_ssim.py
│       ├── arcface_identity.py
│       └── clip_similarity.py
│
├── prompts/
│   └── prompts.json
│
├── results/
│   ├── psnr_matrix.csv
│   ├── identity_scores.csv
│   ├── caat_psnr_results.csv
│   └── final_summary.csv
│
├── docs/
│   ├── meeting_notes/
│   │   ├── 1차_2026-04-01.md
│   │   ├── 2차_2026-04-27.md
│   │   └── 3차_2026-04-30.md
│   ├── experiment_log.md
│   └── insurance_design.md
│
└── data/   (.gitignore로 제외)```

## 🛠 기술 스택

- **워터마킹:** PhotoGuard, Anti-DreamBooth, CAAT
- **이미지 생성:** Stable Diffusion 1.5, FLUX, SDXL
- **평가:** PSNR/SSIM, ArcFace, CLIP
- **개발 환경:** Google Colab Pro+ (A100 GPU)

## 🚀 실행 순서

1. `01_dataset_prep.ipynb` — CelebA 100장 큐레이션
2. `02_watermark_photoguard.ipynb` — PhotoGuard 워터마킹
3. `03_watermark_antidreambooth.ipynb` — Anti-DreamBooth 워터마킹
4. `04_watermark_caat.ipynb` — CAAT 워터마킹
5. `05_transform_sd15.ipynb` — SD 1.5 변형 실험
6. `06_transform_flux.ipynb` — FLUX 변형 실험
7. `07_transform_sdxl.ipynb` — SDXL 변형 실험
8. `08_evaluation.ipynb` — 통합 평가

## 👥 팀 구성

- **현태, 은서** — 워터마킹 + 변형 모델 실험
- **민솔, 서영** — 보험료율 산정, 약관, 사회적 가치 분석

## 📅 일정

- 2026.04.03 — 신청서 접수
- 2026.05.15 — 예선작 제출
- 2026.05.28 — 본선 발표
- 2026.08.21 — GAIP 국제대회 (싱가포르)
