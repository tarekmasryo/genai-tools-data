# 🧠 Generative AI Tools & Platforms 2025

**Author:** [Tarek Masryo](https://github.com/tarekmasryo) · [Kaggle](https://www.kaggle.com/datasets/tarekmasryo/generative-ai-tools-and-platforms-2025)  


---

## TL;DR

> A structured dataset of **113 Generative AI tools** across categories and modalities, enriched with release years, API availability, open-source status, and derived capability counts.  
>  
> - One CSV (`Generative AI Tools - Platforms 2025.csv`)  
> - 22 standardized columns  
> - Ready for analysis, dashboards, and ML prototypes  

---

## Why this dataset exists
Information about Generative AI tools is often fragmented across websites, vendor docs, and product pages.  
This dataset provides a **single, standardized CSV** that researchers and developers can immediately use for:  
- Mapping the GenAI ecosystem  
- Tracking release timelines and adoption trends  
- Benchmarking API coverage and open-source share  
- Training models to recommend tools or cluster by modality  

---

## What’s inside
**Main file — `Generative AI Tools - Platforms 2025.csv` (1 row per tool)**  

**Columns (22):**
- Core info: `tool_name`, `company`, `website`, `source_domain`  
- Taxonomy: `category_canonical`, `modality_canonical`  
- Access: `open_source`, `api_available`, `api_status`  
- Timeline: `release_year`, `years_since_release`  
- Modality flags (binary): `mod_text`, `mod_image`, `mod_video`, `mod_audio`, `mod_code`, `mod_design`, `mod_infra`, `mod_productivity`, `mod_safety`, `mod_multimodal`  
- Derived: `modality_count` (sum of core content-generating modalities)

---

## Data Dictionary

| Column             | Description                                                           |
|--------------------|-----------------------------------------------------------------------|
| tool_name          | Tool/platform name (unique)                                           |
| company            | Vendor/maintainer                                                     |
| category_canonical | Normalized use-case family (e.g., LLMs, Image Gen, Video Gen, RAG)    |
| modality_canonical | Primary capability type: text, image, video, audio, code, multimodal… |
| open_source        | 1 if open-source, else 0                                              |
| api_available      | 1 if public API available, else 0                                     |
| api_status         | API status (`api` or `unavailable`)                                   |
| website            | Official homepage (full URL)                                          |
| source_domain      | Extracted domain for grouping                                         |
| release_year       | First public release/launch year                                      |
| years_since_release| 2025 − release_year                                                   |
| modality flags     | Binary indicators (text/image/video/audio/code/design/infra/…)        |
| modality_count     | Sum of core modalities: text + image + video + audio + code           |

---

## Quick start (pandas)

```python
import pandas as pd

df = pd.read_csv("Generative AI Tools - Platforms 2025.csv")
print(df.shape)

# Distribution by category
print(df["category_canonical"].value_counts().head())

# Average modalities per tool
avg_mods = df["modality_count"].mean()
print("Avg modalities per tool:", round(avg_mods, 2))

# API coverage rate
api_rate = df["api_available"].mean()
print("API availability:", round(api_rate, 2))
```

---

## 💡 Use Cases
- Landscape dashboards for Generative AI  
- Timeline analyses of tool releases and adoption  
- Market benchmarking of API and open-source coverage  
- Capability clustering (e.g., multimodal vs single-modality)  
- Training ML models for tool recommendation systems  

 
---

 ## Related Repositories
- 🔍 [Generative AI Tools EDA & Baseline](https://github.com/tarekmasryo/genai-tools-baseline)

