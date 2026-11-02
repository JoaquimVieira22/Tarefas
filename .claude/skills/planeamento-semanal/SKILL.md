---
name: planeamento-semanal
description: Prepara o plano da semana do Joaquim (Coimbra durante a semana, Ourém ao fim de semana). Usar quando corre a tarefa agendada de domingo à noite, ou quando o Joaquim pede "planeia a minha semana", "o que tenho esta semana?", "plano da semana".
---

# Planeamento semanal

Falar em português de Portugal, tom de assistente pessoal (ver skill `assistente`).
Curto, prático, para ler no telemóvel em 2 minutos.

## Fontes (ler antes de escrever)
1. `memoria/perfil.md` — calendário de vida (universidade, outra empresa, estágio)
1b. `memoria/universidade.md` — testes, entregas e apresentações. Incluir no plano tudo o que
   cai nessa semana **e** um aviso do que vem nas 2 semanas seguintes (para começar a preparar).
   Verificar também a Drive (docs "Resumo de Estudo – …" e "Tarefas pendentes") e o Gmail
   (remetentes @esec.pt, colegas de grupo) à procura de datas novas ou alteradas; se houver,
   atualizar `universidade.md` e o doc correspondente na Drive.
2. `tarefas/pendentes.md` e `tarefas/concluidas.md`
3. `memoria/churrascaria/projeto.md`
4. Gmail (se o conector estiver disponível): e-mails dos últimos 7 dias que pareçam pedir
   resposta ou ação (coordenadora do curso, Câmara, sócios, fornecedores, IEFP/NERSANT,
   prazos, faturas). **Só ler — nunca enviar, responder, apagar ou arquivar.** Ignorar
   publicidade e newsletters. Não copiar conteúdo privado de e-mails para o repositório;
   no plano, basta "Responder à coordenadora sobre as datas do estágio".
5. Folha "Registo de provas" (id `1rO3a_mHd0uB2_YxgyXyV9ahCiHXOJoG69B0VHi72E7Y`), para saber
   o que já foi testado/avaliado.

## Formato do plano
```
# Plano da semana — DD a DD de mês

## Em destaque
1–3 coisas que importam mesmo esta semana (com prazo, se houver).

## Durante a semana (Coimbra)
- Universidade / estágio / outra empresa — o que houver
- E-mails a responder (quem e sobre o quê, numa linha cada)

## Fim de semana em Ourém
- Tarefas de fim de semana (molho, concorrência…), com sugestão concreta:
  ex. "Encomendar no Franganito ao jantar de sábado" ou "Testar molho v4: menos vinagre"

## Espalha Brasas — em que ponto estamos
Uma ou duas linhas; o próximo passo.

## Para pensar (opcional)
Um conselho curto de consultor ou um lembrete de equilíbrio (descanso, estudo).
```
Não inventar compromissos nem prazos: só o que estiver nas fontes. Se uma tarefa estiver
parada há muito, sugerir com tato dividi-la ou largá-la.

## Onde guardar
1. Repositório: `memoria/plano-semana.md` (substituir o anterior). Commit e push.
2. Google Doc "Plano da semana" (id `1tdzmj9xG-Be8-zauK45IJtfKkUPyTMe2MuvMqFbc68E`, pasta
   *Assistente Claude*): substituir o conteúdo **no mesmo documento** (skill
   `google-workspace`; o link não muda).
3. Terminar a resposta com um resumo de 2–3 linhas (é o que aparece na notificação do
   telemóvel) e o link do Doc.

## Se faltar alguma coisa
Se o Gmail ou a Drive não estiverem acessíveis, fazer o plano com o que houver e dizer
numa linha o que não foi possível consultar.

## Tarefa agendada
Corre todos os domingos às 21:40 (hora de Lisboa) **dentro da sessão original do Claude Code**
(`session_01AiKmU4MtvsQCDzDZ5r17Ad`), que tem acesso ao Gmail, à Drive e ao repositório.
Id da tarefa agendada: `trig_01G7JcQEcpnrLytL2vF9ZTw3` (para alterar a hora ou parar).
Se essa sessão for arquivada, a tarefa deixa de correr: recriá-la a partir de uma sessão
que tenha os conectores.
