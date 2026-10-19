# LAB — Vision-Language Models: CLIP & LLaVA

PhD training — Module M1 *Agentic AI & Building AI Agents*
Author: Fadoua El Kebraoui

## Content

| File / folder | Description |
|---|---|
| `LAB_CLIP_LLaVA_Full_Lab_Statement.ipynb` | Completed notebook: code, outputs and answers (Q1–Q36) |
| `images/` | Image database (20 images, 6 classes) used for evaluation and retrieval |
| `vqa_results.csv` | LLaVA VQA results with human evaluation |
| `requirements.txt` | Python dependencies |

## Summary of results

| Deliverable | Result |
|---|---|
| CLIP zero-shot accuracy | **95 %** (19/20 images, 6 classes) — only error: cat6.jpeg, which contains both a cat and a dog |
| Top-5 retrieval ("a person playing football") | The 3 football images ranked first (cosine 0.268, 0.259, 0.258) |
| LLaVA VQA accuracy | **72 %** (18/25) — false-premise questions ("What is visible on the board?") always failed |
| Hallucination example | LLaVA says there is no bicycle, then describes it as "blue" and "in the background" |
| CLIP vs LLaVA comparison | CLIP: discriminative (scores, retrieval) — LLaVA: generative (description, VQA) |
| Mini-project | Multimodal assistant + RAG agent (CLIP retrieval → similarity threshold routing → LLaVA explanation) |

## How to run

1. Open the notebook in Google Colab.
2. `Runtime > Change runtime type > T4 GPU`.
3. Upload the images into a `images/` folder, then run the cells in order.

Models: `openai/clip-vit-base-patch32`, `llava-hf/llava-1.5-7b-hf` (4-bit quantization with bitsandbytes).
