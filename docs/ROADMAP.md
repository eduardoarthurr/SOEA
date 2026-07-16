# ROADMAP.md

# SOEA — Sistema Operacional de Estudos Adaptativo

**Versão planejada:** 1.0
**Status geral:** Planejamento concluído — desenvolvimento ainda não iniciado
**Product Owner:** Eduardo Arthur
**Tecnologias:** Google Sheets + Google Apps Script
**Data-alvo de utilização:** preparação para a prova da DATAPREV em 11 de outubro de 2026

---

# 1. OBJETIVO DO ROADMAP

Este documento apresenta as fases de desenvolvimento da versão 1.0 da Planilha Inteligente SOEA.

O Roadmap deverá ser atualizado pelo Codex ao final de cada fase, registrando:

* status da fase;
* percentual aproximado de conclusão;
* entregas realizadas;
* pendências;
* bloqueios;
* próximo marco;
* data da última atualização.

O Codex não poderá iniciar uma nova fase sem aprovação explícita do Product Owner.

---

# 2. DOCUMENTOS DE REFERÊNCIA

Toda implementação deverá seguir os seguintes documentos:

1. `PRD.md` — requisitos funcionais e regras do produto.
2. `ARQUITETURA.md` — organização técnica da implementação.
3. `ROADMAP.md` — fase atual e marcos do projeto.
4. `TODO.md` — tarefas detalhadas e pendências.
5. `CHANGELOG.md` — histórico das alterações.
6. `REVIEW.md` — relatório de revisão ao final de cada fase.
7. `README.md` — instruções finais de instalação e utilização.

Em caso de divergência, a ordem de prioridade será:

```text
PRD.md
↓
ARQUITETURA.md
↓
ROADMAP.md
↓
TODO.md
↓
Implementação
```

---

# 3. VISÃO GERAL DAS FASES

| Fase | Nome                                | Objetivo                                                    | Status inicial |
| ---- | ----------------------------------- | ----------------------------------------------------------- | -------------- |
| 0    | Documentação e preparação           | Validar os documentos-base do projeto                       | Concluída      |
| 1    | Análise do edital e do curso        | Extrair disciplinas, assuntos, pesos e cobertura            | Não iniciada   |
| 2    | Estrutura da planilha               | Criar abas, cabeçalhos, configurações e interface inicial   | Não iniciada   |
| 3    | Motor do SOEA                       | Implementar ciclo, blocos, sessões, revisões e inteligência | Não iniciada   |
| 4    | Dashboard, simulados e refinamentos | Finalizar relatórios, testes, documentação e versão 1.0     | Não iniciada   |

---

# 4. FASE 0 — DOCUMENTAÇÃO E PREPARAÇÃO

Status: Concluída e aprovada

Entregas:

- PRD concluído;
- arquitetura concluída;
- instruções consolidadas;
- roadmap concluído;
- TODO concluído;
- changelog inicial concluído;
- revisão inicial concluída;
- Prompts 00 a 04 concluídos;
- edital incluído;
- fluxo de execução documentado.

Próxima etapa:

Configuração do ambiente autônomo por meio do Prompt 00.

## Objetivo

Criar e validar a documentação que orientará todo o desenvolvimento.

## Entregas

* [x] Definição do conceito da Planilha Inteligente SOEA.
* [x] Definição da metodologia híbrida de estudos.
* [x] Definição de Continuar Ciclo.
* [x] Definição de Retomar Ciclo.
* [x] Definição de Aproveitar Tempo.
* [x] Definição da Barra de Energia.
* [x] Definição do Banco de Questões.
* [x] Definição do Banco de Erros.
* [x] Definição das revisões automáticas.
* [x] Definição dos simulados.
* [x] Definição do Índice de Prioridade.
* [x] Definição do Índice de Domínio.
* [x] Definição do modelo de dados.
* [x] Criação do `PRD.md`.
* [x] Criação do `ARQUITETURA.md`.
* [x] Criação inicial do `ROADMAP.md`.

## Status

```text
██████████ 100%
```

**Situação:** concluída.

## Critério para encerramento

A fase é considerada concluída quando o Product Owner aprovar o `PRD.md` e o `ARQUITETURA.md`.

---

# 5. FASE 1 — ANÁLISE DO EDITAL E DO CURSO

## Objetivo

Transformar o edital da DATAPREV e o pacote do Estratégia em uma estrutura organizada de disciplinas e assuntos que alimentará a planilha.

## Entradas obrigatórias

* Edital oficial da DATAPREV 2026 anexado ao projeto.
* Link do pacote pós-edital do Estratégia Concursos:

```text
https://www.estrategiaconcursos.com.br/curso/dataprev-perfil-3-desenvolvimento-de-software-pacote-2026-pos-edital/
```

## Atividades

### 5.1 Análise do edital

* Ler integralmente o conteúdo programático do Perfil 3.
* Identificar todas as disciplinas.
* Identificar todos os assuntos e subassuntos.
* Identificar quantidade de questões por módulo.
* Identificar peso das questões.
* Identificar critérios de eliminação.
* Identificar data e duração da prova.
* Identificar exigência de não zerar nenhuma disciplina.
* Preservar a redação original dos tópicos do edital.

### 5.2 Análise do pacote do Estratégia

* Listar todos os cursos e disciplinas do pacote.
* Listar aulas ou módulos quando essas informações estiverem disponíveis.
* Identificar correspondência entre cada tópico do edital e o material.
* Evitar assumir cobertura sem evidência.
* Registrar conteúdos parcialmente cobertos.
* Registrar tópicos não encontrados.

### 5.3 Matriz de cobertura

Gerar uma tabela com:

| Disciplina | Assunto do edital | Curso/aula correspondente | Cobertura                | Observação |
| ---------- | ----------------- | ------------------------- | ------------------------ | ---------- |
| Exemplo    | Exemplo           | Exemplo                   | Completa/Parcial/Ausente | Detalhes   |

### 5.4 Estrutura inicial dos dados

Preparar os registros que futuramente alimentarão:

* `_db_Disciplinas`
* `_db_Assuntos`
* `_db_Config`

Cada disciplina deverá receber:

* identificador;
* nome;
* quantidade de questões;
* peso;
* pontuação máxima;
* prioridade-base;
* ordem inicial;
* status.

Cada assunto deverá receber:

* identificador;
* disciplina;
* nome oficial;
* material correspondente;
* situação da cobertura;
* ordem inicial;
* tempo teórico inicial estimado;
* quantidade inicial de questões;
* observações.

### 5.5 Estratégia inicial de estudos

Propor:

* prioridade-base das disciplinas;
* proporção inicial entre teoria e questões;
* parâmetros iniciais por tipo de matéria;
* distribuição inicial de questões;
* tratamento diferenciado para conhecimentos específicos;
* tratamento mínimo para disciplinas que não podem ser zeradas.

O conteúdo específico deverá receber maior importância porque corresponde a 75 dos 115 pontos da prova.

### 5.6 Documentação

Criar ou atualizar:

* `TODO.md`
* `CHANGELOG.md`
* `REVIEW.md`
* este `ROADMAP.md`

## Entregas esperadas

* Matriz completa edital × Estratégia.
* Lista de disciplinas.
* Lista de assuntos.
* Lista de lacunas do curso.
* Pesos e prioridades iniciais.
* Dados preparados para importação.
* Relatório de inconsistências ou dúvidas.
* `REVIEW.md` da Fase 1.

## Critérios de aceite

* Nenhuma disciplina do Perfil 3 foi omitida.
* Todos os tópicos do edital foram classificados.
* As lacunas do Estratégia estão claramente identificadas.
* Os pesos refletem a estrutura real da prova.
* A análise não confunde material preparatório com fonte oficial.
* Os dados estão prontos para alimentar a planilha.
* O Codex para e aguarda aprovação.

## Status

```text
░░░░░░░░░░ 0%
```

**Situação:** não iniciada.

---

# 6. FASE 2 — ESTRUTURA DA PLANILHA

## Objetivo

Criar a base funcional do Google Sheets e do projeto Google Apps Script, ainda sem implementar toda a inteligência adaptativa.

## Atividades

### 6.1 Instalação inicial

Implementar uma função segura de configuração, por exemplo:

```javascript
setupSOEA()
```

Ela deverá:

* criar abas inexistentes;
* preservar abas já existentes;
* não apagar dados sem confirmação;
* validar cabeçalhos;
* aplicar configurações;
* registrar a instalação no histórico.

### 6.2 Abas visíveis

Criar:

* Dashboard;
* Ciclo;
* Banco de Erros;
* Simulados;
* Estatísticas;
* Configurações.

### 6.3 Abas ocultas

Criar:

* `_db_Disciplinas`
* `_db_Assuntos`
* `_db_Ciclo`
* `_db_Blocos`
* `_db_Sessoes`
* `_db_Questoes`
* `_db_Revisoes`
* `_db_Erros`
* `_db_Simulados`
* `_db_Config`
* `_db_Metricas`
* `_db_Historico`
* `_db_Logs`
* `_db_Backup`

### 6.4 Modelo de dados

* Criar os cabeçalhos definidos no PRD.
* Padronizar datas e horários.
* Implementar validações.
* Aplicar listas suspensas.
* Definir status válidos.
* Proteger as abas ocultas.
* Ocultar as abas internas após a instalação.

### 6.5 Importação dos dados da Fase 1

Popular:

* disciplinas;
* assuntos;
* pesos;
* prioridades-base;
* correspondências com o Estratégia;
* configurações iniciais;
* data da prova.

### 6.6 Estrutura do Apps Script

Criar os arquivos definidos no `ARQUITETURA.md`.

Nesta fase, as funções poderão conter implementações mínimas ou estruturas preparatórias, desde que não sejam apresentadas como concluídas.

### 6.7 Menu inicial

Criar o menu:

```text
SOEA
├── Continuar Ciclo
├── Aproveitar Tempo
├── Registrar Questões
├── Registrar Erro
├── Registrar Simulado
├── Atualizar Dashboard
├── Configurações
├── Verificar Integridade
├── Criar Backup
├── Ajuda
└── Sobre
```

### 6.8 Sidebars iniciais

Criar a estrutura visual mínima para:

* Continuar Ciclo;
* Aproveitar Tempo;
* registro de questões;
* registro de erros;
* registro de simulados;
* configurações.

Nesta fase, elas podem utilizar dados simulados controlados apenas para validar interface, sem falsificar funcionalidades prontas.

### 6.9 Dashboard inicial

Criar o layout e os espaços destinados a:

* dias até a prova;
* bloco atual;
* questões;
* horas;
* revisões;
* erros;
* percentual do edital;
* simulados;
* gráficos.

Os cálculos avançados serão implementados posteriormente.

## Entregas esperadas

* Planilha estruturalmente pronta.
* Todas as abas criadas.
* Abas ocultas protegidas.
* Dados do edital carregados.
* Menu funcionando.
* Sidebars abrindo.
* Dashboard básico montado.
* Projeto Apps Script modular.
* Função de instalação segura.
* `REVIEW.md` da Fase 2.

## Critérios de aceite

* A planilha pode ser criada a partir de um Google Sheets vazio.
* Executar o setup novamente não destrói dados.
* Todas as abas possuem os cabeçalhos corretos.
* As disciplinas e assuntos foram carregados.
* O menu aparece ao abrir.
* As Sidebars abrem sem erros.
* As abas ocultas não exigem edição manual.
* Nenhuma tecnologia externa foi adicionada.
* O Codex para e aguarda aprovação.

## Status

```text
░░░░░░░░░░ 0%
```

**Situação:** não iniciada.

---

# 7. FASE 3 — MOTOR DO SOEA

## Objetivo

Implementar a inteligência principal que transforma a estrutura em uma planilha adaptativa de estudos.

## Prioridade desta fase

Esta é a fase central do projeto.

Caso exista limitação de tempo ou de uso do Codex, priorizar primeiro o fluxo essencial:

```text
Continuar Ciclo
↓
Retomar bloco
↓
Registrar progresso
↓
Concluir bloco
↓
Gerar revisões
↓
Selecionar próximo assunto
```

## Atividades

### 7.1 IDs e integridade

Implementar IDs únicos para:

* ciclos;
* blocos;
* sessões;
* registros de questões;
* revisões;
* erros;
* simulados;
* histórico;
* backups;
* disciplinas;
* assuntos.

Utilizar `LockService` nas operações críticas.

### 7.2 Ciclo

* Criar `CYC-001`.
* Garantir apenas um ciclo ativo.
* Calcular percentual concluído.
* Associar blocos ao ciclo.
* Preservar histórico.

### 7.3 Blocos

* Criar blocos automaticamente.
* Impedir dois blocos em andamento.
* Registrar etapas.
* Retomar bloco incompleto.
* Atualizar progresso.
* Concluir bloco.
* Não repetir tarefas concluídas.

### 7.4 Sessões

* Registrar tempo disponível.
* Registrar energia.
* Iniciar e encerrar sessão.
* Permitir sessões parciais.
* Impedir duas sessões abertas.
* Calcular tempo real.

### 7.5 Continuar Ciclo

Implementar a hierarquia:

1. retomar bloco ativo;
2. tratar revisão prioritária;
3. selecionar assunto pelo Índice de Prioridade;
4. criar bloco;
5. apresentar a próxima ação.

### 7.6 Aproveitar Tempo

* Solicitar tempo disponível.
* Solicitar objetivo opcional.
* Consumir o mesmo bloco atual sempre que possível.
* Permitir questões, revisão ou Banco de Erros.
* Não criar planejamento paralelo.
* Atualizar imediatamente o progresso.
* Avançar normalmente caso o bloco seja concluído.

### 7.7 Barra de Energia

Ajustar a carga conforme:

* Excelente;
* Boa;
* Cansado;
* Muito cansado.

A energia não poderá cancelar o estudo.

### 7.8 Banco de Questões

* Registrar quantidade.
* Registrar acertos.
* Calcular erros.
* Calcular percentual.
* Registrar tempo.
* Calcular tempo médio.
* Consolidar total de questões.
* Alimentar métricas, domínio e prioridade.

### 7.9 Banco de Erros

* Registro rápido.
* Preenchimento automático de disciplina, assunto e bloco.
* Motivo.
* Causa raiz.
* Observação.
* Status.
* Seleção para revisões.
* Indicadores de recorrência.

### 7.10 Revisões

Após a conclusão do bloco, criar:

* D+1;
* D+7;
* D+15;
* D+30.

Regras de desempenho:

* 90% ou mais: consolidada;
* 70% a 89%: concluída com leve aumento de prioridade;
* abaixo de 70%: não consolidada, com revisão extra e aumento relevante de prioridade.

### 7.11 Índice de Prioridade

Implementar cálculo entre 0 e 100 considerando:

* peso da disciplina;
* desempenho;
* quantidade de questões;
* erros;
* revisões atrasadas;
* tempo sem contato;
* proximidade da prova;
* simulados.

A fórmula deverá ser documentada e configurável.

### 7.12 Índice de Domínio

Implementar cálculo entre 0 e 100.

Classificação:

* 0–59: vermelho;
* 60–79: amarelo;
* 80–100: verde.

Evitar domínio artificialmente alto com amostra pequena.

### 7.13 Tempo Estimado Inteligente

* Usar padrões no início.
* Aprender tempo médio por questão.
* Aprender tempo médio por tipo de etapa.
* Personalizar estimativas conforme histórico.
* Manter limites razoáveis.

### 7.14 Métricas

Calcular:

* horas totais;
* horas da semana;
* questões totais;
* questões da semana;
* aproveitamento;
* blocos concluídos;
* revisões;
* erros;
* percentual do edital;
* sequência de estudos;
* metas semanais.

### 7.15 Salvamento e recuperação

* Salvamento automático.
* Histórico funcional.
* Logs técnicos.
* Verificação de integridade.
* Recuperação de sessões órfãs.
* Reconstrução do bloco ativo.
* Backup antes de operações críticas.

## Entregas esperadas

* Continuar Ciclo funcional.
* Retomar Ciclo funcional.
* Aproveitar Tempo funcional.
* Blocos e sessões consistentes.
* Questões registradas.
* Erros registrados.
* Revisões automáticas.
* Índices calculados.
* Métricas atualizadas.
* Salvamento automático.
* Recuperação básica.
* `REVIEW.md` da Fase 3.

## Critérios de aceite

* Um bloco interrompido é retomado corretamente.
* Estudo feito no trabalho é refletido em casa.
* Concluir tudo pelo Aproveitar Tempo avança o ciclo.
* Nunca há dois blocos ativos.
* Nunca há duas sessões abertas.
* Revisões não são duplicadas.
* Questões atualizam os indicadores.
* Erros afetam a prioridade.
* O usuário não edita abas internas.
* O estado sobrevive ao fechamento da planilha.
* O Codex para e aguarda aprovação.

## Status

```text
░░░░░░░░░░ 0%
```

**Situação:** não iniciada.

---

# 8. FASE 4 — DASHBOARD, SIMULADOS, TESTES E ENTREGA

## Objetivo

Finalizar a experiência, implementar simulados, testar os fluxos completos e entregar uma versão 1.0 estável e documentada.

## Atividades

### 8.1 Simulados

Implementar agenda baseada em finais de semana.

Planejamento inicial:

* julho: segundo e quarto sábado;
* agosto: todos os sábados;
* setembro: todos os sábados;
* domingos: preferencialmente correção detalhada;
* últimos 15 dias: possibilidade de mini simulado em dia útil, sem substituir o simulado principal.

O calendário deverá considerar a data real de início do uso. Datas que já passaram não deverão gerar pendências retroativas.

Registrar:

* nome;
* data;
* duração;
* questões;
* acertos;
* erros;
* percentual;
* desempenho por disciplina;
* assuntos problemáticos;
* observações.

### 8.2 Dashboard final

Cards:

* dias até a prova;
* bloco atual;
* horas totais;
* horas semanais;
* questões totais;
* questões semanais;
* aproveitamento;
* revisões pendentes;
* erros pendentes;
* percentual do edital;
* sequência;
* próximo simulado.

Gráficos:

* evolução do aproveitamento;
* questões por semana;
* horas por semana;
* desempenho por disciplina;
* evolução nos simulados.

### 8.3 Estatísticas

Implementar:

* filtros por período;
* disciplina;
* assunto;
* tipo de atividade;
* tendência de desempenho;
* principais causas de erro;
* assuntos com menor domínio;
* assuntos com maior prioridade.

### 8.4 Testes funcionais

Testar obrigatoriamente:

1. instalação em planilha vazia;
2. execução repetida do setup;
3. criação do ciclo;
4. criação de bloco;
5. interrupção no meio;
6. retomada;
7. Aproveitar Tempo parcial;
8. Aproveitar Tempo concluindo o bloco;
9. estudo no trabalho e continuidade em casa;
10. registro de questões;
11. registro de erros;
12. geração de revisões;
13. revisão atrasada;
14. revisão com baixo desempenho;
15. Modo Emergência;
16. energia muito baixa;
17. sessão longa com vários blocos;
18. tentativa de clique duplicado;
19. restauração após inconsistência;
20. backup;
21. registro de simulado;
22. atualização dos gráficos.

### 8.5 Testes de dados

Validar:

* IDs únicos;
* relacionamentos;
* ausência de registros órfãos;
* status válidos;
* datas;
* revisões duplicadas;
* dois blocos ativos;
* duas sessões abertas;
* percentuais;
* totais.

### 8.6 Testes de experiência

Verificar:

* início em menos de 30 segundos;
* mensagens claras;
* ausência de mensagens técnicas;
* facilidade para registrar resultados;
* facilidade para registrar erros;
* visibilidade da próxima ação;
* baixa quantidade de cliques;
* funcionamento no computador do trabalho e de casa.

### 8.7 Performance

* Reduzir leituras repetidas.
* Utilizar escrita em lote.
* Evitar operações célula por célula.
* Revisar gatilhos.
* Revisar tempo de execução.
* Evitar backups excessivos.

### 8.8 Documentação final

Criar ou finalizar:

* `README.md`
* `CHANGELOG.md`
* `REVIEW.md`
* `TODO.md`
* `ROADMAP.md`

O README deverá explicar:

* como criar a planilha;
* como abrir o Apps Script;
* como instalar;
* quais permissões autorizar;
* como executar o setup;
* como usar Continuar Ciclo;
* como usar Aproveitar Tempo;
* como registrar erros;
* como registrar simulados;
* como fazer backup;
* como solucionar problemas comuns.

### 8.9 Entrega

Marcar a versão como:

```text
SOEA v1.0
```

A fase só poderá ser encerrada quando não existirem bugs críticos conhecidos.

## Entregas esperadas

* Simulados funcionais.
* Dashboard final.
* Estatísticas.
* Testes concluídos.
* Bugs críticos corrigidos.
* README final.
* Documentação atualizada.
* Versão 1.0 pronta para uso.
* `REVIEW.md` final.

## Critérios de aceite

* O usuário consegue iniciar e concluir uma sessão.
* Todo progresso é salvo.
* Os indicadores refletem os dados reais.
* O Dashboard é útil e legível.
* Os simulados respeitam os finais de semana.
* Não existem erros críticos conhecidos.
* A instalação está documentada.
* O TODO não possui pendências críticas da versão 1.0.
* O ROADMAP marca o projeto como concluído.
* O CHANGELOG registra a versão 1.0.
* O Codex entrega e aguarda aprovação final.

## Status

```text
░░░░░░░░░░ 0%
```

**Situação:** não iniciada.

---

# 9. MARCOS DO PROJETO

## Marco 1 — Requisitos validados

Condição:

* `PRD.md` aprovado;
* `ARQUITETURA.md` aprovado;
* Roadmap inicial criado.

**Status:** concluído.

---

## Marco 2 — Conteúdo estruturado

Condição:

* edital analisado;
* curso analisado;
* matriz de cobertura aprovada;
* disciplinas e assuntos preparados.

**Status:** pendente.

---

## Marco 3 — Planilha-base pronta

Condição:

* abas;
* dados;
* menu;
* Sidebars;
* setup;
* Dashboard básico.

**Status:** pendente.

---

## Marco 4 — SOEA funcional

Condição:

* ciclo;
* blocos;
* sessões;
* questões;
* erros;
* revisões;
* índices;
* salvamento.

**Status:** pendente.

---

## Marco 5 — Versão 1.0 entregue

Condição:

* Dashboard final;
* simulados;
* testes;
* documentação;
* ausência de bugs críticos.

**Status:** pendente.

---

# 10. CONTROLE DE APROVAÇÃO

| Fase   | Entregue pelo Codex | Revisada pelo Product Owner | Aprovada | Data        |
| ------ | ------------------- | --------------------------- | -------- | ----------- |
| Fase 0 | Sim                 | Sim                         | Sim      | A preencher |
| Fase 1 | Não                 | Não                         | Não      | —           |
| Fase 2 | Não                 | Não                         | Não      | —           |
| Fase 3 | Não                 | Não                         | Não      | —           |
| Fase 4 | Não                 | Não                         | Não      | —           |

---

# 11. BLOQUEIOS E RISCOS

## Risco 1 — Conteúdo do Estratégia indisponível

Tratamento:

* registrar o que foi possível verificar;
* não inventar aulas ou cobertura;
* marcar como “Não verificado”;
* permitir preenchimento posterior.

## Risco 2 — Limite temporário do Codex

Tratamento:

* priorizar MVP;
* manter documentação atualizada;
* concluir primeiro o fluxo principal;
* deixar refinamentos visuais para o final.

## Risco 3 — Escopo excessivo

Tratamento:

* não adicionar funcionalidades fora do PRD;
* registrar sugestões no TODO da versão futura;
* priorizar estabilidade.

## Risco 4 — Tempo gasto desenvolvendo em vez de estudar

Tratamento:

* interromper melhorias após o MVP funcional;
* iniciar o uso assim que a Fase 3 estiver estável;
* concluir refinamentos em paralelo apenas quando indispensáveis.

## Risco 5 — Limitações do Google Apps Script

Tratamento:

* utilizar processamento em lote;
* evitar automações excessivas;
* manter backups equilibrados;
* documentar limitações reais.

---

# 12. REGRA DE ATUALIZAÇÃO

Ao concluir uma fase, o Codex deverá atualizar este documento.

Exemplo:

```text
Fase 2

Status anterior:
Não iniciada — 0%

Status atual:
Concluída — 100%

Entregas:
- Abas criadas
- Menu criado
- Sidebars criadas
- Dados carregados

Próxima fase:
Fase 3 — Motor do SOEA
```

O Codex não deverá apagar o histórico de fases concluídas.

---

# 13. ESTADO ATUAL

```text
FASE 0 — DOCUMENTAÇÃO
██████████ 100%

FASE 1 — ANÁLISE
░░░░░░░░░░ 0%

FASE 2 — ESTRUTURA
░░░░░░░░░░ 0%

FASE 3 — MOTOR DO SOEA
░░░░░░░░░░ 0%

FASE 4 — FINALIZAÇÃO
░░░░░░░░░░ 0%
```

## Próxima ação

Criar o `TODO.md` inicial e, depois, executar o Prompt da Fase 1.

---

# 14. ENCERRAMENTO

Este Roadmap representa o planejamento oficial da versão 1.0 da Planilha Inteligente SOEA.

O foco principal é entregar uma ferramenta funcional rapidamente, sem transformar a preparação para o concurso em um projeto de software excessivamente longo.

A partir do momento em que o fluxo principal estiver estável, a prioridade deverá mudar de desenvolvimento para utilização efetiva da planilha nos estudos.
