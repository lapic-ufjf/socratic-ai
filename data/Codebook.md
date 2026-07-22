# Codebook — Qualitative Analysis

Coding scheme developed inductively for the analysis of the session transcripts
(`session_transcripts_coded.csv`). It contains two classifications:

1. **Interpretive codes** — reported in the paper (Tables 4 and 5), applied in the
   `interpretive_codes` column.
2. **Utterance types** — complementary descriptive classification, not reported in the
   paper, applied in the `utterance_type` column.

> **Note on language.** The study was conducted in Portuguese, so the transcripts and the
> code labels inside the CSV files are in Portuguese (column headers are in English). The
> table below maps each label as it appears in the data to the name used in the paper.

| Label in the CSV (pt-BR) | Code (paper) |
|---|---|
| Elaboração Ativa | Active Elaboration |
| Sinalização de Dificuldade | Difficulty Signaling |
| Confirmação Não-Elaborada | Unelaborated Acknowledgment |
| Resistência ao Método | Method Resistance |
| Regulação da Sessão | Session Regulation |
| Metacognição Explícita | Explicit Metacognition |
| Uso Instrumental do Modelo | Instrumental Use of the Model |

---

## 1. Interpretive codes

### Active Elaboration
**What is it?** The learner produces new content from what they received.

**How to recognize it?** At least one of these variants: rephrasing in their own words, an
example from their own context, a comparative synthesis, a testable hypothesis about code
behavior, a connection between concepts, anchoring in prior knowledge.

### Difficulty Signaling
**What is it?** The learner indicates that they did not understand something.

**How to recognize it?** An explicit statement of non-understanding or a request for
re-explanation without prior rephrasing. *Localized*: the learner names the specific point.
*Non-localized*: they know they did not understand, but not what.

### Unelaborated Acknowledgment
**What is it?** A signal of understanding without behavioral demonstration of the content.

**How to recognize it?** The turn produces no new content: it does not rephrase, exemplify,
or ask questions building on what was received. Responses such as "got it", "ok", "makes
sense", approval of the method.

### Method Resistance
**What is it?** The learner refuses or questions the model's pedagogical strategy, not its
content.

**How to recognize it?** Variants: passive (chooses a direct explanation when offered the
option), explicit (verbalizes refusal of the approach), conceptual critique (questions the
insufficiency of an example), methodological critique (distinguishes a pedagogical example
from real-world use).

### Session Regulation
**What is it?** The learner takes or cedes control over the direction of the conversation.

**How to recognize it?** Opening with an agenda (defines what they want to learn),
self-initiated redirection (changes topic without a question from the model), evaluation
and approval of the method, handing control over to the model.

### Explicit Metacognition
**What is it?** The learner monitors and verbalizes their own learning process.

**How to recognize it?** Verbalizations about their own cognitive state: acknowledging they
forgot something, assessing whether they know enough for a task, monitoring inconsistencies
across turns, evaluating their own level.

### Instrumental Use of the Model
**What is it?** The learner uses the model as a punctual technical reference rather than as
a sequential tutor.

**How to recognize it?** A verification question about partial prior knowledge — the learner
already has a hypothesis and wants confirmation, not to learn from scratch. Markers (in
Portuguese): "mesmo", "é isso?", "seria X?", or stating a hypothesis before the question.

**What is it not?** Active elaboration with a request for confirmation — the difference lies
in whether the content came from the model first. In instrumental use, the content came
from the learner.

---

## 2. Utterance types

| Type (label in the CSV) | Definition |
|---|---|
| Pergunta conceitual (conceptual question) | The learner wants to understand what something is or how it works. The focus is on the concept. E.g., "what is inheritance?", "how does polymorphism work?" |
| Pergunta procedimental (procedural question) | The learner wants to know how to do something, or asks for a practical demonstration. The focus is on execution. E.g., "show me a code example", "how do I implement this in Java?" |
| Confirmação (acknowledgment) | The learner's turn signals receipt without asking or requesting anything. The expected model response is to continue or move on. E.g., "got it", "ok", "right". |
| Mudança de assunto (topic change) | The learner introduces a new topic without the model having suggested the transition. The marker is a break in thematic continuity initiated by the learner. |
| Saturação (saturation) | The learner signals they are done with a topic and do not want to go further into it. |
| Resposta a exercício (exercise answer) | The learner produces a solution to a task proposed by the model. |
| Crítica metodológica (methodological critique) | The learner explicitly criticizes the model's behavior. |
| Instrução ao modelo (instruction to the model) | A turn in which the learner explicitly directs what they want the model to do, without being a question or an exercise answer. |
