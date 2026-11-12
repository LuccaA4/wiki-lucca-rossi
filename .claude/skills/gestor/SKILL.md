---
name: gestor
description: Prepara o panorama da wiki para quem acompanha o trabalho de fora - gestor, coordenação ou outro consultor. Use quando quem abriu a wiki não é o dono dela, ou quando pedirem um resumo do andamento, do que foi concluído, do que está pendente e dos pontos de atenção. Nunca grava nada.
---

# Panorama para quem acompanha de fora

Esta skill é a visão de **leitura** da wiki. Ela não cria, não altera e não apaga nada, nem quando o leitor pedir. Se ele quiser mudar algo, a resposta é falar com o dono da wiki.

## 1. Abertura (sempre, antes do resumo)

Escreva, em até cinco linhas:

- de quem é esta wiki e para que serve: registro dos materiais usados, das análises feitas e das decisões tomadas, com a origem de cada afirmação, lido em `wiki/projeto.md`;
- que ela é somente leitura para quem não é o dono, e que propostas de mudança vão para o dono da wiki.

## 2. O que ler

Nesta ordem, sem pular: `index.md`, `wiki/projeto.md`, `wiki/estado-atual.md`, `wiki/decisoes.md` e as últimas entradas de `log.md`. Abra as análises e as reuniões citadas só quando precisar confirmar um ponto que vai relatar.

## 3. O que entregar

| Seção | Conteúdo | Fonte |
|---|---|---|
| Onde o trabalho está | Em uma frase: para qual cliente, o que está sendo produzido e para quando. Depois, o que ainda falta para chegar lá | `wiki/estado-atual.md`, `wiki/entregas/` |
| Concluído recentemente | A pergunta que foi respondida e a resposta a que se chegou, em linguagem de resultado — não o nome do registro | `log.md`, conclusões com status firme |
| Pendências que importam | As que travam a próxima entrega primeiro, com o que cada uma destrava | `wiki/estado-atual.md` |
| Pontos de atenção | Alertas, conclusões ainda em Hipótese que sustentam entrega, divergências entre fontes, decisões sem concordância registrada | `wiki/estado-atual.md`, análises |
| Última movimentação do dono | Data e assunto das últimas entradas do log, e o que mudou | `log.md` |
| O que o dono espera de quem lê | Decisões pendentes de aprovação, materiais a cobrar, nada se não houver | `wiki/decisoes.md`, pendências |

### Regras de escrita

**Escreva para quem nunca abriu esta wiki.** O leitor não sabe o que é A-002, P-011 ou F-003. O identificador é a referência no fim da frase, nunca o conteúdo dela.

| Não escreva | Escreva |
|---|---|
| A-002 concluída | Entendemos por que as despesas comerciais subiram em 2025: vieram da abertura de duas lojas, e não do aumento das comissões, como se suspeitava no início. O cliente confirmou ([A-002](../../../wiki/analises/A-002-despesas-comerciais-2025.md)) |
| P-011 em aberto | O lucro da contabilidade caiu 3 pontos percentuais, mas o relatório gerencial que o cliente acompanha mostra alta. Entender essa diferença é a prioridade antes da entrega ([P-011](../../../wiki/estado-atual.md)) |
| R-002 realizada | Reunião com o diretor financeiro do cliente em 09/10: trouxe uma explicação nova para a queda do lucro e revelou que parte das vendas sai por outra empresa do grupo ([R-002](../../../wiki/reunioes/R-002-diretor-financeiro-AAAA-MM-DD.md)) |

Outras regras:

- Diga o que mudou **para o projeto**, não o que mudou na wiki. "Uma análise foi criada" não interessa ao leitor; "descobrimos que parte das vendas sai por outra empresa do grupo e pode estar fora dos números que analisamos" interessa.
- Distinga dado, interpretação e hipótese em palavras que o leitor entenda — "ainda é hipótese, não foi testada", "o cliente confirmou" —, em vez de citar o status cru.
- Para afirmação de terceiro, escreva "segundo <quem>, ...".
- Não use abreviação interna sem explicar. Termos do negócio estão no glossário de `wiki/projeto.md`; ao usar um, explique em três palavras na primeira vez.
- Se não encontrar registro de algo, escreva "não encontrei registro" em vez de supor.
- Seja breve: o panorama inteiro cabe em uma tela. Ofereça, em uma linha, abrir qualquer item em detalhe.

## 4. Não faça

- Não grave nada, em nenhuma circunstância.
- Não corrija o que parecer errado ou desatualizado: relate ao leitor e diga que a correção é do dono da wiki.
- Não tire conclusão nova a partir das fontes. Esta skill relata o que está registrado.
- Não copie conteúdo da wiki para fora do projeto (seção 7.8 do `AGENTS.md`).
