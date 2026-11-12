---
name: intake-material
description: Registra materiais usados como evidência, criando ou atualizando a ficha de fonte F-xxx em wiki/fontes/. Use quando o consultor colocar arquivos em raw/, trouxer uma nova versão de um material, pedir para "dar entrada", "registrar" ou "ler este material", trouxer a transcrição de uma reunião, relatar uma reunião ou conversa que servirá de evidência, ou quiser usar uma página da wiki de um colega como base.
---

# Registrar material (fonte)

Cada material usado como evidência ganha uma ficha em `wiki/fontes/`. A ficha diz o que o material é, de onde veio e qual versão é. Com o tempo, a tabela "Uso nas análises" mostra em quais análises ele foi usado e o que se concluiu a partir dele.

## Passos

1. **Localize o que é novo.** Compare os arquivos de `raw/` com a coluna "Arquivo vigente" da tabela de Fontes do `index.md` e com as tabelas "Versões" das fichas. Liste os arquivos sem ficha.
2. **Leia o conteúdo e diga o que conseguiu ler:** tudo; parte (diga o que ficou de fora, como abas, páginas ou imagens); ou nada (formato não suportado, áudio sem transcrição). Não resuma o que não leu.
3. **Verifique se é nova versão de uma fonte existente** (mesmo documento, com data ou número de versão diferente). Se for:
   - acrescente uma linha na tabela "Versões" da ficha existente, sem criar ficha nova;
   - descreva o que mudou, se conseguir comparar;
   - liste as análises que usaram a versão anterior (tabela "Uso nas análises") e proponha uma pendência de revisão para elas;
   - avise o consultor.
4. **Pergunte só o que não consegue deduzir:** quem produziu ou enviou, quando, de qual pasta do projeto veio e se o uso com IA está autorizado. Campo sem resposta fica como "não informado".
5. **Anote a data de modificação do arquivo.** Ela permite detectar, depois, se alguém sobrescreveu o arquivo.
6. **Monte a ficha** com `modelos/fonte.md`. A seção "Conteúdo" descreve o material, sem interpretar. Interpretações vão para análises.
7. **Mostre a proposta de registro** (formato no `AGENTS.md`) e espere aprovação.
8. **Depois de aprovado:** crie ou atualize a ficha, atualize a tabela de Fontes do `index.md` e acrescente uma entrada `fonte` no `log.md`.

Não analise o material a fundo nesta etapa. Se o consultor quiser conclusões, isso é uma análise (skill `maintain-wiki`).

## Casos especiais

- **Reunião (transcrição ou relato):** categoria "reunião". Confirme a qual página de `wiki/reunioes/` ela corresponde; se não houver, proponha criá-la com `modelos/reuniao.md`. Com transcrição, a ficha aponta para o arquivo em `raw/`; sem transcrição, a ficha não tem arquivo e registra se o relato foi anotado na hora ou de memória. Em ambos os casos, a seção "Conteúdo" da ficha descreve o material (data, participantes, duração) e aponta para a página da reunião; os resultados (respostas, informações, combinados), com o minuto ou trecho, são extraídos na seção "Resultados" da página R-xxx (skill `maintain-wiki`). Preencha o campo "fonte" da página da reunião com o ID da ficha.
- **Relato do consultor** (telefonema ou conversa avulsa, sem reunião marcada e sem arquivo): categoria "relato do consultor". O relato vai na seção "Conteúdo" da ficha, com data, quem estava presente e se foi anotado na hora ou de memória. A ficha não tem arquivo em `raw/`.
- **Conversa de outro chat de IA:** peça ao consultor que salve a conversa em um arquivo em `raw/`. Categoria "conversa com IA". Na ficha, separe o que o consultor disse do que a outra IA propôs.
- **Página da wiki de um colega:** categoria "wiki de colega". Registre a wiki, o caminho da página, o autor, a data da consulta, o status que a conclusão tem lá e as fontes que o colega cita. Não copie os arquivos de `raw/` do colega. Escreva em "Confiabilidade e limites": "Conclusão do colega; não é confirmação independente das fontes dele".
- **Áudio, imagem ou PDF digitalizado:** confirme se houve transcrição ou leitura real. Se não houve, registre a ficha com "Leitura pela IA: não lido" e abra uma pendência.
- **Nome de arquivo confuso:** sugira ao consultor renomear **antes** do registro. Depois do registro, ninguém renomeia: a ficha aponta para o nome.
- **Nunca** mova, renomeie, edite ou apague arquivos em `raw/`.
