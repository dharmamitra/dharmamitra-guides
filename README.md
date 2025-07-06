# Dharmamitra: Open Tools for Buddhist Digital Philology

*Accelerating research on Classical Asian source languages with modern machine‑learning workflows.*

---

## Table of Contents

- [About Dharmamitra](#about-dharmamitra)
- [DharmaNexus](#dharmanexus)
- [MITRA Translate](#mitra-translate)
- [MITRA OCR](#mitra-ocr)
- [MITRA Search](#mitra-search)
- [MITRA Dictionaries](#mitra-dictionaries)
- [MITRA Models & API](#mitra-models--api)
  - [ByT5-Sanskrit](#byt5-sanskrit)
- [MITRA Publications](#mitra-publications)
- [Contributing](#contributing)
- [License](#license)
- [Citation](#citation)

---
<div align="center">
  <img src="guides-logo.png" alt="Dharmamitra Logo" width="500">
</div>

## About Dharmamitra

**[Dharmamitra](https://dharmamitra.org)** is a meta‑platform that bundles state‑of‑the‑art NLP, OCR, information‑retrieval, and intertextuality exploration components for anybody working with the Ancient Asian languages Sanskrit, Pāli, Classical Chinese, and Tibetan. All code in this organisation is released under permissive licenses, and we provide large datasets in either public‑domain or under Creative Commons licensing.

---

## DharmaNexus

**[DharmaNexus](https://dharmanexus.org)** is a web platform for the exploration of intertextuality for literature preserved in Pāli, Sanskrit, Chinese, and Tibetan. Its technical foundation and user interface are a continuation of [BuddhaNexus](https://buddhanexus.net), and it is tightly integrated into MITRASearch and provides modernized algorithms that integrate sophisticated multilingual matching with deep semantic similarity capabilities provided by [Gemma 2 MITRA-E](https://huggingface.co/buddhist-nlp/gemma-2-mitra-e).

---

## MITRA Translate

> *Neural machine translation models fine‑tuned for Buddhist domain texts.*
We offer free-for-access machine translation capabilities live at [Dharmamitra](https://dharmanexus.org). 
- **Languages supported:**
  - Sanskrit → English
  - Pāli → English
  - Tibetan → English  
  - Classical Chinese → English

We support translate-from-image, just upload your image to the translator! 
- **English Explained Mode:** 
By setting the target language to `English (Explained)`, additional grammatical explanations are added to the translation, based on dedicated grammatical preprocessing models. These explanations include word segmentation, lemmatization, morpho-syntactic analysis, and context-aware meanings for each word.

- **Model:** Standalone many-to-one translation model is available on 🤗 [Hugging Face](https://huggingface.co/buddhist-nlp/gemma-2-mitra-it).
---

## MITRA OCR
> *High‑accuracy OCR based on Google Gemini engine.*
We now feature fast OCR powered by the Gemini engine for high-accuracy text extraction from Sanskrit, Tibetan, and Chinese typeset documents.

- **Features:**
  - Upload PDFs up to 100MB in size
  - Automatic conversion to IAST/Wylie transliteration when needed
  - Direct image upload to translator for screenshot-to-translation workflow
  - Integrated with MITRA Translate for seamless OCR → translation pipeline


> *Note: We are currently also developing our own customized OCR models optimized specifically for Buddhist texts.*

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

### ByT5-Sanskrit

> *A unified byte-level language model for Sanskrit NLP tasks, achieving state-of-the-art performance on word segmentation, lemmatization, morphosyntactic tagging, and dependency parsing.*

**ByT5-Sanskrit** is a specialized pretrained language model designed for processing the morphologically rich Sanskrit language. Built on the byte-level ByT5 architecture, it eliminates the need for complex tokenization schemes and achieves excellent performance across multiple Sanskrit NLP tasks.

#### Key Features

- **Byte-level Processing**: No complex tokenization required, making it robust to unseen data
- **Multitask Capabilities**: Joint training for word segmentation, lemmatization, and morphosyntactic tagging
- **State-of-the-Art Performance**: Outperforms previous approaches on established Sanskrit NLP benchmarks
- **Versatile Applications**: Used in linguistic annotation, information retrieval, and machine translation pipelines

#### Model Variants

- **Base Model**: Pretrained ByT5-Sanskrit available on [Hugging Face](https://huggingface.co/sebastian-nehrdich/byt5-sanskrit-base)
- **Multitask Model**: Fine-tuned for joint Sanskrit NLP tasks available on [Hugging Face](https://huggingface.co/sebastian-nehrdich/byt5-sanskrit-multitask)

#### Python Package

For easy integration, we provide the **Dharmamitra Sanskrit Grammar** Python package:

```bash
pip install dharmamitra-sanskrit-grammar
```

This package offers a simple API for accessing the model's capabilities without running the full model locally.



#### Repository

The complete inference scripts and applications are available in the [ByT5-Sanskrit Analyzers repository](https://github.com/sebastian-nehrdich/byt5-sanskrit-analyzers), which includes various downstream applications and usage examples.

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

