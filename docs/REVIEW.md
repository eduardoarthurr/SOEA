# REVIEW.md

# SOEA — Sistema Operacional de Estudos Adaptativo

**Versão atual:** 0.0.1
**Fase funcional atual:** Fase 1 — Análise do edital e do curso
**Próxima ação:** executar o Prompt 00 antes de iniciar a Fase 1
**Status da documentação:** Fase 0 concluída e aprovada
**Status do ambiente autônomo:** Não configurado
**Product Owner:** Eduardo Arthur
**Tecnologias:** Google Sheets + Google Apps Script
**Data da última atualização:** 16/07/2026

---

# 1. OBJETIVO DESTE DOCUMENTO

Este documento registra a entrega, a revisão e a aprovação de cada etapa do desenvolvimento da Planilha Inteligente SOEA.

Ele deverá ser atualizado pelo Codex ao final de cada fase para informar de forma clara:

* o que foi implementado;
* quais arquivos foram criados;
* quais arquivos foram alterados;
* qual ambiente foi utilizado;
* se as alterações foram implantadas no Google Apps Script;
* se a planilha real foi validada;
* quais testes foram executados;
* quais resultados foram obtidos;
* quais bugs foram encontrados;
* quais bugs foram corrigidos;
* quais limitações foram identificadas;
* quais pendências permanecem;
* quais pontos precisam ser avaliados pelo Product Owner;
* se a fase está pronta para aprovação;
* qual é a próxima etapa permitida.

O Codex não poderá iniciar uma nova fase sem a aprovação explícita do Product Owner.

A configuração do ambiente autônomo pelo Prompt 00 não é uma fase funcional do produto, mas deverá ser concluída antes das fases que dependem de implantação e testes no Google Sheets.

---

# 2. REGRAS DE ATUALIZAÇÃO

Ao final de cada fase ou etapa de configuração, o Codex deverá:

1. Atualizar este documento.
2. Preservar todas as revisões anteriores.
3. Informar a fase ou etapa executada.
4. Informar a versão correspondente.
5. Informar a data da execução.
6. Informar o responsável pela implementação.
7. Resumir as entregas.
8. Listar os arquivos criados.
9. Listar os arquivos alterados.
10. Informar se houve implantação no Google Apps Script.
11. Informar qual planilha foi utilizada.
12. Informar os testes executados.
13. Informar o resultado real dos testes.
14. Registrar bugs encontrados.
15. Registrar as correções realizadas.
16. Registrar limitações.
17. Registrar pendências.
18. Registrar riscos.
19. Informar o que deverá ser avaliado pelo Product Owner.
20. Informar se a etapa está pronta para aprovação.
21. Parar e aguardar a decisão do Product Owner.

O Codex não deverá:

* apagar revisões anteriores;
* substituir resultados reais por estimativas;
* marcar testes como aprovados sem executá-los;
* declarar implantação quando apenas criou arquivos locais;
* declarar uma fase aprovada antes da decisão do Product Owner;
* iniciar automaticamente a fase seguinte;
* registrar senhas, tokens, cookies ou credenciais neste documento.

---

# 3. STATUS POSSÍVEIS

Cada revisão poderá possuir um dos seguintes estados:

```text
Não iniciada
Em andamento
Aguardando revisão
Aprovada
Aprovada com ressalvas
Correções solicitadas
Reprovada
Bloqueada
```

Para o ambiente autônomo, poderão ser utilizados:

```text
PRONTO_COMPLETO
PRONTO_PARA_ENVIO
INTERVENCAO_NECESSARIA
BLOQUEADO
```

As Fases 2, 3 e 4 somente poderão ser executadas autonomamente quando o ambiente estiver classificado como:

```text
PRONTO_COMPLETO
```

---

# 4. FORMATO PADRÃO DE REVISÃO

O Codex deverá utilizar a estrutura abaixo ao registrar uma nova fase.

```md
# REVISÃO DA FASE X — NOME DA FASE

## Informações gerais

**Versão:**  
**Data:**  
**Responsável pela implementação:**  
**Status:**  
**Ambiente autônomo:**  
**Planilha utilizada:**  
**Projeto Apps Script:**  

---

## Objetivo da fase

Descrever brevemente o objetivo.

---

## Entregas realizadas

- Item implementado.
- Item implementado.

---

## Implantação

**Arquivos enviados com clasp:** Sim/Não  
**Execução real no Apps Script:** Sim/Não  
**Validação na planilha:** Sim/Não  
**Segunda implantação após correções:** Sim/Não/Não aplicável  

Descrever o processo executado.

---

## Arquivos criados

- `Arquivo.gs`
- `Arquivo.html`
- `Documento.md`

---

## Arquivos alterados

- `ArquivoExistente.gs`
- `ROADMAP.md`
- `TODO.md`
- `CHANGELOG.md`
- `REVIEW.md`

---

## Dados criados ou importados

- Disciplinas:
- Assuntos:
- Configurações:
- Registros de teste:
- Outros:

---

## Testes realizados

### TESTE-XXX — Nome do teste

**Cenário:**  
**Pré-condição:**  
**Resultado esperado:**  
**Resultado obtido:**  
**Status:**  
**Evidência:**  
**Correção realizada:**  
**Regressão executada:**  

---

## Resumo dos testes

**Aprovados:**  
**Reprovados:**  
**Bloqueados:**  
**Pendentes do Product Owner:**  
**Não aplicáveis:**  

---

## Bugs encontrados

Nenhum.

ou:

- `BUG-001` — descrição.
  - Severidade:
  - Causa:
  - Correção:
  - Status:

---

## Limitações conhecidas

Nenhuma.

ou:

- `LIM-001` — descrição.

---

## Pendências

Nenhuma pendência impeditiva.

ou:

- Item pendente.

---

## Riscos identificados

Nenhum.

ou:

- Risco identificado.
  - Impacto:
  - Tratamento:

---

## Dados de teste

**Estratégia utilizada:**  
**Identificação dos registros:**  
**Limpeza realizada:** Sim/Não/Não aplicável  
**Integridade após limpeza:**  

---

## Pontos para validação do Product Owner

- Verificar item.
- Confirmar item.
- Avaliar a experiência de uso.

---

## Critérios de aceite

- [ ] Critério validado.
- [ ] Critério validado.

---

## Resultado da fase

**Pronta para aprovação:** Sim/Não  
**Status:** Aguardando revisão do Product Owner  

---

## Decisão do Product Owner

**Status:** Aguardando decisão  
**Data:**  
**Observações:**  

---

## Próxima fase

Nome da próxima fase.

A execução somente poderá começar após aprovação explícita.
```

---

# 5. REVISÃO DA FASE 0 — DOCUMENTAÇÃO E PREPARAÇÃO

## Informações gerais

**Versão:** 0.0.1
**Data da conclusão:** 16/07/2026
**Responsável pela preparação:** Eduardo Arthur e assistência de IA
**Status:** Aprovada
**Implementação no Google Sheets:** Não aplicável
**Ambiente autônomo:** Ainda não configurado

---

## Objetivo da fase

Definir completamente o escopo, os requisitos, a arquitetura, o planejamento, as regras de execução e os documentos de acompanhamento da versão 1.0 da Planilha Inteligente SOEA.

A Fase 0 é exclusivamente documental.

Nenhuma implementação em Google Sheets ou Google Apps Script deveria ser iniciada durante esta fase.

---

## Entregas realizadas

Foram concluídas as seguintes definições:

* conceito do Sistema Operacional de Estudos Adaptativo;
* objetivo da Planilha Inteligente SOEA;
* escopo da versão 1.0;
* metodologia híbrida de estudos;
* fluxo Continuar Ciclo;
* fluxo Retomar Ciclo;
* funcionalidade Aproveitar Tempo;
* Barra de Energia;
* Modo Emergência;
* ciclos de estudo;
* blocos de estudo;
* sessões parciais;
* registro de questões;
* Banco de Erros;
* revisões automáticas;
* sistema de simulados;
* Índice de Prioridade;
* Índice de Domínio;
* Tempo Estimado Inteligente;
* métricas;
* Dashboard;
* Estatísticas;
* configurações;
* backups;
* integridade;
* recuperação;
* abas visíveis;
* abas ocultas;
* modelo de dados;
* arquitetura modular do Google Apps Script;
* utilização do `clasp`;
* operação autônoma no Google Sheets;
* divisão do projeto em fases;
* aprovação obrigatória do Product Owner;
* fluxo exato de execução no Codex.

---

## Documentos criados

Foram criados e consolidados:

* `docs/PRD.md`
* `docs/ARQUITETURA.md`
* `docs/INSTRUCOES.md`
* `docs/ROADMAP.md`
* `docs/TODO.md`
* `docs/CHANGELOG.md`
* `docs/REVIEW.md`
* `README.md`
* `FluxoCodex.md`
* `.gitignore`

Também foram criados os prompts:

* `prompts/00_Configurar_Ambiente_Autonomo.md`
* `prompts/01_Fase_Analise.md`
* `prompts/02_Fase_Estrutura.md`
* `prompts/03_Fase_Motor.md`
* `prompts/04_Fase_Finalizacao.md`

Foi disponibilizada a fonte oficial:

* `fontes/edital-dataprev-2026.pdf`

---

## Documentos que serão gerados durante a execução

Os documentos abaixo não são pendências da Fase 0.

Eles serão produzidos pelo Codex nas etapas correspondentes:

* `docs/AMBIENTE_AUTONOMO.md` — Prompt 00;
* `analises/00_Resumo_Fase_1.md` — Fase 1;
* `analises/01_Estrutura_Prova.md` — Fase 1;
* `analises/02_Analise_Estrategia.md` — Fase 1;
* `analises/03_Matriz_Cobertura.md` — Fase 1;
* `analises/04_Lacunas_Materiais.md` — Fase 1;
* `analises/05_Estrategia_Inicial.md` — Fase 1;
* `analises/06_Validacao_Dados.md` — Fase 1;
* `dados/disciplinas.csv` — Fase 1;
* `dados/assuntos.csv` — Fase 1;
* `dados/config_inicial.csv` — Fase 1;
* `docs/INSTALACAO_FASE_2.md` — Fase 2;
* `docs/TESTES_FASE_2.md` — Fase 2;
* `docs/FORMULAS_SOEA.md` — Fase 3;
* `docs/TESTES_FASE_3.md` — Fase 3;
* `docs/TESTES_FASE_4.md` — Fase 4;
* arquivos de `apps-script/` — a partir do Prompt 00 e da Fase 2;
* README definitivo do produto — Fase 4.

---

## Implementação realizada

Nenhuma funcionalidade do SOEA foi implementada no Google Sheets ou no Google Apps Script durante a Fase 0.

Essa ausência de implementação é intencional e está de acordo com o escopo da fase.

O ambiente autônomo também não foi configurado durante a Fase 0.

A configuração deverá ser realizada por meio do:

```text
prompts/00_Configurar_Ambiente_Autonomo.md
```

---

## Testes e verificações realizados

### TESTE-F0-001 — Coerência entre PRD e Arquitetura

**Cenário:** comparar os requisitos do `PRD.md` com a organização técnica definida no `ARQUITETURA.md`.

**Resultado esperado:** a arquitetura deverá suportar os requisitos sem introduzir tecnologias proibidas.

**Resultado obtido:** os documentos foram revisados e alinhados para utilizar exclusivamente Google Sheets, Google Apps Script, HTML Service e recursos nativos do Google.

**Status:** Aprovado.

---

### TESTE-F0-002 — Coerência entre Roadmap e TODO

**Cenário:** verificar se todas as fases do `ROADMAP.md` possuem tarefas correspondentes no `TODO.md`.

**Resultado esperado:** as fases deverão possuir atividades concretas, verificáveis e separadas.

**Resultado obtido:** as fases de análise, estrutura, Motor e finalização foram representadas no planejamento e nos prompts correspondentes.

**Status:** Aprovado.

---

### TESTE-F0-003 — Controle documental

**Cenário:** verificar se os documentos necessários para preservar o contexto do Codex estão disponíveis.

**Resultado esperado:** PRD, Arquitetura, Instruções, Roadmap, TODO, Changelog e Review disponíveis.

**Resultado obtido:** todos os documentos obrigatórios foram criados.

**Status:** Aprovado.

---

### TESTE-F0-004 — Cobertura dos prompts

**Cenário:** verificar se existe um prompt específico para cada etapa do projeto.

**Resultado esperado:** existir um prompt para configuração do ambiente e um prompt para cada fase funcional.

**Resultado obtido:** foram criados os Prompts 00, 01, 02, 03 e 04.

**Status:** Aprovado.

---

### TESTE-F0-005 — Autonomia de implantação

**Cenário:** verificar se as instruções obrigam o Codex a implantar e testar na planilha real.

**Resultado esperado:** os Prompts 2, 3 e 4 não poderão se limitar à criação de arquivos locais.

**Resultado obtido:** o `INSTRUCOES.md` e os Prompts 2, 3 e 4 exigem `clasp push`, execução real, validação na planilha, correção e repetição dos testes.

**Status:** Aprovado documentalmente.

**Observação:** a capacidade real será validada pelo Prompt 00.

---

### TESTE-F0-006 — Ordem segura de execução

**Cenário:** verificar se o Codex é impedido de executar todas as fases de uma vez.

**Resultado esperado:** cada fase deverá exigir aprovação explícita antes da próxima.

**Resultado obtido:** o fluxo oficial determina execução na ordem Prompt 00 → Fase 1 → Fase 2 → Fase 3 → Fase 4, com aprovação entre as etapas.

**Status:** Aprovado.

---

### TESTE-F0-007 — Disponibilidade da fonte oficial

**Cenário:** verificar se o edital oficial está disponível no repositório.

**Resultado esperado:** existir um PDF na pasta `fontes/` com nome padronizado.

**Resultado obtido:** o arquivo `fontes/edital-dataprev-2026.pdf` foi incluído.

**Status:** Aprovado.

---

### TESTE-F0-008 — Proteção de credenciais

**Cenário:** verificar se o repositório possui regras para evitar o versionamento de credenciais.

**Resultado esperado:** arquivos de autenticação, tokens e variáveis de ambiente deverão estar protegidos.

**Resultado obtido:** o `.gitignore` foi criado com regras para credenciais, tokens, arquivos de ambiente e dependências locais.

**Status:** Aprovado.

---

## Resumo das verificações

**Aprovadas:** 8
**Reprovadas:** 0
**Bloqueadas:** 0
**Pendentes do Product Owner:** 0
**Não aplicáveis:** implantação e testes funcionais do Google Sheets

---

## Bugs encontrados

Nenhum bug de implementação foi encontrado, pois a implementação do produto ainda não foi iniciada.

Durante a revisão do repositório, foram identificadas inconsistências documentais de status no `REVIEW.md` e no `TODO.md`.

A inconsistência deste arquivo é corrigida por esta versão consolidada.

A correção do `TODO.md` deverá ser aplicada separadamente.

---

## Limitações conhecidas

* O conteúdo do edital ainda não foi processado pelo Codex.
* A página pública do pacote do Estratégia ainda não foi analisada formalmente.
* A cobertura do material do Estratégia ainda não foi classificada.
* Os arquivos CSV de disciplinas, assuntos e configurações ainda não foram gerados.
* A fórmula exata do Índice de Prioridade será definida e documentada na Fase 3.
* A fórmula exata do Índice de Domínio será definida e documentada na Fase 3.
* A planilha ainda não foi criada.
* O projeto Apps Script ainda não foi criado ou vinculado.
* O `clasp` ainda não foi validado no ambiente de execução.
* O acesso visual do Codex ao Google Sheets ainda não foi comprovado.
* As limitações reais do Apps Script ainda serão verificadas durante a implementação.
* A aparência final será desenvolvida e validada nas Fases 2 a 4.

Essas limitações são esperadas para o estágio atual e não impedem a aprovação documental da Fase 0.

---

## Pendências

Não existe pendência impeditiva na documentação da Fase 0.

As próximas atividades são de execução:

1. configurar o ambiente autônomo pelo Prompt 00;
2. alcançar o estado `PRONTO_COMPLETO`;
3. revisar e aprovar a configuração;
4. executar a Fase 1 somente após a aprovação do ambiente.

---

## Riscos identificados

### RISCO-001 — Escopo excessivo

O projeto possui várias funcionalidades.

**Impacto:** o desenvolvimento da ferramenta pode consumir tempo excessivo.

**Tratamento:** manter o escopo da versão 1.0, priorizar o fluxo principal e adiar melhorias não essenciais.

---

### RISCO-002 — Desenvolvimento prejudicar os estudos

A ferramenta existe para apoiar a preparação para o concurso.

**Impacto:** o tempo gasto no desenvolvimento pode superar o benefício obtido.

**Tratamento:** utilizar o MVP assim que o fluxo principal da Fase 3 estiver estável e impedir expansão de escopo.

---

### RISCO-003 — Limitações do ambiente Codex

O ambiente poderá apresentar limitações de terminal, autenticação, navegador, Computer Use ou acesso ao Google.

**Impacto:** o Codex poderá criar arquivos, mas não conseguir executar testes reais.

**Tratamento:** executar o Prompt 00 antes das fases funcionais e somente considerar autonomia completa com o estado `PRONTO_COMPLETO`.

---

### RISCO-004 — Autenticação Google

Login, autenticação em dois fatores, CAPTCHA e consentimento OAuth exigem intervenção do Product Owner.

**Impacto:** interrupções temporárias durante a configuração.

**Tratamento:** o Codex deverá parar somente na etapa de segurança, solicitar a menor intervenção possível e continuar do ponto em que parou.

---

### RISCO-005 — Acesso ao conteúdo do Estratégia

A página pública poderá não apresentar todas as aulas ou módulos.

**Impacto:** cobertura incompleta ou não verificável.

**Tratamento:** classificar informações inacessíveis como `Não verificado` e não inventar correspondências.

---

### RISCO-006 — Alteração ou exclusão de dados

Erros de setup, migração, recuperação ou limpeza poderão afetar dados reais.

**Impacto:** perda ou corrupção de progresso.

**Tratamento:** setup idempotente, backups, locks, dados de teste identificados, validação de integridade e confirmação antes de operações destrutivas.

---

### RISCO-007 — Execução de todas as fases de uma vez

Uma instrução genérica ao Codex poderá fazê-lo avançar sem revisão.

**Impacto:** erros de uma fase contaminarem as seguintes.

**Tratamento:** executar apenas um prompt por vez e exigir aprovação explícita entre as fases.

---

## Pontos validados pelo Product Owner

O Product Owner confirmou:

* [x] O objetivo da planilha está correto.
* [x] O escopo da versão 1.0 está correto.
* [x] Google Sheets e Google Apps Script serão as tecnologias principais.
* [x] Tecnologias externas não fazem parte da versão 1.0.
* [x] As abas visíveis estão definidas.
* [x] As abas ocultas estão definidas.
* [x] O fluxo Continuar Ciclo está definido.
* [x] O fluxo Retomar Ciclo está definido.
* [x] O fluxo Aproveitar Tempo está definido.
* [x] A Barra de Energia está definida.
* [x] As revisões estão vinculadas aos blocos.
* [x] O sistema de simulados está previsto.
* [x] O Índice de Prioridade será implementado.
* [x] O Índice de Domínio será implementado.
* [x] O processo de aprovação por fases está correto.
* [x] O Roadmap está adequado.
* [x] O TODO cobre as entregas planejadas.
* [x] Os Prompts 00 a 04 estão prontos.
* [x] O edital oficial foi incluído.
* [x] O fluxo exato de envio ao Codex foi documentado.
* [x] A documentação está pronta para iniciar o Prompt 00.

---

## Critérios de aceite da Fase 0

* [x] PRD criado e consolidado.
* [x] Arquitetura criada e consolidada.
* [x] Instruções permanentes criadas.
* [x] Roadmap criado.
* [x] TODO criado.
* [x] Changelog criado.
* [x] Review criado.
* [x] README inicial criado.
* [x] Fluxo do Codex documentado.
* [x] Prompt 00 criado.
* [x] Prompt 01 criado.
* [x] Prompt 02 criado.
* [x] Prompt 03 criado.
* [x] Prompt 04 criado.
* [x] Edital disponível para o Codex.
* [x] Link público do Estratégia registrado nos documentos.
* [x] Proteção básica de credenciais definida.
* [x] Product Owner aprovou os documentos.
* [x] Nenhuma implementação funcional foi iniciada antecipadamente.
* [x] Próxima ação definida como execução do Prompt 00.

---

## Resultado da fase

**Pronta para aprovação:** Sim
**Status:** Aprovada pelo Product Owner
**Pendências impeditivas:** Nenhuma

---

## Decisão do Product Owner

**Status:** Aprovada
**Data:** 16/07/2026

**Observações:**

A documentação de planejamento do SOEA foi revisada e aprovada.

Os documentos principais, o edital oficial, o fluxo de execução e os Prompts 00, 01, 02, 03 e 04 estão preparados.

A implementação funcional ainda não foi iniciada.

A próxima ação autorizada é executar somente o Prompt 00 para configurar e validar o ambiente autônomo.

O Prompt 01 não poderá ser executado antes da conclusão e aprovação do Prompt 00.

---

## Próxima etapa

```text
PROMPT 00 — CONFIGURAÇÃO DO AMBIENTE AUTÔNOMO
```

Objetivo:

* validar Node.js;
* validar npm;
* instalar ou validar o `clasp`;
* autenticar o `clasp`;
* criar ou vincular a planilha;
* criar ou vincular o projeto Apps Script;
* testar `clasp push`;
* executar uma função real;
* validar o Google Sheets;
* validar o Chrome conectado;
* produzir `docs/AMBIENTE_AUTONOMO.md`;
* alcançar o estado `PRONTO_COMPLETO`.

Após a execução do Prompt 00, o Codex deverá parar e aguardar aprovação.

A Fase 1 somente poderá começar depois da aprovação do ambiente autônomo.

---

# 6. REVISÃO DA CONFIGURAÇÃO DO AMBIENTE AUTÔNOMO

## Informações gerais

**Prompt:** 00 — Configurar Ambiente Autônomo
**Data:** Não iniciado
**Responsável pela execução:** Codex
**Status:** Não iniciada
**Resultado esperado:** `PRONTO_COMPLETO`

---

## Objetivo

Configurar a ponte entre os arquivos locais, o `clasp`, o Google Apps Script e o Google Sheets para permitir implantação e testes autônomos.

---

## Entregas esperadas

* validação do Node.js;
* validação do npm;
* instalação ou validação do `clasp`;
* autenticação oficial do Google;
* criação ou localização da planilha;
* criação ou localização do projeto Apps Script;
* configuração do `.clasp.json`;
* primeiro `clasp push`;
* primeira execução real;
* teste de escrita e leitura;
* limpeza da aba temporária;
* segundo envio;
* segunda execução;
* validação visual;
* criação de `docs/AMBIENTE_AUTONOMO.md`.

---

## Critérios de aceite

* [ ] Node.js 20 ou superior validado.
* [ ] npm validado.
* [ ] `clasp` instalado.
* [ ] API do Apps Script habilitada.
* [ ] `clasp` autenticado.
* [ ] Planilha criada ou vinculada.
* [ ] Projeto Apps Script vinculado.
* [ ] `.clasp.json` válido.
* [ ] `clasp push` executado.
* [ ] Função real executada.
* [ ] Escrita temporária validada.
* [ ] Leitura validada.
* [ ] Limpeza validada.
* [ ] Segundo envio validado.
* [ ] Segunda execução validada.
* [ ] Chrome conectado validado.
* [ ] Google Sheets acessível.
* [ ] Google Apps Script acessível.
* [ ] `AMBIENTE_AUTONOMO.md` criado.
* [ ] Status final `PRONTO_COMPLETO`.

---

## Resultado

**Status:** Não iniciada
**Decisão do Product Owner:** Aguardando execução

---

# 7. REVISÃO DA FASE 1 — ANÁLISE DO EDITAL E DO CURSO

## Informações gerais

**Versão prevista:** 0.1.0
**Status:** Não iniciada
**Dependência:** Prompt 00 aprovado com status `PRONTO_COMPLETO`

---

## Objetivo

Analisar o edital oficial e a página pública do pacote do Estratégia, produzindo relatórios e arquivos de dados para a construção da planilha.

---

## Entregas esperadas

* `analises/00_Resumo_Fase_1.md`
* `analises/01_Estrutura_Prova.md`
* `analises/02_Analise_Estrategia.md`
* `analises/03_Matriz_Cobertura.md`
* `analises/04_Lacunas_Materiais.md`
* `analises/05_Estrategia_Inicial.md`
* `analises/06_Validacao_Dados.md`
* `dados/disciplinas.csv`
* `dados/assuntos.csv`
* `dados/config_inicial.csv`

---

## Resultado

**Status:** Não iniciada
**Decisão do Product Owner:** Aguardando execução

---

# 8. REVISÃO DA FASE 2 — ESTRUTURA DO GOOGLE SHEETS

## Informações gerais

**Versão prevista:** 0.2.0
**Status:** Não iniciada
**Dependências:**

* Prompt 00 aprovado;
* ambiente `PRONTO_COMPLETO`;
* Fase 1 aprovada.

---

## Objetivo

Criar, implantar e testar a estrutura do Google Sheets e do Google Apps Script.

---

## Entregas esperadas

* estrutura completa de `apps-script/`;
* `setupSOEA()` idempotente;
* abas visíveis;
* abas ocultas;
* cabeçalhos;
* importação dos dados;
* menu `SOEA`;
* Sidebars;
* Dashboard estrutural;
* Configurações;
* integridade estrutural;
* backup estrutural;
* `docs/INSTALACAO_FASE_2.md`;
* `docs/TESTES_FASE_2.md`.

---

## Resultado

**Status:** Não iniciada
**Decisão do Product Owner:** Aguardando execução

---

# 9. REVISÃO DA FASE 3 — MOTOR DO SOEA

## Informações gerais

**Versão prevista:** 0.3.0
**Status:** Não iniciada
**Dependências:**

* ambiente `PRONTO_COMPLETO`;
* Fase 2 aprovada.

---

## Objetivo

Implementar, implantar e testar o Motor Adaptativo do SOEA.

---

## Entregas esperadas

* ciclo;
* blocos;
* sessões;
* Continuar Ciclo;
* Retomar Ciclo;
* Aproveitar Tempo;
* Barra de Energia;
* Modo Emergência;
* registro de questões;
* Banco de Erros;
* revisões;
* Índice de Prioridade;
* Índice de Domínio;
* Tempo Estimado Inteligente;
* métricas;
* Dashboard funcional;
* integridade avançada;
* recuperação;
* backup;
* `docs/FORMULAS_SOEA.md`;
* `docs/TESTES_FASE_3.md`.

---

## Resultado

**Status:** Não iniciada
**Decisão do Product Owner:** Aguardando execução

---

# 10. REVISÃO DA FASE 4 — FINALIZAÇÃO E ENTREGA DA VERSÃO 1.0

## Informações gerais

**Versão prevista:** 1.0.0
**Status:** Não iniciada
**Dependências:**

* ambiente `PRONTO_COMPLETO`;
* Fase 3 aprovada.

---

## Objetivo

Finalizar os simulados, o Dashboard, as Estatísticas, os testes, a documentação e a implantação da versão SOEA v1.0.0.

---

## Entregas esperadas

* sistema de simulados;
* agenda de simulados;
* correção de simulados;
* Dashboard final;
* Estatísticas;
* testes de instalação;
* testes de atualização;
* regressões;
* revisão de segurança;
* revisão de performance;
* limpeza dos dados de teste;
* implantação final;
* `README.md` definitivo;
* `docs/TESTES_FASE_4.md`;
* versão `SOEA v1.0.0`.

---

## Resultado

**Status:** Não iniciada
**Decisão do Product Owner:** Aguardando execução

---

# 11. MODELOS DE DECISÃO DO PRODUCT OWNER

## Aprovação

```text
Fase aprovada.

Pode registrar a aprovação no ROADMAP.md e no REVIEW.md.

Não execute a próxima fase ainda.
```

---

## Autorização da próxima fase

```text
Pode iniciar a próxima fase.

Execute somente o prompt correspondente.

Ao concluir, pare e aguarde minha revisão.
```

---

## Aprovação com ressalvas

```text
Fase aprovada com ressalvas.

Pendências aceitas:

- item;
- item.

Mantenha as pendências no TODO.md.

Não execute a próxima fase ainda.
```

---

## Correções solicitadas

```text
Correções solicitadas.

Itens que precisam ser ajustados:

- item;
- item.

Corrija, execute novamente os testes afetados e atualize a documentação.

Não inicie a próxima fase.
```

---

## Reprovação

```text
Fase reprovada.

Motivos:

- descrição;
- descrição.

Revise a fase antes de prosseguir.

Não inicie a próxima fase.
```

---

## Aprovação final

```text
Fase 4 aprovada.

A versão SOEA v1.0.0 está aprovada para uso.

Atualize ROADMAP.md, REVIEW.md e CHANGELOG.md.

Marque a versão como estável.

Não inicie uma versão 2.0.
```

---

# 12. HISTÓRICO DE REVISÕES

| Etapa                 |            Versão | Status       | Data       | Observação                             |
| --------------------- | ----------------: | ------------ | ---------- | -------------------------------------- |
| Fase 0 — Documentação |             0.0.1 | Aprovada     | 16/07/2026 | Documentação de planejamento concluída |
| Prompt 00 — Ambiente  | ambiente-autonomo | Não iniciado | —          | Próxima etapa                          |
| Fase 1 — Análise      |             0.1.0 | Não iniciada | —          | Depende do Prompt 00                   |
| Fase 2 — Estrutura    |             0.2.0 | Não iniciada | —          | Depende da aprovação da Fase 1         |
| Fase 3 — Motor        |             0.3.0 | Não iniciada | —          | Depende da aprovação da Fase 2         |
| Fase 4 — Finalização  |             1.0.0 | Não iniciada | —          | Depende da aprovação da Fase 3         |

---

# 13. ESTADO ATUAL DO PROJETO

```text
FASE 0 — DOCUMENTAÇÃO E PREPARAÇÃO
Concluída e aprovada

PROMPT 00 — AMBIENTE AUTÔNOMO
Não iniciado

FASE 1 — ANÁLISE DO EDITAL E DO CURSO
Não iniciada

FASE 2 — ESTRUTURA DO GOOGLE SHEETS
Não iniciada

FASE 3 — MOTOR DO SOEA
Não iniciada

FASE 4 — FINALIZAÇÃO E VERSÃO 1.0
Não iniciada
```

---

# 14. PRÓXIMA AÇÃO AUTORIZADA

Executar somente:

```text
prompts/00_Configurar_Ambiente_Autonomo.md
```

O Codex não está autorizado a executar os Prompts 01, 02, 03 ou 04 neste momento.

Ao concluir o Prompt 00, o Codex deverá:

1. criar `docs/AMBIENTE_AUTONOMO.md`;
2. atualizar `TODO.md`;
3. atualizar `CHANGELOG.md`;
4. atualizar este `REVIEW.md`;
5. informar o status do ambiente;
6. parar;
7. aguardar aprovação do Product Owner.

O resultado necessário para continuar será:

```text
PRONTO_COMPLETO
```

---

# 15. ENCERRAMENTO

O `REVIEW.md` é o documento oficial de comunicação entre o Codex e o Product Owner ao final de cada etapa.

Sua função é garantir que:

* nenhuma etapa avance sem validação;
* o Product Owner saiba exatamente o que foi entregue;
* a implantação real seja distinguida da criação local de arquivos;
* testes não sejam declarados sem execução;
* bugs e limitações sejam transparentes;
* os dados sejam preservados;
* o projeto permaneça alinhado ao PRD;
* o desenvolvimento possa ser retomado sem perda de contexto;
* o Codex pare ao final de cada fase;
* a versão 1.0 somente seja considerada estável após aprovação final.
