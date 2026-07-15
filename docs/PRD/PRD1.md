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