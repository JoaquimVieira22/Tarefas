---
name: registo-provas
description: Regista provas do molho da casa e avaliações de churrasqueiras concorrentes da Espalha Brasas na folha do Google Sheets, e compara resultados. Usar quando o Joaquim disser coisas como "molho versão 3: mais alho, o pai deu 4", "encomendámos no Franganito, frango 9 €, demorou 25 min", "regista esta prova", "qual molho está a ganhar?", "compara a concorrência".
---

# Registo de provas — Espalha Brasas

Falar em português de Portugal, tom de assistente (ver skill `assistente`).

**Folha:** "Registo de provas – Espalha Brasas" (pasta Drive *Assistente Claude*)
- id: `1rO3a_mHd0uB2_YxgyXyV9ahCiHXOJoG69B0VHi72E7Y`
- link: https://docs.google.com/spreadsheets/d/1rO3a_mHd0uB2_YxgyXyV9ahCiHXOJoG69B0VHi72E7Y/edit

Usar a skill `google-workspace` (referência de Sheets) antes de escrever. Acrescentar
linhas com `append_values` — nunca apagar nem reescrever linhas existentes sem o Joaquim pedir.

## Separador `Molho` (colunas A–J)
Data | Versão | Ingredientes e quantidades | O que mudou | Nota Joaquim (1–5) | Nota Pai (1–5) | Nota Mãe (1–5) | Nota outros (1–5) | Média | Comentários

- **Data:** AAAA-MM-DD (hoje, se não disser outra).
- **Versão:** número seguinte ao último registado (ler a coluna B antes), salvo se ele disser.
- **Ingredientes:** se disser só "igual à anterior mas com mais alho", copiar os da versão
  anterior e ajustar; preencher "O que mudou".
- **Notas:** números de 1 a 5; vazio se a pessoa não provou. Mais de um "outro" → média
  na coluna H e nomes nos Comentários.
- **Média:** calculá-la tu e escrever o número (1 casa decimal).
- A receita é **secreta**: nunca a copiar para outro sítio (repositório, e-mails, docs).

## Separador `Concorrência` (colunas A–N)
Data | Churrasqueira | Localidade | Canal (telefone/balcão/app) | Preço frango (€) | Outros preços | Tempo a atender | Tempo de espera (min) | Embalagem / temperatura | Qualidade frango (1–5) | Molho (1–5) | Pontos fortes | Pontos fracos | Notas

- Preços como número (9 → 9), sem "€".
- O que não souber fica vazio — **não inventar**. No fim, numa linha, perguntar só o que
  faltar de importante (preço do frango, qualidade).

## Depois de registar
1. Confirmar numa linha o que ficou guardado (ex.: "Registei a versão 3 — média 3,7.").
2. Se fizer sentido, um comentário curto de consultor: ex. "A versão com mais alho subiu
   meio ponto; experimenta na próxima mexer só no picante."

## Comparar ("qual molho está a ganhar?", "compara a concorrência")
- Ler os dados com `get_values`.
- Molho: ranking por média, o que distingue as melhores versões, sugestão do próximo teste.
- Concorrência: tabela com preço, espera, qualidade; o preço médio do frango na zona;
  pontos fracos comuns que a Espalha Brasas pode aproveitar; sugerir onde encomendar a seguir.
- Se surgir uma conclusão importante (ex.: preço de referência do frango na zona), guardá-la
  em `memoria/churrascaria/projeto.md` e no doc da Drive correspondente (ver skill `assistente`).
