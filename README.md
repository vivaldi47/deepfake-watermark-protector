# deepfake-watermark-protector

deepfake-watermarking-insurance/
├── README.md
├── .gitignore
├── requirements.txt
│
├── notebooks/
│   ├── 01_dataset_prep.ipynb
│   ├── 02_watermark_photoguard.ipynb
│   ├── 03_watermark_antidreambooth.ipynb
│   ├── 04_watermark_caat.ipynb            ← atp → caat 변경
│   ├── 05_transform_sd15.ipynb
│   ├── 06_transform_flux.ipynb
│   ├── 07_transform_sdxl.ipynb
│   └── 08_evaluation.ipynb
│
├── src/
│   ├── watermark/
│   │   └── __init__.py
│   ├── transform/
│   │   └── __init__.py
│   └── metrics/
│       ├── __init__.py
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
│   ├── caat_psnr_results.csv               ← 1장 테스트 + 100장 배치 결과
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
└── data/                                   ← .gitignore로 제외
