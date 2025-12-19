# Dongxiang–Chinese Translation Project

## Project Overview

The **Dongxiang–Chinese Translation Project** is an open, non-profit initiative dedicated to building high-quality bilingual resources and translation tools for Dongxiang, a low-resource and underrepresented language, with the goal of supporting language preservation, accessibility, and computational research.

## Background

Dongxiang (Santa) is a minority language spoken primarily in **Gansu Province, China**. Due to the scarcity of digitized corpora and linguistic resources, Dongxiang is considered a low-resource language in the field of Natural Language Processing (NLP). This project aims to bridge that gap by systematically constructing bilingual dictionaries, aligned sentence data, and experimental translation systems between **Dongxiang and Chinese**, while also providing a public-facing platform for cultural and linguistic dissemination.

## Key Features

- **Dongxiang ↔ Chinese bilingual translation system** supporting word-level and sentence-level translation, designed specifically for low-resource language settings;
- **Carefully curated Dongxiang–Chinese dictionary**, with systematic cleaning, normalization, and disambiguation to improve linguistic clarity and computational usability;
- **NLP-oriented dataset design**, enabling downstream tasks such as machine translation, alignment, and representation learning;
- **Public-facing web platform**, providing accessible translation tools while promoting Dongxiang language and cultural awareness;
- **Extensible and research-friendly project structure**, allowing seamless integration of new data, models, and evaluation strategies.

## Project Structure

```bash
.
├── about.html                                          # Project website
├── bilingual.html                
├── customs.html                
├── dictionary.html                
├── history.html                
├── index.html
├── overview.html
├── status.html
├── 404.html                  
│
├── photos/                                             # Images used by the website and documentation
│
├── src/                                                # Source code and data for the translation project
│   ├── Dongxiang_bilingual_book_process.ipynb          # Processes bilingual book data
│   ├── Dongxiang_dictionary_process_and_analysis.ipynb # Parses and analyzes the raw Dongxiang–Chinese dictionary
│   ├── Dongxiang_unpublished_data_process.ipynb        # Processes unpublished Dongxiang language data
│   ├── NLLB_training(Chinese___Dongxiang).ipynb        # Fine-tunes an NLLB model for Chinese → Dongxiang translation
│   ├── NLLB_training(Dongxiang___Chinese).ipynb        # Fine-tunes an NLLB model for Dongxiang → Chinese translation
│   ├── Test.ipynb                                      # Testing and exploratory experiments
│   ├── word_search.ipynb                               # Converts the raw dictionary into a searchable display
│   │
│   └── data/                                           # Linguistic data resources
│       ├── Dongxian_Dictionary11.txt                   # Raw Dongxiang–Chinese dictionary 
│       ├── df_bilingual_book.csv                       # Processed bilingual book data
│       ├── df_interior.csv                             # Processed internal dataset
│       ├── 东乡语366句会话句 少数民族语汉英日俄对照.txt   # Raw bilingual book
│       ├── 东乡语料文字部分1.txt                        # Raw internal dataset
│       ├── 东乡语料文字部分2.txt                        # Raw internal dataset
│       └── word_search.csv                             # CSV derived from Dongxian_Dictionary11.txt for word lookup
│
├── README.md                                           # Project overview and usage instructions
└── LICENSE                                             # Open-source license
```

## Data Description

The Dongxiang–Chinese Translation Project is built on both lexical and sentence-level bilingual data. At the lexical level, a Dongxiang–Chinese dictionary is used to construct a searchable word lookup engine. The dictionary is also used in our EDA process. At the sentence level, bilingual training data is compiled from publicly published materials, as well as internal datasets provided by the Dongxiang County government and Mr. Chen Yuanlong. These sources offer aligned Dongxiang–Chinese sentence pairs suitable for downstream translation modeling. We provide both raw and cleaned datasets to support transparency, reproducibility, and flexible reuse for further experiments and modeling.

## Models

We build our translation system on top of **NLLB-200-distilled-600M**, a multilingual neural machine translation model released by Meta as part of the No Language Left Behind (NLLB) project. NLLB-200 is designed to support translation across more than 200 languages, with a particular emphasis on low-resource and underrepresented languages. This broad multilingual coverage makes the model a practical and principled choice for low-resource translation research.

Our model was fine-tuned using **42,868 Dongxiang–Chinese bilingual sentence pairs**, which were processed and cleaned in previous steps. Given the limited size of the training corpus, fine-tuning the baseline NLLB model is more appropriate than introducing aggressive architectural modifications. We used Adafactor as the optimizer during training. Adafactor is a memory-efficient adaptive optimization algorithm. Benefiting from the distilled model size and the use of Adafactor, the full fine-tuning process can be completed within 12 hours on a single NVIDIA A100 GPU, and can also be executed on Google Colab.

All relevant training configurations, hyperparameters, and experiment settings are documented in detail across **two NLLB Jupyter notebooks (`.ipynb`)** included in the repository. An early stopping mechanism was initially planned to prevent overfitting; however, due to the limited size and variability of the training data, the validation loss did not exhibit stable or informative behavior. As a result, early stopping was effectively disabled through our hyperparameter settings.

## How to use 

## Why This Project Matters

## Roadmap

## License and Data Usage

This project is an open, non-profit initiative intended for research, educational, and language preservation purposes only. Unless otherwise stated, the source code and project materials are provided under the **MIT License**.
Please refer to the `LICENSE` file for full license text.

### Data Usage Statement

All datasets released as part of this project have been reviewed and published with appropriate consent.
The Dongxiang–Chinese linguistic data, including dictionary entries and aligned text resources, are shared with the permission of relevant contributors and are intended to support low-resource language research and cultural preservation.

## Acknowledgements

This project would not have been possible without the generous support of institutions and individuals dedicated to the documentation and preservation of the Dongxiang language.

We would like to express our sincere gratitude to:

- The People’s Government of Dongxiang County for its support of Dongxiang language documentation and preservation efforts.
- Mr. Chen Yuanlong (陈元龙), Deputy Director of the United Front Work Department of the Gansu Provincial Party Committee, one of the compilers of the *Dongxiang–Chinese Dictionary*, who oversaw the collection and provision of relevant internal Dongxiang–Chinese bilingual datasets for this project.

We are grateful to everyone who supports open research, linguistic diversity, and responsible data sharing.
