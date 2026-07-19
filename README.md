# Traditional vs. Socratic AI Chatbot Tutoring for Learning Object-Oriented Programming

## Repository structure

```
.
├── README.md                          # this file
├── prompt.md                          # English translation of the Socratic system prompt (as presented in the paper)
├── data/
│   ├── README.md                      # data dictionary, coding notes, and known caveats
│   ├── experiment_config.yaml         # Searchat Behavior platform export (consent form, pre-questionnaire,
│   │                                   #   immediate post-test, task descriptions, Socratic system prompt)
│   ├── participants_consolidated.csv  # one row per participant: demographics, prior-knowledge Likert
│   │                                   #   ratings, open-ended UX answers, test scores, interaction metrics
│   ├── session_transcripts_coded.csv  # turn-by-turn session transcripts with qualitative coding
│   ├── ux_thematic_coding.csv         # thematic coding of open-ended UX answers
│   └── Codebook.md                    # qualitative codebook (in Portuguese — see note below)
└── analysis/
    ├── notebook.ipynb                 # statistical analysis and the paper's difference diagram
    └── requirements.txt               # Python dependencies for the notebook
```

`data/README.md` documents the columns of each CSV file and lists notes on
language, identifiers, and a few known discrepancies between files — read it
before working with the raw data.

## How to reproduce

The analysis notebook only depends on `numpy`, `scipy`, and `matplotlib`.

```bash
cd analysis
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

**Note:** the notebook does not read the CSV files programmatically. The
`score_immediate` / `score_retention` arrays it defines were manually
transcribed from `data/participants_consolidated.csv`, in the same
T1–T6, S1–S6 order used throughout the repository (verified to match
exactly). The notebook computes descriptive statistics, Cliff's delta,
between-group Mann-Whitney U tests, within-group Wilcoxon signed-rank tests,
and produces the individual pre/post difference diagram used in the paper.

## Authors and affiliation

Thiago José Lopes, Yeshuá Silveira de Souza Siqueira, Jairo Francisco de
Souza, Marcelo de Oliveira Costa Machado

LApIC, Universidade Federal de Juiz de Fora (UFJF), Brazil

## License

Not yet finalized in this repository. The suggested licensing split is code
(`analysis/`) under the **MIT License**, and data/instruments
(`data/`, `prompt.md`) under **CC BY 4.0**, pending confirmation by the
authors.

## Citation

```bibtex
@inproceedings{TODO_SBIE2026,
  title     = {TODO: paper title},
  author    = {Lopes, Thiago José and Siqueira, Yeshuá Silveira de Souza and Souza, Jairo Francisco de and Machado, Marcelo de Oliveira Costa},
  booktitle = {Anais do Simpósio Brasileiro de Informática na Educação (SBIE)},
  year      = {2026},
  note      = {To be added upon publication in the SBIE 2026 proceedings.}
}
```
