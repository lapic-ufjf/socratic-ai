# Codebook — Análise Qualitativa

Esquema de codificação desenvolvido indutivamente para a análise das transcrições
(`session_transcripts_coded.csv`). Contém duas classificações:

1. **Códigos interpretativos** — reportados no artigo (Tabelas 4 e 5), aplicados na coluna
   `codigos interpretativos`.
2. **Tipos de enunciado** — classificação descritiva complementar, não reportada no artigo,
   aplicada na coluna `codigo descritivo`.

Correspondência com os nomes em inglês usados no artigo:

| Código (português) | Code (paper) |
|---|---|
| Elaboração Ativa | Active Elaboration |
| Sinalização de Dificuldade | Difficulty Signaling |
| Confirmação Não-Elaborada | Unelaborated Acknowledgment |
| Resistência ao Método | Method Resistance |
| Regulação da Sessão | Session Regulation |
| Metacognição Explícita | Explicit Metacognition |
| Uso Instrumental do Modelo | Instrumental Use of the Model |

---

## 1. Códigos interpretativos

### Elaboração Ativa
**O que é?** O aluno produz conteúdo novo a partir do que recebeu.

**Como reconhecer?** Pelo menos uma destas variantes: reformulação com palavras próprias,
exemplo de contexto próprio, síntese comparativa, hipótese testável sobre comportamento do
código, conexão entre conceitos, ancoragem em conhecimento prévio.

### Sinalização de Dificuldade
**O que é?** O aluno indica que não compreendeu algo.

**Como reconhecer?** Declaração explícita de não-compreensão ou pedido de reexplicação sem
reformulação prévia. *Localizada*: o aluno nomeia o ponto específico. *Não-localizada*: sabe
que não entendeu, não sabe o quê.

### Confirmação Não-Elaborada
**O que é?** Sinalização de compreensão sem demonstração comportamental do conteúdo.

**Como reconhecer?** O turno não produz conteúdo novo: não reformula, não exemplifica, não
pergunta a partir do que recebeu. Respostas como "entendi", "ok", "faz sentido", aprovação
do método.

### Resistência ao Método
**O que é?** O aluno recusa ou questiona a estratégia pedagógica do modelo, não o conteúdo.

**Como reconhecer?** Variantes: passiva (escolhe explicação direta quando oferecida opção),
explícita (verbaliza recusa da abordagem), crítica conceitual (questiona insuficiência do
exemplo), crítica metodológica (distingue exemplo pedagógico de uso real).

### Regulação da Sessão
**O que é?** O aluno toma ou cede controle sobre a direção da conversa.

**Como reconhecer?** Abertura com agenda (define o que quer aprender), redirecionamento por
iniciativa (muda de tópico sem pergunta do modelo), avaliação e aprovação do método,
passagem de controle ao modelo.

### Metacognição Explícita
**O que é?** O aluno monitora e verbaliza o próprio processo de aprendizagem.

**Como reconhecer?** Verbalizações sobre o próprio estado cognitivo: reconhecer que
esqueceu, avaliar se sabe o suficiente para uma tarefa, monitorar inconsistências entre
turnos, avaliar o próprio nível.

### Uso Instrumental do Modelo
**O que é?** O aluno usa o modelo como referência técnica pontual, não como tutor sequencial.

**Como reconhecer?** Pergunta de verificação de conhecimento prévio parcial — o aluno já tem
uma hipótese e quer confirmar, não aprender do zero. Marcadores: "mesmo", "é isso?", "seria
X?", ou formulação de hipótese antes da pergunta.

**O que não é?** Elaboração ativa com pedido de confirmação — a diferença está em se o
conteúdo veio do modelo primeiro. No uso instrumental, o conteúdo veio do aluno.

---

## 2. Tipos de enunciado

| Tipo | Definição |
|---|---|
| Pergunta conceitual | O aluno quer entender o que é ou como funciona algo. O foco é no conceito. Ex: "o que é herança?", "como o polimorfismo funciona?" |
| Pergunta procedimental | O aluno quer saber como fazer algo, ou pede uma demonstração prática. O foco é na execução. Ex: "me mostra um exemplo em código", "como eu implemento isso em Java?" |
| Confirmação | O turno do aluno sinaliza recebimento sem fazer pergunta nem pedir nada. A resposta esperada do modelo é continuar ou avançar. Ex: "entendi", "ok", "certo". |
| Mudança de assunto | O aluno introduz um tópico novo sem que o modelo tenha sugerido essa transição. O marcador é a quebra de continuidade temática por iniciativa do aluno. |
| Saturação | O aluno sinaliza que terminou com aquele tópico e não quer mais avançar nele. |
| Resposta a exercício | O aluno produz uma solução para uma tarefa proposta pelo modelo. |
| Crítica metodológica | O aluno critica o comportamento do modelo de forma explícita. |
| Instrução ao modelo | Turno em que o aluno dirige explicitamente o que quer que o modelo faça, sem ser uma pergunta nem uma resposta a exercício. |
