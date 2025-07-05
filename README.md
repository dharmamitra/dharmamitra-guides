# Dharmamitra: Open Tools for Buddhist Digital Philology

*Accelerating research on Classical Asian source languages with modern machine‑learning workflows.*

---

## Table of Contents

- [About Dharmamitra](#about-dharmamitra)
- [DharmaNexus](#dharmanexus)
- [MITRA Translate](#mitra-translate)
- [MITRA OCR](#mitra-ocr)
- [MITRA Search](#mitra-search)
- [MITRA Dictionaries](#mitra-dictionaries)
- [MITRA Models & API](#mitra-models--api)
- [MITRA Publications](#mitra-publications)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)
- [Citation](#citation)

---
<div align="center">
  <img src="guides-logo.png" alt="Dharmamitra Logo" width="500">
</div>

## About Dharmamitra

**[Dharmamitra](https://dharmamitra.org)** is a meta‑platform that bundles state‑of‑the‑art NLP, OCR and information‑retrieval components for scholars working with the Ancient Asian languages Sanskrit, Pāli, Classical Chinese, and Tibetan.  Each tool can be used stand‑alone or orchestrated as part of a full research pipeline—from raw page scans to bilingual, semantically searchable corpora.

The project grew out of the original *BuddhaNexus* stack (2014‑2024) and has since been completely refactored for scalability, open licensing, and transparent citation.  All code in this organisation is released under permissive licenses, and every dataset is either public‑domain or Creative Commons.

---

## DharmaNexus

**[DharmaNexus](https://dharmanexus.org)** is a web platform for the exploration of intertextuality for literature preserved in Pāli, Sanskrit, Chinese, and Tibetan. Its technical foundation and user interface are a continuation of [BuddhaNexus](https://buddhanexus.net), and it is tightly integrated into MITRASearch and provides modernized algorithms that integrate sophisticated multilingual matching with deep semantic similarity capabilities provided by [Gemma 2 MITRA-E](https://huggingface.co/buddhist-nlp/gemma-2-mitra-e).

---

## MITRA Translate

> *Neural machine translation models fine‑tuned for Buddhist domain texts.*

- **Languages supported:**
  - Sanskrit → English
  - Pāli → English
  - Tibetan → English  
  - Classical Chinese → English

- **Model:** Standalone many-to-one translation model is available on 🤗 Hugging Face: (`dharmamitra/mitra‑translate‑<lang>`) 

---

## MITRA OCR

> *High‑accuracy OCR based on Google Gemini engine.*

---

## MITRA Search

> *Approximate‑nearest‑neighbour semantic search across all four languages.*

---

## MITRA Dictionaries

> Auto‑generated **Sanskrit ↔ Tibetan** termbanks derived from 600 k parallel sentence pairs (≈ 4 million entries).

- **Format:** StarDict (works with GoldenDict, StarDict, SDCV)
- **Size:** \~10 GB per direction after unzip
- **License:** CC BY‑SA 4.0
- **Repo:** [dharmamitra‑stardict‑dictionaries ↗](https://github.com/dharmamitra/dharmamitra-stardict-dictionaries)


---

## MITRA Models & API


---

## MITRA Publications

*Chronological list of key peer‑reviewed outputs underpinning the project.*

### 2023

- **MITRA‑zh: An efficient, open machine translation solution for Buddhist Chinese.** *Sebastian Nehrdich, Marcus Bingenheimer, Justin Brody, Kurt Keutzer.* *Proceedings of the Joint 3rd Intl. Conf. on NLP for Digital Humanities & 8th IWCLUL*, Tokyo, pp. 266–277. [ACL Anthology](https://aclanthology.org/2023.nlp4dh-1.29/)

### 2024

- **Breakthroughs in Tibetan NLP & Digital Humanities.** *Marieke Meelen, Sebastian Nehrdich, Kurt Keutzer.* *Revue d’Études Tibétaines*, No. 72 (July 2024, Proceedings of the IATS 2022 Panel), pp. 5–25.
- **One Model is All You Need: ByT5‑Sanskrit, a Unified Model for Sanskrit NLP Tasks.** *Sebastian Nehrdich, Oliver Hellwig, Kurt Keutzer.* *Findings of EMNLP 2024*.

### 2025

- **MITRA‑zh‑eval: Using a Buddhist Chinese Language Evaluation Dataset to Assess Machine Translation and Evaluation Metrics.** *Sebastian Nehrdich, Avery Chen, Marcus Bingenheimer, Lu Huang, Rouying Tang, Xiang Wei, Leijie Zhu, Kurt Keutzer.* *Proc. 5th Intl. Conf. on NLP for Digital Humanities*, Albuquerque, pp. 129–137. [ACL Anthology](https://aclanthology.org/2025.nlp4dh-1.12/) · DOI: 10.18653/v1/2025.nlp4dh-1.12


---


---

## Contributing


---

## License


---

## Citation


Happy researching! 🚀

