---
name: review-workspace
description: Revisa a saúde da wiki sem alterar nada - arquivos em raw/ sem ficha, fichas apontando para arquivos ausentes ou sobrescritos, links quebrados, conclusões sem evidência, decisões sem concordância registrada, status inconsistentes entre páginas, pendências antigas, conclusões substituídas ainda usadas e reuniões sem resultados registrados. Use quando o consultor pedir para revisar, verificar ou auditar a wiki, ou antes de uma entrega.
---

# Revisar a wiki

Esta skill **só lê e relata**. Correções são propostas depois, pela skill `maintain-wiki`, com aprovação do consultor.

## Verificações

**Fontes**
- Arquivos em `raw/` sem ficha em `wiki/fontes/`.
- Fichas cujo arquivo não existe mais em `raw/`.
- Arquivos com data de modificação diferente da anotada na ficha (podem ter sido sobrescritos).
- Fichas com "Leitura pela IA" parcial ou "não lido" sem pendência aberta.
- Fichas sem nenhum uso em análises (podem ser material ainda não trabalhado, o que é normal; apenas liste).

**Rastreabilidade**
- Conclusões sem evidência e sem a indicação de que vêm só de raciocínio.
- Divergência entre a tabela "Fontes usadas" das análises e a tabela "Uso nas análises" das fichas.
- Decisões sem conclusões de apoio ou sem registro de quem concordou.
- Argumentos de entregas apoiados em conclusões Substituídas, Descartadas ou ainda Hipótese.

**Reuniões**
- Reuniões com data passada ainda como "planejada".
- Reuniões "realizadas" sem a seção "Resultados" preenchida ou sem fonte (F-xxx).
- Perguntas da pauta com resposta "Parcial" ou "Sem resposta" que não viraram pendência.
- Pendências respondidas numa reunião que continuam abertas em `wiki/estado-atual.md`.

**Consistência**
- IDs citados que não existem; IDs repetidos; números pulados sem explicação.
- Status diferente do mesmo ID em lugares diferentes (análise × tema × estado atual × índice).
- Conclusões "Acordada" ou "Validada" sem quem e quando.
- Páginas que não aparecem no `index.md`, ou entradas do índice sem página.
- Links relativos quebrados.

**Atualidade**
- Fontes com nova versão cujas análises ainda usam a versão anterior.
- Pendências abertas há mais de 15 dias.
- `wiki/estado-atual.md` com data anterior à última entrada do `log.md`.

## Relatório

Apresente agrupado por gravidade:

1. **Corrigir antes de usar** — pode levar a uma conclusão errada (ex.: entrega apoiada em conclusão substituída).
2. **Corrigir em breve** — rastreabilidade incompleta (ex.: conclusão sem evidência).
3. **Observações** — organização (ex.: link quebrado, página fora do índice).

Para cada item: o que encontrou, onde (arquivo e ID) e a correção sugerida. Termine perguntando quais correções o consultor quer que você prepare.
