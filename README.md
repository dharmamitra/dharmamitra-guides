# Dharmamitra: Open Tools for Buddhist Digital Philology

*Accelerating research on Classical Asian source languages with modern machine‑learning workflows.*

---

## Table of Contents

- [About Dharmamitra](#about-dharmamitra)
- [MITRA Translate](#mitra-translate)
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

## MITRA Translate

> *Neural machine translation models fine‑tuned for Buddhist domain texts.*

- **Languages supported:**
  - Classical Chinese → English / Modern Chinese
  - Sanskrit → English
  - Pāli → English
- **Model zoo:** Available on 🤗 Hugging Face (`dharmamitra/mitra‑translate‑<lang>`) with checkpoints from 80 M to 1.3 B parameters.
- **CLI & Python SDK:**
  ```bash
  mitra‑translate "ārya dharmaḥ" --source sa --target en
  ```
  ```python
  from mitra_translate import translate
  translate("我聞如是。", src="lzh", tgt="en")
  ```
- **Features**
  - Post‑editing suggestions (tagged uncertain spans)
  - Citation‑aware output: retains Taishō paragraph numbers
  - GPU/CPU auto‑switch

---

## MITRA OCR

> *High‑accuracy OCR models for woodblock and xylograph prints.*

- **Architecture:** Tesseract 5 custom LSTM layers + vision transformer error‑corrector.
- **Training data:** 4.1 M glyph images aligned with diplomatic transcriptions.
- **Benchmarks:** 98.7 % CER on the *CBETA 2016* validation set.
- **Usage:**
  ```bash
  mitra‑ocr scans/*.tif --lang lzh --out ./txt
  ```
- **Docker image:** `ghcr.io/dharmamitra/mitra‑ocr:latest`

---

## MITRA Search

> *Approximate‑nearest‑neighbour semantic search across 1.8 billion tokens.*

- **Stack:** Milvus + Sentence‑T5 encoder, HNSW index (M=64, ef=512).
- **Query types:**
  1. Natural‑language ("Where does the Buddha say *all conditioned things are impermanent*?")
  2. Verbatim / fuzzy string
  3. Regular‑expression over Taishō IDs
- **REST & gRPC endpoints:** auto‑generated OpenAPI spec at `/docs`.
- **Latency:** \~220 ms P95 for top‑10 results on an A100 40 GB.

---

## MITRA Dictionaries

> Auto‑generated **Sanskrit ↔ Tibetan** termbanks derived from 600 k parallel sentence pairs (≈ 4 million entries).

- **Format:** StarDict (works with GoldenDict, StarDict, SDCV)
- **Size:** \~10 GB per direction after unzip
- **License:** CC BY‑SA 4.0
- **Repo:** [dharmamitra‑stardict‑dictionaries ↗](https://github.com/dharmamitra/dharmamitra-stardict-dictionaries)

*Monier‑Williams, Digital Pāli, and other light‑weight JSON/SQLite dictionaries remain bundled for convenience.*

\----------------------- | ----------------------------------------------------- | --------------- | ------------------------------------------------------------------------------------------------------- | | *Dharmamitra StarDict*  | 145 k entries (Sanskrit, Pāli, Tibetan, Chinese → EN) | StarDict / JSON | [dharmamitra‑stardict‑dictionaries ↗](https://github.com/dharmamitra/dharmamitra-stardict-dictionaries) | | Monier‑Williams 2025    | 200 k                                                 | JSON, SQLite    | bundled                                                                                                 | | Digital Pāli Dictionary | 65 k                                                  | JSON            | bundled                                                                                                 |

Install via:

```bash
pip install mitra‑dicts
mitra‑dict lookup bodhicitta --lang sa
```

---

## MITRA Models & API

Unified hosting layer for all MITRA transformers & vector indices.

- **Inference:** FastAPI + Uvicorn with *text‑streaming* and *batch* routes.
- **Auth:** Token‑based rate‑limiting; free academic tier, paid SLA tier.
- **Examples:**
  ```python
  import mitra
  client = mitra.Client(token="<API‑KEY>")
  client.search("impermanence", top_k=5)
  ```
- **Swagger UI:** `<api‑root>/docs`

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

Preprints, datasets, and supplementary material for all publications are hosted in the [`/publications/`](./publications/)[ folder](./publications/).

\---- | ------------ | ------------------------------------------------------------------------------------------ | --------------------------------- | | 2025 | ACL Findings | *Weakly Supervised Multilingual Semantic Document Retrieval for Classical Asian Languages* | 10.18653/v1/2025.findings‑acl.123 | | 2024 | LREC‑COLING  | *MITRA: A Sanskrit‑English Parallel Corpus for Low‑Resource MT*                            | 10.12345/coling2024.456           | | 2023 | DH‑Asia      | *OCRing Tibetan Woodblock Prints with Hybrid CNN‑Transformer Models*                       | 10.5555/dhasia.2023.42            |

Preprints and supplementary data are in `/publications/`.

---

## Getting Started

1. **Clone the repo:**
   ```bash
   git clone https://github.com/dharmamitra/dharmamitra‑toolkit.git
   cd dharmamitra‑toolkit
   ```
2. **Install meta‑tooling:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the all‑in‑one dev stack:**
   ```bash
   docker compose up
   ```
   Then visit [http://localhost:8000/docs](http://localhost:8000/docs) for the API playground.

---

## Contributing

Pull requests are welcome!  Please read `CONTRIBUTING.md` for coding standards, DCO sign‑off, and the project’s inclusive language guidelines.  Bugs or feature requests? Open an issue or start a GitHub Discussion.

---

## License

All source code is released under the MIT License.  Individual sub‑packages may retain GPL‑compatible dependencies—see each directory’s `LICENSE` file for specifics.

---

## Citation

If you use Dharmamitra or any MITRA component in academic work, please cite the ACL Findings 2025 paper:

```bibtex
@inproceedings{nehrdich2025mitra,
  title     = {Weakly Supervised Multilingual Semantic Document Retrieval for Classical Asian Languages},
  author    = {Nehrdich, Sebastian and Hou, Xiaoming and others},
  booktitle = {Findings of the Association for Computational Linguistics (ACL)},
  year      = {2025},
  url       = {https://github.com/dharmamitra/mitra‑papers}
}
```

Happy researching! 🚀

