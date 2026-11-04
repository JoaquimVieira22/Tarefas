---
name: custos-menu
description: Calcula o custo de cada prato e o preço de venda do menu da Espalha Brasas (food cost), a partir dos preços dos ingredientes e das embalagens, na folha "Espalha Brasas – Custos e preços do menu". Usar quando o Joaquim disser "o frango custa 3,80 €/kg no talho X", "quanto custa fazer uma dose de migas?", "a que preço vendo o entrecosto?", "regista este preço", "faz as contas do menu", "qual é a margem?".
---

# Custos e preços do menu — Espalha Brasas

Português de Portugal, tom de consultor de restauração (ver skill `assistente`).
Toda a informação fica **só na Google Drive**.

**Folha:** "Espalha Brasas – Custos e preços do menu" (pasta *Assistente Claude*)
- id `1axUvlK4M4XGXtwHHPvIFlTNyc8yK91WPdBUI6D14IPI`
- link https://docs.google.com/spreadsheets/d/1axUvlK4M4XGXtwHHPvIFlTNyc8yK91WPdBUI6D14IPI/edit
- Antes de escrever, ler a skill `google-workspace` (referência de Sheets).
- **A folha está em português (pt_PT): nas fórmulas usar `;` como separador, não `,`.**

## Separadores
| Separador | Colunas | Quem preenche |
|---|---|---|
| `Ingredientes` | A Ingrediente/material · B Unidade de compra (kg, L, un) · C Preço por unidade (€) · D Fornecedor · E Data do preço · F Notas | Assistente, com os preços que o Joaquim der |
| `Doses` | A Prato · B Ingrediente (nome **igual** ao de `Ingredientes`) · C Quantidade por dose, na unidade de compra (ex.: 0,5 kg) · **D Custo (fórmula, não mexer)** · E Notas | Assistente, com as receitas/doses |
| `Pratos` | A Prato · **B Custo ingredientes (fórmula)** · C Embalagem por dose (€) · **D Custo total (fórmula)** · **E Preço sugerido (fórmula)** · F Preço escolhido · **G Food cost real (fórmula)** · H Notas | Assistente; o preço final (F) é decisão do Joaquim |
| `Pressupostos` | B2 = food cost alvo (32%) · B3 = IVA (por confirmar com o contabilista) | Só mudar se o Joaquim pedir |

As fórmulas das colunas a negrito estão na linha 2 e calculam a coluna inteira
(ARRAYFORMULA): **nunca escrever valores nessas colunas** nem apagar a linha 2.
O preço sugerido = custo total ÷ food cost alvo.

## Como trabalhar
1. **Registar um preço:** acrescentar ou atualizar a linha em `Ingredientes` (preço como número,
   sem "€"; data AAAA-MM-DD; fornecedor). Se o mesmo ingrediente já existir, atualizar o preço e
   pôr o preço antigo nas Notas — não duplicar a linha (o VLOOKUP usa a primeira).
2. **Registar uma dose:** uma linha em `Doses` por ingrediente do prato. Incluir também o que se
   esquece: carvão/lenha por dose, molho, óleo da batata, guardanapos. Se o Joaquim não souber
   a quantidade, propor um valor marcado **[PRESSUPOSTO]** nas Notas.
3. **Prato novo:** acrescentar em `Pratos` só o nome (A), a embalagem (C) e notas.
4. **Depois de escrever, ler de volta** (`get_values`) e verificar que não há `#ERROR!`/`#N/A`
   (normalmente um nome de ingrediente escrito de forma diferente).
5. **Responder** com uma tabela curta: prato, custo por dose, preço sugerido, food cost do preço
   escolhido. Comparar com os preços da concorrência (separador `Concorrência` da folha
   "Registo de provas", id `1rO3a_mHd0uB2_YxgyXyV9ahCiHXOJoG69B0VHi72E7Y`) e dar opinião: ex.
   "a 9 € ficas 0,50 € acima da média da zona; o molho e as migas justificam-no".

## Conselhos de consultor (usar quando fizer sentido)
- Food cost alvo 28–35%; os acompanhamentos (arroz, batata, migas) costumam ter margem maior e
  compensam a carne.
- Arredondar preços para valores fáceis ao telefone (8,50 € e não 8,37 €).
- Rever os preços da carne todos os meses depois de abrir; atualizar a data do preço.
- A receita do molho é **secreta**: em `Doses` registar só "Molho da casa" com o custo total
  por dose, nunca os ingredientes.
