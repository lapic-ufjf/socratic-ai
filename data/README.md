# Data

This directory contains the experiment configuration exported from the
Searchat Behavior platform and the resulting participant data, session
transcripts, and qualitative coding used in the paper.

## Files

### `experiment_config.yaml`

Full export of the experiment as configured on the Searchat Behavior
platform. Includes:

- `icf` — the informed consent form (TCLE) text, with researcher names and
  institutional affiliation.
- `surveys` — the pre-questionnaire (`type: pre`, name "Questionário":
  demographics, prior OOP experience, and Likert self-assessments of prior
  knowledge of inheritance, polymorphism, and abstract classes) and the
  immediate post-test (`type: post`, name "Mostre o que você aprendeu!": ten
  open-ended conceptual questions).
- `tasks` — the two experimental conditions, each with its task description
  and, for the Socratic condition, the `systemInstruction` given to the
  model. The Traditional condition task is titled
  `(N) Herança, Polimorfismo e Classes Abstratas`; the Socratic condition is
  titled `(S) Herança, Polimorfismo e Classes Abstratas`.

The **delayed retention test is not included in this file** — only the
pre-questionnaire and the immediate post-test are exported here. The
resulting retention scores are still available in
`participants_consolidated.csv` (`score_retention`), but the instrument
(question wording) itself is not present in this repository. The
instrument for the open-ended UX questions answered in
`participants_consolidated.csv` (`q_overall_experience` and related columns)
is likewise not present in this file.

The Socratic system prompt in this file (`systemInstruction`) is in
Portuguese, as it was actually used in the study. `prompt.md` at the
repository root is the English translation presented in the paper.

### `participants_consolidated.csv`

One row per participant (n = 12). Row order follows the participant IDs used
in Table 1 of the paper.

| Column | Description | Original question (pt-BR) |
|---|---|---|
| `participant_id` | Paper identifier (T1–T6, S1–S6) | — |
| `group` | Condition: `T` = Traditional, `S` = Socratic | Grupo |
| `age_range` | Age range | Idade |
| `program` | Undergraduate program | Curso |
| `prior_oop_experience` | Previous contact with OOP | Você já estudou orientação a objetos anteriormente? |
| `prior_knowledge_inheritance` | Likert self-assessment | Avalie seu nível de concordância com a afirmação: Eu tenho conhecimento sobre herança em orientação a objetos. |
| `prior_knowledge_polymorphism` | Likert self-assessment | Avalie seu nível de concordância com a afirmação: Eu tenho conhecimento sobre polimorfismo em orientação a objetos. |
| `prior_knowledge_abstract_classes` | Likert self-assessment | Avalie seu nível de concordância com a afirmação: Eu tenho conhecimento sobre classes abstratas em orientação a objetos. |
| `q_overall_experience` | Open-ended UX question 1 | Como você descreveria sua experiência utilizando a ferramenta de chat para aprender os conteúdos da atividade? |
| `q_knowledge_adequacy` | Open-ended UX question 2 | Você acredita que a interação com a ferramenta forneceu conhecimento suficiente para responder ao pós-questionário? Justifique sua resposta. |
| `q_interaction_strategy` | Open-ended UX question 3 | Como você descreveria a forma como a ferramenta respondia às suas perguntas? O que você achou dessa forma de interação? |
| `q_additional_comments` | Open-ended UX question 4 | Gostaria de acrescentar algum comentário, percepção ou experiência que não tenha sido contemplado nas perguntas anteriores? |
| `score_immediate` | Immediate post-test score, normalized to [0, 1] | Questionário Pós Intervenção |
| `score_retention` | Delayed retention test score (one week later), normalized to [0, 1] | Questionário de Retenção |
| `interaction_time_seconds` | Total interaction time in seconds | Tempo de Interação (segundos) |
| `prompt_count` | Number of prompts submitted | Quantidade de prompts disparados |

Likert scale mapping used in the paper: Discordo totalmente = −2, Discordo
parcialmente = −1, Neutro = 0, Concordo parcialmente = +1, Concordo
totalmente = +2.

### `session_transcripts_coded.csv`

Turn-by-turn transcripts of the chat sessions (334 coded turns across all 12
participants) with qualitative coding applied. See `Codebook.md` for the
coding scheme.

| Column | Description |
|---|---|
| `participant_id` | Paper identifier (T1–T6, S1–S6) |
| `tarefa` | Task/condition label as recorded during coding, e.g. `(S) Herança, Polimorfismo e Classes Abstratas`. Note: the Traditional condition is recorded here as `(T) ...`, not `(N) ...` as in `experiment_config.yaml` — see the note in the main README. |
| `papel` | Turn role: `user` or `model` |
| `mensagem` | Raw message text (pt-BR) |
| `codificacao aberta` | Open, inductive first-pass coding notes (free text) |
| `codigos interpretativos` | Interpretive code(s) reported in the paper (Tables 4 and 5 — see `Codebook.md` §1). Turns may carry multiple codes, separated by `;` or `+`. Left empty for uncoded turns (mostly `model` turns). |
| `codigo descritivo` | Descriptive utterance-type code, **not reported in the paper** (see `Codebook.md` §2). Free text; contains some inconsistent casing and a few typos in the source data. |
| `evidencia` | Supporting note/evidence for the coding decision (often empty) |

### `ux_thematic_coding.csv`

Thematic coding of the open-ended UX answers from
`participants_consolidated.csv` (19 coded excerpts).

| Column | Description |
|---|---|
| `participant_id` | Paper identifier (T1–T6, S1–S6) |
| `group` | Condition: `T` = Traditional, `S` = Socratic |
| `category` | Thematic category. Four categories appear in the data: `Atribuição de responsabilidade pelo aprendizado`, `Natureza da interação percebida`, `Percepção do papel pedagógico do chatbot`, and `Aceitação positiva da ferramenta`. **The fourth category, "Aceitação positiva da ferramenta", is not reported in the paper.** |
| `evidence` | Quoted excerpt (pt-BR) supporting the category assignment |

### `Codebook.md`

The qualitative codebook, in Portuguese — the language of the analysis. It
documents both the seven interpretive codes reported in the paper (with a
Portuguese↔English name mapping) and the descriptive utterance-type
classification that is not reported in the paper.

## Notes

- Raw data, transcripts, and qualitative coding are in Portuguese, the
  language in which the study was conducted.
- `participant_id` (T1–T6, S1–S6) matches the identifiers used in the
  paper's tables, figure, and quotes.
- The dataset includes two classifications **not** reported in the paper:
  the descriptive utterance-type classification ("tipo de enunciado") in
  `session_transcripts_coded.csv`, and the fourth thematic category
  ("Aceitação positiva da ferramenta") in `ux_thematic_coding.csv`.
