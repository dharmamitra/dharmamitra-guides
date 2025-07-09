## MITRA Translate

> *Neural machine translation models fine‑tuned for Buddhist domain texts available live at [Dharmamitra](https://dharmamitra.org).*  
<div align="center">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/jt2-ZDRahOQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

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