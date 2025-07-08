---

## DharmaNexus

**[DharmaNexus](https://dharmanexus.org)** is a multilingual text database for Classical Asian languages that serves as the foundation for the Dharmamitra platform. It hosts our ever-growing collection of texts in Pāli, Sanskrit, Chinese, and Tibetan and is tightly integrated with [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search) and [MITRA Deep Research](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-deep-research). This provides advanced fuzzy, semantic, and cross-lingual search capabilities, and is one of the few databases that provide search capabilities over large Sanskrit collections. 

In addition to its role as a database, DharmaNexus offers a web platform for exploring intertextuality between these texts, in monolingual as well as multilingual settings. This feature, along with its technical foundation, is a continuation of the [BuddhaNexus](https://buddhanexus.net) project. It employs modernized algorithms that combine multilingual matching with deep semantic similarity from [Gemma 2 MITRA-E](https://huggingface.co/buddhist-nlp/gemma-2-mitra-e).


---
 

### Getting Started

DharmaNexus offers a **simple and intuitive way to explore vast collections of Buddhist texts** in Pāli, Sanskrit, Chinese, and Tibetan.

1. **Choose your language:** Start by selecting your preferred language from the main interface.
2. **Select a text:** Browse the available menu to quickly find a text of interest. Whether you know exactly what you're looking for or just want to explore, DharmaNexus makes navigation easy. You can browse the collections with their individual categories to get to a text, or you can type in the name of the text or the catalog number you are looking for to jump in directly. For full text and semantic search, you can of course use [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search) to jump directly to a passage that you are interested in. 

3. **Read and navigate:** The platform opens your chosen text in a clean reading view. You can:
   - **Scroll** through the content
   - **Jump to specific sections** using standard numbering systems (e.g., SuttaCentral or Taishō numbers, or Derge folio numbers)
   - **Switch between texts** via the 'change text' option that opens the main menu again
4. **Customize your view:**
   - Read in the original script or in transliteration
 
> _Whether you are a scholar, translator, or simply curious, DharmaNexus makes it easy to navigate and read through large multilingual digital collections of Classical Asian literature in Pāli, Sanskrit, Chinese, and Tibetan._

### How Intertextuality Exploration Works 

DharmaNexus helps you find intertextual connections within and between texts in Pāli, Sanskrit, Chinese, and Tibetan.

**1. See the matches:** While reading, you can choose to reveal intertextual connections by toggling the **Show Matches** switch. When enabled, DharmaNexus highlights passages in your text that have similarities in other texts in the database. 
   - After clicking on such a highlighted text passage, the matches with other texts are then shown in a new column. Hovering over a parallel will highlight the corresponding segment in the source text.
   - Clicking on a specific parallel will open that text in a **third column**, allowing you to compare the two texts side-by-side.

**2. Filter your results:** You can narrow down the matches with filters:

*   **Similarity Score:** This controls how similar a passage must be to be considered a match. A score of 100 indicates a perfect, verbatim match, while a lower score allows for more variation, showing passages that are semantically similar but not identical.
*   **Match Length:** Sets the minimum number of characters for a parallel. You might use a shorter length when looking for verse parallels and a longer one for prose to ensure the matches are significant.
*   **Limit or Exclude:** Focus your search by including or excluding specific collections or texts. For example, you could exclude all commentaries to see only parallels within the canonical texts.

**3. Choose your view:** DharmaNexus provides different ways to see the results:

*   **Text View:** The default view, showing your text with highlighted matches.
*   **Table View:** A sortable table of all matches, which can be downloaded as a spreadsheet.
*   **Graph View:** Visualizes the distribution of matches for your selected text via a histogram. This chart shows which other texts or collections contain the most parallels, helping you quickly identify the most relevant connections at a glance.
*   **Numbers View:** Uses standard numbering systems to locate matches in Pāli and Chinese texts.

---

### Underlying Data

#### Pāli

The Pāli textual corpus in DharmaNexus is drawn from several high-quality digital editions:

*   The core canonical texts (Sutta, Vinaya, and Abhidhamma) are sourced from [SuttaCentral](https://suttacentral.net/)'s segmented texts from their [bilara-data](https://github.com/suttacentral/bilara-data) repository. This allows for precise linking to SuttaCentral.
*   The commentarial literature (Aṭṭhakathā, Ṭīkā, and Anya) is from the Chaṭṭha Saṅgāyana edition published by the [Vipassana Research Institute (VRI)](https://tipitaka.org/).

The complete Pāli data can be found on [GitHub](https://github.com/dharmamitra/dharmanexus-pali).

#### Sanskrit

The Sanskrit corpus is extensive and has been gathered from multiple academic projects:

*   [Göttingen Register of Electronic Texts in Indian Languages (GRETIL)](http://gretil.sub.uni-goettingen.de/gretil.html)
*   [Digital Sanskrit Buddhist Canon (DSBC)](https://www.dsbcproject.org/)
*   [Muktabodha Indological Research Institute](https://muktabodha.org/)
*   [SuttaCentral](https://suttacentral.net/)

The complete Sanskrit data can be found on [GitHub](https://github.com/dharmamitra/dharmanexus-sanskrit).

We also do our own independent data collection efforts within the Dharmamitra project. The Sanskrit collection is therefore growing constantly. 
#### Chinese

The Chinese textual corpus was obtained from the [Chinese Buddhist Electronic Text Association (CBETA)](https://cbeta.org/).

The complete Chinese data can be found on [GitHub](https://github.com/dharmamitra/dharmanexus-chinese).

#### Tibetan

The Tibetan textual corpora are obtained from various sources, including the Asian Classics Input Projects (ACIP) for the Tibetan Buddhist Canon, and the [Tsadra Foundation](https://tsadra.org/)'s [Dharma Cloud](https://dharmacloud.tsadra.org/).

In close collaboration with the [Tsadra Foundation](https://tsadra.org/), major collections such as the *rin chen gter mdzod*, *rNying ma rgyud ’bum*, and *rNying ma bka’ ma* will be added over time. 

The complete Tibetan data can be found on [GitHub](https://github.com/dharmamitra/dharmanexus-tibetan). 


### Technical Background 

DharmaNexus uses the ByT5-Sanskrit model for word segmentation of Sanskrit texts from various text collections (See Sanskrit data description), which are then indexed on [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search), which has access to all the data available in DharmaNexus. For Tibetan, a special substitution-based stemmer based on [Paul Hackett's Tibetan Verb Lexicon](https://www.shambhala.com/a-tibetan-verb-lexicon-15252.html?srsltid=AfmBOoqO0LtadFcogdBf_YR8L207hBf8ycgHiyKw259R3TrLebxZJgjt) is used. Pāli uses a slightly adapted version of the ByT5-Sanskrit model for word segmentation. For Chinese, we use the standard analyzers provided by Elasticsearch. In addition to token-based search, DharmaNexus is also searchable in [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search) via deep semantic embeddings on sentence and paragraph level.

---

## FAQ

For frequently asked questions about DharmaNexus, see the [DharmaNexus section](https://dharmamitra.github.io/dharmamitra-guides/faq/#mitra-search-dharmanexus) in our main FAQ document.  