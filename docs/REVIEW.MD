# REVIEW.md

# SOEA — Sistema Operacional de Estudos Adaptativo

**Versão atual:** 0.0.1
**Fase atual:** Fase 0 — Documentação e preparação
**Status da revisão:** Aguardando validação do Product Owner
**Product Owner:** Eduardo Arthur
**Tecnologias:** Google Sheets + Google Apps Script

---

# 1. OBJETIVO DESTE DOCUMENTO

Este documento registra a entrega de cada fase do desenvolvimento da Planilha Inteligente SOEA.

Ele deverá ser atualizado pelo Codex ao final de cada fase para informar, de forma clara:

* o que foi implementado;
* quais arquivos foram criados;
* quais arquivos foram alterados;
* quais testes foram realizados;
* quais pendências permanecem;
* quais bugs foram encontrados;
* quais limitações foram identificadas;
* quais pontos precisam ser validados pelo Product Owner;
* se a fase está pronta para aprovação.

O Codex não poderá iniciar a fase seguinte antes da aprovação explícita do Product Owner.

---

# 2. REGRAS DE ATUALIZAÇÃO

Ao final de cada fase, o Codex deverá:

1. Atualizar este documento.
2. Informar a fase concluída.
3. Resumir as entregas.
4. Listar arquivos criados.
5. Listar arquivos alterados.
6. Informar os testes executados.
7. Informar os resultados.
8. Registrar bugs conhecidos.
9. Registrar limitações.
10. Registrar pendências.
11. Indicar o que o Product Owner deve testar.
12. Informar se considera a fase pronta para aprovação.
13. Parar e aguardar resposta.

O Codex não deverá apagar revisões anteriores.

Cada nova fase deverá gerar uma nova seção neste arquivo.

---

# 3. STATUS POSSÍVEIS

Cada revisão poderá possuir um dos seguintes estados:

```text
Aguardando revisão

Aprovada

Aprovada com ressalvas

Reprovada

Correções solicitadas

Bloqueada
```

---

# 4. FORMATO PADRÃO DE REVISÃO

Utilizar o modelo abaixo ao final de cada fase:

```md
# REVISÃO DA FASE X — NOME DA FASE

## Informações gerais

Versão:

Data:

Responsável pela implementação:

Status:

---

## Objetivo da fase

Descrever brevemente o objetivo.

---

## Entregas realizadas

- Item implementado.
- Item implementado.

---

## Arquivos criados

- `Arquivo.gs`
- `Arquivo.html`

---

## Arquivos alterados

- `ArquivoExistente.gs`
- `ROADMAP.md`
- `TODO.md`
- `CHANGELOG.md`

---

## Testes realizados

### Teste 1

Cenário:

Resultado esperado:

Resultado obtido:

Status:

### Teste 2

Cenário:

Resultado esperado:

Resultado obtido:

Status:

---

## Bugs encontrados

Nenhum.

ou

- `BUG-001` — descrição.

---

## Limitações conhecidas

Nenhuma.

ou

- `LIM-001` — descrição.

---

## Pendências

Nenhuma.

ou

- Item pendente.

---

## Riscos identificados

Nenhum.

ou

- Risco identificado.

---

## Pontos para validação do Product Owner

- Verificar item.
- Confirmar item.
- Testar fluxo.

---

## Critérios de aceite

- [ ] Critério validado.
- [ ] Critério validado.

---

## Resultado da fase

Pronta para aprovação:

Sim ou Não.

Justificativa:

---

## Decisão do Product Owner

Status:

Data:

Observações:

---

## Próxima fase

Nome da próxima fase.

A execução só poderá começar após aprovação explícita.
```

---

# 5. REVISÃO DA FASE 0 — DOCUMENTAÇÃO E PREPARAÇÃO

## Informações gerais

**Versão:** 0.0.1
**Data:** a preencher
**Responsável pela preparação:** Eduardo Arthur e assistência de IA
**Status:** Aguardando revisão

---

## Objetivo da fase

Definir completamente o escopo, os requisitos, a arquitetura, o planejamento e os documentos de acompanhamento da versão 1.0 da Planilha Inteligente SOEA.

---

## Entregas realizadas

* Definição do conceito da Planilha Inteligente SOEA.
* Definição da metodologia híbrida de estudos.
* Definição do fluxo Continuar Ciclo.
* Definição do fluxo Retomar Ciclo.
* Definição da funcionalidade Aproveitar Tempo.
* Definição da Barra de Energia.
* Definição dos blocos e sessões.
* Definição do Banco de Questões.
* Definição do Banco de Erros.
* Definição das revisões automáticas.
* Definição do sistema de simulados.
* Definição do Índice de Prioridade.
* Definição do Índice de Domínio.
* Definição do Tempo Estimado Inteligente.
* Definição das abas visíveis.
* Definição das abas ocultas.
* Definição do modelo de dados.
* Definição da arquitetura do Google Apps Script.
* Definição das fases de desenvolvimento.
* Definição do processo de aprovação pelo Product Owner.

---

## Documentos criados

* `PRD.md`
* `ARQUITETURA.md`
* `ROADMAP.md`
* `TODO.md`
* `CHANGELOG.md`
* `REVIEW.md`

---

## Documentos pendentes

* `README.md` inicial ou esqueleto.

O README completo será finalizado na Fase 4.

---

## Implementação realizada

Nenhuma implementação em Google Sheets ou Google Apps Script foi iniciada.

Esta fase foi exclusivamente dedicada à documentação e à engenharia de requisitos.

---

## Testes realizados

### Teste 1 — Coerência entre PRD e Arquitetura

**Cenário:** comparar os requisitos do `PRD.md` com a organização proposta no `ARQUITETURA.md`.

**Resultado esperado:** nenhuma tecnologia ou decisão arquitetural deve contrariar o PRD.

**Resultado obtido:** aguardando validação final do Product Owner.

**Status:** Pendente.

---

### Teste 2 — Coerência entre Roadmap e TODO

**Cenário:** verificar se as fases do `ROADMAP.md` estão representadas por tarefas no `TODO.md`.

**Resultado esperado:** todas as fases possuem tarefas concretas e verificáveis.

**Resultado obtido:** estrutura criada e pronta para validação.

**Status:** Pendente de aprovação.

---

### Teste 3 — Controle documental

**Cenário:** verificar se os documentos necessários para manter o contexto do Codex foram definidos.

**Resultado esperado:** PRD, Arquitetura, Roadmap, TODO, Changelog e Review disponíveis.

**Resultado obtido:** todos os documentos principais foram criados.

**Status:** Aprovado tecnicamente.

---

## Bugs encontrados

Nenhum bug de implementação, pois o desenvolvimento ainda não foi iniciado.

---

## Limitações conhecidas

* O conteúdo do edital ainda não foi processado pelo Codex.
* O conteúdo do pacote do Estratégia ainda não foi comparado formalmente com o edital.
* A fórmula exata do Índice de Prioridade ainda será definida durante a Fase 3.
* A fórmula exata do Índice de Domínio ainda será definida durante a Fase 3.
* A aparência final da planilha ainda não foi criada.
* As limitações reais do Apps Script serão validadas durante a implementação.

---

## Pendências

* Consolidar o `PRD.md` em um único arquivo.
* Revisar a numeração final dos capítulos do PRD.
* Confirmar o `ARQUITETURA.md`.
* Confirmar o `ROADMAP.md`.
* Confirmar o `TODO.md`.
* Confirmar o `CHANGELOG.md`.
* Criar um esqueleto inicial do `README.md`, caso desejado antes da Fase 1.
* Preparar o edital oficial para envio ao Codex.
* Preparar o link do pacote do Estratégia.
* Criar o Prompt da Fase 1.

---

## Riscos identificados

### Risco 1 — Escopo excessivo

O projeto possui muitas funcionalidades.

**Tratamento:** priorizar o fluxo principal e impedir inclusão de novos recursos fora do PRD.

### Risco 2 — Tempo de desenvolvimento

A preparação para o concurso não poderá ser prejudicada pelo desenvolvimento da ferramenta.

**Tratamento:** começar a utilizar a planilha assim que o fluxo central da Fase 3 estiver estável.

### Risco 3 — Limite temporário do Codex

A opção gratuita poderá possuir limites de uso.

**Tratamento:** manter toda a documentação atualizada e executar o projeto por fases independentes.

### Risco 4 — Acesso ao conteúdo do Estratégia

A página pode não apresentar todos os módulos publicamente ou exigir autenticação.

**Tratamento:** classificar conteúdos não verificáveis como “Não verificado” e não inventar correspondências.

---

## Pontos para validação do Product Owner

O Product Owner deverá confirmar:

* [ ] O objetivo da planilha está correto.
* [ ] O escopo da versão 1.0 está correto.
* [ ] Google Sheets + Google Apps Script continuam sendo as únicas tecnologias.
* [ ] As abas visíveis estão corretas.
* [ ] As abas ocultas estão corretas.
* [ ] O fluxo Continuar Ciclo está correto.
* [ ] O fluxo Aproveitar Tempo está correto.
* [ ] As revisões estão corretamente vinculadas aos blocos.
* [ ] O processo de aprovação por fases está correto.
* [ ] O Roadmap está adequado.
* [ ] O TODO cobre todas as entregas.
* [ ] O projeto está pronto para iniciar a Fase 1.

---

## Critérios de aceite da Fase 0

* [x] PRD criado.
* [x] Arquitetura criada.
* [x] Roadmap criado.
* [x] TODO criado.
* [x] Changelog criado.
* [x] Review criado.
* [ ] Product Owner aprovou todos os documentos.
* [ ] Prompt da Fase 1 está pronto.
* [ ] Edital está disponível para o Codex.
* [ ] Link do Estratégia está disponível para o Codex.

---

## Resultado da fase

**Pronta para aprovação:** Parcialmente.

A documentação-base foi criada, mas ainda depende da aprovação formal do Product Owner e da consolidação final do PRD.

---

## Decisão do Product Owner

**Status:** Aguardando decisão
**Data:** a preencher

**Observações:**

A preencher pelo Product Owner.

---

## Próxima fase

**Fase 1 — Análise do edital e do pacote do Estratégia.**

A execução só poderá começar após:

1. aprovação da Fase 0;
2. consolidação dos documentos;
3. disponibilização do edital;
4. disponibilização do link do pacote;
5. criação e envio do Prompt da Fase 1.

---

# 6. MODELO DE DECISÃO DO PRODUCT OWNER

Ao revisar uma fase, o Product Owner deverá responder utilizando um dos formatos abaixo.

## Aprovação

```text
Fase aprovada.

Pode iniciar a próxima fase.
```

## Aprovação com ressalvas

```text
Fase aprovada com ressalvas.

Pendências aceitas:
- item.

Pode iniciar a próxima fase, mantendo as pendências no TODO.md.
```

## Correções solicitadas

```text
Correções solicitadas.

Itens que precisam ser ajustados:
- item;
- item.

Não iniciar a próxima fase.
```

## Reprovação

```text
Fase reprovada.

Motivo:
- descrição.

Revisar a fase antes de prosseguir.
```

---

# 7. HISTÓRICO DE REVISÕES

| Fase   | Versão | Status             | Data        | Observação                  |
| ------ | ------ | ------------------ | ----------- | --------------------------- |
| Fase 0 | 0.0.1  | Aguardando revisão | A preencher | Documentação inicial criada |
| Fase 1 | 0.1.0  | Não iniciada       | —           | —                           |
| Fase 2 | 0.2.0  | Não iniciada       | —           | —                           |
| Fase 3 | 0.3.0  | Não iniciada       | —           | —                           |
| Fase 4 | 1.0.0  | Não iniciada       | —           | —                           |

---

# 8. ENCERRAMENTO

O `REVIEW.md` é o documento de comunicação entre o Codex e o Product Owner ao final de cada fase.

Sua função é garantir que:

* nenhuma etapa avance sem validação;
* o Product Owner saiba exatamente o que foi entregue;
* bugs e limitações sejam transparentes;
* o projeto permaneça alinhado ao PRD;
* o desenvolvimento possa ser retomado sem perda de contexto.
