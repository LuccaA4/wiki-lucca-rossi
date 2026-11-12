---
name: maintain-wiki
description: Prepara e grava atualizações da wiki com aprovação do consultor - análises e suas conclusões, decisões, pendências, temas, entregas e revisões após nova evidência. Use quando o consultor pedir para registrar, salvar ou preservar algo da conversa ("vamos registrar", "salve na wiki", "registre desde a última atualização"), quando uma nova evidência mudar uma premissa ou conclusão, ao montar a linha de argumentos de uma apresentação ou relatório, ou ao preparar a pauta de uma reunião e registrar seus resultados.
---

# Manter a wiki

## 1. Separe o que registrar

Releia a conversa desde o último registro feito neste chat (ou desde o início, se não houve). Separe:

- o que o consultor afirmou ou decidiu → **[Consultor]**
- o que você propôs → **[IA]**
- o que foi combinado, e com quem → **[Acordado]**
- dúvidas, alternativas e caminhos abandonados, que também são registro

Use a tabela "Onde cada coisa vai" do `AGENTS.md` para decidir o destino de cada item. Se houver evidência nova sem ficha (um relato, um arquivo novo), registre a fonte antes (skill `intake-material`).

## 2. Análise

- **Uma análise responde a uma pergunta.** Se o trabalho continua a mesma pergunta, atualize a análise existente; se a pergunta é outra, crie uma nova.
- Use `modelos/analise.md`. São obrigatórios: pergunta e motivo; fontes usadas, com versão e parte usada; método e premissas; conclusões com status, evidência e autoria; caminhos descartados; pendências.
- Cada conclusão cita as fontes com local preciso (aba, página, trecho, minuto). Se a conclusão vem só de raciocínio, sem fonte, diga isso.
- **Atualize a ficha de cada fonte usada**, na tabela "Uso nas análises": análise, versão usada, o que se extraiu e as conclusões que ela apoia. É assim que se sabe, a partir de qualquer arquivo, o que foi concluído com ele.
- Atualize o tema relacionado. Se o assunto aparece em duas ou mais análises e ainda não tem tema, proponha criar um.

## 3. Decisão

- Registre em `wiki/decisoes.md` com `modelos/decisao.md`.
- Toda decisão cita as conclusões que a justificam, as alternativas consideradas e quem concordou.
- Se o consultor decidiu sozinho, escreva isso. Se não está claro quem concordou, escreva "Concordância não está clara" e abra uma pendência.

## 4. Pendência

- Registre em `wiki/estado-atual.md`, na tabela "Pendências abertas", com o próximo número P-xxx, a origem (análise, decisão ou fonte) e o que destrava a pendência.
- Ao resolver, mova a linha para "Pendências resolvidas" e diga como foi resolvida, com link.

## 5. Revisão após nova evidência

1. Encontre as conclusões afetadas: veja, na ficha da fonte alterada, a tabela "Uso nas análises"; procure também a premissa alterada nas análises.
2. Para cada conclusão afetada, proponha: **manter** (explique por quê), **ajustar** ou **substituir**.
3. Para substituir, crie a nova conclusão. Use a mesma análise se a pergunta for a mesma e a mudança for pequena; use uma nova análise de revisão se o método ou as fontes mudaram. Mude a antiga para "Substituída por A-xxx.Cy — motivo, data". **Não apague o texto antigo.**
4. Procure o ID antigo em toda a wiki e atualize as menções. Decisões e entregas apoiadas na conclusão antiga viram pendência de revisão.
5. Registre no histórico de revisões da análise e no `log.md` (tipo `revisão`), com o motivo.

## 6. Tema

- Use `modelos/tema.md`. O tema resume as conclusões vigentes sobre o assunto, com status e links; não cria conclusão nova.
- Mantenha "Como o entendimento evoluiu": uma linha por mudança relevante, com data e análise.

## 7. Entrega

- Use `modelos/entrega.md`. Cada argumento aponta para conclusões ou decisões.
- Sinalize argumentos apoiados em Hipótese ou Interpretação: eles precisam ser apresentados como tal ou validados antes.
- Registre o que ficou de fora e por quê, e o caminho do arquivo final no projeto (PowerPoint, Excel, relatório).

## 8. Reunião

**Antes (pauta).** Crie a página em `wiki/reunioes/` com `modelos/reuniao.md`, situação "planejada". Cada item da pauta cita a origem (P-xxx, A-xxx.Cn, F-xxx) e o material de apoio (ficha ou arquivo em `raw/`, com link). Perguntas que não vêm de nenhum registro são marcadas [Consultor] ou [IA]. Liste a reunião no `index.md` e nos próximos passos de `wiki/estado-atual.md`.

**Depois (resultados).** Com a transcrição ou o relato registrado como fonte (skill `intake-material`), preencha a seção "Resultados" da página: cada resposta com quem respondeu e o minuto ou trecho; o que foi dito é "segundo <pessoa>", não fato. Mude a situação para "realizada" e preencha o campo "fonte". Em seguida:

- mova para "Pendências resolvidas" as pendências respondidas, com link para a reunião;
- abra pendências para as perguntas que ficaram sem resposta ou com resposta parcial;
- leve as informações que mudam premissas ou conclusões para a revisão (seção 5);
- registre conclusões e decisões nas análises e em `decisoes.md`, e liste-as em "O que esta reunião gerou na wiki".

## 9. Fechamento de toda gravação

- [ ] Proposta mostrada e aprovada pelo consultor
- [ ] Páginas criadas ou alteradas seguindo os modelos
- [ ] Tabela "Uso nas análises" das fichas de fonte atualizada
- [ ] Menções de IDs alterados atualizadas em toda a wiki
- [ ] Página da reunião atualizada, se o registro veio de uma reunião
- [ ] `index.md` atualizado
- [ ] `wiki/estado-atual.md` atualizado (onde paramos, próximos passos, pendências)
- [ ] Uma entrada no `log.md` (`modelos/entrada-log.md`)
- [ ] Informe ao consultor quais arquivos foram criados ou alterados
