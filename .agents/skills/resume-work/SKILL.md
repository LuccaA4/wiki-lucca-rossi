---
name: resume-work
description: Prepara a retomada do trabalho a partir dos registros da wiki, sem alterar arquivos. Use quando o consultor perguntar "onde paramos?", "qual o próximo passo?", pedir para retomar um tema, abrir um novo chat para continuar o trabalho, quiser um resumo do que foi feito, concluído, descartado e do que falta, ou quiser saber quais reuniões vêm a seguir.
---

# Retomar o trabalho

Esta skill **não grava nada**. Ela reconstrói o ponto de partida a partir do que está registrado.

## Leitura

1. `wiki/estado-atual.md` — foco, onde parou, próximos passos, pendências.
2. As últimas entradas do `log.md` (pelo menos as cinco últimas, ou todas desde a data que o consultor indicar).
3. Se o consultor indicou um tema: a página do tema e as análises e decisões ligadas a ele.
4. As fichas das fontes citadas, só se for preciso para explicar uma conclusão ou pendência.
5. As páginas de `wiki/reunioes/`: as planejadas e a última realizada.

## Resposta

Use esta estrutura, com IDs e links:

- **O que foi feito** — em ordem, uma linha por etapa, a partir do log.
- **Conclusões atuais** — com status. Destaque as que ainda são Hipótese ou Interpretação.
- **Alternativas descartadas** — com o motivo registrado.
- **Decisões** — com quem concordou.
- **Pendências abertas** — o que destrava cada uma.
- **Próximas reuniões** — data, objetivo e itens da pauta ainda em aberto, com link para a página R-xxx.
- **Próximo passo sugerido** — o registrado em `estado-atual.md`; se você sugerir outro, diga que a sugestão é sua.
- **Materiais para consultar** — fichas e arquivos relevantes para o próximo passo.
- **Lacunas** — o que deveria estar registrado e não está (ex.: decisão sem motivo, `estado-atual.md` mais antigo que o log).

Não reconstrua motivos que não estão registrados: diga "não registrado". Termine perguntando por onde o consultor quer continuar.
