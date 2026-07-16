# TODO.md

# SOEA — Sistema Operacional de Estudos Adaptativo

**Versão planejada:** 1.0.0
**Status geral:** documentação aprovada; ambiente autônomo ainda não configurado
**Fase funcional atual:** Fase 1 — ainda não iniciada
**Próxima ação autorizada:** executar somente o Prompt 00
**Product Owner:** Eduardo Arthur
**Tecnologias:** Google Sheets + Google Apps Script
**Concurso:** DATAPREV 2026 — Perfil 3 — Desenvolvimento de Software
**Data prevista da prova:** 11 de outubro de 2026
**Data da última atualização:** 16 de julho de 2026

---

# 1. OBJETIVO DESTE DOCUMENTO

Este documento contém as tarefas necessárias para configurar, construir, testar, revisar e entregar a versão 1.0.0 da Planilha Inteligente SOEA.

O `TODO.md` deverá ser atualizado continuamente pelo Codex.

Ele deverá permitir que o Product Owner identifique:

* a etapa atual;
* as tarefas concluídas;
* as tarefas em andamento;
* as tarefas bloqueadas;
* as tarefas ainda não iniciadas;
* os bugs abertos;
* as limitações;
* as dependências;
* os testes executados;
* os testes pendentes;
* os itens adiados;
* a próxima ação permitida.

O Codex não poderá apagar tarefas ou históricos sem justificativa.

---

# 2. LEGENDA DE STATUS

Cada tarefa deverá utilizar um dos seguintes estados:

```text
[ ] Não iniciada
[-] Em andamento
[x] Concluída
[!] Bloqueada
[~] Adiada para versão futura
```

## Regras

* `[ ]` significa que a tarefa ainda não foi iniciada.
* `[-]` significa que a tarefa está sendo executada.
* `[x]` significa que a tarefa foi implementada e validada.
* `[!]` significa que existe um impedimento real.
* `[~]` significa que a tarefa não faz parte da versão 1.0 ou foi formalmente adiada.

Uma tarefa não poderá ser marcada como concluída apenas porque:

* o código foi escrito;
* um arquivo foi criado;
* a sintaxe parece correta;
* a alteração foi enviada com `clasp`;
* uma função existe no editor;
* o Codex acredita que funcionará.

Quando a tarefa envolver Google Sheets ou Google Apps Script, a conclusão deverá exigir, conforme aplicável:

1. implementação local;
2. validação local;
3. envio com `clasp push`;
4. execução real;
5. validação na planilha;
6. correção de erros;
7. repetição dos testes;
8. registro no documento de testes;
9. atualização da documentação.

---

# 3. REGRAS GERAIS DE UTILIZAÇÃO

## 3.1 Antes de iniciar qualquer etapa

O Codex deverá:

* [ ] Ler `docs/PRD.md`.
* [ ] Ler `docs/ARQUITETURA.md`.
* [ ] Ler `docs/INSTRUCOES.md`.
* [ ] Ler `docs/ROADMAP.md`.
* [ ] Ler `docs/TODO.md`.
* [ ] Ler `docs/CHANGELOG.md`.
* [ ] Ler `docs/REVIEW.md`.
* [ ] Ler o prompt autorizado.
* [ ] Verificar a fase atual.
* [ ] Verificar se a etapa anterior foi aprovada.
* [ ] Verificar dependências.
* [ ] Verificar bloqueios.
* [ ] Verificar riscos de perda de dados.
* [ ] Verificar o status do ambiente autônomo, quando aplicável.
* [ ] Marcar a tarefa principal como `Em andamento`.
* [ ] Não iniciar tarefas de fases posteriores.

As tarefas desta seção são recorrentes e deverão ser verificadas novamente no início de cada fase.

---

## 3.2 Durante a execução

O Codex deverá:

* [ ] Preservar os arquivos existentes.
* [ ] Preservar os dados existentes.
* [ ] Evitar alterações fora do escopo.
* [ ] Registrar decisões técnicas relevantes.
* [ ] Registrar bugs encontrados.
* [ ] Registrar limitações encontradas.
* [ ] Criar backup antes de operações críticas.
* [ ] Solicitar intervenção humana somente nos casos permitidos.
* [ ] Não solicitar senha, token, cookie ou código de autenticação.
* [ ] Não transferir ao Product Owner tarefas técnicas executáveis pelo Codex.
* [ ] Não inventar dados, resultados ou testes.

---

## 3.3 Ao concluir uma tarefa

O Codex deverá:

* [ ] Validar o resultado.
* [ ] Executar os testes correspondentes.
* [ ] Corrigir problemas encontrados.
* [ ] Executar regressões relacionadas.
* [ ] Marcar a tarefa como concluída somente após validação.
* [ ] Atualizar `docs/CHANGELOG.md`.
* [ ] Atualizar `docs/ROADMAP.md`, quando necessário.
* [ ] Atualizar `docs/REVIEW.md`.
* [ ] Atualizar o documento de testes correspondente.
* [ ] Registrar bugs ou limitações.
* [ ] Preservar as evidências possíveis.
* [ ] Parar ao final da fase.
* [ ] Não iniciar a próxima fase sem aprovação explícita.

---

# 4. FASE 0 — DOCUMENTAÇÃO E PREPARAÇÃO

**Status:** concluída e aprovada.

---

## 4.1 Documentos-base

* [x] Definir o conceito da Planilha Inteligente SOEA.
* [x] Definir o objetivo da versão 1.0.
* [x] Definir Google Sheets e Google Apps Script como tecnologias obrigatórias.
* [x] Definir tecnologias fora do escopo.
* [x] Criar `docs/PRD.md`.
* [x] Criar `docs/ARQUITETURA.md`.
* [x] Criar `docs/INSTRUCOES.md`.
* [x] Criar `docs/ROADMAP.md`.
* [x] Criar `docs/TODO.md`.
* [x] Criar `docs/CHANGELOG.md`.
* [x] Criar `docs/REVIEW.md`.
* [x] Criar `README.md` inicial.
* [x] Criar `FluxoCodex.md`.
* [x] Criar `.gitignore`.
* [x] Padronizar os nomes dos arquivos.
* [x] Padronizar o nome do edital.
* [x] Registrar a aprovação da Fase 0.

---

## 4.2 Requisitos definidos

* [x] Definir Continuar Ciclo.
* [x] Definir Retomar Ciclo.
* [x] Definir Aproveitar Tempo.
* [x] Definir sessões de estudo.
* [x] Definir Barra de Energia.
* [x] Definir Modo Emergência.
* [x] Definir blocos de estudo.
* [x] Definir etapas dos blocos.
* [x] Definir IDs internos.
* [x] Definir registro de questões.
* [x] Definir Banco de Erros.
* [x] Definir revisões automáticas.
* [x] Definir simulados.
* [x] Definir agenda de simulados.
* [x] Definir Índice de Prioridade.
* [x] Definir Índice de Domínio.
* [x] Definir Tempo Estimado Inteligente.
* [x] Definir salvamento automático.
* [x] Definir histórico.
* [x] Definir logs.
* [x] Definir backup.
* [x] Definir recuperação.
* [x] Definir integridade.
* [x] Definir abas visíveis.
* [x] Definir abas ocultas.
* [x] Definir arquitetura dos arquivos Apps Script.
* [x] Definir processo de aprovação por fases.
* [x] Definir execução autônoma com `clasp`.
* [x] Definir testes reais no Google Sheets.
* [x] Definir estratégia de dados de teste.
* [x] Definir limpeza segura dos dados de teste.

---

## 4.3 Prompts

* [x] Criar `prompts/00_Configurar_Ambiente_Autonomo.md`.
* [x] Criar `prompts/01_Fase_Analise.md`.
* [x] Criar `prompts/02_Fase_Estrutura.md`.
* [x] Criar `prompts/03_Fase_Motor.md`.
* [x] Criar `prompts/04_Fase_Finalizacao.md`.
* [x] Adaptar o Prompt 2 para implantação autônoma.
* [x] Adaptar o Prompt 3 para implantação autônoma.
* [x] Adaptar o Prompt 4 para implantação autônoma.
* [x] Impedir avanço automático entre as fases.
* [x] Documentar mensagens para autorização de cada fase.

---

## 4.4 Fontes

* [x] Adicionar o edital oficial.
* [x] Salvar como `fontes/edital-dataprev-2026.pdf`.
* [x] Registrar o link público do pacote do Estratégia no Prompt 1.
* [x] Definir o edital como fonte oficial.
* [x] Definir o Estratégia como fonte de cobertura dos materiais.
* [x] Definir o tratamento para informações não verificadas.

---

## 4.5 Aprovação documental

* [x] Confirmar versão consolidada do `PRD.md`.
* [x] Confirmar versão final do `ARQUITETURA.md`.
* [x] Confirmar versão final do `INSTRUCOES.md`.
* [x] Confirmar versão inicial do `ROADMAP.md`.
* [x] Confirmar versão inicial do `TODO.md`.
* [x] Confirmar versão inicial do `CHANGELOG.md`.
* [x] Confirmar versão consolidada do `REVIEW.md`.
* [x] Confirmar fluxo de execução.
* [x] Registrar aprovação da Fase 0 no `ROADMAP.md`.
* [x] Registrar aprovação da Fase 0 no `REVIEW.md`.
* [x] Definir o Prompt 00 como próxima ação.
* [x] Não iniciar implementação funcional antecipadamente.

---

# 5. PROMPT 00 — CONFIGURAÇÃO DO AMBIENTE AUTÔNOMO

**Status:** não iniciado.

**Arquivo:** `prompts/00_Configurar_Ambiente_Autonomo.md`

**Objetivo obrigatório:** atingir `PRONTO_COMPLETO`.

---

## 5.1 Leitura e preparação

* [ ] Ler todos os documentos obrigatórios.
* [ ] Confirmar que a Fase 0 está aprovada.
* [ ] Confirmar que somente o Prompt 00 foi autorizado.
* [ ] Confirmar o diretório correto do projeto.
* [ ] Verificar permissões de escrita.
* [ ] Verificar sistema operacional.
* [ ] Verificar terminal disponível.
* [ ] Verificar conexão com a internet.
* [ ] Verificar Git, quando disponível.

---

## 5.2 Node.js e npm

* [ ] Executar `node --version`.
* [ ] Confirmar Node.js 20 ou superior.
* [ ] Executar `npm --version`.
* [ ] Confirmar npm funcional.
* [ ] Registrar versões no relatório.
* [ ] Corrigir incompatibilidade de forma segura, quando possível.
* [ ] Não alterar ambiente corporativo sem autorização.

---

## 5.3 Instalação do clasp

* [ ] Executar `clasp --version`.
* [ ] Testar `npx clasp --version`, quando necessário.
* [ ] Instalar `@google/clasp` globalmente, quando permitido.
* [ ] Utilizar instalação local quando a global exigir privilégios.
* [ ] Registrar o método utilizado.
* [ ] Definir o comando oficial para as fases seguintes.
* [ ] Confirmar que o `clasp` responde corretamente.

---

## 5.4 Proteção de credenciais

* [ ] Verificar `.gitignore`.
* [ ] Proteger `.clasprc.json`.
* [ ] Proteger `credentials.json`.
* [ ] Proteger `client_secret*.json`.
* [ ] Proteger `token.json`.
* [ ] Proteger diretórios de tokens.
* [ ] Proteger `.env`.
* [ ] Proteger `node_modules/`.
* [ ] Verificar ausência de credenciais versionadas.
* [ ] Não registrar tokens em documentos.
* [ ] Não registrar tokens no chat.

---

## 5.5 Chrome e Computer Use

* [ ] Confirmar Chrome instalado.
* [ ] Confirmar perfil correto do Chrome.
* [ ] Confirmar conta Google conectada.
* [ ] Confirmar extensão ou plugin conectado.
* [ ] Confirmar Computer Use habilitado.
* [ ] Confirmar permissão para operar o Chrome.
* [ ] Confirmar acesso ao Google Sheets.
* [ ] Confirmar acesso ao Google Apps Script.
* [ ] Registrar limitações visuais, caso existam.

---

## 5.6 API e autenticação

* [ ] Verificar acesso externo ao Apps Script.
* [ ] Habilitar a configuração oficial necessária.
* [ ] Executar `clasp login`.
* [ ] Solicitar intervenção humana somente para segurança.
* [ ] Não solicitar senha ou código pelo chat.
* [ ] Confirmar autenticação pelo terminal.
* [ ] Executar `clasp list`.
* [ ] Confirmar que a conta correta foi utilizada.

---

## 5.7 Projeto e planilha

* [ ] Verificar se já existe projeto SOEA.
* [ ] Verificar se já existe planilha SOEA.
* [ ] Evitar duplicidade.
* [ ] Confirmar projeto correto.
* [ ] Confirmar planilha correta.
* [ ] Criar pasta `apps-script/`, quando ausente.
* [ ] Criar projeto Apps Script vinculado ao Sheets.
* [ ] Criar ou validar `.clasp.json`.
* [ ] Criar ou validar `appsscript.json`.
* [ ] Confirmar `scriptId`.
* [ ] Confirmar vínculo real com a planilha.

---

## 5.8 Teste de diagnóstico

* [ ] Criar `apps-script/EnvironmentCheck.gs`.
* [ ] Implementar `validarAmbienteSOEA()`.
* [ ] Criar aba temporária.
* [ ] Escrever dados temporários.
* [ ] Ler dados temporários.
* [ ] Validar o conteúdo.
* [ ] Excluir a aba temporária.
* [ ] Garantir que nenhuma aba temporária permaneceu.
* [ ] Retornar resultado estruturado.
* [ ] Registrar a versão do teste.

---

## 5.9 Primeiro envio e execução

* [ ] Executar `clasp status`.
* [ ] Executar `clasp push`.
* [ ] Confirmar envio concluído.
* [ ] Executar `clasp open-script`.
* [ ] Confirmar arquivos no editor remoto.
* [ ] Executar `validarAmbienteSOEA()`.
* [ ] Concluir autorização oficial, quando necessária.
* [ ] Confirmar execução sem erro.
* [ ] Confirmar escrita e leitura.
* [ ] Confirmar limpeza.
* [ ] Abrir a planilha vinculada.
* [ ] Confirmar que a planilha correta foi utilizada.

---

## 5.10 Segundo envio e segunda execução

* [ ] Alterar a versão do diagnóstico.
* [ ] Executar novo `clasp push`.
* [ ] Confirmar que a alteração chegou ao editor.
* [ ] Executar novamente a função.
* [ ] Confirmar segundo resultado.
* [ ] Confirmar ciclo local → remoto → planilha.
* [ ] Confirmar que o Codex consegue corrigir e reenviar.

---

## 5.11 Documentação do ambiente

* [ ] Criar `docs/AMBIENTE_AUTONOMO.md`.
* [ ] Registrar sistema operacional.
* [ ] Registrar Node.js.
* [ ] Registrar npm.
* [ ] Registrar `clasp`.
* [ ] Registrar forma de instalação.
* [ ] Registrar autenticação.
* [ ] Registrar planilha.
* [ ] Registrar projeto Apps Script.
* [ ] Registrar Chrome.
* [ ] Registrar Computer Use.
* [ ] Registrar testes.
* [ ] Registrar intervenções humanas.
* [ ] Registrar limitações.
* [ ] Classificar o ambiente.

---

## 5.12 Critérios de conclusão do Prompt 00

* [ ] Node.js compatível.
* [ ] npm funcional.
* [ ] `clasp` funcional.
* [ ] `clasp` autenticado.
* [ ] API do Apps Script habilitada.
* [ ] Planilha vinculada.
* [ ] Projeto Apps Script vinculado.
* [ ] `.clasp.json` válido.
* [ ] Primeiro `clasp push` aprovado.
* [ ] Primeira execução real aprovada.
* [ ] Escrita temporária aprovada.
* [ ] Leitura aprovada.
* [ ] Limpeza aprovada.
* [ ] Segundo envio aprovado.
* [ ] Segunda execução aprovada.
* [ ] Chrome conectado.
* [ ] Google Sheets acessível.
* [ ] Apps Script acessível.
* [ ] `AMBIENTE_AUTONOMO.md` criado.
* [ ] `TODO.md` atualizado.
* [ ] `CHANGELOG.md` atualizado.
* [ ] `REVIEW.md` atualizado.
* [ ] Status final `PRONTO_COMPLETO`.
* [ ] Parar e aguardar aprovação.

---

# 6. FASE 1 — ANÁLISE DO EDITAL E DO CURSO

**Status:** não iniciada.

**Dependência:** Prompt 00 concluído e aprovado.

---

## 6.1 Entradas

* [ ] Confirmar `docs/AMBIENTE_AUTONOMO.md`.
* [ ] Confirmar status `PRONTO_COMPLETO`.
* [ ] Confirmar aprovação do Prompt 00.
* [ ] Confirmar disponibilidade do edital.
* [ ] Confirmar que o PDF corresponde ao edital correto.
* [ ] Confirmar Perfil 3 — Desenvolvimento de Software.
* [ ] Confirmar data e versão do edital.
* [ ] Acessar a página pública do pacote do Estratégia.
* [ ] Registrar o link utilizado.
* [ ] Registrar limitações de acesso.
* [ ] Não presumir acesso à assinatura.

---

## 6.2 Estrutura da prova

* [ ] Identificar banca organizadora.
* [ ] Identificar data da prova.
* [ ] Identificar duração da prova.
* [ ] Identificar quantidade total de questões.
* [ ] Identificar Conhecimentos Gerais.
* [ ] Identificar Conhecimentos Específicos.
* [ ] Identificar quantidade por grupo.
* [ ] Identificar pesos.
* [ ] Identificar pontuação máxima.
* [ ] Identificar nota mínima.
* [ ] Identificar critérios de eliminação.
* [ ] Identificar regra de não zerar disciplinas.
* [ ] Identificar regras de desempate relevantes.
* [ ] Identificar demais regras úteis ao planejamento.
* [ ] Citar a fonte de cada informação.

---

## 6.3 Disciplinas

* [ ] Extrair disciplinas de Conhecimentos Gerais.
* [ ] Extrair disciplinas de Conhecimentos Específicos.
* [ ] Preservar nomes oficiais.
* [ ] Criar IDs únicos.
* [ ] Definir grupo.
* [ ] Definir quantidade de questões, quando disponível.
* [ ] Definir peso.
* [ ] Definir pontuação máxima.
* [ ] Definir prioridade-base.
* [ ] Definir ordem inicial.
* [ ] Definir status.
* [ ] Validar duplicidade.
* [ ] Validar caracteres especiais.

---

## 6.4 Assuntos

* [ ] Extrair todos os tópicos.
* [ ] Extrair subtópicos relevantes.
* [ ] Preservar a redação oficial.
* [ ] Associar à disciplina correta.
* [ ] Criar IDs únicos.
* [ ] Definir ordem.
* [ ] Definir status.
* [ ] Identificar tópicos amplos.
* [ ] Subdividir somente quando necessário.
* [ ] Evitar assuntos excessivamente pequenos.
* [ ] Evitar unir conteúdos distintos.
* [ ] Validar registros órfãos.
* [ ] Validar duplicidade.

---

## 6.5 Pacote do Estratégia

* [ ] Listar cursos identificáveis.
* [ ] Listar disciplinas.
* [ ] Identificar aulas.
* [ ] Identificar módulos.
* [ ] Identificar PDFs informados.
* [ ] Identificar videoaulas informadas.
* [ ] Identificar simulados informados.
* [ ] Identificar trilhas ou bancos relacionados.
* [ ] Registrar conteúdo extra.
* [ ] Registrar conteúdo não verificável.
* [ ] Não copiar conteúdo protegido.
* [ ] Não solicitar credenciais.

---

## 6.6 Comparação edital × Estratégia

Para cada assunto:

* [ ] Localizar material correspondente.
* [ ] Registrar curso.
* [ ] Registrar aula ou módulo.
* [ ] Classificar como `Completa`.
* [ ] Classificar como `Parcial`.
* [ ] Classificar como `Ausente`.
* [ ] Classificar como `Não verificada`.
* [ ] Registrar observações.
* [ ] Registrar lacuna.
* [ ] Registrar material complementar.
* [ ] Registrar conteúdo excedente.
* [ ] Garantir que nenhum assunto fique sem classificação.

---

## 6.7 Estratégia inicial de estudos

* [ ] Priorizar Conhecimentos Específicos.
* [ ] Garantir contato com todas as disciplinas.
* [ ] Evitar risco de zerar disciplina.
* [ ] Definir proporção teoria × questões.
* [ ] Definir tempos iniciais.
* [ ] Definir questões iniciais.
* [ ] Definir tratamento para assunto novo.
* [ ] Definir tratamento para assunto conhecido.
* [ ] Definir tratamento para disciplina teórica.
* [ ] Definir tratamento para Português.
* [ ] Definir tratamento para Inglês.
* [ ] Definir tratamento para Raciocínio Lógico.
* [ ] Definir tratamento para Legislação.
* [ ] Definir tratamento para Atualidades e IA.
* [ ] Definir tratamento para Conhecimentos Específicos.
* [ ] Definir parâmetros iniciais editáveis.

---

## 6.8 Arquivos de análise

* [ ] Criar `analises/`.
* [ ] Criar `analises/00_Resumo_Fase_1.md`.
* [ ] Criar `analises/01_Estrutura_Prova.md`.
* [ ] Criar `analises/02_Analise_Estrategia.md`.
* [ ] Criar `analises/03_Matriz_Cobertura.md`.
* [ ] Criar `analises/04_Lacunas_Materiais.md`.
* [ ] Criar `analises/05_Estrategia_Inicial.md`.
* [ ] Criar `analises/06_Validacao_Dados.md`.

---

## 6.9 Dados de importação

* [ ] Criar `dados/`.
* [ ] Criar `dados/disciplinas.csv`.
* [ ] Criar `dados/assuntos.csv`.
* [ ] Criar `dados/config_inicial.csv`.
* [ ] Validar UTF-8.
* [ ] Validar cabeçalhos.
* [ ] Validar IDs.
* [ ] Validar relacionamentos.
* [ ] Validar pesos.
* [ ] Validar nomes.
* [ ] Validar datas.
* [ ] Validar valores permitidos.
* [ ] Validar campos obrigatórios.
* [ ] Validar linhas vazias.
* [ ] Validar caracteres especiais.
* [ ] Validar registros `Não verificado`.
* [ ] Preparar formato reutilizável pelo setup.

---

## 6.10 Entrega da Fase 1

* [ ] Conferir todos os relatórios.
* [ ] Conferir todos os CSVs.
* [ ] Registrar contagens.
* [ ] Registrar limitações.
* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar `TODO.md`.
* [ ] Atualizar `REVIEW.md`.
* [ ] Registrar a revisão da Fase 1.
* [ ] Não criar Apps Script.
* [ ] Não alterar a planilha.
* [ ] Parar e aguardar aprovação.

---

# 7. FASE 2 — ESTRUTURA DO GOOGLE SHEETS

**Status:** não iniciada.

**Dependências:**

* ambiente `PRONTO_COMPLETO`;
* Fase 1 aprovada.

---

## 7.1 Validação inicial

* [ ] Confirmar aprovação da Fase 1.
* [ ] Confirmar ambiente `PRONTO_COMPLETO`.
* [ ] Confirmar projeto Apps Script correto.
* [ ] Confirmar planilha correta.
* [ ] Confirmar `.clasp.json`.
* [ ] Confirmar dados da Fase 1.
* [ ] Validar CSVs.
* [ ] Criar backup do projeto remoto, quando necessário.
* [ ] Comparar arquivos remotos e locais.
* [ ] Não usar `--force` sem análise.

---

## 7.2 Estrutura do Apps Script

* [ ] Criar ou validar `appsscript.json`.
* [ ] Criar `Main.gs`.
* [ ] Criar `Setup.gs`.
* [ ] Criar `Constants.gs`.
* [ ] Criar `SeedData.gs`.
* [ ] Criar `Repository.gs`.
* [ ] Criar `MenuController.gs`.
* [ ] Criar `SidebarController.gs`.
* [ ] Criar `SoeaEngine.gs`.
* [ ] Criar `CycleService.gs`.
* [ ] Criar `BlockService.gs`.
* [ ] Criar `SessionService.gs`.
* [ ] Criar `QuestionService.gs`.
* [ ] Criar `ReviewService.gs`.
* [ ] Criar `ErrorBankService.gs`.
* [ ] Criar `SimulationService.gs`.
* [ ] Criar `PriorityService.gs`.
* [ ] Criar `MasteryService.gs`.
* [ ] Criar `DashboardService.gs`.
* [ ] Criar `MetricsService.gs`.
* [ ] Criar `HistoryService.gs`.
* [ ] Criar `BackupService.gs`.
* [ ] Criar `ConfigService.gs`.
* [ ] Criar `IdService.gs`.
* [ ] Criar `ValidationService.gs`.
* [ ] Criar `RecoveryService.gs`.
* [ ] Criar `Utils.gs`.

---

## 7.3 Arquivos HTML

* [ ] Criar `SidebarSession.html`.
* [ ] Criar `SidebarOpportunity.html`.
* [ ] Criar `SidebarQuestionResult.html`.
* [ ] Criar `SidebarErrorEntry.html`.
* [ ] Criar `SidebarReview.html`.
* [ ] Criar `SidebarSimulation.html`.
* [ ] Criar `SidebarSettings.html`.
* [ ] Criar `SidebarAbout.html`.
* [ ] Criar `Styles.html`.
* [ ] Criar `Scripts.html`.
* [ ] Criar `Components.html`.
* [ ] Criar função `include`.
* [ ] Evitar bibliotecas externas.
* [ ] Evitar CDN.

---

## 7.4 SeedData

* [ ] Converter `disciplinas.csv`.
* [ ] Converter `assuntos.csv`.
* [ ] Converter `config_inicial.csv`.
* [ ] Preservar IDs.
* [ ] Preservar acentos.
* [ ] Preservar textos oficiais.
* [ ] Escapar caracteres.
* [ ] Registrar origem.
* [ ] Registrar contagens.
* [ ] Comparar CSV e constantes.
* [ ] Validar relacionamentos.

---

## 7.5 Setup

* [ ] Implementar `setupSOEA()`.
* [ ] Utilizar `LockService`.
* [ ] Validar planilha.
* [ ] Validar versão estrutural.
* [ ] Criar backup quando necessário.
* [ ] Criar abas ausentes.
* [ ] Preservar abas existentes.
* [ ] Criar cabeçalhos ausentes.
* [ ] Validar cabeçalhos existentes.
* [ ] Aplicar formatação.
* [ ] Aplicar validações.
* [ ] Importar dados ausentes.
* [ ] Preservar configurações editadas.
* [ ] Ocultar abas internas.
* [ ] Proteger abas internas.
* [ ] Registrar histórico.
* [ ] Registrar logs.
* [ ] Executar integridade.
* [ ] Exibir resumo.
* [ ] Liberar lock em `finally`.

---

## 7.6 Idempotência

* [ ] Impedir abas duplicadas.
* [ ] Impedir cabeçalhos duplicados.
* [ ] Impedir disciplinas duplicadas.
* [ ] Impedir assuntos duplicados.
* [ ] Impedir configurações duplicadas.
* [ ] Preservar dados existentes.
* [ ] Preservar IDs.
* [ ] Preservar configurações editadas.
* [ ] Preservar formatações autorizadas.
* [ ] Não criar ciclo durante setup.
* [ ] Não apagar progresso futuro.
* [ ] Testar segunda execução real.

---

## 7.7 Abas visíveis

Criar e formatar:

* [ ] `Dashboard`.
* [ ] `Ciclo`.
* [ ] `Banco de Erros`.
* [ ] `Simulados`.
* [ ] `Estatísticas`.
* [ ] `Configurações`.

Para cada aba:

* [ ] Criar título.
* [ ] Definir larguras.
* [ ] Definir alturas.
* [ ] Congelar áreas.
* [ ] Aplicar formatos.
* [ ] Aplicar estado vazio.
* [ ] Evitar dados fictícios.
* [ ] Validar legibilidade.

---

## 7.8 Abas ocultas

Criar:

* [ ] `_db_Disciplinas`.
* [ ] `_db_Assuntos`.
* [ ] `_db_Ciclo`.
* [ ] `_db_Blocos`.
* [ ] `_db_Sessoes`.
* [ ] `_db_Questoes`.
* [ ] `_db_Revisoes`.
* [ ] `_db_Erros`.
* [ ] `_db_Simulados`.
* [ ] `_db_Config`.
* [ ] `_db_Metricas`.
* [ ] `_db_Historico`.
* [ ] `_db_Logs`.
* [ ] `_db_Backup`.

Para cada aba interna:

* [ ] Criar cabeçalhos.
* [ ] Congelar cabeçalho.
* [ ] Aplicar formatos.
* [ ] Aplicar validações.
* [ ] Aplicar proteção.
* [ ] Ocultar.
* [ ] Validar acesso pelo script.

---

## 7.9 Importação

* [ ] Importar disciplinas.
* [ ] Importar assuntos.
* [ ] Importar configurações.
* [ ] Importar pesos.
* [ ] Importar prioridades-base.
* [ ] Importar correspondências.
* [ ] Importar data da prova.
* [ ] Importar parâmetros.
* [ ] Comparar quantidades.
* [ ] Validar IDs.
* [ ] Validar relacionamentos.
* [ ] Validar duplicidade.
* [ ] Validar acentos.
* [ ] Validar textos.

---

## 7.10 Menu SOEA

* [ ] Implementar `onOpen()`.
* [ ] Criar menu `SOEA`.
* [ ] Adicionar Continuar Ciclo.
* [ ] Adicionar Aproveitar Tempo.
* [ ] Adicionar Registrar Questões.
* [ ] Adicionar Registrar Erro.
* [ ] Adicionar Registrar Simulado.
* [ ] Adicionar Atualizar Dashboard.
* [ ] Adicionar Configurações.
* [ ] Adicionar Verificar Integridade.
* [ ] Adicionar Criar Backup.
* [ ] Adicionar Ajuda.
* [ ] Adicionar Sobre.
* [ ] Confirmar funções existentes.
* [ ] Tratar funcionalidades futuras.

---

## 7.11 Sidebars

* [ ] Validar abertura de todas.
* [ ] Validar títulos.
* [ ] Validar campos.
* [ ] Validar labels.
* [ ] Validar cancelamento.
* [ ] Validar carregamento.
* [ ] Validar tratamento de erro.
* [ ] Impedir clique repetido.
* [ ] Preservar dados digitados.
* [ ] Não exibir stack trace.
* [ ] Tornar Configurações funcional.
* [ ] Tornar Ajuda funcional.
* [ ] Tornar Sobre funcional.
* [ ] Exibir indisponibilidade clara nas funcionalidades futuras.

---

## 7.12 Dashboard estrutural

* [ ] Criar dias até a prova.
* [ ] Criar bloco atual.
* [ ] Criar horas totais.
* [ ] Criar horas da semana.
* [ ] Criar questões totais.
* [ ] Criar questões da semana.
* [ ] Criar aproveitamento.
* [ ] Criar revisões pendentes.
* [ ] Criar erros pendentes.
* [ ] Criar percentual do edital.
* [ ] Criar sequência.
* [ ] Criar próximo simulado.
* [ ] Criar áreas de gráficos.
* [ ] Utilizar `Ainda sem dados`.
* [ ] Não criar métricas fictícias.

---

## 7.13 Configurações

* [ ] Criar interface visível.
* [ ] Ler `_db_Config`.
* [ ] Validar tipos.
* [ ] Validar datas.
* [ ] Validar números.
* [ ] Validar listas.
* [ ] Permitir somente campos editáveis.
* [ ] Salvar alterações.
* [ ] Atualizar interface.
* [ ] Registrar histórico.
* [ ] Preservar alterações durante setup.

---

## 7.14 Integridade estrutural

* [ ] Implementar `verificarIntegridadeSOEA()`.
* [ ] Verificar abas.
* [ ] Verificar cabeçalhos.
* [ ] Verificar disciplinas.
* [ ] Verificar assuntos.
* [ ] Verificar IDs duplicados.
* [ ] Verificar assuntos órfãos.
* [ ] Verificar configurações.
* [ ] Verificar versão.
* [ ] Verificar planilha vinculada.
* [ ] Classificar resultados.
* [ ] Não corrigir destrutivamente.

---

## 7.15 Backup estrutural

* [ ] Implementar `criarBackupSOEA()`.
* [ ] Criar ID.
* [ ] Registrar data.
* [ ] Registrar tipo.
* [ ] Registrar motivo.
* [ ] Registrar versão.
* [ ] Preservar estrutura.
* [ ] Preservar configurações.
* [ ] Preservar disciplinas.
* [ ] Preservar assuntos.
* [ ] Registrar histórico.
* [ ] Evitar duplicidade excessiva.

---

## 7.16 Implantação real

* [ ] Validar sintaxe local.
* [ ] Validar HTML.
* [ ] Validar manifesto.
* [ ] Executar `clasp status`.
* [ ] Executar `clasp push`.
* [ ] Abrir o Apps Script.
* [ ] Confirmar arquivos.
* [ ] Executar `setupSOEA()`.
* [ ] Autorizar permissões necessárias.
* [ ] Abrir a planilha.
* [ ] Validar estrutura real.
* [ ] Corrigir falhas.
* [ ] Executar novo `clasp push`.
* [ ] Repetir testes.

---

## 7.17 Testes da Fase 2

* [ ] Testar setup em planilha vazia.
* [ ] Testar segunda execução.
* [ ] Testar cabeçalhos.
* [ ] Testar abas ocultas.
* [ ] Testar proteções.
* [ ] Testar importação.
* [ ] Testar menu.
* [ ] Testar todas as Sidebars.
* [ ] Testar Configurações.
* [ ] Testar Dashboard.
* [ ] Testar integridade.
* [ ] Testar backup.
* [ ] Testar persistência de configuração.
* [ ] Testar recarregamento.
* [ ] Testar acesso em outro computador ou sessão.
* [ ] Testar ausência de duplicidade.
* [ ] Testar ausência de dados fictícios.

---

## 7.18 Documentação e entrega

* [ ] Criar `docs/INSTALACAO_FASE_2.md`.
* [ ] Criar `docs/TESTES_FASE_2.md`.
* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar `TODO.md`.
* [ ] Atualizar `REVIEW.md`.
* [ ] Registrar arquivos criados.
* [ ] Registrar testes.
* [ ] Registrar bugs.
* [ ] Registrar correções.
* [ ] Registrar limitações.
* [ ] Não implementar o Motor.
* [ ] Parar e aguardar aprovação.

---

# 8. FASE 3 — MOTOR DO SOEA

**Status:** não iniciada.

**Dependências:**

* ambiente `PRONTO_COMPLETO`;
* Fase 2 aprovada.

---

## 8.1 Preparação

* [ ] Confirmar aprovação da Fase 2.
* [ ] Confirmar projeto correto.
* [ ] Confirmar planilha correta.
* [ ] Criar backup.
* [ ] Definir ambiente de teste.
* [ ] Definir identificação dos dados de teste.
* [ ] Revisar serviços existentes.
* [ ] Revisar Sidebars.
* [ ] Revisar cabeçalhos.
* [ ] Revisar pendências.
* [ ] Revisar logs.

---

## 8.2 IDs

* [ ] Implementar IDs de ciclos.
* [ ] Implementar IDs de blocos.
* [ ] Implementar IDs de sessões.
* [ ] Implementar IDs de questões.
* [ ] Implementar IDs de revisões.
* [ ] Implementar IDs de erros.
* [ ] Implementar IDs de simulados.
* [ ] Implementar IDs de histórico.
* [ ] Implementar IDs de backups.
* [ ] Utilizar `LockService`.
* [ ] Não reutilizar IDs.
* [ ] Não depender da última linha.
* [ ] Testar linhas apagadas.
* [ ] Testar concorrência.
* [ ] Testar clique duplicado.

---

## 8.3 Ciclo

* [ ] Criar primeiro ciclo.
* [ ] Utilizar `CYC-001`.
* [ ] Garantir apenas um ciclo ativo.
* [ ] Registrar data de início.
* [ ] Associar blocos.
* [ ] Atualizar progresso.
* [ ] Atualizar assuntos iniciados.
* [ ] Atualizar assuntos concluídos.
* [ ] Preservar histórico.
* [ ] Bloquear dois ciclos ativos.
* [ ] Concluir ciclo quando aplicável.

---

## 8.4 Blocos

* [ ] Criar bloco.
* [ ] Associar ciclo.
* [ ] Associar disciplina.
* [ ] Associar assunto.
* [ ] Registrar origem.
* [ ] Registrar prioridade.
* [ ] Registrar domínio.
* [ ] Registrar tempo previsto.
* [ ] Registrar questões previstas.
* [ ] Definir etapa inicial.
* [ ] Iniciar bloco.
* [ ] Pausar bloco.
* [ ] Retomar bloco.
* [ ] Atualizar bloco.
* [ ] Concluir bloco.
* [ ] Impedir dois blocos ativos.
* [ ] Impedir repetição de etapa concluída.
* [ ] Impedir duplicidade por clique.

---

## 8.5 Etapas

* [ ] Implementar Teoria.
* [ ] Implementar Questões.
* [ ] Implementar Correção.
* [ ] Implementar Banco de Erros.
* [ ] Implementar Conclusão.
* [ ] Registrar progresso por etapa.
* [ ] Registrar tempo previsto.
* [ ] Registrar tempo realizado.
* [ ] Registrar quantidade prevista.
* [ ] Registrar quantidade realizada.
* [ ] Calcular etapa atual.
* [ ] Preservar etapa parcial.
* [ ] Não depender da Sidebar.

---

## 8.6 Sessões

* [ ] Criar sessão.
* [ ] Associar bloco.
* [ ] Registrar tipo.
* [ ] Registrar origem.
* [ ] Registrar energia.
* [ ] Registrar tempo disponível.
* [ ] Registrar horário inicial.
* [ ] Registrar horário final.
* [ ] Calcular duração.
* [ ] Registrar progresso.
* [ ] Pausar sessão.
* [ ] Concluir sessão.
* [ ] Cancelar sessão.
* [ ] Impedir duas sessões abertas.
* [ ] Recuperar sessão órfã.
* [ ] Permitir várias sessões por bloco.

---

## 8.7 Continuar Ciclo

* [ ] Validar integridade mínima.
* [ ] Garantir ciclo ativo.
* [ ] Verificar sessão aberta.
* [ ] Verificar bloco ativo.
* [ ] Solicitar tempo.
* [ ] Solicitar energia.
* [ ] Calcular carga.
* [ ] Retomar bloco, quando existir.
* [ ] Verificar revisão prioritária.
* [ ] Selecionar assunto.
* [ ] Criar bloco.
* [ ] Mostrar justificativa.
* [ ] Mostrar tempo.
* [ ] Mostrar questões.
* [ ] Solicitar confirmação.
* [ ] Criar sessão somente após confirmação.
* [ ] Atualizar aba Ciclo.
* [ ] Atualizar Dashboard.

---

## 8.8 Retomar Ciclo

* [ ] Carregar o mesmo bloco.
* [ ] Carregar o mesmo assunto.
* [ ] Identificar etapa atual.
* [ ] Identificar progresso.
* [ ] Calcular restante.
* [ ] Ajustar ao tempo disponível.
* [ ] Não repetir atividade concluída.
* [ ] Não criar bloco novo.
* [ ] Preservar tempo realizado.
* [ ] Preservar questões realizadas.
* [ ] Mostrar ponto de retomada.

---

## 8.9 Aproveitar Tempo

* [ ] Solicitar tempo disponível.
* [ ] Solicitar objetivo.
* [ ] Solicitar energia, quando necessário.
* [ ] Oferecer Questões.
* [ ] Oferecer Revisão.
* [ ] Oferecer Banco de Erros.
* [ ] Oferecer Tanto faz.
* [ ] Consultar bloco ativo.
* [ ] Consultar revisões.
* [ ] Consultar erros.
* [ ] Consultar prioridades.
* [ ] Dividir etapa.
* [ ] Não criar ciclo paralelo.
* [ ] Não criar bloco duplicado.
* [ ] Atualizar progresso.
* [ ] Concluir bloco, quando aplicável.
* [ ] Criar revisões, quando aplicável.
* [ ] Garantir continuidade posterior.

---

## 8.10 Barra de Energia

* [ ] Implementar Excelente.
* [ ] Implementar Boa.
* [ ] Implementar Cansado.
* [ ] Implementar Muito cansado.
* [ ] Ajustar teoria.
* [ ] Ajustar questões.
* [ ] Ajustar complexidade.
* [ ] Priorizar revisões.
* [ ] Priorizar Banco de Erros.
* [ ] Não cancelar estudo automaticamente.
* [ ] Não registrar atividade inexistente.

---

## 8.11 Modo Emergência

* [ ] Definir limite de tempo.
* [ ] Ler limite da configuração.
* [ ] Detectar energia muito baixa.
* [ ] Selecionar atividade curta.
* [ ] Revisar poucos erros.
* [ ] Resolver pequeno lote.
* [ ] Concluir parte de etapa.
* [ ] Realizar revisão curta.
* [ ] Preservar progresso.
* [ ] Não concluir bloco ficticiamente.
* [ ] Testar tempo inferior a 30 minutos.

---

## 8.12 Questões

* [ ] Registrar fonte.
* [ ] Registrar quantidade.
* [ ] Registrar acertos.
* [ ] Calcular erros.
* [ ] Calcular percentual.
* [ ] Registrar tempo.
* [ ] Calcular tempo médio.
* [ ] Associar bloco.
* [ ] Associar sessão.
* [ ] Associar disciplina.
* [ ] Associar assunto.
* [ ] Validar quantidade.
* [ ] Validar acertos.
* [ ] Validar tempo.
* [ ] Atualizar bloco.
* [ ] Atualizar métricas.
* [ ] Atualizar domínio.
* [ ] Atualizar prioridade.
* [ ] Não armazenar enunciados protegidos.

---

## 8.13 Banco de Erros

* [ ] Preencher disciplina automaticamente.
* [ ] Preencher assunto automaticamente.
* [ ] Preencher bloco automaticamente.
* [ ] Preencher sessão automaticamente.
* [ ] Registrar motivo.
* [ ] Registrar causa-raiz.
* [ ] Registrar observação.
* [ ] Registrar referência opcional.
* [ ] Registrar data.
* [ ] Definir status inicial.
* [ ] Permitir mudança de status.
* [ ] Filtrar erros.
* [ ] Pesquisar erros.
* [ ] Selecionar erros para revisão.
* [ ] Calcular recorrência.
* [ ] Atualizar prioridade.
* [ ] Atualizar Dashboard.
* [ ] Sincronizar aba visível.

---

## 8.14 Conclusão de bloco

* [ ] Validar bloco.
* [ ] Validar etapas.
* [ ] Validar sessão.
* [ ] Registrar resultados pendentes.
* [ ] Atualizar tempos.
* [ ] Atualizar questões.
* [ ] Atualizar erros.
* [ ] Marcar bloco concluído.
* [ ] Encerrar sessão.
* [ ] Criar revisões.
* [ ] Atualizar assunto.
* [ ] Atualizar domínio.
* [ ] Atualizar prioridade.
* [ ] Atualizar ciclo.
* [ ] Atualizar métricas.
* [ ] Atualizar Dashboard.
* [ ] Registrar histórico.
* [ ] Impedir conclusão duplicada.

---

## 8.15 Revisões

* [ ] Criar D+1.
* [ ] Criar D+7.
* [ ] Criar D+15.
* [ ] Criar D+30.
* [ ] Utilizar data real de conclusão.
* [ ] Impedir duplicidade.
* [ ] Marcar Pendente.
* [ ] Marcar Atrasada.
* [ ] Registrar data realizada.
* [ ] Registrar resultado.
* [ ] Registrar questões.
* [ ] Registrar acertos.
* [ ] Selecionar erros.
* [ ] Aplicar regra de 90% ou mais.
* [ ] Aplicar regra de 70% a 89%.
* [ ] Aplicar regra abaixo de 70%.
* [ ] Criar revisão extra.
* [ ] Atualizar prioridade.
* [ ] Atualizar domínio.

---

## 8.16 Índice de Prioridade

* [ ] Definir fórmula.
* [ ] Definir pesos.
* [ ] Ler pesos da configuração.
* [ ] Considerar peso do edital.
* [ ] Considerar baixo domínio.
* [ ] Considerar desempenho.
* [ ] Considerar volume de questões.
* [ ] Considerar erros.
* [ ] Considerar recorrência.
* [ ] Considerar revisões atrasadas.
* [ ] Considerar tempo sem contato.
* [ ] Considerar proximidade da prova.
* [ ] Considerar simulados.
* [ ] Considerar contato mínimo.
* [ ] Normalizar entre 0 e 100.
* [ ] Evitar divisão por zero.
* [ ] Explicar componentes.
* [ ] Retornar justificativa.
* [ ] Testar cenários extremos.

---

## 8.17 Índice de Domínio

* [ ] Definir fórmula.
* [ ] Definir pesos.
* [ ] Considerar questões.
* [ ] Considerar volume.
* [ ] Considerar revisões.
* [ ] Considerar simulados.
* [ ] Considerar erros recorrentes.
* [ ] Considerar tempo sem contato.
* [ ] Implementar confiança da amostra.
* [ ] Impedir domínio artificialmente alto.
* [ ] Normalizar entre 0 e 100.
* [ ] Classificar vermelho.
* [ ] Classificar amarelo.
* [ ] Classificar verde.
* [ ] Testar amostra pequena.
* [ ] Testar alto desempenho.
* [ ] Testar baixo desempenho.

---

## 8.18 Tempo Estimado Inteligente

* [ ] Definir tempos padrão.
* [ ] Registrar tempos reais.
* [ ] Calcular tempo por questão.
* [ ] Calcular tempo de teoria.
* [ ] Calcular tempo de correção.
* [ ] Calcular tempo de revisão.
* [ ] Definir amostra mínima.
* [ ] Utilizar mediana ou média aparada.
* [ ] Tratar valores extremos.
* [ ] Aplicar mínimo.
* [ ] Aplicar máximo.
* [ ] Ajustar pela energia.
* [ ] Ajustar pelo tempo disponível.
* [ ] Mostrar estimativa.

---

## 8.19 Métricas

* [ ] Horas totais.
* [ ] Horas diárias.
* [ ] Horas semanais.
* [ ] Horas mensais.
* [ ] Questões totais.
* [ ] Questões diárias.
* [ ] Questões semanais.
* [ ] Questões mensais.
* [ ] Acertos.
* [ ] Erros.
* [ ] Aproveitamento.
* [ ] Blocos concluídos.
* [ ] Assuntos iniciados.
* [ ] Assuntos concluídos.
* [ ] Revisões pendentes.
* [ ] Revisões concluídas.
* [ ] Revisões atrasadas.
* [ ] Erros pendentes.
* [ ] Percentual do edital.
* [ ] Sequência de estudos.
* [ ] Metas semanais.
* [ ] Utilizar operações em lote.

---

## 8.20 Dashboard e Ciclo

* [ ] Atualizar cards com dados reais.
* [ ] Mostrar ciclo ativo.
* [ ] Mostrar bloco atual.
* [ ] Mostrar etapa.
* [ ] Mostrar horas.
* [ ] Mostrar questões.
* [ ] Mostrar aproveitamento.
* [ ] Mostrar revisões.
* [ ] Mostrar erros.
* [ ] Mostrar percentual do edital.
* [ ] Mostrar sequência.
* [ ] Mostrar justificativa.
* [ ] Mostrar próxima ação.
* [ ] Utilizar estado sem dados.
* [ ] Não armazenar dados oficiais no Dashboard.

---

## 8.21 Histórico e logs

* [ ] Registrar ciclo criado.
* [ ] Registrar bloco criado.
* [ ] Registrar bloco pausado.
* [ ] Registrar bloco retomado.
* [ ] Registrar bloco concluído.
* [ ] Registrar sessão criada.
* [ ] Registrar sessão concluída.
* [ ] Registrar sessão recuperada.
* [ ] Registrar questões.
* [ ] Registrar erros.
* [ ] Registrar revisões.
* [ ] Registrar prioridade.
* [ ] Registrar domínio.
* [ ] Registrar backup.
* [ ] Registrar recuperação.
* [ ] Separar histórico e log técnico.
* [ ] Não salvar credenciais.
* [ ] Não mostrar stack trace ao usuário.

---

## 8.22 Integridade

* [ ] Verificar abas.
* [ ] Verificar cabeçalhos.
* [ ] Verificar IDs duplicados.
* [ ] Verificar relacionamentos.
* [ ] Verificar ciclos ativos.
* [ ] Verificar blocos ativos.
* [ ] Verificar sessões abertas.
* [ ] Verificar sessões órfãs.
* [ ] Verificar blocos órfãos.
* [ ] Verificar revisões órfãs.
* [ ] Verificar revisões duplicadas.
* [ ] Verificar questões órfãs.
* [ ] Verificar erros órfãos.
* [ ] Verificar tempos negativos.
* [ ] Verificar percentuais.
* [ ] Verificar acertos.
* [ ] Verificar progresso.
* [ ] Verificar configurações.
* [ ] Classificar resultados.

---

## 8.23 Recuperação

* [ ] Detectar sessão antiga.
* [ ] Detectar sessão órfã.
* [ ] Detectar dois ciclos.
* [ ] Detectar dois blocos.
* [ ] Detectar duas sessões.
* [ ] Localizar bloco correto.
* [ ] Reconstruir etapa.
* [ ] Encerrar sessão com segurança.
* [ ] Preservar progresso.
* [ ] Criar backup.
* [ ] Registrar recuperação.
* [ ] Solicitar decisão quando houver risco.

---

## 8.24 Backup

* [ ] Criar backup antes de migração.
* [ ] Criar backup antes de recuperação.
* [ ] Criar backup antes de correção em massa.
* [ ] Criar backup antes de limpeza.
* [ ] Registrar ID.
* [ ] Registrar data.
* [ ] Registrar tipo.
* [ ] Registrar motivo.
* [ ] Registrar versão.
* [ ] Registrar entidades.
* [ ] Evitar excesso.
* [ ] Validar conteúdo.
* [ ] Documentar restauração assistida.

---

## 8.25 Implantação e testes reais

* [ ] Validar código localmente.
* [ ] Executar `clasp status`.
* [ ] Executar `clasp push`.
* [ ] Executar funções no Apps Script.
* [ ] Criar dados controlados de teste.
* [ ] Testar ciclo.
* [ ] Testar bloco.
* [ ] Testar sessão.
* [ ] Testar interrupção.
* [ ] Testar retomada.
* [ ] Testar Aproveitar Tempo.
* [ ] Testar energia.
* [ ] Testar Modo Emergência.
* [ ] Testar questões.
* [ ] Testar erros.
* [ ] Testar conclusão.
* [ ] Testar revisões.
* [ ] Testar prioridade.
* [ ] Testar domínio.
* [ ] Testar métricas.
* [ ] Testar Dashboard.
* [ ] Testar integridade.
* [ ] Testar recuperação.
* [ ] Testar backup.
* [ ] Testar clique duplicado.
* [ ] Testar persistência.
* [ ] Testar setup novamente.
* [ ] Corrigir falhas.
* [ ] Executar novo `clasp push`.
* [ ] Executar regressões.

---

## 8.26 Limpeza de testes

* [ ] Identificar registros de teste.
* [ ] Criar backup.
* [ ] Remover somente registros identificados.
* [ ] Preservar dados oficiais.
* [ ] Preservar configurações.
* [ ] Atualizar Dashboard.
* [ ] Executar integridade.
* [ ] Confirmar ausência de resíduos.
* [ ] Registrar limpeza.

---

## 8.27 Documentação e entrega

* [ ] Criar `docs/FORMULAS_SOEA.md`.
* [ ] Criar `docs/TESTES_FASE_3.md`.
* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar `TODO.md`.
* [ ] Atualizar `REVIEW.md`.
* [ ] Registrar funções públicas.
* [ ] Registrar fórmulas.
* [ ] Registrar testes.
* [ ] Registrar bugs.
* [ ] Registrar correções.
* [ ] Registrar limitações.
* [ ] Não implementar a Fase 4.
* [ ] Parar e aguardar aprovação.

---

# 9. FASE 4 — FINALIZAÇÃO E ENTREGA DA VERSÃO 1.0

**Status:** não iniciada.

**Dependências:**

* ambiente `PRONTO_COMPLETO`;
* Fase 3 aprovada.

---

## 9.1 Preparação

* [ ] Confirmar aprovação da Fase 3.
* [ ] Confirmar ambiente.
* [ ] Revisar bugs.
* [ ] Revisar logs.
* [ ] Revisar testes da Fase 3.
* [ ] Criar backup `PRE_FASE_4`.
* [ ] Criar ambiente controlado de teste.
* [ ] Confirmar projeto de teste.
* [ ] Confirmar planilha de teste.
* [ ] Identificar dados de teste.
* [ ] Preservar vínculo principal.

---

## 9.2 Bugs pendentes

* [ ] Classificar bugs críticos.
* [ ] Classificar bugs altos.
* [ ] Classificar bugs médios.
* [ ] Classificar bugs baixos.
* [ ] Corrigir todos os críticos.
* [ ] Corrigir todos os altos impeditivos.
* [ ] Corrigir médios que afetem o estudo.
* [ ] Registrar baixos adiados.
* [ ] Criar IDs `BUG-XXX`.
* [ ] Criar testes de regressão.

---

## 9.3 Sistema de simulados

* [ ] Criar simulado planejado.
* [ ] Criar simulado manual.
* [ ] Registrar simulado realizado.
* [ ] Editar registro incompleto.
* [ ] Corrigir simulado.
* [ ] Cancelar simulado.
* [ ] Consultar simulados.
* [ ] Filtrar simulados.
* [ ] Impedir duplicidade.
* [ ] Registrar ID.
* [ ] Registrar nome.
* [ ] Registrar datas.
* [ ] Registrar duração.
* [ ] Registrar questões.
* [ ] Registrar acertos.
* [ ] Calcular erros.
* [ ] Calcular percentual.
* [ ] Registrar status.
* [ ] Registrar origem.
* [ ] Registrar observação.
* [ ] Atualizar métricas.
* [ ] Atualizar prioridade.
* [ ] Atualizar domínio.
* [ ] Atualizar Dashboard.

---

## 9.4 Agenda de simulados

* [ ] Ler data da prova em `_db_Config`.
* [ ] Considerar data atual.
* [ ] Considerar data de instalação.
* [ ] Não criar datas retroativas.
* [ ] Não criar após a prova.
* [ ] Julho: segundo sábado.
* [ ] Julho: quarto sábado.
* [ ] Agosto: todos os sábados.
* [ ] Setembro: todos os sábados.
* [ ] Últimos 15 dias: mini simulados.
* [ ] Reservar domingo para correção.
* [ ] Registrar origem automática.
* [ ] Permitir edição.
* [ ] Permitir cancelamento.
* [ ] Não recriar cancelado.
* [ ] Garantir idempotência.
* [ ] Testar segunda geração.

---

## 9.5 Correção de simulados

* [ ] Registrar desempenho geral.
* [ ] Registrar desempenho por disciplina.
* [ ] Registrar assuntos problemáticos.
* [ ] Registrar erros de conteúdo.
* [ ] Registrar interpretação.
* [ ] Registrar atenção.
* [ ] Registrar problemas de tempo.
* [ ] Registrar observações.
* [ ] Criar ações recomendadas.
* [ ] Enviar erros selecionados ao Banco de Erros.
* [ ] Atualizar métricas.
* [ ] Atualizar prioridade.
* [ ] Atualizar domínio.
* [ ] Atualizar Estatísticas.
* [ ] Atualizar Dashboard.

---

## 9.6 Sidebar de simulados

* [ ] Visualizar planejado.
* [ ] Registrar realização.
* [ ] Registrar duração.
* [ ] Registrar questões.
* [ ] Registrar acertos.
* [ ] Registrar observação.
* [ ] Iniciar correção.
* [ ] Editar.
* [ ] Cancelar.
* [ ] Validar campos.
* [ ] Impedir clique repetido.
* [ ] Mostrar carregamento.
* [ ] Preservar dados em falha.
* [ ] Mostrar resumo.

---

## 9.7 Dashboard final

Cards:

* [ ] Dias até a prova.
* [ ] Ciclo ativo.
* [ ] Bloco atual.
* [ ] Etapa atual.
* [ ] Horas totais.
* [ ] Horas da semana.
* [ ] Questões totais.
* [ ] Questões da semana.
* [ ] Aproveitamento.
* [ ] Revisões pendentes.
* [ ] Revisões atrasadas.
* [ ] Erros pendentes.
* [ ] Percentual do edital.
* [ ] Sequência.
* [ ] Próximo simulado.
* [ ] Último simulado.
* [ ] Resultado do último simulado.
* [ ] Meta semanal.
* [ ] Domínio geral, quando previsto.

Gráficos:

* [ ] Evolução de aproveitamento.
* [ ] Questões por semana.
* [ ] Horas por semana.
* [ ] Desempenho por disciplina.
* [ ] Evolução dos simulados.
* [ ] Erros por causa-raiz.
* [ ] Revisões.
* [ ] Menor domínio.
* [ ] Maior prioridade.
* [ ] Intervalos dinâmicos.
* [ ] Estado sem dados.
* [ ] Ausência de `#N/A`.
* [ ] Ausência de `#REF!`.

---

## 9.8 Estatísticas

* [ ] Filtro por período.
* [ ] Filtro por disciplina.
* [ ] Filtro por assunto.
* [ ] Filtro por tipo de atividade.
* [ ] Filtro por status.
* [ ] Filtro por fonte.
* [ ] Filtro por simulado.
* [ ] Horas.
* [ ] Questões.
* [ ] Acertos.
* [ ] Erros.
* [ ] Aproveitamento.
* [ ] Desempenho por disciplina.
* [ ] Desempenho por assunto.
* [ ] Revisões.
* [ ] Erros recorrentes.
* [ ] Causas-raiz.
* [ ] Simulados.
* [ ] Menor domínio.
* [ ] Maior prioridade.
* [ ] Evolução.
* [ ] Metas semanais.

---

## 9.9 Abas visíveis finais

### Banco de Erros

* [ ] Revisar filtros.
* [ ] Revisar status.
* [ ] Destacar novos.
* [ ] Destacar recorrentes.
* [ ] Destacar antigos.
* [ ] Destacar resolvidos.
* [ ] Permitir atualização segura.
* [ ] Sincronizar com `_db_Erros`.

### Ciclo

* [ ] Mostrar ciclo.
* [ ] Mostrar bloco.
* [ ] Mostrar disciplina.
* [ ] Mostrar assunto.
* [ ] Mostrar etapa.
* [ ] Mostrar progresso.
* [ ] Mostrar tempos.
* [ ] Mostrar questões.
* [ ] Mostrar sessão.
* [ ] Mostrar revisão.
* [ ] Mostrar justificativa.
* [ ] Mostrar próxima ação.

### Configurações

* [ ] Revisar campos editáveis.
* [ ] Validar tipos.
* [ ] Validar limites.
* [ ] Proteger campos técnicos.
* [ ] Registrar alterações.
* [ ] Restaurar padrões editáveis.
* [ ] Solicitar confirmação.
* [ ] Não apagar dados de estudo.

---

## 9.10 Experiência de uso

* [ ] Iniciar sessão em menos de 30 segundos.
* [ ] Reduzir cliques.
* [ ] Remover campos calculáveis.
* [ ] Evitar diálogos excessivos.
* [ ] Priorizar Sidebars.
* [ ] Padronizar mensagens.
* [ ] Padronizar carregamento.
* [ ] Padronizar cancelamento.
* [ ] Padronizar sucesso.
* [ ] Padronizar falha.
* [ ] Mostrar resumo de sessão.
* [ ] Mostrar resumo de bloco.
* [ ] Mostrar resumo de revisão.
* [ ] Mostrar resumo de simulado.
* [ ] Não mostrar stack trace.
* [ ] Não mostrar JSON técnico.

---

## 9.11 Acessibilidade

* [ ] Revisar contraste.
* [ ] Revisar tamanho dos textos.
* [ ] Revisar labels.
* [ ] Revisar botões.
* [ ] Indicar obrigatoriedade.
* [ ] Indicar carregamento.
* [ ] Indicar erro.
* [ ] Indicar sucesso.
* [ ] Não depender apenas de cor.
* [ ] Utilizar texto ou símbolo.
* [ ] Testar navegação por teclado, quando possível.

---

## 9.12 Performance

* [ ] Revisar leituras.
* [ ] Revisar escritas.
* [ ] Utilizar operações em lote.
* [ ] Evitar chamadas em loops.
* [ ] Revisar recálculos.
* [ ] Revisar gráficos.
* [ ] Revisar cache.
* [ ] Revisar locks.
* [ ] Revisar gatilhos.
* [ ] Revisar backups.
* [ ] Revisar leitura de configurações.
* [ ] Medir setup.
* [ ] Medir Continuar Ciclo.
* [ ] Medir Aproveitar Tempo.
* [ ] Medir conclusão de sessão.
* [ ] Medir conclusão de bloco.
* [ ] Medir Dashboard.
* [ ] Medir Estatísticas.
* [ ] Medir agenda.
* [ ] Medir integridade.
* [ ] Medir backup.
* [ ] Não inventar tempos.

---

## 9.13 Segurança e permissões

* [ ] Revisar manifesto.
* [ ] Confirmar runtime V8.
* [ ] Confirmar fuso.
* [ ] Remover escopos desnecessários.
* [ ] Confirmar ausência de APIs externas.
* [ ] Confirmar ausência de CDN.
* [ ] Confirmar ausência de credenciais.
* [ ] Confirmar ausência de conteúdo protegido.
* [ ] Confirmar proteção de abas.
* [ ] Confirmar locks.
* [ ] Confirmar IDs.
* [ ] Confirmar validações.
* [ ] Confirmar backups.
* [ ] Confirmar logs sem dados sensíveis.
* [ ] Documentar permissões no README.

---

## 9.14 Backup e recuperação final

* [ ] Validar backup manual.
* [ ] Validar backup automático crítico.
* [ ] Validar IDs.
* [ ] Validar conteúdo.
* [ ] Validar retenção.
* [ ] Validar remoção segura.
* [ ] Validar consulta.
* [ ] Não aceitar backup vazio.
* [ ] Testar sessão órfã.
* [ ] Testar dois ciclos.
* [ ] Testar dois blocos.
* [ ] Testar duas sessões.
* [ ] Testar revisão duplicada.
* [ ] Testar configuração ausente.
* [ ] Testar cabeçalho ausente.
* [ ] Confirmar backup antes da correção.
* [ ] Solicitar autorização para correção destrutiva.

---

## 9.15 Limpeza do código

* [ ] Remover código morto.
* [ ] Remover funções duplicadas.
* [ ] Remover comentários temporários.
* [ ] Remover dados fictícios.
* [ ] Remover logs de depuração.
* [ ] Remover arquivos não utilizados.
* [ ] Remover `FEATURE_NOT_AVAILABLE` das funções concluídas.
* [ ] Preservar diagnósticos úteis.
* [ ] Preservar testes seguros.
* [ ] Validar includes.
* [ ] Validar referências.
* [ ] Validar funções públicas.
* [ ] Validar menu.

---

## 9.16 Testes de instalação

* [ ] Instalar em planilha vazia.
* [ ] Validar permissões.
* [ ] Validar abas.
* [ ] Validar cabeçalhos.
* [ ] Validar seeds.
* [ ] Validar menu.
* [ ] Validar Sidebars.
* [ ] Validar Dashboard.
* [ ] Validar Configurações.
* [ ] Validar integridade.
* [ ] Validar backup.
* [ ] Executar segunda instalação.
* [ ] Confirmar idempotência.

---

## 9.17 Teste de atualização

* [ ] Atualizar cópia da Fase 3.
* [ ] Preservar disciplinas.
* [ ] Preservar assuntos.
* [ ] Preservar configurações.
* [ ] Preservar ciclos.
* [ ] Preservar blocos.
* [ ] Preservar sessões.
* [ ] Preservar questões.
* [ ] Preservar erros.
* [ ] Preservar revisões.
* [ ] Preservar IDs.
* [ ] Criar somente campos ausentes.
* [ ] Confirmar ausência de corrupção.

---

## 9.18 Regressão da Fase 3

* [ ] Criar ciclo.
* [ ] Continuar Ciclo.
* [ ] Interromper.
* [ ] Retomar.
* [ ] Registrar questões.
* [ ] Registrar erro.
* [ ] Concluir bloco.
* [ ] Criar revisões.
* [ ] Impedir revisão duplicada.
* [ ] Realizar revisão alta.
* [ ] Realizar revisão média.
* [ ] Realizar revisão baixa.
* [ ] Aproveitar Tempo parcial.
* [ ] Aproveitar Tempo concluindo bloco.
* [ ] Modo Emergência.
* [ ] Energia baixa.
* [ ] Clique duplicado.
* [ ] Duas sessões.
* [ ] Dois blocos.
* [ ] Persistência.
* [ ] Prioridade.
* [ ] Domínio.
* [ ] Amostra pequena.
* [ ] Integridade.
* [ ] Backup.
* [ ] Recuperação.

---

## 9.19 Testes de simulados

* [ ] Gerar agenda inicial.
* [ ] Gerar agenda novamente.
* [ ] Confirmar idempotência.
* [ ] Confirmar datas futuras.
* [ ] Confirmar nenhum simulado após a prova.
* [ ] Confirmar ausência de retroativos.
* [ ] Cancelar simulado.
* [ ] Confirmar que não reaparece.
* [ ] Editar data.
* [ ] Registrar simulado válido.
* [ ] Rejeitar zero questões.
* [ ] Rejeitar duração negativa.
* [ ] Rejeitar acertos acima do total.
* [ ] Corrigir simulado.
* [ ] Atualizar métricas.
* [ ] Atualizar prioridade.
* [ ] Atualizar domínio.
* [ ] Atualizar Banco de Erros.
* [ ] Atualizar Dashboard.
* [ ] Atualizar Estatísticas.

---

## 9.20 Testes do Dashboard e Estatísticas

* [ ] Testar sem dados.
* [ ] Testar poucos dados.
* [ ] Testar volume maior.
* [ ] Testar datas.
* [ ] Testar percentuais.
* [ ] Testar totais.
* [ ] Testar cards.
* [ ] Testar gráficos.
* [ ] Testar filtros.
* [ ] Testar atualização após sessão.
* [ ] Testar atualização após questões.
* [ ] Testar atualização após erro.
* [ ] Testar atualização após revisão.
* [ ] Testar atualização após simulado.
* [ ] Testar após limpeza.
* [ ] Confirmar ausência de `#N/A`.
* [ ] Confirmar ausência de `#REF!`.

---

## 9.21 Dados de teste

* [ ] Identificar todos os dados de teste.
* [ ] Criar backup.
* [ ] Remover somente dados de teste.
* [ ] Preservar dados oficiais.
* [ ] Preservar configurações.
* [ ] Atualizar Dashboard.
* [ ] Atualizar Estatísticas.
* [ ] Executar integridade.
* [ ] Confirmar ausência de resíduos.
* [ ] Registrar a limpeza.

---

## 9.22 Implantação principal

* [ ] Confirmar `.clasp.json` principal.
* [ ] Confirmar projeto principal.
* [ ] Confirmar planilha principal.
* [ ] Criar backup `PRE_V1_FINAL`.
* [ ] Executar `clasp status`.
* [ ] Executar `clasp push`.
* [ ] Executar migração segura.
* [ ] Abrir planilha principal.
* [ ] Validar estrutura.
* [ ] Validar menu.
* [ ] Validar Sidebars.
* [ ] Validar Dashboard.
* [ ] Validar Estatísticas.
* [ ] Validar simulados.
* [ ] Executar integridade.
* [ ] Executar backup.
* [ ] Executar regressão rápida.
* [ ] Confirmar ausência de dados de teste.

---

## 9.23 README definitivo

* [ ] Explicar objetivo.
* [ ] Explicar tecnologias.
* [ ] Explicar versão.
* [ ] Explicar requisitos.
* [ ] Explicar permissões.
* [ ] Explicar instalação.
* [ ] Criar seção `Comece em 5 minutos`.
* [ ] Explicar configuração inicial.
* [ ] Explicar Continuar Ciclo.
* [ ] Explicar Retomar Ciclo.
* [ ] Explicar Aproveitar Tempo.
* [ ] Explicar energia.
* [ ] Explicar Modo Emergência.
* [ ] Explicar questões.
* [ ] Explicar Banco de Erros.
* [ ] Explicar revisões.
* [ ] Explicar simulados.
* [ ] Explicar Dashboard.
* [ ] Explicar Estatísticas.
* [ ] Explicar Configurações.
* [ ] Explicar backup.
* [ ] Explicar recuperação.
* [ ] Explicar integridade.
* [ ] Incluir solução de problemas.
* [ ] Incluir limitações.
* [ ] Explicar estrutura.
* [ ] Explicar segurança.

---

## 9.24 Documentação e versão

* [ ] Criar `docs/TESTES_FASE_4.md`.
* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar `TODO.md`.
* [ ] Atualizar `REVIEW.md`.
* [ ] Atualizar `README.md`.
* [ ] Atualizar versão em `Constants.gs`.
* [ ] Atualizar Sidebar Sobre.
* [ ] Atualizar configurações internas.
* [ ] Preparar `SOEA v1.0.0`.
* [ ] Não marcar como estável antes da aprovação.
* [ ] Não criar Fase 5.
* [ ] Não iniciar versão 2.0.
* [ ] Parar e aguardar aprovação final.

---

# 10. TESTES DE ACEITAÇÃO DO PRODUCT OWNER

Os testes técnicos deverão ser executados pelo Codex.

O Product Owner avaliará principalmente conteúdo, clareza, aparência e usabilidade.

---

## 10.1 Prompt 00

* [ ] Confirmar conta Google correta.
* [ ] Confirmar permissões solicitadas.
* [ ] Confirmar que nenhuma senha foi solicitada pelo chat.
* [ ] Aprovar status `PRONTO_COMPLETO`.

---

## 10.2 Fase 1

* [ ] Conferir disciplinas.
* [ ] Conferir assuntos.
* [ ] Conferir pesos.
* [ ] Conferir estrutura da prova.
* [ ] Conferir matriz de cobertura.
* [ ] Conferir lacunas.
* [ ] Conferir estratégia inicial.
* [ ] Aprovar os dados de importação.

---

## 10.3 Fase 2

* [ ] Conferir abas.
* [ ] Conferir organização.
* [ ] Conferir títulos.
* [ ] Conferir dados importados.
* [ ] Conferir menu.
* [ ] Conferir Sidebars.
* [ ] Conferir Dashboard básico.
* [ ] Conferir Configurações.
* [ ] Avaliar legibilidade.
* [ ] Aprovar estrutura.

O Product Owner não deverá precisar executar novamente todos os testes técnicos do setup.

---

## 10.4 Fase 3

* [ ] Avaliar seleção de assunto.
* [ ] Avaliar justificativa.
* [ ] Avaliar Continuar Ciclo.
* [ ] Avaliar Retomar Ciclo.
* [ ] Avaliar Aproveitar Tempo.
* [ ] Avaliar energia.
* [ ] Avaliar Modo Emergência.
* [ ] Avaliar registro de questões.
* [ ] Avaliar Banco de Erros.
* [ ] Avaliar revisões.
* [ ] Avaliar prioridade.
* [ ] Avaliar domínio.
* [ ] Avaliar Dashboard.
* [ ] Avaliar quantidade de cliques.
* [ ] Aprovar Motor.

---

## 10.5 Fase 4

* [ ] Avaliar simulados.
* [ ] Avaliar agenda.
* [ ] Avaliar Dashboard final.
* [ ] Avaliar gráficos.
* [ ] Avaliar Estatísticas.
* [ ] Avaliar Configurações.
* [ ] Avaliar legibilidade.
* [ ] Avaliar fluxo completo.
* [ ] Avaliar README.
* [ ] Confirmar ausência de dados de teste.
* [ ] Aprovar versão 1.0.0.

---

# 11. BUGS E BLOQUEIOS

## 11.1 Bugs abertos

Nenhum bug registrado.

---

## 11.2 Bloqueios abertos

Nenhum bloqueio registrado.

---

## 11.3 Formato de bug

```text
Identificador: BUG-XXX
Fase:
Funcionalidade:
Severidade:
Descrição:
Comportamento esperado:
Comportamento obtido:
Impacto:
Forma de reprodução:
Causa:
Solução:
Teste de regressão:
Status:
```

---

## 11.4 Formato de bloqueio

```text
Identificador: BLQ-XXX
Fase:
Etapa:
Descrição:
Impacto:
Tentativas realizadas:
Ação necessária:
Responsável:
Status:
```

---

# 12. ITENS ADIADOS PARA VERSÃO FUTURA

* [~] Aplicação web.
* [~] Aplicativo mobile.
* [~] Sistema multiusuário.
* [~] Suporte a múltiplos concursos.
* [~] Integração automática com o Estratégia.
* [~] Integração automática com plataformas de questões.
* [~] Importação automática de editais.
* [~] Inteligência artificial integrada à planilha.
* [~] Integração com Google Calendar.
* [~] Sincronização entre contas.
* [~] Notificações externas.
* [~] Gamificação avançada.
* [~] Aplicativo comercial.
* [~] Sistema de assinatura.
* [~] Hospedagem externa.
* [~] Banco de dados externo.
* [~] APIs externas.

Esses itens não deverão ser implementados na versão 1.0.0.

---

# 13. ESTADO ATUAL

```text
FASE 0 — DOCUMENTAÇÃO E PREPARAÇÃO
Concluída e aprovada

PROMPT 00 — CONFIGURAÇÃO DO AMBIENTE AUTÔNOMO
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

# 14. PRÓXIMA TAREFA AUTORIZADA

Executar somente:

```text
prompts/00_Configurar_Ambiente_Autonomo.md
```

Objetivo:

```text
Configurar e validar o ambiente autônomo.
Alcançar o estado PRONTO_COMPLETO.
```

O Codex não está autorizado a:

* executar o Prompt 01;
* analisar o edital;
* criar os CSVs;
* criar a estrutura definitiva da planilha;
* implementar o Motor;
* implementar simulados;
* executar todas as fases em sequência.

Ao concluir o Prompt 00, deverá:

1. criar `docs/AMBIENTE_AUTONOMO.md`;
2. atualizar este `TODO.md`;
3. atualizar `docs/CHANGELOG.md`;
4. atualizar `docs/REVIEW.md`;
5. apresentar os resultados;
6. parar;
7. aguardar aprovação do Product Owner.

---

# 15. CONDIÇÃO PARA INICIAR A FASE 1

A Fase 1 somente poderá começar quando:

* [ ] o Prompt 00 estiver concluído;
* [ ] `docs/AMBIENTE_AUTONOMO.md` existir;
* [ ] o ambiente estiver como `PRONTO_COMPLETO`;
* [ ] o `clasp push` tiver sido validado;
* [ ] a execução real tiver sido validada;
* [ ] o Google Sheets estiver acessível;
* [ ] o Google Apps Script estiver acessível;
* [ ] o Product Owner tiver aprovado o Prompt 00;
* [ ] o Product Owner tiver autorizado explicitamente a Fase 1.

---

# 16. ENCERRAMENTO

O objetivo deste documento é manter o desenvolvimento:

* controlado;
* verificável;
* autônomo quando tecnicamente possível;
* seguro;
* alinhado ao escopo;
* separado em fases;
* dependente de aprovação entre as etapas;
* transparente quanto a testes e limitações.

A prioridade da versão 1.0.0 é entregar uma planilha:

* funcional;
* estável;
* útil;
* fácil de usar;
* acessível pela conta Google;
* sem infraestrutura externa;
* com dados preservados;
* implantada e testada.

O desenvolvimento não deverá consumir mais importância do que a preparação para a prova.

A próxima ação é exclusivamente a execução do Prompt 00.
