## MITRA Translate

> *Neural machine translation models fine‑tuned for Buddhist domain texts available live at [Dharmamitra](https://dharmamitra.org).*  

<span style="color: #990000; font-weight: bold;">The user guides currently available on this website do not yet reflect the updated Dharmamitra user interface. We appreciate your patience while our team is actively working on revising them.</span>

We offer free-for-access machine translation capabilities live at [Dharmamitra](https://dharmanexus.org). Currently, our main model uses a combination of in-context-learning and the Gemini API. 

### Languages supported
- Sanskrit → English
- Pāli → English
- Tibetan → English
- Classical Chinese → English

We primarily focus on English as the target language, but support for other languages is growing. Notably, Korean is also well-supported due to a large user base.

We support translate-from-image, just upload your image to the translator!  

**English Explained Mode:** 
By setting the target language to `English (Explained)`, additional grammatical explanations are added to the translation, based on dedicated grammatical preprocessing models. These explanations include word segmentation, lemmatization, morpho-syntactic analysis, and context-aware meanings for each word.

**Model:** Standalone many-to-one translation model is available on 🤗 [Hugging Face](https://huggingface.co/buddhist-nlp/gemma-2-mitra-it). 
