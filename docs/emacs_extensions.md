## Emacs Extensions

### Dharmamitra Emacs Extension

The **[Dharmamitra Emacs Extension](https://github.com/dharmamitra/dharmamitra-emacs)** brings the power of Dharmamitra's translation and analysis tools directly into the Emacs environment.

![Screenshot of Dharmamitra grammar analysis](https://github.com/dharmamitra/dharmamitra-emacs/raw/main/screenshot.png)

#### Features

*   Grammar analysis for Sanskrit
*   English translations for Sanskrit, Chinese, Tibetan, Pali
*   Segmentation and lemmatization
*   Detailed grammatical analysis with meanings

#### Installation

1.  Download `dharmamitra.el` from the [repository](https://github.com/dharmamitra/dharmamitra-emacs).
2.  Add the following to your `.emacs` or `init.el`:

```emacs-lisp
;; Add the directory containing dharmamitra.el to load-path
(add-to-list 'load-path "/path/to/directory/containing/dharmamitra")
(require 'dharmamitra)
```

#### Configuration

##### Translation Settings

By default, translations are included in the analysis output. To disable translations (which makes the system significantly faster), add this to your `.emacs`:

```emacs-lisp
(setq dharmamitra-text-include-translation nil)
```

To re-enable translations:

```emacs-lisp
(setq dharmamitra-text-include-translation t)
```

##### Key Bindings

In order to enable the key binding, add this to your `.emacs`:

```emacs-lisp
;; Bind to a different key globally
(global-set-key (kbd "C-c g") #'dharmamitra-text-analyze-grammar)

;; Or bind for specific modes
(add-hook 'sanskrit-mode-hook
          (lambda ()
            (local-set-key (kbd "C-c g") #'dharmamitra-text-analyze-grammar)))
```

#### Usage

1.  Select the text you want to analyze.
2.  Press `C-c g` (or your custom keybinding).
3.  The analysis will appear in a separate buffer showing:
    *   Original text
    *   Segmented form
    *   Lemmatized form
    *   Translation (if enabled)
    *   Detailed grammatical analysis

The analysis buffer will be named `*Dharmamitra Text Grammar*`.

#### Requirements

*   Emacs 26.1 or later
*   `curl` (for API requests)
*   Internet connection to access `dharmamitra.org`

---



---

### Dharmamitra Search

**[Dharmamitra Search](https://github.com/dharmamitra/dharmamitra-search-emacs)**: Comfortable semantic search of the entire [DharmaNexus](https://dharmamitra.github.io/dharmamitra-guides/dharmanexus/) corpus — right from Emacs.

`dharmamitra-search.el` lets you highlight _any_ text in any buffer, hit a single key, and instantly browse cross-lingual search results (Sanskrit · Tibetan · Chinese · Pāli) returned by Dharmamitra's semantic-search API. This brings most of the functionality of [MITRA Search](https://dharmamitra.github.io/dharmamitra-guides/mitra_tools/search/) directly into the emacs editor. 

![Dharmamitra Search Demo](https://github.com/dharmamitra/dharmamitra-search-emacs/raw/main/screenshot.png)

_(screenshot: mark text → `C-c C-d` → clickable results window)_

---

#### ⏳ Installation

##### Manual Installation 

If you don’t use a package manager like `straight.el`, you can install `dharmamitra-search.el` manually in just a few steps:

1.  **Download the file**  
    Clone the repository or download `dharmamitra-search.el` directly and place it in a directory of your choice, for example `~/.emacs.d/lisp/`.

2.  **Add it to your load path**  
    In your `.emacs` or `init.el` file:  
    ```emacs-lisp
    (add-to-list 'load-path "~/.emacs.d/lisp/")  
    (require 'dharmamitra-search)
    ```
3.  **Bind the search command to a key**  
    You can customize this as you like. For example:  
    ```emacs-lisp
    (global-set-key (kbd "C-c C-d") #'dharmamitra-search-region)
    ```
4.  **Optional: Customize settings**  
    Run `M-x customize-group RET dharmamitra-search RET` to adjust the API endpoint or appearance.

##### `straight.el` / `use-package` 

```emacs-lisp
(use-package dharmamitra-search
  :straight (dharmamitra-search
             :type git
             :host github
             :repo "https://github.com/dharmamitra/dharmamitra-search-emacs")
  :bind ("C-c C-d" . dharmamitra-search-region))
``` 