# Instruções para a IA nesta wiki

Esta pasta é a wiki de projeto de **um consultor** da Markestrat. Ela atende duas pessoas:

1. **O consultor dono da wiki**, que trabalha com você no chat e aprova tudo o que for gravado.
2. **Quem chegar depois**: outro consultor, a equipe ou o próprio dono meses depois. Essa pessoa não participou das conversas e precisa entender **quais materiais foram usados, que análises foram feitas com cada um, a que conclusões e decisões se chegou, por quê e quem concordou**.

Escreva sempre para o segundo leitor: frases completas, sem abreviações internas e com link para a origem de cada afirmação.

## 1. Mapa da pasta

```text
wiki-<consultor>/
├── AGENTS.md              # Estas instruções
├── CLAUDE.md              # Importa este arquivo para o Claude (@AGENTS.md)
├── index.md               # Catálogo de tudo o que existe na wiki + roteiro de leitura
├── log.md                 # Histórico cronológico: o fluxo do trabalho
├── modelos/               # Modelos de cada tipo de página. Use-os sempre
├── raw/                   # Materiais de origem colocados pelo consultor. SOMENTE LEITURA
├── analises-consultor/    # Arquivos de trabalho do consultor e da IA (planilhas, bases tratadas). Regras na seção 7
└── wiki/
    ├── projeto.md         # Contexto: cliente, objetivo, escopo, equipe, wikis consultadas
    ├── estado-atual.md    # Onde o trabalho parou, próximos passos e pendências (P-xxx)
    ├── decisoes.md        # Registro de decisões (D-xxx)
    ├── fontes/            # Uma ficha por material usado como evidência (F-xxx)
    ├── analises/          # Uma página por análise, com suas conclusões (A-xxx, A-xxx.Cn)
    ├── temas/             # Síntese do que se sabe sobre cada assunto
    ├── entregas/          # Linha de argumentos de apresentações e relatórios (E-xxx)
    └── reunioes/          # Uma página por reunião: pauta antes, resultados depois (R-xxx)
```

## 2. A lógica: uma cadeia rastreável

```text
FONTE  ──►  ANÁLISE  ──►  CONCLUSÃO  ──►  DECISÃO  ──►  ENTREGA
F-001       A-001         A-001.C1        D-001         E-001
```

- **Toda evidência é uma fonte com ficha (F-xxx).** Isso inclui arquivos em `raw/`, páginas de wikis de colegas e relatos que o consultor faz no chat (reunião, telefonema, conversa).
- **Toda conclusão nasce dentro de uma análise** (A-xxx.Cn) e cita as fontes que a sustentam, com versão e local (aba, página, trecho).
- **Toda decisão** (D-xxx) cita as conclusões que a justificam e diz quem concordou.
- **Toda entrega** (E-xxx) liga cada argumento às conclusões ou decisões que o sustentam.
- **Temas** resumem o que se sabe sobre um assunto, mas não criam conclusões: apontam para as análises.
- **Toda reunião tem uma página** (R-xxx), criada antes dela com a pauta; cada item da pauta cita de onde veio (P-xxx, A-xxx.Cn, F-xxx) e o material de apoio. Depois da reunião, a mesma página recebe os resultados extraídos da transcrição ou do relato, com o minuto ou trecho. A transcrição é uma fonte (F-xxx, categoria "reunião"); o que vira conclusão ou decisão é registrado na análise ou em `decisoes.md`, e a página da reunião aponta para lá. Lidas em ordem, as páginas de reunião contam a trajetória do projeto.
- A ficha de cada fonte mantém a tabela **"Uso nas análises"**: em quais análises o material foi usado e o que se concluiu a partir dele. A página de cada análise mantém a tabela **"Fontes usadas"**. As duas tabelas precisam concordar.

**Cada coisa tem um único lugar de origem.** Uma conclusão é escrita por extenso só na sua análise; uma decisão, só em `decisoes.md`; uma pendência, só em `estado-atual.md`; o conteúdo de uma reunião (pauta e resultados), só na sua página R-xxx. Nos outros lugares, cite o ID com link e, no máximo, um resumo de uma linha.

## 3. Onde cada coisa vai

| Se o conteúdo é... | Registre em... |
|---|---|
| Material novo em `raw/` ou nova versão de um material | Ficha em `wiki/fontes/` (skill `intake-material`) |
| Reunião marcada (com o cliente, a equipe ou um colega) | Página em `wiki/reunioes/`, com a pauta, antes da reunião |
| Transcrição ou relato de uma reunião realizada | Ficha de fonte da categoria "reunião" (skill `intake-material`) + seção "Resultados" da página da reunião |
| Relato do consultor sobre conversa ou telefonema avulso que servirá de evidência | Ficha de fonte da categoria "relato do consultor", com o relato escrito na ficha |
| Conteúdo de outro chat de IA | Peça ao consultor que salve a conversa em `raw/`; depois, crie a ficha |
| Página da wiki de um colega usada como base | Ficha de fonte da categoria "wiki de colega" |
| Análise de dados, leitura de entrevistas, comparação de alternativas, teste de hipótese | Página em `wiki/analises/` |
| Planilha, base tratada ou outro arquivo de trabalho de uma análise, do consultor ou da IA | Pasta `analises-consultor/`, com link na seção "Como fizemos" da análise e na tabela "Arquivos de trabalho" do `index.md` |
| Ideia ou hipótese que surgiu na conversa | Conclusão com status "Hipótese" na análise relacionada; se não houver, nova análise |
| Escolha sobre o que fazer ou recomendar (caminho, método, escopo, recomendação) | `wiki/decisoes.md` |
| Dúvida, informação que falta, tarefa a fazer | Pendência P-xxx em `wiki/estado-atual.md` |
| Sequência de argumentos de uma apresentação ou relatório | Página em `wiki/entregas/` |
| Síntese do que se sabe sobre um assunto recorrente | Página em `wiki/temas/` |
| Cliente, escopo, equipe, glossário | `wiki/projeto.md` |

## 4. Identificadores e nomes de arquivo

| Tipo | ID | Arquivo |
|---|---|---|
| Fonte | `F-001` | `wiki/fontes/F-001-<slug>.md` |
| Análise | `A-001` | `wiki/analises/A-001-<slug>.md` |
| Conclusão | `A-001.C1` | Dentro da página da análise |
| Decisão | `D-001` | Dentro de `wiki/decisoes.md` |
| Pendência | `P-001` | Dentro de `wiki/estado-atual.md` |
| Entrega | `E-001` | `wiki/entregas/E-001-<slug>.md` |
| Reunião | `R-001` | `wiki/reunioes/R-001-<slug>-AAAA-MM-DD.md` |
| Tema | sem ID | `wiki/temas/<slug>.md` |

- Números são sequenciais por tipo e **nunca reaproveitados**, nem quando algo é descartado.
- `<slug>`: até seis palavras, minúsculas, sem acentos, separadas por hífen.
- Datas sempre no formato `AAAA-MM-DD`.
- Links sempre relativos, no formato Markdown: `[F-001](../fontes/F-001-base-vendas.md)`. Para caminhos com espaço, use `[texto](<../../raw/nome com espaço.xlsx>)`.

### Como citar um identificador

**Nomeie a coisa antes do código**, em qualquer texto corrido — nas páginas da wiki e nas respostas no chat. O identificador é a referência no fim da frase, nunca o conteúdo dela. Isso vale também para o dono da wiki: ninguém decora o que é A-003 ou F-002.

| Não escreva | Escreva |
|---|---|
| A-003 está concluída | A análise do giro de estoque por loja está concluída (A-003) |
| segundo F-002 | segundo a base de vendas 2023–2025 (F-002) |
| P-011 é a prioridade | Conciliar o lucro da contabilidade com o do relatório gerencial do cliente é a prioridade (P-011) |
| A-004.C2 é hipótese | Ainda é hipótese que a queda do lucro venha da mudança no mix de produtos (A-004.C2) |

Duas exceções práticas: em **tabelas e listas** cuja coluna já identifica a coisa, o código sozinho basta; e, dentro de um mesmo texto, só a **primeira menção** precisa do nome.

## 5. Status e autoria

**Status de conclusões**

| Status | Significa | O registro precisa dizer |
|---|---|---|
| Hipótese | Ideia a testar; evidência insuficiente | O que falta para testar |
| Interpretação | Leitura sustentada por evidência, feita pelo consultor ou pela IA, sem acordo da equipe | As evidências |
| Acordada com a equipe | A equipe concordou | Quem e quando |
| Validada com o cliente | O cliente concordou | Quem do cliente, quando e onde ficou registrado |
| Descartada | Abandonada | Motivo, quem e quando |
| Substituída | Trocada por outra conclusão | ID da nova conclusão e motivo |

**Status de decisões:** Proposta · Acordada com a equipe · Validada com o cliente · Substituída por D-xxx · Revogada. Se não estiver claro quem concordou, escreva "Concordância não está clara" e abra uma pendência.

**Situação de reuniões:** Planejada · Realizada · Cancelada · Remarcada (com a nova data).

**Autoria.** Marque quem disse o quê: **[Consultor]**, **[IA]**, **[Acordado]** (com quem), **[Colega: nome]**, **[Cliente: cargo]**. Uma proposta sua que o consultor aceitou continua sendo de autoria [IA], revisada pelo consultor.

## 6. O que não confundir

- A afirmação de uma fonte não é um fato comprovado. Escreva "segundo F-003, ..." e não "...".
- Uma interpretação do consultor ou sua não é uma decisão da equipe.
- A conclusão de um colega não representa concordância do cliente nem confirmação independente das fontes dele.
- A ausência de um registro não prova que o trabalho não aconteceu. Diga "não encontrei registro".
- Uma explicação ausente não deve ser inventada. Escreva "não registrado".
- Quando você propõe uma ideia ou faz uma análise nova, diga isso; não a apresente como conhecimento já estabelecido.

## 7. Regras de gravação

1. **Nada é gravado sem aprovação.** Antes de criar ou alterar arquivos, mostre a proposta de registro (seção 8) e espere a concordância. A aprovação vale para o conteúdo mostrado; qualquer acréscimo que mude o sentido exige nova proposta. Perguntas e consultas não geram registro.
2. **`raw/` é somente leitura.** Nunca edite, renomeie, mova ou apague arquivos ali. Uma nova versão de um material deve ser salva pelo consultor como **novo arquivo**, sem sobrescrever o anterior, porque análises antigas continuam apontando para a versão que usaram.
3. **Wikis dos colegas são somente leitura.** Não edite, não mova e não rode comandos ou scripts que gravem nelas. Se um comando mencionar a pasta de um colega, não o execute.
4. **Não apague conhecimento.** Para mudar uma conclusão ou decisão, altere o status, mantenha o texto anterior e registre no histórico. Apague só duplicatas ou erros de digitação, com aprovação e registro no log.
5. **Atualize todas as menções.** Ao mudar o status ou o conteúdo de um ID, procure esse ID em toda a wiki (temas, fichas, decisões, entregas, reuniões, estado atual, índice) e atualize as menções.
6. **Feche toda gravação aprovada** atualizando: `index.md` (se houver página nova ou mudança de título ou status), `wiki/estado-atual.md` (se mudou o foco, os próximos passos ou as pendências) e `log.md` (sempre, uma entrada por registro aprovado).
7. **Use os modelos** de `modelos/`. Não crie pastas, tipos de página ou campos novos sem aprovação do consultor; se forem necessários, proponha e registre no log como `manutenção`.
8. **Confidencialidade.** Respeite as restrições de `wiki/projeto.md`. Não copie conteúdo desta wiki para fora do projeto.
9. **Esta wiki tem um dono.** Se a conta do sistema que está rodando você não é a do dono (Lucca Rossi), trate a wiki como somente leitura: não crie, não altere e não apague nada. Leia, responda o que foi perguntado e relate o que encontrou, citando IDs e links; se algo parecer errado ou desatualizado, diga ao leitor em vez de corrigir. Quem quiser propor uma mudança fala com o dono da wiki. No Claude Code, um hook em `.claude/settings.json` bloqueia as ferramentas de escrita nesse caso. Nas demais ferramentas de IA não há trava técnica, e esta regra é o que vale.
   **Primeira resposta, quando a conta não é a do dono.** Rode a skill `gestor`: ela faz a abertura (o que é esta wiki e que é somente leitura) e entrega o panorama do trabalho. Se o leitor já pediu outra coisa, faça a abertura da skill e depois atenda o pedido.
10. **`analises-consultor/` guarda os arquivos de trabalho.** Ficam nessa pasta, e não em `raw/`, as planilhas de cálculo, as bases tratadas e os gráficos feitos pelo consultor ou pela IA. `raw/` guarda só o material recebido como evidência.
    - Nome do arquivo: `AAAA-MM-DD_<descrição>`, com a data de criação.
    - Enquanto está em elaboração, o arquivo pode ser editado. Quando uma conclusão passa a citá-lo, ele fica **congelado**: qualquer mudança vira um arquivo novo, com nova data, e a análise registra qual arquivo usou.
    - Todo arquivo da pasta aparece na tabela "Arquivos de trabalho" do `index.md` e é citado na seção "Como fizemos" da análise a que pertence.
    - Arquivo de trabalho não é fonte: as evidências continuam sendo as fichas F-xxx dos materiais em `raw/`.
    - A IA só grava nessa pasta com aprovação, como em qualquer registro (regra 1).

## 8. Formato da proposta de registro

```markdown
### Proposta de registro
**Resumo:** <uma ou duas frases>
**Arquivos:**
- criar `wiki/analises/A-004-<slug>.md`
- alterar `wiki/fontes/F-002-<slug>.md` — tabela "Uso nas análises"
- alterar `wiki/temas/<slug>.md` — seção "O que sabemos hoje"
- alterar `index.md`, `wiki/estado-atual.md`, `log.md`
**Conteúdo:** <o texto que será gravado, com IDs, status e autoria>
**Confira especialmente:** <pontos em que você interpretou, completou lacunas ou ficou em dúvida>
```

## 9. Pedidos comuns

| O consultor pede... | Faça |
|---|---|
| "Onde paramos?", retomar um tema, começar novo chat | Skill `resume-work`. Não grave nada |
| Colocou material em `raw/` ou pede para ler um material | Skill `intake-material` |
| "Registre", "salve na wiki", "preserve o que discutimos" | Skill `maintain-wiki` |
| Preparar uma reunião, montar a pauta | Skill `maintain-wiki`, seção de reunião: página em `wiki/reunioes/` |
| Transcrição de reunião em `raw/` | Skill `intake-material` (ficha da fonte) e depois `maintain-wiki` (resultados na página da reunião) |
| Nova evidência muda uma premissa ou conclusão | Skill `maintain-wiki`, seção de revisão |
| Revisar, verificar ou auditar a wiki | Skill `review-workspace` |
| Uma pergunta sobre o projeto | Responda nomeando cada análise, fonte, conclusão ou entrega antes do seu código, como manda a seção 4, com link. Diga o que não encontrou e não grave. Se surgir algo que valha registrar, ofereça em uma linha |
| Consultar wikis de colegas | Leia, cite wiki, página e autor, aponte divergências. Não grave na wiki do colega |
| Quem abriu a wiki não é o dono, ou pediram um panorama do andamento | Skill `gestor`. Não grave nada |

**Ao começar qualquer sessão,** leia `index.md` e `wiki/estado-atual.md` antes de responder sobre o projeto.
