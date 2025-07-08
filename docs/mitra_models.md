## MITRA Models & API

### ByT5-Sanskrit

> *A unified byte-level language model for Sanskrit NLP tasks, achieving state-of-the-art performance on word segmentation, lemmatization, morphosyntactic tagging, and dependency parsing.*

**ByT5-Sanskrit** is a specialized pretrained language model designed for processing the morphologically rich Sanskrit language. Built on the byte-level ByT5 architecture, it eliminates the need for complex tokenization schemes and achieves excellent performance across multiple Sanskrit NLP tasks. The model was trained on data from Oliver Hellwig's [Digital Corpus of Sanskrit (DCS)](http://www.sanskrit-linguistics.org/) and follows the annotation standards established by that corpus.

**Publication**: *One Model is All You Need: ByT5-Sanskrit, a Unified Model for Sanskrit NLP Tasks* ([EMNLP 2024](https://aclanthology.org/2024.findings-emnlp.805/))

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