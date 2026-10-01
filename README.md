<h1 align="center">Ishita Jain</h1>
<h3 align="center">Machine Learning Engineer in the making · Satellite & Geospatial AI · Research</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/ishita-jain22/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:ishitaajain22@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://www.kaggle.com/ishitaj22"><img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white"/></a>
</p>

---

## 🎯 At a Glance

| | |
|---|---|
| **Looking for** | ML / Data Science / Applied AI internships and entry-level roles *(TODO: confirm)* |
| **Strongest at** | End-to-end ML: data pipeline → modelling → honest evaluation → API/CLI delivery |
| **Domain depth** | Satellite imagery (Sentinel-1/2), agriculture, energy, financial-crime analytics |
| **Research** | Original diffusion-model work on cloud removal, written as an IEEE-format paper |
| **Habit that sets me apart** | Leakage audits, chronological splits, model cards, and documenting where models fail |

---

## 📈 Results at a Glance

| Project | What it does | Headline result |
|---|---|---|
| 🌫️ **SpecDiff** | Spectrally-constrained diffusion for satellite cloud removal | **S-SSIM 0.8234**, PSNR 33.61, **18.8% lower NDVI error** vs Stage 1 |
| ⚡ **Grid ML** | Predicts gas-turbine energy yield from sensor data | **R² 0.983**, MAE 1.53 MWh, **47% better** than baseline |
| 🌾 **Bhoomi** | Crop monitoring + irrigation advice for a Punjab command area | Sentinel-1/2 fusion, 2 classifiers, validated against PAU guidelines |
| 🏧 **SIH260184** | Predicts likely ATM cash-out locations for cybercrime response | Ranking model on 34+ leakage-safe features *(in progress)* |

---

## 🧪 Featured Projects

### 1. SpecDiff: Cloud Removal That Preserves Spectral Truth
**Problem:** Clouds block optical satellite imagery, and most generative fixes look plausible but corrupt vegetation indices like NDVI, which downstream analysis depends on.
**What I built:**
- **Spectral Index Preservation Loss (SIPL)**, applied at every denoising timestep of a diffusion model
- **Spectral-SSIM (S-SSIM)**, a composite metric that measures spectral fidelity, not just pixel similarity
- 9-channel U-Net (33.6M params), two-stage training on SEN12MS-CR (Sentinel-1 radar + Sentinel-2 optical)

**Result:** S-SSIM **0.8234**, PSNR **33.61**, SSIM **0.735**, NDVI MAE **0.048** (an **18.8% reduction** from Stage 1)
**Engineering:** Handled API failures, corrupted files and session limits in the data pipeline.
**Stack:** `PyTorch` `Diffusion Models` `Sentinel-1/2` `Kaggle` `LaTeX`
🔗 [Code](TODO_REPO_URL) · [Paper](TODO_PAPER_URL)

---

### 2. Bhoomi: Crop Monitoring & Irrigation Advisory *(ISRO Hackathon 2025)*
**Problem:** Farmers in Punjab need timely, field-level irrigation guidance.
**What I built:** A full-stack system that fuses Sentinel-1 + Sentinel-2, classifies crops (including rice vs wheat) with Random Forests, detects crop phenology, and runs a water-balance advisory engine.
**Rigor:** Recommendations cross-checked against Punjab Agricultural University guidelines; ground-truth points hand-extracted via Google Earth Engine.
**Stack:** `Python` `Google Earth Engine` `Random Forest` `Remote Sensing`
🔗 [Code](TODO_REPO_URL) · [Demo](TODO_DEMO_URL)

---

### 3. Gas Turbine Energy Yield Prediction *(ML for the Power Grid)*
**Problem:** Predict turbine energy yield (MWh) from 8 sensor readings.
**Decisions that mattered:**
- Excluded **CO and NOx**, which are measured post-combustion at the same timestamp as the target (**data leakage**)
- Used a **chronological split**, not a shuffled one
- Reported failure modes: heteroscedastic residuals at high load and degraded accuracy outside the trained −5°C to 32°C range

**Result:** Random Forest MAE **1.53 MWh**, R² **0.983**, versus Linear Regression MAE 2.90 (**47% improvement**)
**Deliverables:** Model card + a plain-language summary for a non-technical plant manager.
**Stack:** `scikit-learn` `Pandas` `Time-series` `Model Cards`
🔗 [Code](TODO_REPO_URL)

---

### 4. SIH260184: ATM Cash-Out Location Prediction *(Smart India Hackathon 2026, in progress)*
**Problem:** Help police intervene before stolen funds are withdrawn.
**Approach:** Candidate-ranking over ATMs with LightGBM / XGBoost; engineered account, transaction, temporal and receive→withdrawal behaviour features; strict no-lookahead feature rules; chronological train/validation/test split; separate fraud risk-scoring stage.
**Stack:** `LightGBM` `XGBoost` `Feature Engineering` `Geospatial`
🔗 [Code](TODO_REPO_URL)

---

### 5. More Builds
- 🎞️ **SlideFlow AI:** Chrome extension (Manifest V3) for voice and typed control of Google Slides using Web Speech API, Slides REST API, OAuth and Gemini. [Code](TODO_REPO_URL)
- 🧑‍💻 **Intelligent Code Reviewer & Explainer:** CLI tool using the Gemini API with validated structured output and rich terminal rendering. [Code](TODO_REPO_URL)
- 🔌 **Task API:** CRUD REST API in FastAPI with custom error handling and Swagger docs. [Code](TODO_REPO_URL)

---

## 🛠️ Skills

| Area | Tools |
|---|---|
| **ML / DL** | PyTorch, scikit-learn, LightGBM, XGBoost, Random Forests, diffusion models, U-Net |
| **Data** | Pandas, NumPy, feature engineering, leakage-safe validation, time-series splits |
| **Geospatial** | Google Earth Engine, Sentinel-1/2, NDVI & spectral indices, GeoPackage data |
| **Engineering** | Python, FastAPI, REST APIs, CLI tools, Chrome extensions (JS), Git |
| **Research** | LaTeX / IEEE papers, ablation-minded evaluation, metric design |
| **Languages** | Python, JavaScript, Java |

---

## 🧭 How I Work

- **I check for leakage first.** If a feature wouldn't exist at prediction time, it's out.
- **I report failure modes**, not only the best number. Every model gets limitations written down.
- **I explain results to non-technical people**, including plant managers and farmers.
- **I ship**: models behind APIs, CLIs and extensions, not just notebooks.

---

<p align="center">
  <b>Let's talk.</b> I'm happy to walk through any project, the metrics, and what I'd do differently.<br/>
  📫 <a href="mailto:TODO_EMAIL">TODO_EMAIL</a> · <a href="TODO_LINKEDIN">LinkedIn</a>
</p>
