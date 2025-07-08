---

## DharmaNexus

**[DharmaNexus](https://dharmanexus.org)** is a web platform for the exploration of intertextuality for literature preserved in Pāli, Sanskrit, Chinese, and Tibetan. It also functions as the main textual reference database for [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-search) [MITRA Deep Research](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/#mitra-deep-research). Its technical foundation and user interface are a continuation of [BuddhaNexus](https://buddhanexus.net), and it is tightly integrated into MITRASearch and provides modernized algorithms that integrate sophisticated multilingual matching with deep semantic similarity capabilities provided by [Gemma 2 MITRA-E](https://huggingface.co/buddhist-nlp/gemma-2-mitra-e).

---

### How it Works

DharmaNexus helps you find intertextual connections within and between texts in Pāli, Sanskrit, Chinese, and Tibetan.

**1. Select a text:** Choose a language and then select a text to analyze. This is the text from where the exploration starts.

**2. See the matches:** DharmaNexus automatically highlights passages in your text that have similarities in other texts in the database. This is done via a colored heatmap that indicates the amount of textual reuse at a given position. When you click on a highlighted passage, the platform shows you the overlapping text sections from other texts in a new column.

**3. Filter your results:** You can narrow down the matches with filters:

*   **Similarity Score:** Control how similar the text passages should be.
*   **Match Length:** Set a minimum length for matches.
*   **Limit or Exclude:** Focus your search on specific collections or texts.

**4. Choose your view:** DharmaNexus provides different ways to see the results:

*   **Text View:** The default view, showing your text with highlighted matches.
*   **Table View:** A sortable table of all matches.
*   **Graph View:** Charts that visualize where matches are found.
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

The Tibetan textual corpora are obtained from various sources, including the **Asian Classics Input Projects (ACIP)** for the Tibetan Buddhist Canon, and the **[Tsadra Foundation](https://tsadra.org/)'s [Dharma Cloud](https://dharmacloud.tsadra.org/)**.

In close collaboration with the [Tsadra Foundation](https://tsadra.org/), major collections such as the *rin chen gter mdzod*, *rNying ma rgyud ’bum*, and *rNying ma bka’ ma* will be added over time. 

The complete Tibetan data can be found on [GitHub](https://github.com/dharmamitra/dharmanexus-tibetan). 


