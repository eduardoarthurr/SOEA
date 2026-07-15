# ===================================================================
# PRD - SOEA
# Sistema Operacional de Estudos Adaptativo
# Parte 2
#
# Fluxo Inteligente do Sistema
# ===================================================================

> ## Observação
>
> Neste projeto, o termo **"Ciclo"** representa uma passagem organizada pelo conteúdo do edital, sendo a principal estrutura de controle da preparação.
>
> Essa nomenclatura foi adotada para manter consistência com as funcionalidades **Continuar Ciclo** e **Retomar Ciclo**.
>
> Ela não corresponde necessariamente ao conceito tradicional de "ciclo de estudos" utilizado por alguns métodos de preparação para concursos.

# 13. FILOSOFIA OPERACIONAL

O SOEA não trabalha por dias.

O SOEA não trabalha por horários.

O SOEA não trabalha por cronogramas.

O SOEA trabalha por CICLOS.

Cada ciclo representa a evolução completa do usuário dentro do edital.

Sempre que o usuário iniciar uma nova sessão de estudos, o Planilha Inteligente deverá identificar automaticamente onde ele parou e qual é a próxima melhor ação.

Toda a inteligência do sistema gira em torno do ciclo.

Jamais deverá existir mais de um ciclo ativo.

Todo avanço realizado, independentemente do local (casa, trabalho, biblioteca, notebook ou computador), deverá atualizar exatamente o mesmo ciclo.

O sistema nunca poderá criar ciclos paralelos.

---
# 14. MOTOR DO SOEA

Toda decisão da planilha deverá passar pelo Motor do SOEA.

O Motor do SOEA será implementado integralmente em Google Apps Script.

Ele será responsável por:

• localizar o estado atual do ciclo;

• localizar blocos pendentes;

• localizar revisões pendentes;

• calcular o Índice de Prioridade;

• gerar o próximo bloco;

• registrar progresso;

• atualizar métricas;

• atualizar Dashboard;

Nenhuma aba deverá acessar diretamente os dados para tomar decisões.

Toda decisão deverá passar pelo Motor do SOEA.

# 15. HIERARQUIA DE PRIORIDADES

Sempre que uma nova sessão for iniciada a Planilha Inteligente deverá seguir obrigatoriamente esta ordem.

1.

Existe um bloco iniciado?

↓

SIM

↓

Continuar exatamente desse ponto.

---

2.

Não existe bloco iniciado?

↓

Existe revisão pendente?

↓

SIM

↓

Executar revisão.

---

3.

Não existe revisão?

↓

Selecionar o assunto com maior Índice de Prioridade.

---

4.

Após concluir o bloco.

↓

Perguntar se ainda existe tempo disponível.

---

5.

Se existir tempo.

↓

Gerar automaticamente o próximo bloco.

---

Esta ordem nunca poderá ser alterada.

---

# 16. CONTINUAR CICLO

## Objetivo

Eliminar completamente a decisão do usuário.

O botão principal do sistema será:

🎯 CONTINUAR CICLO

Este botão nunca deverá gerar um planejamento novo.

Ele deverá apenas descobrir qual é a próxima ação do ciclo.

---

## Entradas

Estado atual do ciclo.

Sessão anterior.

Tempo disponível.

Índice de Prioridade.

Revisões.

Banco de Erros.

Origem dos dados

Todas as informações deverão ser obtidas exclusivamente das abas ocultas da planilha.

Jamais deverão ser utilizadas informações digitadas manualmente durante a geração do bloco.

Caso o bloco tenha sido parcialmente concluído através da funcionalidade "Aproveitar Tempo", o progresso deverá ser considerado normalmente.

Ao retornar ao ciclo principal, o sistema continuará exatamente do ponto restante.

Jamais deverá repetir tarefas já concluídas.

---

## Regras

Se existir um bloco iniciado.

↓

Continuar exatamente desse ponto.

Jamais iniciar outro assunto.

Jamais gerar outro bloco.

Jamais reorganizar o ciclo.

---

## Critério de Aceite

Se o usuário interromper um bloco na metade.

Ao clicar em CONTINUAR CICLO.

A Planilha Inteligente deverá continuar exatamente do ponto onde o usuário parou.

---

# 17. RETOMAR CICLO

## Objetivo

Garantir continuidade absoluta.

---

## Cenário

Ontem.

Java Collections.

Teoria concluída.

25 questões previstas.

Usuário respondeu apenas 14.

Precisou encerrar os estudos.

Hoje.

Ao abrir a Planilha Inteligente.

A Planilha Inteligente deverá responder automaticamente.

"Existe um bloco em andamento."

"Faltam 11 questões."

"Clique em Continuar Ciclo."

Jamais deverá iniciar outro assunto.

---

## Regra

Todo bloco iniciado possui prioridade máxima.

---

# 18. BLOCO DE ESTUDO

O bloco é a menor unidade do sistema.

Um bloco poderá conter.

Teoria.

Questões.

Correção.

Banco de Erros.

Revisão.

Nunca mais de um assunto.

---

## Estrutura

Nome da disciplina

↓

Nome do assunto

↓

Objetivo

↓

Tempo estimado

↓

Etapas

↓

Conclusão

---

# 19. IDENTIFICADOR DO CICLO

## Objetivo

O Ciclo representa a macroestrutura da preparação.

Cada ciclo corresponde a uma passagem completa pelo edital.

Todo bloco obrigatoriamente pertence a um único ciclo.

O identificador do ciclo será utilizado exclusivamente pelo Google Apps Script.

O usuário não precisará manipulá-lo manualmente.

---

## Estrutura

Todo ciclo deverá possuir um identificador único.

Exemplos.

CYC-000001

CYC-000002

CYC-000003

...

O identificador deverá ser incremental durante toda a vida útil da planilha.

---

## Finalidade

O ID do Ciclo será utilizado para:

• organizar toda a preparação;

• agrupar blocos relacionados;

• medir quantas passagens completas foram realizadas pelo edital;

• registrar evolução histórica;

• facilitar futuras reutilizações da planilha para outros concursos;

• impedir inconsistências entre blocos.

---

## Relação com o Edital

Na versão 1.0 existirá apenas um Ciclo ativo.

O identificador do ciclo será:

CYC-001

Esse identificador existirá apenas para organização interna da planilha.

O usuário não visualizará nem manipulará esse identificador.

Caso futuramente seja necessária uma nova passagem completa pelo edital, o Google Apps Script poderá criar automaticamente um novo ciclo.

---

## Relação com os Blocos

Todo ciclo deverá possuir um identificador.

Versão 1.0

CYC-001

---

## Estados do Ciclo

Todo ciclo deverá possuir um estado.

Ativo

Concluído

Arquivado

O estado será atualizado automaticamente pelo Google Apps Script.

---

## Regras

Nunca poderá existir mais de um ciclo ativo.

Ao concluir todos os blocos do edital, o ciclo atual deverá ser marcado como "Concluído".

Caso exista necessidade de uma nova passagem pelo edital, o Google Apps Script deverá criar automaticamente um novo ciclo.

Todo bloco novo deverá ser associado ao ciclo ativo.

---

## Critérios de Aceite

O sistema será considerado correto quando:

✔ Existir apenas um ciclo ativo.

✔ Todo bloco estiver associado a um ciclo.

✔ O histórico de ciclos permanecer preservado.

✔ O Dashboard conseguir informar quantos ciclos completos já foram concluídos.

✔ A criação de um novo ciclo não apagar o histórico anterior.

---

# 20. IDENTIFICADOR DO BLOCO

## Objetivo

Cada bloco de estudo gerado pelo Motor do SOEA deverá possuir um identificador único.

Esse identificador será utilizado para controlar o progresso do usuário durante todo o ciclo de estudos.

O usuário nunca visualizará esse identificador.

Ele será utilizado exclusivamente pelo Google Apps Script.

---

## Estrutura

Todo bloco deverá possuir um ID único.

Exemplo.

BLK-000001

BLK-000002

BLK-000003

...

O formato deverá permanecer crescente durante toda a vida útil da planilha.

---

## Finalidade

O ID do Bloco será utilizado para:

• identificar exatamente qual bloco está ativo;

• impedir duplicidade de blocos;

• reconstruir o estado do ciclo caso ocorra alguma inconsistência;

• registrar histórico completo das sessões;

• facilitar futuras evoluções do sistema;

• permitir rastreabilidade completa.

---

## Relação com o Ciclo

Cada bloco pertence obrigatoriamente a um único ciclo.

Jamais poderá existir um bloco sem ciclo.

Jamais poderá existir um bloco associado a dois ciclos.

---

## Relação com as Sessões

Uma sessão poderá consumir:

• parte de um bloco;

• um bloco inteiro;

• vários blocos.

Entretanto um bloco sempre será identificado pelo mesmo ID.

Mesmo que ele seja concluído em sessões diferentes.

---

## Relação com a funcionalidade "Aproveitar Tempo"

Caso o usuário utilize a funcionalidade Aproveitar Tempo.

O sistema continuará utilizando exatamente o mesmo ID do bloco.

Exemplo.

BLK-000154

25 questões.

Durante o trabalho.

Usuário resolve 10.

↓

O bloco continua sendo:

BLK-000154

Chegando em casa.

O sistema identifica automaticamente que o bloco BLK-000154 ainda não foi concluído.

Ele apresenta apenas as questões restantes.

Jamais cria um novo bloco.

---

## Estados do Bloco

Todo bloco deverá possuir um estado.

Não iniciado

Em andamento

Concluído

Cancelado

O estado deverá ser atualizado automaticamente pelo Google Apps Script.

Jamais deverá ser alterado manualmente.

---

## Critério de Aceite

O sistema será considerado correto quando:

✔ Nunca existir mais de um bloco "Em andamento";

✔ Todo bloco possuir um ID único;

✔ O mesmo bloco puder ser continuado em qualquer sessão;

✔ O bloco permanecer consistente mesmo após interrupções;

✔ Nenhum bloco concluído voltar para o estado "Em andamento".

---

# 20. SESSÕES

O SOEA trabalha por sessões.

Não por dias.

Cada vez que o usuário estudar será considerada uma nova sessão.

Não importa onde.

Não importa o horário.

Não importa a duração.

Toda sessão é válida.

---

## Início da Sessão

Ao clicar em

🎯 CONTINUAR CICLO

A Planilha Inteligente deverá perguntar apenas duas coisas.

Quanto tempo disponível?

As sessões não possuem horário.

As sessões não possuem duração mínima.

Toda sessão deverá ser considerada válida independentemente da duração.

O sistema trabalha por progresso.

Nunca por quantidade de horas.

Como está sua energia?

Nada além disso.

---

## Tempo disponível

Opções padrão.

30 minutos

1 hora

2 horas

3 horas

4 horas

Personalizado

---

## Barra de Energia

Objetivo.

Adaptar a carga.

Nunca cancelar o estudo.

Opções.

😀 Excelente

🙂 Boa

😐 Cansado

😴 Muito cansado

A Barra de Energia nunca deverá impedir o estudo.

Ela apenas altera a complexidade do bloco.

Jamais reduz a consistência do usuário.

O objetivo é manter o hábito diário.

---

## Comportamento

Energia Excelente

↓

Blocos completos.

Energia Boa

↓

Fluxo normal.

Energia Cansado

↓

Reduzir teoria.

Aumentar revisões.

Energia Muito Cansado

↓

Não iniciar conteúdos muito complexos.

Priorizar.

Banco de Erros.

Questões.

Revisões.

Jamais cancelar a sessão.

---

# 21. GERAÇÃO DO BLOCO

Após receber.

Tempo.

Energia.

Estado do ciclo.

A Planilha Inteligente deverá calcular automaticamente.

Quanto cabe dentro daquela sessão.

---

## Exemplo

Tempo disponível

2 horas.

Sistema responde.

Java

Collections

45 minutos teoria

25 questões

20 minutos correção

Tempo previsto

1h58

---

Outro exemplo.

Tempo disponível.

35 minutos.

Sistema responde.

Finalizar questões restantes.

Correção.

Banco de Erros.

Tempo previsto

32 minutos.

---

# 22. TEMPO ESTIMADO INTELIGENTE

Todo bloco deverá possuir.

Tempo total.

Tempo de teoria.

Tempo de questões.

Tempo de correção.

Exemplo.

Java Collections

Teoria

40 min

Questões

30 min

Correção

15 min

Tempo total

1h25

Esses tempos deverão ser configuráveis.

O tempo deverá ser recalculado automaticamente conforme o histórico do usuário.

Exemplo.

Tempo médio por questão.

Tempo médio de teoria.

Tempo médio de revisão.

O sistema deverá aprender continuamente o ritmo do usuário.

Sempre que existir histórico suficiente, as estimativas deverão ser personalizadas.

As estimativas genéricas deverão ser utilizadas apenas durante os primeiros blocos de estudo.

---

# 23. QUESTÕES

O sistema nunca mostrará apenas.

Resolver questões.

Sempre mostrará.

Quantidade.

Tempo médio.

Objetivo.

Exemplo.

25 questões.

Tempo estimado.

35 minutos.

Objetivo.

Fixação do conteúdo.

---

# 24. CONCLUSÃO DO BLOCO

Quando todas as etapas forem concluídas.

Mostrar.

✅ Bloco concluído.

Hoje você realizou:

✔ questoes resolvidas

✔ tempo usado para para teoria

✔ quantos blocos feitos

✔ tempo estudado


Em seguida perguntar.

Ainda possui tempo?

SIM

NÃO

---

## Se responder NÃO

Salvar automaticamente.

Atualizar o ciclo.

Atualizar Dashboard.

Atualizar revisões.

Encerrar sessão.

---

## Se responder SIM

Gerar automaticamente o próximo bloco.

---

# 25. APROVEITAR TEMPO

Objetivo.

Aproveitar oportunidades inesperadas durante o dia.

Exemplos.

Intervalo.

Reunião cancelada.

Atividade finalizada antes do previsto.

Tempo livre no trabalho.

O sistema nunca deverá criar um planejamento alternativo.

Apenas avançar o ciclo principal.

---

## Fluxo

Usuário clica.

⚡ Aproveitar Tempo

Pergunta.

Quanto tempo possui?

15

30

45

60 minutos

---

Sistema identifica.

Qual é o bloco atual.

Divide esse bloco.

Entrega apenas a parte que cabe naquele tempo.

Objetivo da sessão.

○ Questões

○ Revisão

○ Banco de Erros

○ Tanto faz

Caso o usuário escolha "Tanto faz", o Motor do SOEA decidirá automaticamente qual atividade possui maior prioridade.

---

## Exemplo

Bloco.

25 questões.

Usuário possui.

20 minutos.

Sistema responde.

Resolver 12 questões.

Fim.

---

Mais tarde.

Usuário chega em casa.

Clica.

CONTINUAR CICLO.

Sistema responde.

Restam.

13 questões.

Correção.

Ou seja.

Aproveitar Tempo nunca cria outro ciclo.

Ela apenas adianta o ciclo principal.

---

# 26. MISSÃO EXTRA

Após concluir um bloco.

Se existir tempo disponível.

O sistema perguntará.

Ainda deseja continuar?

SIM

NÃO

---

Se SIM.

Gerar automaticamente.

Novo bloco.

Jamais repetir o assunto anterior.

Jamais gerar bloco aleatório.

Sempre respeitar o Índice de Prioridade.

---

# 27. MODO EMERGÊNCIA

Objetivo.

Nunca perder a constância.

Caso o usuário possua menos de 30 minutos.

Ou marque energia muito baixa.

A Planilha Inteligente deverá criar automaticamente.

Uma sessão mínima.

Exemplo.

Revisão.

↓

10 questões.

↓

Banco de Erros.

↓

Fim.

O Modo Emergência jamais deverá ser ativado automaticamente.

Ele será consequência da combinação entre:

Tempo disponível muito baixo.

+

Energia muito baixa.


---

# 28. FLUXO GERAL

INICIAR SESSÃO

↓

Existe bloco iniciado?

↓

SIM

↓

Retomar bloco

↓

Concluir bloco

↓

Ainda possui tempo?

↓

SIM

↓

Próximo bloco

↓

Ainda possui tempo?

↓

SIM

↓

Próximo bloco

↓

NÃO

↓

Encerrar sessão

↓

Atualizar abas ocultas

↓

Atualizar Dashboard

↓

Fim

---

# 29. PRINCÍPIO DA CONTINUIDADE

O usuário poderá estudar:

No trabalho.

Na faculdade.

Na biblioteca.

Em casa.

No notebook.

No computador.

Em qualquer navegador.

Todo estudo realizado deverá atualizar exatamente o mesmo ciclo.

Toda atualização deverá ocorrer imediatamente após a conclusão do bloco.

Não deverá existir sincronização manual.

O usuário nunca deverá clicar em "Salvar".

Todo salvamento será automático.

Exemplo.

Durante o trabalho.

Usuário concluiu completamente Java Collections.

Chegando em casa.

Ao clicar em Continuar Ciclo.

O sistema nunca deverá repetir Collections.

Ele deverá iniciar automaticamente o próximo assunto.

---

# 30. PRINCÍPIO DA NÃO DUPLICIDADE

Jamais poderão existir.

Dois blocos ativos.

Duas sessões abertas.

Dois ciclos.

Duas revisões iguais.

Se o usuário concluir qualquer atividade em uma Aproveitar Tempo.

Essa atividade deverá desaparecer automaticamente da próxima sessão.

O sistema sempre trabalhará sobre um único estado do ciclo.

Em nenhuma hipótese poderão existir dois blocos ativos.

Caso seja detectada qualquer inconsistência.

O Motor do SOEA deverá reconstruir automaticamente o estado correto do ciclo utilizando os registros das abas ocultas.

---

# 31. CRITÉRIOS DE ACEITAÇÃO

O fluxo será considerado correto quando:

✔ Nunca repetir um bloco já concluído.

✔ Nunca perder progresso.

✔ Nunca criar dois blocos ativos.

✔ Sempre continuar exatamente do ponto onde parou.

✔ Sempre atualizar automaticamente o Dashboard.

✔ Sempre atualizar automaticamente as abas ocultas.

✔ Nunca depender de intervenção manual do usuário.

# FIM DA PARTE 2