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

The repository is organized to clearly separate data resources, processing logic, experimental components, and the public-facing website. This structure is designed to support both linguistic data curation and future NLP model development.

.
├── data/
│   ├── raw/                 # Original dictionary and bilingual resources
│   ├── cleaned/             # Cleaned and normalized Dongxiang–Chinese data
│   ├── aligned/             # Aligned word- and sentence-level bilingual pairs
│   └── metadata/            # Linguistic tags, annotations, and auxiliary files
│
├── scripts/
│   ├── preprocessing/       # Data cleaning, normalization, and deduplication
│   ├── alignment/           # Word and sentence alignment utilities
│   └── evaluation/          # Analysis and evaluation scripts
│
├── models/
│   ├── baselines/           # Dictionary-based and rule-based translation methods
│   └── neural/              # Experimental neural translation models (WIP)
│
├── website/
│   ├── public/              # Static assets for the GitHub Pages site
│   └── src/                 # Website source files and configuration
│
├── docs/                    # Project documentation and technical notes
├── README.md                # Project overview and usage instructions
└── LICENSE                  # Open-source license


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
