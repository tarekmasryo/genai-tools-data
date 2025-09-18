# Data Dictionary — Generative AI Tools & Platforms (2025)

## Generative AI Tools - Platforms 2025.csv
| Column             | Type   | Description |
|--------------------|--------|-------------|
| tool_name          | str    | Tool/platform name (unique within dataset) |
| company            | str    | Vendor or maintainer |
| category_canonical | str    | Standardized use-case family (e.g., LLMs, Image Gen, Video Gen, RAG, Infra, Safety, …) |
| modality_canonical | str    | Primary capability family: {text, image, video, audio, code, design, infra, productivity, safety, multimodal} |
| open_source        | int    | 1 if open-source, else 0 |
| api_available      | int    | 1 if public API available, else 0 |
| api_status         | str    | API availability status (`api` or `unavailable`) |
| website            | str    | Official homepage (full URL) |
| source_domain      | str    | Extracted domain from website for grouping |
| release_year       | int    | First public release/launch year |
| years_since_release| int    | Computed as `2025 − release_year` |
| mod_text           | int    | 1 if text generation supported |
| mod_image          | int    | 1 if image generation supported |
| mod_video          | int    | 1 if video generation supported |
| mod_audio          | int    | 1 if audio generation supported |
| mod_code           | int    | 1 if code generation supported |
| mod_design         | int    | 1 if design-related capability |
| mod_infra          | int    | 1 if infrastructure-related capability |
| mod_productivity   | int    | 1 if productivity-related capability |
| mod_safety         | int    | 1 if safety/guardrails capability |
| mod_multimodal     | int    | 1 if multimodal capability |
| modality_count     | int    | Sum of core modalities (`mod_text` + `mod_image` + `mod_video` + `mod_audio` + `mod_code`) |
