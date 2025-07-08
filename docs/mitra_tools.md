## MITRA Translate

> *Neural machine translation models fine‑tuned for Buddhist domain texts available live at [Dharmamitra](https://dharmamitra.org).*  

We offer free-for-access machine translation capabilities live at [Dharmamitra](https://dharmanexus.org). 

### Languages supported
- Sanskrit → English
- Pāli → English
- Tibetan → English
- Classical Chinese → English

We support translate-from-image, just upload your image to the translator!  

**English Explained Mode:** 
By setting the target language to `English (Explained)`, additional grammatical explanations are added to the translation, based on dedicated grammatical preprocessing models. These explanations include word segmentation, lemmatization, morpho-syntactic analysis, and context-aware meanings for each word.

**Model:** Standalone many-to-one translation model is available on 🤗 [Hugging Face](https://huggingface.co/buddhist-nlp/gemma-2-mitra-it).

---

## MITRA Sanskrit Grammar

> *Advanced grammatical analysis for Sanskrit texts with Sandhi segmentation, lemmatization, and detailed morphological annotations available live at [Dharmamitra](https://dharmamitra.org).*

We provide comprehensive grammatical analysis capabilities for Sanskrit powered by the state-of-the-art [ByT5-Sanskrit](https://dharmamitra.github.io/dharmamitra-guides/mitra_models/#byt5-sanskrit) model.

### Features
- **Sandhi Segmentation**: Automatic breaking down of compound words and Sandhi formations
- **Lemmatization**: Identification of base forms and dictionary entries for each word
- **Grammatical Tags**: Detailed morphological analysis including case, gender, number, tense, mood, and voice
- **Lexical Candidates**: Multiple possible meanings and interpretations for each word
- **Interactive Interface**: Click the 'grammar' button after entering Sanskrit text to access detailed annotations

### How to Use
- Enter a Sanskrit sentence into the translation field at [Dharmamitra](https://dharmamitra.org)
- Click the 'grammar' button that appears
- A side menu opens displaying comprehensive grammatical analysis including Sandhi segmentation, lemmatization, and grammatical tags
- Explore lexical candidates and morphological details for each word!

### Technical Details
[ByT5-Sanskrit](https://dharmamitra.github.io/dharmamitra-guides/mitra_models/#byt5-sanskrit) is a grammatical annotation model trained on the [Digital Corpus of Sanskrit](http://www.sanskrit-linguistics.org/) by Oliver Hellwig

---

## MITRA OCR
> *Fast OCR powered by the Gemini engine for high-accuracy text extraction from Sanskrit, Tibetan, and Chinese typeset documents available live at [Dharmamitra](https://dharmamitra.org).* 

### Features
- Upload PDFs up to 100MB in size
- Automatic conversion to IAST/Wylie transliteration when needed
- Direct image upload to translator for screenshot-to-translation workflow
- Integrated with MITRA Translate for seamless OCR → translation pipeline

> *Note: We are currently also developing our own customized OCR models optimized specifically for Buddhist texts.*

---

## MITRA Search
> *Semantic search across document collections in Pāli, Sanskrit, Tibetan, and Chinese available live at [Dharmamitra](https://dharmanexus.org).*

### Features
- Powerful semantic search using state-of-the-art multilingual embedding models and sophisticated linguistic preprocessing 
- search for semantically related passages in the same language and across different languages (Sanskrit to Tibetan, Pāli to Chinese etc.)
- Search for high-level concepts and ideas expressed in modern languages like English 
- Filter options to narrow down results to language, collection, category, and even individual text
- Results link directly into [DharmaNexus](https://dharmanexus.org), where further multilingual parallels and intertextuality can be explored. 

---

## MITRA Deep Research

> *Advanced translation mode that provides comprehensive research context by integrating deep semantic search across entire data collections.*

**MITRA Deep Research** is an enhanced translation experience that goes beyond simple text translation. By setting the target language in MITRA Translate to `Deep Research`, users receive not just a translation, but also comprehensive semantic analysis that leverages the full power of [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search) and [DharmaNexus](https://dharmanexus.org).

### Features
- **Comprehensive Translation**: Enhanced translations that incorporate semantic search results from across all language collections
- **Parallel Discovery**: Automatic identification of parallel passages, translations, and related texts in different languages
- **Contextual Analysis**: Deep semantic search reveals how concepts are expressed across the entire corpus
- **DharmaNexus Integration**: Direct links to [DharmaNexus](https://dharmanexus.org) for exploring intertextual relationships and multilingual parallels
- **Topical Queries**: Support for topical questions like "the definition of cetanā" with comprehensive literature evidence
- **Evidence-Based Results**: All additional information is sourced from the extensive DharmaNexus database  
- **Integration of Relevant Passages from Secondary Literature**: MITRA Deep Research will automatically check for relevant passages in secondary literature and cite it if good matches appear

This mode provides a significantly superior translation experience by incorporating possibly relevant textual evidence and deeper context, making it ideal for serious translation, research, and academic work.

--- 

# FAQ: MITRA Tools & [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/)

## MITRA Tools

**Q: What languages does MITRA Translate support?**  
A: Sanskrit, Pāli, Tibetan, and Classical Chinese to English. "English (Explained)" mode provides grammatical explanations.

**Q: Can I translate text from images or PDFs?**  
A: Yes! You can upload images or PDFs (up to 100MB) for OCR and translation. The system supports direct screenshot-to-translation workflows.

**Q: What is "English (Explained)" mode?**  
A: This mode adds grammatical explanations, including word segmentation, lemmatization, and morpho-syntactic analysis, to the translation.

**Q: How do I access Sanskrit grammatical analysis?**  
A: Enter Sanskrit text and click the 'grammar' button to see detailed analysis, including Sandhi segmentation and lemmatization.

**Q: Is there a browser extension?**  
A: Yes, MITRA browser extensions for Chrome and Firefox allow instant translation and grammatical analysis on any webpage.

**Q: Are the tools free to use?**  
A: Yes, all MITRA tools are free for access at [Dharmamitra](https://dharmamitra.org).

---

## [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/)

**Q: What is [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/)?**  
A: [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/) is a web platform for exploring intertextuality in Buddhist literature across Pāli, Sanskrit, Chinese, and Tibetan. It powers [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search) and [MITRA Deep Research](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-deep-research).

**Q: How does [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/) find parallels?**  
A: It uses advanced semantic search and multilingual matching to highlight similar passages across texts and languages.

**Q: What data sources does [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/) use?**  
A: [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/) draws from SuttaCentral, CBETA, DSBC, GRETIL, Muktabodha, ACIP, and more, with ongoing data expansion.

**Q: Can I filter or customize my search?**  
A: Yes, you can filter by similarity score, match length, collection, and text. Multiple result views (text, table, graph, numbers) are available.

**Q: Is [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/) integrated with MITRA tools?**  
A: Yes, [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search) and [MITRA Deep Research](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-deep-research) use [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/) for semantic search and parallel discovery. 