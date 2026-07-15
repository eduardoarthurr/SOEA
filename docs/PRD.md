# PRD - Product Requirements Document

# SOEA
## Sistema Operacional de Estudos Adaptativo
> Menos tempo planejando.
> Mais tempo aprendendo.

Versão: 1.0

Status: Em Desenvolvimento

Autor: Eduardo Arthur

Documento: PRD.md

---

# 1. VISÃO GERAL

## 1.1 Objetivo

O Sistema Operacional de Estudos Adaptativo (SOEA) é uma planilha inteligente desenvolvida utilizando Google Sheets e Google Apps Script.
Seu objetivo é oferecer funcionalidades normalmente encontradas em aplicações de gerenciamento de estudos, porém utilizando exclusivamente o ecossistema Google.
Dessa forma o usuário poderá acessar sua preparação de qualquer computador utilizando apenas sua conta Google, sem necessidade de hospedagem, servidores, banco de dados externo ou instalação de software.

Ao invés de funcionar como um cronograma ou planner tradicional, o SOEA atuará como um assistente pessoal de estudos, tomando automaticamente todas as decisões relacionadas ao planejamento da preparação para concursos públicos.

A Planilha Inteligente SOEA foi inicialmente concebido para a preparação para o concurso da DATAPREV 2026, Perfil 3 - Desenvolvimento de Software, porém sua arquitetura deverá ser suficientemente flexível para permitir reutilização futura em outros concursos.

O SOEA deve adaptar continuamente o plano de estudos conforme:

- desempenho do usuário;
- quantidade de tempo disponível;
- revisões pendentes;
- banco de erros;
- proximidade da prova;
- evolução no edital.

O sistema deverá reduzir ao máximo a carga cognitiva do usuário relacionada ao planejamento dos estudos, permitindo que toda sua energia mental seja destinada exclusivamente ao aprendizado.

---

# 2. CONTEXTO DO PROJETO

## 2.1 Concurso

Este sistema está sendo desenvolvido para apoiar a preparação do concurso:

Empresa:
DATAPREV

Cargo:
Analista de Tecnologia da Informação

Perfil:
Perfil 3 – Desenvolvimento de Software

Banca:
FGV

Data prevista da prova:
11 de Outubro de 2026

---

## 2.2 Fontes de Estudo

O SOEA NÃO produzirá conteúdo.

Ele será apenas um sistema de gerenciamento inteligente.

As fontes utilizadas na preparação serão:

### Teoria

Pacote Pós-Edital do Estratégia Concursos:

https://www.estrategiaconcursos.com.br/curso/dataprev-perfil-3-desenvolvimento-de-software-pacote-2026-pos-edital/

### Questões

Banco de Questões Estratégia

### Simulados

Estratégia Concursos

---

## 2.3 Edital

O edital oficial será anexado ao projeto.

Todo o sistema deverá ser baseado EXCLUSIVAMENTE no conteúdo programático do edital.

O curso do Estratégia deverá servir apenas como referência para localizar o conteúdo correspondente.

Caso o edital possua algum tópico não contemplado pelo curso, o sistema deverá sinalizar essa ausência.

O edital SEMPRE terá prioridade sobre qualquer curso preparatório.

O arquivo oficial do edital da DATAPREV 2026 será anexado ao Codex durante a fase de análise.

# 2.4 PREMISSAS DO PROJETO

A implementação da versão 1.0 deverá considerar as seguintes premissas:

- O usuário possui uma conta Google.
- A planilha será utilizada por apenas um usuário.
- O acesso principal ocorrerá por computadores no trabalho e em casa.
- O acesso por celular será eventual e não será prioridade de interface.
- A sincronização dos dados será realizada automaticamente pelo Google Sheets.
- Não haverá múltiplos usuários, perfis ou níveis de permissão.
- Não haverá autenticação adicional além da conta Google.
- Não haverá integração com serviços externos.
- Não haverá necessidade de hospedagem ou infraestrutura própria.
- O sistema será inicialmente configurado exclusivamente para o concurso da DATAPREV 2026.
- Disciplinas e assuntos serão extraídos do edital e carregados durante a configuração inicial.
- O usuário não deverá cadastrar manualmente os assuntos do edital.
---

# 3. PERFIL DO USUÁRIO

## 3.1 Usuário Principal

O sistema foi projetado considerando o seguinte perfil.

• Trabalha em horário comercial.

• Estuda principalmente à noite.

• Possui dias imprevisíveis.

• Algumas vezes consegue estudar durante o trabalho.

• Outras vezes não consegue estudar absolutamente nada.

• Costuma estudar pelo computador.

• Eventualmente poderá acessar pelo celular.

• Utilizará principalmente Google Chrome.

---

## 3.2 Rotina

A rotina do usuário NÃO é fixa.

O sistema nunca poderá assumir horários.

O usuário normalmente fará:

Trabalho

↓

Casa

↓

Jantar

↓

Academia

↓

Estudo

Entretanto essa sequência poderá mudar diariamente.

Por esse motivo o sistema jamais utilizará horários fixos.

Ele trabalhará apenas com:

Tempo disponível na sessão atual.

---

# 4. PROBLEMA

Atualmente o maior problema enfrentado pelo usuário não é falta de conteúdo.

O maior problema é a fadiga de decisão.

Todos os dias surgem perguntas como:

"O que estudar hoje?"

"Será que devo revisar?"

"Será que faço questões?"

"Será que continuo Java?"

"Será que já posso passar para Spring?"

"O que devo fazer primeiro?"

Esse tipo de decisão gera desgaste mental.

O objetivo do SOEA é eliminar completamente esse problema.

---

# 5. OBJETIVOS DO SISTEMA

A Planilha SOEA deverá:

✔ eliminar decisões diárias.

✔ manter constância.

✔ adaptar-se ao tempo disponível.

✔ aproveitar tempos livres.

✔ registrar evolução.

✔ controlar revisões.

✔ controlar banco de erros.

✔ controlar simulados.

✔ controlar questões.

✔ controlar progresso do edital.

✔ gerar automaticamente a próxima ação.

---

# 6. O QUE O SISTEMA NÃO É

É extremamente importante definir o que o SOEA NÃO deverá ser.

O sistema NÃO é:

❌ Agenda.

❌ Planner.

❌ Calendário.

❌ Cronograma.

❌ Lista de tarefas.

❌ Aplicativo Pomodoro.

❌ Plataforma de estudos.

O SOEA é um Sistema Operacional de Estudos.

Seu objetivo é tomar decisões automaticamente.

---

# 7. FILOSOFIA DO PROJETO

Toda decisão de engenharia deverá respeitar os princípios abaixo.

Caso alguma funcionalidade viole um destes princípios, ela deverá ser descartada.

---

## P1 — Eliminar decisões

O usuário nunca deverá decidir qual matéria estudar.

O sistema deverá decidir.

---

## P2 — Nunca perder progresso

Toda sessão deverá ser salva automaticamente.

Ao retornar, o usuário continuará exatamente do ponto onde parou.

---

## P3 — Adaptabilidade

O sistema deverá adaptar-se ao tempo disponível.

Nunca exigir horários fixos.

---

## P4 — Constância

O objetivo do sistema é aumentar a quantidade de dias estudados.

Não aumentar apenas as horas estudadas.

---

## P5 — Baixa carga cognitiva

O usuário deve conseguir iniciar os estudos em menos de 30 segundos após abrir a planilha.

---

## P6 — Prioridade Inteligente

Toda escolha realizada pelo sistema deverá utilizar o Índice de Prioridade.

Jamais utilizar ordem fixa.

---

## P7 — Continuidade

O sistema nunca deverá abandonar um bloco iniciado.

Antes de iniciar um novo bloco deverá concluir o anterior.

---

## P8 — Simplicidade

Sempre que existir duas soluções.

A solução mais simples deverá ser escolhida.

---

## P9 — Estabilidade

O sistema deverá priorizar estabilidade.

Novas funcionalidades nunca deverão comprometer funcionalidades existentes.

---

## P10 — Foco na Aprovação

Toda funcionalidade deverá possuir impacto direto na preparação para o concurso.

Se uma funcionalidade não contribuir para aumentar a probabilidade de aprovação, ela deverá ser descartada.

---

# 8. METODOLOGIA DE ESTUDO

O SOEA utilizará um método híbrido.

Não utilizará cronogramas.

Não utilizará ciclos tradicionais.

Cada assunto seguirá obrigatoriamente a sequência abaixo.

Teoria

↓

Questões

↓

Correção

↓

Banco de Erros

↓

Revisão

↓

Próximo Assunto

Jamais será permitido estudar um assunto inteiro antes da resolução de questões.

Questões fazem parte do processo de aprendizagem.

---

# 9. PRINCÍPIOS DA APRENDIZAGEM

O sistema será baseado em quatro pilares.

## Aprendizagem Ativa

Resolver questões desde o primeiro contato com o conteúdo.

---

## Repetição Espaçada

Revisões automáticas.

---

## Feedback Contínuo

Toda sessão gera aprendizado.

---

## Aprendizagem Adaptativa

O sistema adapta automaticamente a sequência conforme o desempenho do usuário.

---
# 10. STACKS TECONOLOGICAS
Toda implementação deverá utilizar exclusivamente as tecnologias abaixo.

## Interface

Google Sheets

## Lógica

Google Apps Script

## Persistência

Google Sheets

## Menus

Google Apps Script

## Sidebars

Google Apps Script HTML Service

## Gráficos

Google Sheets

## Documentação

Markdown

## Controle do Projeto

PRD.md

ROADMAP.md

CHANGELOG.md

TODO.md

# 11. ESCOPO TECNOLOGICO

O projeto NÃO deverá utilizar:

React

Next.js

Angular

Vue

Node.js

Python

Docker

Firebase

MySQL

PostgreSQL

MongoDB

Hospedagem

Servidores

APIs externas

Toda a implementação deverá permanecer dentro do Google Sheets utilizando Google Apps Script.

# 12. ARQUITETURA GERAL

O SOEA será composto por dois componentes.

## Google Sheets

Responsável por:

Interface

Visualização

Armazenamento

Gráficos

Relatórios

---

## Google Apps Script

Responsável por:

Toda lógica de negócio.

Toda automação.

Todos os cálculos.

Todos os menus.

Todos os botões.

Todo o fluxo do sistema.

Nenhuma regra de negócio deverá ficar espalhada em fórmulas da planilha.

Toda inteligência deverá permanecer centralizada no Apps Script.

## Regra Arquitetural

Toda regra de negócio deverá permanecer centralizada no Google Apps Script.

O Google Sheets será responsável apenas por:

• Interface

• Armazenamento

• Visualização

• Relatórios

As fórmulas deverão ser utilizadas apenas para cálculos simples.

Nenhuma funcionalidade crítica deverá depender exclusivamente de fórmulas espalhadas pela planilha.

## Organização da Planilha

A planilha será composta por dois grupos de abas.

### Abas Visíveis

Dashboard

Ciclo

Banco de Erros

Simulados

Estatísticas

Configurações

### Abas Ocultas

_Disciplinas

_Assuntos

_Ciclo

_Questoes

_Revisoes

_Sessoes

_Historico

_Logs

_Metricas

_Backup

As abas ocultas jamais deverão ser editadas manualmente pelo usuário.

Toda manipulação será realizada exclusivamente pelo Google Apps Script.

---
# 13. OBJETIVO DA VERSÃO 1.0

Esta versão tem como objetivo criar a melhor planilha inteligente possível.

Ela deverá ser:

• estável;

• simples;

• rápida;

• intuitiva;

• acessível de qualquer computador;

• sincronizada automaticamente pela conta Google;

• livre de infraestrutura própria;

• de baixa manutenção.

Toda decisão técnica deverá priorizar estabilidade e simplicidade.

# 14. DOCUMENTAÇÃO DO PROJETO

O projeto deverá conter obrigatoriamente os seguintes documentos.

PRD.md

Documento mestre.

Fonte oficial do projeto.

---

ROADMAP.md

Mostrar a fase atual do desenvolvimento.

Sempre atualizado.

---

CHANGELOG.md

Registrar todas as alterações realizadas no projeto.

---

TODO.md

Lista completa de funcionalidades pendentes.

---

Nenhuma implementação deverá ser realizada sem que estes documentos estejam presentes e atualizados.

---

# 15. DIRETRIZES PARA O DESENVOLVIMENTO

Antes de implementar qualquer funcionalidade, o desenvolvedor deverá:

1. Consultar o PRD.
2. Atualizar o ROADMAP, quando houver alteração de fase.
3. Atualizar o TODO com a atividade que será executada.

Somente após isso iniciar a implementação.

Após concluir a implementação, deverá:

1. Atualizar o CHANGELOG.
2. Marcar os itens concluídos no TODO.
3. Atualizar o ROADMAP.
4. Atualizar o PRD somente quando houver mudança de requisito.

Nenhuma funcionalidade deverá descaracterizar o objetivo principal do projeto.

O SOEA é uma planilha inteligente.

Jamais deverá evoluir para uma aplicação Web durante esta versão.

Caso uma funcionalidade exija tecnologias externas ao Google Sheets ou ao Google Apps Script, ela deverá ser adiada para uma versão futura.

O desenvolvedor deverá registrar no TODO.md:

- a funcionalidade adiada;
- a justificativa técnica;
- a tecnologia necessária;
- o impacto esperado;
- a recomendação para uma futura versão.

Ao final de cada fase o desenvolvimento deverá parar aguardando aprovação do usuário antes de prosseguir.

---

# FIM DA PARTE 1
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
# ===================================================================
# PRD - SOEA
# Sistema Operacional de Estudos Adaptativo
# PARTE 3A
#
# Modelo de Dados e Estrutura da Planilha
# ===================================================================

# 32. MODELO DE DADOS

A Planilha Inteligente SOEA utilizará o Google Sheets como mecanismo de persistência de dados.

Todas as informações utilizadas pelo Motor do SOEA serão armazenadas em abas ocultas da própria planilha.

O usuário jamais deverá manipular essas abas diretamente.

Toda leitura, escrita, atualização e exclusão deverá ocorrer exclusivamente através do Google Apps Script.

O Google Sheets será responsável por:

- Interface
- Armazenamento
- Relatórios
- Dashboard
- Gráficos

O Google Apps Script será responsável por:

- Toda regra de negócio
- Geração dos blocos
- Atualização dos indicadores
- Controle do ciclo
- Controle das revisões
- Banco de erros
- Simulados
- Menus
- Sidebars
- Automação completa da planilha

---

# 33. ESTRUTURA DA PLANILHA

A planilha será dividida em dois grupos.

## Abas Visíveis

Representam a interface utilizada pelo usuário.

São as únicas abas que poderão ser manipuladas manualmente.

## Abas Ocultas

Representam o banco de dados interno da planilha.

Jamais deverão ser editadas manualmente.

Toda manipulação será realizada exclusivamente pelo Google Apps Script.

---

# 34. ABAS VISÍVEIS

A versão 1.0 deverá possuir apenas as seguintes abas.

## Dashboard

Página inicial.

Responsável por apresentar:

• Resumo da preparação.

• Próximo bloco.

• Revisões pendentes.

• Estatísticas.

• Indicadores.

• Simulados.

• Banco de erros.

---

## Ciclo

Exibe exclusivamente o bloco atual.

Também será utilizada para:

• Continuar Ciclo

• Aproveitar Tempo

• Encerrar Sessão

---

## Banco de Erros

Consulta completa dos erros registrados.

Permite filtros por:

Disciplina

Assunto

Data

Motivo

Status

---

## Simulados

Histórico dos simulados.

Registro de desempenho.

Comparação entre simulados.

---

## Estatísticas

Indicadores completos da preparação.

---

## Configurações

Interface para alteração das configurações.

Esta aba nunca armazenará os dados.

Ela apenas editará os registros existentes na aba _db_Config.

---

# 35. ABAS OCULTAS

Todas as abas abaixo serão criadas automaticamente.

Jamais deverão ser editadas manualmente.

_db_Disciplinas

_db_Assuntos

_db_Ciclo

_db_Blocos

_db_Sessoes

_db_Questoes

_db_Revisoes

_db_Erros

_db_Simulados

_db_Config

_db_Metricas

_db_Historico

_db_Backup

---

# 36. _db_Disciplinas

## Objetivo

Armazenar todas as disciplinas presentes no edital.

Esses dados serão criados automaticamente durante a configuração inicial da planilha.

O usuário nunca cadastrará disciplinas manualmente.

---

## Campos

disciplina_id

nome

peso_edital

prioridade_base

ordem

status

ultima_atualizacao

---

## Regras

Cada disciplina deverá possuir um identificador único.

O peso será utilizado pelo Índice de Prioridade.

---

# 37. _db_Assuntos

## Objetivo

Armazenar todos os assuntos do edital.

Esses registros serão gerados automaticamente pelo Codex durante a configuração inicial.

O Codex deverá:

- analisar o edital;

- analisar o curso do Estratégia;

- localizar o conteúdo correspondente;

- criar automaticamente os registros.

---

## Campos

assunto_id

disciplina_id

nome

ordem_estudo

tempo_teoria_padrao

questoes_padrao

possui_correspondencia

status

ultima_atualizacao

---

## Regras

Nenhum assunto será cadastrado manualmente.

Caso não exista conteúdo correspondente no Estratégia.

O campo:

possui_correspondencia

deverá ser marcado como FALSE.

---

# 38. _db_Ciclo

## Objetivo

Representar a preparação atual.

Na versão 1.0 existirá apenas um ciclo ativo.

---

## Campos

ciclo_id

status

data_inicio

data_fim

percentual_edital

total_blocos

blocos_concluidos

ultima_atualizacao

---

## Estados

Ativo

Concluído

Arquivado

---

## Regras

Na versão 1.0 existirá apenas:

CYC-001

O usuário nunca visualizará esse identificador.

---

# 39. _db_Blocos

## Objetivo

Representar cada execução de estudo.

Cada assunto do edital gera exatamente um bloco.

---

## Campos

bloco_id

ciclo_id

disciplina_id

assunto_id

status

tempo_previsto

tempo_real

questoes_previstas

questoes_realizadas

percentual

data_inicio

data_conclusao

ultima_atualizacao

---

## Estados

Não iniciado

Em andamento

Concluído

Cancelado

---

## Regras

Nunca poderão existir dois blocos "Em andamento".

Cada bloco pertence obrigatoriamente a:

- um ciclo;

- uma disciplina;

- um assunto.

---

# 40. _db_Sessoes

## Objetivo

Registrar todas as sessões de estudo.

---

## Campos

sessao_id

bloco_id

tipo

tempo_previsto

tempo_real

energia

hora_inicio

hora_fim

data

status

ultima_atualizacao

---

## Tipos

Continuar Ciclo

Aproveitar Tempo

Modo Emergência

---

## Regras

Toda sessão deverá pertencer a um bloco.

Jamais existirão sessões órfãs.

---

# 41. _db_Questoes

## Objetivo

Registrar apenas indicadores das questões.

A planilha não armazenará os enunciados.

---

## Campos

questao_id

bloco_id

disciplina_id

assunto_id

fonte

quantidade

acertos

erros

percentual

tempo_total

tempo_medio

ultima_atualizacao

---

## Regras

Sempre que uma sessão terminar.

As estatísticas deverão ser atualizadas automaticamente.

---

# 42. _db_Revisoes

## Objetivo

Controlar todas as revisões.

---

## Campos

revisao_id

bloco_id

tipo

data_prevista

data_realizada

status

resultado

ultima_atualizacao

---

## Tipos

D+1

D+7

D+15

D+30

Extra

---

## Estados

Pendente

Concluída

Atrasada

---

## Regras

Ao concluir um bloco.

O Google Apps Script deverá criar automaticamente todas as revisões previstas.

As revisões pertencem ao bloco.

Nunca ao ciclo.

---

# 43. _db_Erros

## Objetivo

Representar o Banco de Erros.

---

## Campos

erro_id

bloco_id

disciplina_id

assunto_id

motivo

causa_raiz

observacao

status

data

ultima_atualizacao

---

## Motivos

Não conhecia

Esqueci

Interpretação

Confusão

Desatenção

Chute

Outro

---

## Estados

Novo

Revisado

Resolvido

---

## Regras

Cada erro pertence obrigatoriamente a um bloco.

---

# 44. _db_Simulados

## Objetivo

Registrar todos os simulados.

---

## Campos

simulado_id

nome

data

tempo

questoes

acertos

erros

percentual

observacoes

ultima_atualizacao

---

# 45. _db_Config

## Objetivo

Centralizar todas as configurações da planilha.

A aba Configurações funcionará apenas como interface.

Os valores reais permanecerão nesta aba.

---

## Campos

tempo_padrao_teoria

tempo_padrao_questao

questoes_padrao

dias_revisao

meta_horas_semana

meta_questoes_semana

peso_desempenho

peso_revisoes

peso_edital

ultima_atualizacao

---

## Regras

Toda alteração realizada pelo usuário deverá atualizar automaticamente esta aba.

---

# 46. _db_Metricas

## Objetivo

Centralizar todos os indicadores utilizados pelo Dashboard.

---

## Campos

horas_estudadas

questoes_realizadas

questoes_corretas

questoes_erradas

blocos_concluidos

revisoes_realizadas

simulados_realizados

percentual_edital

indice_prioridade

indice_dominio

sequencia_dias

ultimo_estudo

ultima_atualizacao

---

## Regras

Todos os indicadores serão atualizados automaticamente pelo Google Apps Script.

---

# 47. _db_Historico

## Objetivo

Registrar todas as ações relevantes realizadas na planilha.

---

## Exemplos

Sessão iniciada

Sessão encerrada

Bloco iniciado

Bloco concluído

Revisão criada

Erro registrado

Simulado registrado

Configuração alterada

---

## Campos

historico_id

tipo

descricao

referencia_id

data

hora

ultima_atualizacao

---

# 48. _db_Backup

## Objetivo

Permitir recuperação dos dados.

---

## Regras

Toda alteração crítica deverá gerar automaticamente um ponto de restauração.

A política de retenção será configurável.

---

# FIM DA PARTE 3A
# ===================================================================
# PRD - SOEA
# Sistema Operacional de Estudos Adaptativo
# PARTE 3B
#
# Motor do SOEA, Regras de Negócio e Inteligência da Planilha
# ===================================================================

# 49. MOTOR DO SOEA

## Objetivo

O Motor do SOEA representa o núcleo inteligente da planilha.

Toda decisão deverá ser tomada exclusivamente por ele.

Nenhuma aba visível deverá possuir lógica de decisão.

Toda regra deverá permanecer centralizada no Google Apps Script.

---

## Responsabilidades

O Motor deverá ser responsável por:

• localizar o estado atual do ciclo;

• localizar o bloco ativo;

• verificar revisões pendentes;

• verificar Banco de Erros;

• calcular o Índice de Prioridade;

• calcular o Índice de Domínio;

• gerar o próximo bloco;

• registrar sessões;

• atualizar métricas;

• atualizar Dashboard;

• salvar automaticamente o progresso.

---

# 50. FLUXO DE DECISÃO

Sempre que o usuário clicar em:

CONTINUAR CICLO

o Motor deverá executar obrigatoriamente a sequência abaixo.

PASSO 1

Verificar existência de bloco em andamento.

↓

SIM

↓

Retomar exatamente esse bloco.

↓

NÃO

↓

PASSO 2

Existem revisões pendentes?

↓

SIM

↓

Inserir revisão no próximo bloco.

↓

NÃO

↓

PASSO 3

Calcular Índice de Prioridade.

↓

Selecionar assunto.

↓

Gerar novo bloco.

---

Nenhuma etapa poderá ser ignorada.

---

# 51. GERAÇÃO DE BLOCOS

Todo bloco deverá ser criado automaticamente.

Jamais manualmente.

O Motor deverá utilizar:

• disciplina;

• assunto;

• prioridade;

• tempo disponível;

• energia;

• histórico;

• proximidade da prova.

---

Todo bloco deverá possuir.

ID

Disciplina

Assunto

Tempo previsto

Questões

Objetivo

Status

---

# 52. APROVEITAR TEMPO

A funcionalidade Aproveitar Tempo nunca criará um novo bloco.

Ela apenas consumirá parte do bloco atual.

Fluxo.

Usuário informa.

Tempo disponível.

↓

Motor identifica.

Bloco atual.

↓

Seleciona parte do bloco.

↓

Atualiza progresso.

↓

Salvar automaticamente.

---

Caso todo o bloco seja concluído.

O sistema deverá marcá-lo como concluído.

Gerar revisões.

E atualizar o Dashboard.

---

# 53. ALGORITMO DO ÍNDICE DE PRIORIDADE

O Índice de Prioridade deverá ser recalculado sempre que:

• uma sessão terminar;

• uma revisão for concluída;

• um simulado for registrado;

• um erro for registrado;

• um bloco for concluído.

---

O cálculo deverá considerar.

Peso do edital.

+

Desempenho.

+

Quantidade de erros.

+

Revisões atrasadas.

+

Tempo sem estudar.

+

Proximidade da prova.

---

Quanto maior.

Maior prioridade.

---

# 54. ALGORITMO DO ÍNDICE DE DOMÍNIO

Representa o domínio do usuário sobre determinado assunto.

Deverá considerar.

Acertos.

↓

Revisões.

↓

Simulados.

↓

Reincidência de erros.

---

Quanto maior.

Maior domínio.

---

Nunca deverá diminuir por ausência de estudo.

Apenas por desempenho.

---

# 55. GERAÇÃO DAS REVISÕES

As revisões nunca serão cadastradas manualmente.

Ao concluir um bloco.

O Motor deverá criar automaticamente.

D+1

D+7

D+15

D+30

---

Cada revisão deverá permanecer vinculada ao bloco que a originou.

---

Caso uma revisão atrase.

Ela nunca será excluída.

Seu estado passará para:

ATRASADA.

---

# 56. BANCO DE ERROS

Sempre que uma questão for registrada como incorreta.

O usuário poderá informar.

Motivo.

↓

O Motor registrará automaticamente.

Disciplina.

Assunto.

Bloco.

Data.

Motivo.

---

O Banco de Erros será utilizado para.

• Revisões.

• Índice de Prioridade.

• Estatísticas.

• Dashboard.

---

# 57. TEMPO ESTIMADO INTELIGENTE

Durante os primeiros blocos.

A planilha utilizará tempos padrão.

Após existir histórico suficiente.

O Motor deverá calcular automaticamente.

Tempo médio de teoria.

Tempo médio por questão.

Tempo médio de revisão.

Tempo médio por bloco.

---

As estimativas deverão tornar-se personalizadas.

---

# 58. DASHBOARD

O Dashboard nunca armazenará informações.

Ele será apenas uma camada de visualização.

Todos os dados deverão ser obtidos automaticamente das abas ocultas.

---

O Dashboard deverá apresentar.

• Próximo bloco.

• Revisões pendentes.

• Questões realizadas.

• Horas estudadas.

• Blocos concluídos.

• Simulados.

• Banco de Erros.

• Evolução.

• Percentual do edital.

---

# 59. SINCRONIZAÇÃO

Toda alteração deverá ser salva automaticamente.

Jamais deverá existir botão:

Salvar.

O usuário nunca deverá preocupar-se com sincronização.

Toda alteração será imediatamente persistida.

---

# 60. PERFORMANCE

O Motor deverá evitar:

Leituras desnecessárias.

Atualizações repetidas.

Recalcular indicadores sem necessidade.

---

Sempre que possível.

Os cálculos deverão utilizar apenas os registros alterados.

---

# 61. BACKUP

Toda alteração crítica deverá gerar um registro.

Caso ocorra falha.

O Google Apps Script deverá permitir restaurar o último estado consistente.

---

# 62. REGRAS DE INTEGRIDADE

Jamais poderá existir.

• bloco sem assunto;

• bloco sem disciplina;

• sessão sem bloco;

• revisão sem bloco;

• erro sem bloco;

• questão sem bloco.

---

Nunca poderá existir.

Mais de um bloco "Em andamento".

Mais de um ciclo ativo.

---

Toda inconsistência deverá ser corrigida automaticamente.

---

# 63. CRITÉRIOS GERAIS DE ACEITAÇÃO

O SOEA será considerado corretamente implementado quando:

✔ O usuário nunca precisar decidir o que estudar.

✔ O progresso nunca for perdido.

✔ O Dashboard for atualizado automaticamente.

✔ O ciclo continuar exatamente do ponto onde foi interrompido.

✔ As revisões forem geradas automaticamente.

✔ O Banco de Erros funcionar automaticamente.

✔ Os Índices forem recalculados automaticamente.

✔ Nenhuma aba oculta precisar de edição manual.

✔ Toda lógica permanecer centralizada no Google Apps Script.

✔ A planilha funcionar integralmente dentro do Google Sheets.

---

# 64. EVOLUÇÕES FUTURAS

Os itens abaixo estão fora do escopo da versão 1.0.

• Multiusuário.

• Multi-concurso.

• Aplicação Web.

• Aplicativo Mobile.

• Integração com APIs externas.

• Inteligência Artificial para geração de questões.

• Integração automática com plataformas de questões.

• Sincronização entre diferentes contas Google.

---

# 65. ENCERRAMENTO DA ESPECIFICAÇÃO

Com a conclusão das Partes 1, 2, 3A e 3B, considera-se encerrada a especificação funcional da versão 1.0 da Planilha Inteligente SOEA.

Todo o desenvolvimento deverá seguir rigorosamente este PRD.

Caso seja identificada qualquer necessidade de alteração de requisitos durante a implementação, o PRD deverá ser atualizado antes da implementação.

Qualquer funcionalidade que não esteja prevista neste documento deverá ser considerada fora do escopo da versão 1.0 até aprovação do Product Owner.

# FIM DA PARTE 3B
# ===================================================================
# PRD - SOEA
# Sistema Operacional de Estudos Adaptativo
# PARTE 4
#
# Experiência do Usuário, Critérios de Qualidade,
# Implementação e Encerramento do Projeto
# ===================================================================

# 66. EXPERIÊNCIA DO USUÁRIO (UX)

## Objetivo

Toda a experiência do usuário deverá seguir um único princípio.

"O usuário deve gastar seu tempo estudando e não planejando."

A planilha deverá eliminar completamente dúvidas como:

• O que estudar hoje?

• Qual disciplina escolher?

• Devo revisar ou iniciar conteúdo novo?

• Quantas questões devo fazer?

Todas essas decisões serão tomadas automaticamente pelo Motor do SOEA.

---

# 67. FLUXO DE UTILIZAÇÃO

A utilização diária da planilha deverá seguir o fluxo abaixo.

Abrir Google Sheets

↓

Dashboard

↓

Clique em "Continuar Ciclo"

↓

Informar:

Tempo disponível

Energia

↓

Motor do SOEA

↓

Gerar bloco

↓

Executar estudo

↓

Concluir bloco

↓

Ainda possui tempo?

↓

SIM

↓

Próximo bloco

↓

NÃO

↓

Salvar automaticamente

↓

Encerrar sessão

---

O usuário nunca deverá navegar entre diversas abas para descobrir o que fazer.

---

# 68. EXPERIÊNCIA ESPERADA

A utilização da planilha deverá ser intuitiva.

Objetivos.

• Menos de 30 segundos para iniciar os estudos.

• Nenhuma configuração diária.

• Nenhum planejamento manual.

• Nenhuma atualização manual de indicadores.

• Nenhum botão "Salvar".

• Nenhuma necessidade de consultar abas ocultas.

---

# 69. PADRONIZAÇÃO VISUAL

Todas as abas deverão seguir o mesmo padrão.

Tipografia consistente.

Paleta de cores única.

Ícones padronizados.

Botões padronizados.

Indicadores padronizados.

---

Toda alteração visual deverá manter consistência em toda a planilha.

---

# 70. DASHBOARD

O Dashboard será a principal interface do usuário.

Ao abrir a planilha ele deverá visualizar imediatamente.

Próximo bloco.

↓

Tempo previsto.

↓

Revisões pendentes.

↓

Questões realizadas.

↓

Horas estudadas.

↓

Percentual do edital.

↓

Banco de Erros.

↓

Indicadores.

---

Nenhuma informação deverá exigir navegação desnecessária.

---

# 71. SIDEBARS

Toda interação complexa deverá ocorrer através de Sidebars do Google Apps Script.

Evitar excesso de caixas de diálogo.

Evitar excesso de prompts.

Sempre que possível.

Utilizar apenas uma Sidebar.

---

# 72. MENU PERSONALIZADO

Ao abrir a planilha.

O Google Apps Script deverá criar automaticamente um menu.

SOEA

↓

Continuar Ciclo

↓

Aproveitar Tempo

↓

Dashboard

↓

Banco de Erros

↓

Simulados

↓

Configurações

↓

Atualizar Dados

↓

Sobre

---

# 73. TRATAMENTO DE ERROS

Toda operação deverá possuir tratamento de exceções.

Caso ocorra qualquer erro.

A planilha deverá:

registrar no Histórico;

informar o usuário de forma clara;

evitar perda de dados;

preservar o estado atual do ciclo.

Jamais apresentar mensagens técnicas ao usuário.

---

# 74. TESTES

Antes da conclusão da versão 1.0.

O desenvolvimento deverá validar.

✔ Continuação do ciclo.

✔ Aproveitar Tempo.

✔ Banco de Erros.

✔ Revisões.

✔ Dashboard.

✔ Simulados.

✔ Sessões.

✔ Índices.

✔ Salvamento automático.

✔ Recuperação após interrupções.

---

# 75. CRITÉRIOS DE QUALIDADE

A versão 1.0 somente poderá ser considerada concluída quando.

✔ Todas as funcionalidades previstas estiverem implementadas.

✔ Não existirem erros conhecidos críticos.

✔ O Dashboard atualizar automaticamente.

✔ O Motor do SOEA tomar todas as decisões.

✔ O usuário nunca precisar editar abas ocultas.

✔ A planilha funcionar integralmente utilizando apenas Google Sheets e Google Apps Script.

---

# 76. DOCUMENTAÇÃO

O projeto deverá conter obrigatoriamente.

PRD.md

Documento mestre.

---

ROADMAP.md

Situação atual do desenvolvimento.

---

CHANGELOG.md

Registro cronológico das alterações.

---

TODO.md

Lista das funcionalidades pendentes.

---

README.md

Documento de utilização da planilha.

Deverá conter.

Objetivo.

Instalação.

Primeira configuração.

Fluxo de utilização.

Perguntas frequentes.

Limitações.

---

# 77. ROADMAP DA IMPLEMENTAÇÃO

O desenvolvimento será dividido nas seguintes fases.

Fase 1

Análise.

• Edital.

• Curso Estratégia.

• Comparação.

• Estrutura inicial.

---

Fase 2

Construção da planilha.

• Abas.

• Formatação.

• Estrutura.

---

Fase 3

Motor do SOEA.

• Apps Script.

• Menus.

• Sidebars.

• Fluxos.

---

Fase 4

Dashboard.

• Indicadores.

• Estatísticas.

• Banco de Erros.

• Simulados.

---

Fase 5

Testes.

Correções.

Documentação.

Entrega.

---

Cada fase deverá ser concluída integralmente antes do início da próxima.

---

# 78. LIMITAÇÕES DA VERSÃO 1.0

Estão fora do escopo.

Aplicação Web.

Aplicativo Mobile.

Integrações externas.

Multiusuário.

Múltiplos concursos.

Sincronização entre contas Google.

Inteligência Artificial integrada.PRD

Essas funcionalidades poderão ser consideradas em versões futuras.

---

# 79. EVOLUÇÕES FUTURAS

Após a conclusão da versão 1.0.

Poderão ser avaliadas.

Versão Web.

Versão Mobile.

Suporte a múltiplos concursos.

Sincronização com plataformas de questões.

Importação automática do edital.

Assistente com IA.

Análise preditiva do desempenho.

Integração com Google Calendar.

---

# 80. CRITÉRIO DE SUCESSO DO PROJETO

O projeto será considerado um sucesso quando o usuário conseguir preparar-se para o concurso utilizando exclusivamente a Planilha Inteligente SOEA como ferramenta de gerenciamento dos estudos.

O usuário não deverá depender de cronogramas externos, planners ou controles paralelos.

Todo o planejamento deverá ocorrer automaticamente pela planilha.

---

# 81. ENCERRAMENTO DO PRD

Este documento representa a especificação oficial da versão 1.0 da Planilha Inteligente SOEA.

Qualquer alteração funcional deverá ser registrada previamente no PRD antes da implementação.

O PRD passa a ser a única fonte oficial de requisitos do projeto.

Toda implementação realizada pelo Codex deverá seguir rigorosamente este documento.

Caso exista divergência entre código e PRD.

O PRD prevalecerá.

# FIM DO PRD
