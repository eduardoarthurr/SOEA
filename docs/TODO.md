# TODO.md

# SOEA — Sistema Operacional de Estudos Adaptativo

**Versão planejada:** 1.0
**Status geral:** planejamento concluído; desenvolvimento ainda não iniciado
**Product Owner:** Eduardo Arthur
**Tecnologias:** Google Sheets + Google Apps Script
**Concurso:** DATAPREV 2026 — Perfil 3 — Desenvolvimento de Software
**Data da prova:** 11 de outubro de 2026

---

# 1. OBJETIVO DESTE DOCUMENTO

Este documento contém as tarefas necessárias para construir a versão 1.0 da Planilha Inteligente SOEA.

O `TODO.md` deverá ser atualizado continuamente pelo Codex.

Cada tarefa poderá assumir um dos seguintes estados:

```text
[ ] Não iniciada
[-] Em andamento
[x] Concluída
[!] Bloqueada
[~] Adiada para versão futura
```

O Codex deverá:

* marcar tarefas concluídas;
* registrar novas subtarefas identificadas durante o desenvolvimento;
* registrar bugs;
* registrar bloqueios;
* registrar itens adiados;
* nunca excluir tarefas sem justificativa;
* nunca marcar uma tarefa como concluída sem implementação e validação.

---

# 2. REGRAS DE UTILIZAÇÃO

Antes de iniciar qualquer fase, o Codex deverá:

* [ ] Ler o `PRD.md`.
* [ ] Ler o `ARQUITETURA.md`.
* [ ] Ler o `ROADMAP.md`.
* [ ] Ler este `TODO.md`.
* [ ] Verificar a fase atual.
* [ ] Verificar dependências pendentes.
* [ ] Identificar bloqueios.
* [ ] Atualizar o status da tarefa iniciada para `Em andamento`.

Ao concluir uma tarefa, deverá:

* [ ] Validar o resultado.
* [ ] Marcar a tarefa como concluída.
* [ ] Atualizar o `CHANGELOG.md`.
* [ ] Atualizar o `ROADMAP.md`, quando necessário.
* [ ] Registrar no `REVIEW.md` o que foi entregue.
* [ ] Adicionar bugs ou limitações encontrados.
* [ ] Não iniciar a próxima fase sem aprovação do Product Owner.

---

# 3. FASE 0 — DOCUMENTAÇÃO E PREPARAÇÃO

## 3.1 Documentos-base

* [x] Definir o conceito da Planilha Inteligente SOEA.
* [x] Definir o objetivo da versão 1.0.
* [x] Definir Google Sheets e Google Apps Script como tecnologias obrigatórias.
* [x] Definir tecnologias fora do escopo.
* [x] Criar o `PRD.md`.
* [x] Criar o `ARQUITETURA.md`.
* [x] Criar o `ROADMAP.md`.
* [x] Criar o `TODO.md`.
* [ ] Criar o `CHANGELOG.md` inicial.
* [ ] Criar o `REVIEW.md` inicial.
* [ ] Criar o `README.md` inicial ou um esqueleto para preenchimento posterior.

## 3.2 Requisitos definidos

* [x] Definir Continuar Ciclo.
* [x] Definir Retomar Ciclo.
* [x] Definir Aproveitar Tempo.
* [x] Definir sessões de estudo.
* [x] Definir Barra de Energia.
* [x] Definir blocos de estudo.
* [x] Definir IDs internos.
* [x] Definir Banco de Questões.
* [x] Definir Banco de Erros.
* [x] Definir revisões automáticas.
* [x] Definir simulados.
* [x] Definir Índice de Prioridade.
* [x] Definir Índice de Domínio.
* [x] Definir Tempo Estimado Inteligente.
* [x] Definir salvamento automático.
* [x] Definir histórico, logs e backup.
* [x] Definir abas visíveis.
* [x] Definir abas ocultas.
* [x] Definir arquitetura dos arquivos Apps Script.
* [x] Definir processo de aprovação por fases.

## 3.3 Aprovação da documentação

* [ ] Confirmar versão consolidada do `PRD.md`.
* [ ] Confirmar versão final do `ARQUITETURA.md`.
* [ ] Confirmar versão inicial do `ROADMAP.md`.
* [ ] Confirmar versão inicial do `TODO.md`.
* [ ] Registrar aprovação da Fase 0 no `ROADMAP.md`.

---

# 4. FASE 1 — ANÁLISE DO EDITAL E DO CURSO

## 4.1 Entradas

* [ ] Confirmar disponibilidade do edital oficial da DATAPREV 2026.
* [ ] Confirmar que o edital anexado corresponde à versão correta.
* [ ] Confirmar o Perfil 3 — Desenvolvimento de Software.
* [ ] Acessar o pacote pós-edital do Estratégia.
* [ ] Registrar o link utilizado na análise.
* [ ] Registrar limitações de acesso à página, caso existam.

## 4.2 Análise da estrutura da prova

* [ ] Identificar quantidade total de questões.
* [ ] Identificar quantidade de questões de Conhecimentos Gerais.
* [ ] Identificar quantidade de questões de Conhecimentos Específicos.
* [ ] Identificar pesos das questões.
* [ ] Identificar pontuação máxima.
* [ ] Identificar nota mínima.
* [ ] Identificar regra de não zerar disciplinas.
* [ ] Identificar duração da prova.
* [ ] Confirmar data da prova.
* [ ] Registrar banca organizadora.
* [ ] Registrar demais regras relevantes ao planejamento.

## 4.3 Extração das disciplinas

* [ ] Extrair todas as disciplinas de Conhecimentos Gerais.
* [ ] Extrair Conhecimentos Específicos do Perfil 3.
* [ ] Preservar os nomes oficiais do edital.
* [ ] Criar IDs únicos das disciplinas.
* [ ] Definir quantidade de questões por disciplina, quando disponível.
* [ ] Definir peso.
* [ ] Definir pontuação máxima.
* [ ] Definir prioridade-base.
* [ ] Definir ordem inicial de estudo.
* [ ] Definir status inicial.

## 4.4 Extração dos assuntos

* [ ] Extrair todos os tópicos do conteúdo programático.
* [ ] Extrair subtópicos relevantes.
* [ ] Preservar a redação oficial.
* [ ] Associar cada assunto à disciplina correta.
* [ ] Criar IDs únicos dos assuntos.
* [ ] Definir ordem inicial.
* [ ] Definir status inicial.
* [ ] Identificar assuntos amplos que precisam ser subdivididos.
* [ ] Evitar divisões excessivamente pequenas.
* [ ] Evitar unir tópicos que exigem tratamentos diferentes.

## 4.5 Análise do pacote do Estratégia

* [ ] Listar todos os cursos do pacote.
* [ ] Listar disciplinas presentes.
* [ ] Identificar aulas e módulos disponíveis.
* [ ] Identificar PDFs.
* [ ] Identificar videoaulas, quando informado.
* [ ] Identificar simulados presentes.
* [ ] Identificar banco de questões ou trilhas relacionadas.
* [ ] Registrar cursos extras que não correspondem ao edital.
* [ ] Não presumir cobertura sem evidência.

## 4.6 Comparação edital × Estratégia

Para cada assunto do edital:

* [ ] Identificar curso correspondente.
* [ ] Identificar aula ou módulo correspondente.
* [ ] Classificar cobertura como `Completa`.
* [ ] Classificar cobertura como `Parcial`.
* [ ] Classificar cobertura como `Ausente`.
* [ ] Classificar cobertura como `Não verificada`.
* [ ] Registrar observações.
* [ ] Registrar necessidade de material complementar.
* [ ] Registrar conteúdos do curso que excedem o edital.

## 4.7 Matriz de cobertura

* [ ] Criar tabela Disciplina × Assunto × Material.
* [ ] Incluir situação da cobertura.
* [ ] Incluir observações.
* [ ] Incluir prioridade.
* [ ] Incluir material complementar necessário.
* [ ] Validar que nenhum tópico ficou sem classificação.

## 4.8 Estratégia inicial

* [ ] Definir maior prioridade para Conhecimentos Específicos.
* [ ] Garantir contato mínimo com todas as disciplinas.
* [ ] Evitar risco de zerar qualquer disciplina.
* [ ] Definir proporção inicial de teoria e questões.
* [ ] Definir duração inicial de teoria por tipo de assunto.
* [ ] Definir quantidade inicial de questões.
* [ ] Definir parâmetros para assuntos já dominados.
* [ ] Definir parâmetros para assuntos novos.
* [ ] Definir parâmetros para matérias predominantemente teóricas.
* [ ] Definir parâmetros para Português.
* [ ] Definir parâmetros para Inglês.
* [ ] Definir parâmetros para Raciocínio Lógico.
* [ ] Definir parâmetros para Legislação.
* [ ] Definir parâmetros para Atualidades e IA.
* [ ] Definir parâmetros para Conhecimentos Específicos.

## 4.9 Dados de importação

* [ ] Preparar dados de `_db_Disciplinas`.
* [ ] Preparar dados de `_db_Assuntos`.
* [ ] Preparar configurações iniciais de `_db_Config`.
* [ ] Validar IDs.
* [ ] Validar relacionamentos.
* [ ] Validar pesos.
* [ ] Validar nomes.
* [ ] Validar caracteres especiais.
* [ ] Validar datas.
* [ ] Preparar formato reutilizável pelo setup.

## 4.10 Entregas da Fase 1

* [ ] Entregar análise do edital.
* [ ] Entregar análise do Estratégia.
* [ ] Entregar matriz de cobertura.
* [ ] Entregar lista de disciplinas.
* [ ] Entregar lista de assuntos.
* [ ] Entregar lacunas.
* [ ] Entregar prioridades iniciais.
* [ ] Entregar dados prontos para importação.
* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar este `TODO.md`.
* [ ] Criar `REVIEW.md` da Fase 1.
* [ ] Parar e aguardar aprovação.

---

# 5. FASE 2 — ESTRUTURA DO GOOGLE SHEETS

## 5.1 Projeto inicial

* [ ] Criar projeto do Google Apps Script.
* [ ] Criar `Main.gs`.
* [ ] Criar `Setup.gs`.
* [ ] Criar `MenuController.gs`.
* [ ] Criar `SidebarController.gs`.
* [ ] Criar `SoeaEngine.gs`.
* [ ] Criar serviços previstos no `ARQUITETURA.md`.
* [ ] Criar `Repository.gs`.
* [ ] Criar `IdService.gs`.
* [ ] Criar `ValidationService.gs`.
* [ ] Criar `RecoveryService.gs`.
* [ ] Criar `Utils.gs`.
* [ ] Criar `Constants.gs`.

## 5.2 Setup

* [ ] Implementar `setupSOEA()`.
* [ ] Verificar se a planilha está vazia.
* [ ] Criar abas ausentes.
* [ ] Preservar abas existentes.
* [ ] Preservar dados existentes.
* [ ] Validar cabeçalhos.
* [ ] Criar configurações padrão.
* [ ] Registrar instalação no histórico.
* [ ] Permitir nova execução sem duplicar abas.
* [ ] Tratar erros.
* [ ] Exibir mensagem de conclusão.

## 5.3 Abas visíveis

Criar e formatar:

* [ ] Dashboard.
* [ ] Ciclo.
* [ ] Banco de Erros.
* [ ] Simulados.
* [ ] Estatísticas.
* [ ] Configurações.

## 5.4 Abas ocultas

Criar:

* [ ] `_db_Disciplinas`
* [ ] `_db_Assuntos`
* [ ] `_db_Ciclo`
* [ ] `_db_Blocos`
* [ ] `_db_Sessoes`
* [ ] `_db_Questoes`
* [ ] `_db_Revisoes`
* [ ] `_db_Erros`
* [ ] `_db_Simulados`
* [ ] `_db_Config`
* [ ] `_db_Metricas`
* [ ] `_db_Historico`
* [ ] `_db_Logs`
* [ ] `_db_Backup`

## 5.5 Cabeçalhos e dados

* [ ] Criar cabeçalhos conforme o PRD.
* [ ] Padronizar nomes de colunas.
* [ ] Congelar cabeçalhos.
* [ ] Aplicar formatação de datas.
* [ ] Aplicar formatação de horas.
* [ ] Aplicar formatação de percentuais.
* [ ] Aplicar validações de status.
* [ ] Aplicar validações de energia.
* [ ] Aplicar validações de tipo de sessão.
* [ ] Aplicar validações de revisão.
* [ ] Aplicar validações de motivos de erro.
* [ ] Ocultar abas internas.
* [ ] Proteger abas internas.

## 5.6 Importação

* [ ] Importar disciplinas.
* [ ] Importar assuntos.
* [ ] Importar pesos.
* [ ] Importar prioridades-base.
* [ ] Importar correspondências com o Estratégia.
* [ ] Importar data da prova.
* [ ] Importar parâmetros iniciais.
* [ ] Validar quantidade de registros.
* [ ] Validar relacionamentos.

## 5.7 Menu SOEA

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

## 5.8 Sidebars iniciais

* [ ] Criar `SidebarSession.html`.
* [ ] Criar `SidebarOpportunity.html`.
* [ ] Criar `SidebarQuestionResult.html`.
* [ ] Criar `SidebarErrorEntry.html`.
* [ ] Criar `SidebarReview.html`.
* [ ] Criar `SidebarSimulation.html`.
* [ ] Criar `SidebarSettings.html`.
* [ ] Criar `SidebarAbout.html`.
* [ ] Criar estilos compartilhados.
* [ ] Criar scripts compartilhados.
* [ ] Validar abertura de todas as Sidebars.
* [ ] Validar mensagens.
* [ ] Evitar dependências externas.

## 5.9 Dashboard inicial

* [ ] Criar cabeçalho.
* [ ] Criar card de dias até a prova.
* [ ] Criar card de bloco atual.
* [ ] Criar card de horas.
* [ ] Criar card de questões.
* [ ] Criar card de aproveitamento.
* [ ] Criar card de revisões.
* [ ] Criar card de erros.
* [ ] Criar card de percentual do edital.
* [ ] Reservar espaços para gráficos.
* [ ] Não apresentar dados falsos como definitivos.

## 5.10 Testes da estrutura

* [ ] Testar setup em planilha vazia.
* [ ] Testar segunda execução do setup.
* [ ] Testar cabeçalhos.
* [ ] Testar abas ocultas.
* [ ] Testar proteções.
* [ ] Testar menu.
* [ ] Testar Sidebars.
* [ ] Testar importação.
* [ ] Testar mensagens de erro.
* [ ] Testar acesso em outro computador.

## 5.11 Entregas da Fase 2

* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar este `TODO.md`.
* [ ] Criar `REVIEW.md` da Fase 2.
* [ ] Documentar arquivos criados.
* [ ] Documentar limitações.
* [ ] Parar e aguardar aprovação.

---

# 6. FASE 3 — MOTOR DO SOEA

## 6.1 IDs

* [ ] Implementar IDs de disciplinas.
* [ ] Implementar IDs de assuntos.
* [ ] Implementar `CYC-001`.
* [ ] Implementar IDs de blocos.
* [ ] Implementar IDs de sessões.
* [ ] Implementar IDs de questões.
* [ ] Implementar IDs de revisões.
* [ ] Implementar IDs de erros.
* [ ] Implementar IDs de simulados.
* [ ] Implementar IDs de histórico.
* [ ] Implementar IDs de backups.
* [ ] Utilizar `LockService`.
* [ ] Testar duplicidade.

## 6.2 Ciclo

* [ ] Criar ciclo ativo.
* [ ] Garantir apenas um ciclo ativo.
* [ ] Associar blocos ao ciclo.
* [ ] Atualizar blocos concluídos.
* [ ] Calcular percentual do edital.
* [ ] Concluir ciclo quando aplicável.
* [ ] Preservar histórico.

## 6.3 Assuntos e blocos

* [ ] Identificar próximo assunto elegível.
* [ ] Criar bloco.
* [ ] Associar disciplina.
* [ ] Associar assunto.
* [ ] Associar ciclo.
* [ ] Registrar status.
* [ ] Registrar etapa atual.
* [ ] Registrar tempo previsto.
* [ ] Registrar questões previstas.
* [ ] Iniciar bloco.
* [ ] Atualizar bloco.
* [ ] Concluir bloco.
* [ ] Impedir dois blocos ativos.
* [ ] Impedir repetição de etapa concluída.
* [ ] Permitir retomada.

## 6.4 Sessões

* [ ] Criar sessão.
* [ ] Registrar tipo.
* [ ] Registrar energia.
* [ ] Registrar tempo disponível.
* [ ] Registrar horário inicial.
* [ ] Registrar horário final.
* [ ] Registrar tempo real.
* [ ] Encerrar sessão.
* [ ] Impedir duas sessões abertas.
* [ ] Recuperar sessão órfã.
* [ ] Permitir sessão parcial.

## 6.5 Continuar Ciclo

* [ ] Verificar estrutura.
* [ ] Verificar ciclo ativo.
* [ ] Verificar sessão ativa.
* [ ] Verificar bloco ativo.
* [ ] Retomar bloco, quando existir.
* [ ] Verificar revisões pendentes.
* [ ] Calcular prioridade.
* [ ] Selecionar assunto.
* [ ] Criar bloco.
* [ ] Abrir Sidebar.
* [ ] Apresentar etapa atual.
* [ ] Apresentar tempo.
* [ ] Apresentar quantidade de questões.
* [ ] Registrar progresso.
* [ ] Perguntar se ainda possui tempo.
* [ ] Gerar próximo bloco, quando aplicável.

## 6.6 Aproveitar Tempo

* [ ] Solicitar tempo disponível.
* [ ] Solicitar objetivo.
* [ ] Oferecer Questões.
* [ ] Oferecer Revisão.
* [ ] Oferecer Banco de Erros.
* [ ] Oferecer Tanto faz.
* [ ] Consultar o mesmo bloco ativo.
* [ ] Dividir etapa.
* [ ] Não criar ciclo paralelo.
* [ ] Não criar bloco duplicado.
* [ ] Atualizar progresso.
* [ ] Concluir bloco, quando aplicável.
* [ ] Gerar revisões, quando aplicável.
* [ ] Garantir continuidade posterior.

## 6.7 Barra de Energia

* [ ] Implementar Excelente.
* [ ] Implementar Boa.
* [ ] Implementar Cansado.
* [ ] Implementar Muito cansado.
* [ ] Ajustar teoria.
* [ ] Ajustar quantidade de questões.
* [ ] Priorizar revisões quando necessário.
* [ ] Priorizar Banco de Erros quando necessário.
* [ ] Não cancelar sessão.
* [ ] Testar Modo Emergência.

## 6.8 Registro de questões

* [ ] Registrar fonte.
* [ ] Registrar quantidade.
* [ ] Registrar acertos.
* [ ] Calcular erros.
* [ ] Calcular percentual.
* [ ] Registrar tempo.
* [ ] Calcular tempo médio.
* [ ] Associar bloco.
* [ ] Associar disciplina.
* [ ] Associar assunto.
* [ ] Atualizar bloco.
* [ ] Atualizar métricas.
* [ ] Atualizar domínio.
* [ ] Atualizar prioridade.

## 6.9 Banco de Erros

* [ ] Preencher disciplina automaticamente.
* [ ] Preencher assunto automaticamente.
* [ ] Preencher bloco automaticamente.
* [ ] Registrar motivo.
* [ ] Registrar causa raiz.
* [ ] Registrar observação.
* [ ] Registrar data.
* [ ] Definir status Novo.
* [ ] Permitir status Revisado.
* [ ] Permitir status Resolvido.
* [ ] Filtrar erros.
* [ ] Selecionar erros para revisão.
* [ ] Calcular recorrência.
* [ ] Atualizar prioridade.
* [ ] Atualizar Dashboard.

## 6.10 Revisões

* [ ] Criar D+1.
* [ ] Criar D+7.
* [ ] Criar D+15.
* [ ] Criar D+30.
* [ ] Impedir duplicidade.
* [ ] Marcar Pendente.
* [ ] Marcar Atrasada.
* [ ] Registrar data realizada.
* [ ] Registrar resultado.
* [ ] Selecionar erros do bloco.
* [ ] Sugerir questões.
* [ ] Aplicar regra de 90% ou mais.
* [ ] Aplicar regra de 70% a 89%.
* [ ] Aplicar regra abaixo de 70%.
* [ ] Criar revisão extra.
* [ ] Atualizar prioridade.
* [ ] Atualizar domínio.

## 6.11 Índice de Prioridade

* [ ] Definir fórmula inicial.
* [ ] Documentar fórmula.
* [ ] Definir pesos configuráveis.
* [ ] Considerar peso do edital.
* [ ] Considerar baixo desempenho.
* [ ] Considerar volume de questões.
* [ ] Considerar erros.
* [ ] Considerar revisões atrasadas.
* [ ] Considerar tempo sem contato.
* [ ] Considerar proximidade da prova.
* [ ] Considerar simulados.
* [ ] Normalizar entre 0 e 100.
* [ ] Aplicar limites.
* [ ] Testar cenários extremos.

## 6.12 Índice de Domínio

* [ ] Definir fórmula inicial.
* [ ] Documentar fórmula.
* [ ] Considerar questões.
* [ ] Considerar revisões.
* [ ] Considerar simulados.
* [ ] Considerar erros recorrentes.
* [ ] Considerar amostra mínima.
* [ ] Normalizar entre 0 e 100.
* [ ] Classificar vermelho.
* [ ] Classificar amarelo.
* [ ] Classificar verde.
* [ ] Testar amostra pequena.
* [ ] Testar alto desempenho.
* [ ] Testar baixo desempenho.

## 6.13 Tempo Estimado Inteligente

* [ ] Definir tempos padrão.
* [ ] Registrar tempos reais.
* [ ] Calcular tempo por questão.
* [ ] Calcular tempo de teoria.
* [ ] Calcular tempo de correção.
* [ ] Calcular tempo de revisão.
* [ ] Definir quantidade mínima de histórico.
* [ ] Personalizar estimativa.
* [ ] Aplicar limites mínimos.
* [ ] Aplicar limites máximos.
* [ ] Mostrar estimativa ao usuário.

## 6.14 Métricas

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
* [ ] Revisões concluídas.
* [ ] Revisões atrasadas.
* [ ] Erros pendentes.
* [ ] Percentual do edital.
* [ ] Sequência de estudos.
* [ ] Metas semanais.

## 6.15 Histórico e logs

* [ ] Registrar sessão iniciada.
* [ ] Registrar sessão encerrada.
* [ ] Registrar bloco criado.
* [ ] Registrar bloco concluído.
* [ ] Registrar revisão criada.
* [ ] Registrar revisão realizada.
* [ ] Registrar erro.
* [ ] Registrar simulado.
* [ ] Registrar alteração de configuração.
* [ ] Registrar exceções.
* [ ] Separar histórico funcional de log técnico.

## 6.16 Integridade e recuperação

* [ ] Verificar ciclo ativo.
* [ ] Verificar bloco ativo.
* [ ] Verificar sessão ativa.
* [ ] Verificar IDs duplicados.
* [ ] Verificar registros órfãos.
* [ ] Verificar revisões duplicadas.
* [ ] Encerrar sessões órfãs.
* [ ] Reconstruir bloco ativo.
* [ ] Preservar progresso.
* [ ] Exibir mensagem clara.
* [ ] Registrar recuperação.

## 6.17 Backup

* [ ] Criar política de backup.
* [ ] Criar backup diário.
* [ ] Criar backup antes de operação crítica.
* [ ] Criar backup antes de restauração.
* [ ] Definir retenção.
* [ ] Remover backups antigos.
* [ ] Restaurar último estado.
* [ ] Registrar restauração.
* [ ] Testar recuperação.

## 6.18 Testes da Fase 3

* [ ] Interromper bloco no meio.
* [ ] Fechar e abrir planilha.
* [ ] Retomar corretamente.
* [ ] Utilizar Aproveitar Tempo parcialmente.
* [ ] Concluir bloco por Aproveitar Tempo.
* [ ] Estudar no trabalho e continuar em casa.
* [ ] Registrar questões.
* [ ] Registrar erros.
* [ ] Criar revisões.
* [ ] Realizar revisão.
* [ ] Gerar revisão extra.
* [ ] Testar energia baixa.
* [ ] Testar menos de 30 minutos.
* [ ] Testar sessão longa.
* [ ] Testar clique duplicado.
* [ ] Testar falha no meio da operação.
* [ ] Testar recuperação.
* [ ] Validar métricas.
* [ ] Validar prioridade.
* [ ] Validar domínio.

## 6.19 Entregas da Fase 3

* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar este `TODO.md`.
* [ ] Criar `REVIEW.md` da Fase 3.
* [ ] Documentar fórmula dos índices.
* [ ] Documentar bugs conhecidos.
* [ ] Parar e aguardar aprovação.

---

# 7. FASE 4 — DASHBOARD, SIMULADOS, TESTES E ENTREGA

## 7.1 Agenda de simulados

* [ ] Considerar data real de início.
* [ ] Não criar simulados retroativos.
* [ ] Agendar apenas em finais de semana.
* [ ] Julho: segundo e quarto sábado.
* [ ] Agosto: todos os sábados.
* [ ] Setembro: todos os sábados.
* [ ] Últimos 15 dias: permitir mini simulado.
* [ ] Reservar domingo para correção.
* [ ] Tornar regras configuráveis.

## 7.2 Registro de simulados

* [ ] Registrar ID.
* [ ] Registrar nome.
* [ ] Registrar data.
* [ ] Registrar duração.
* [ ] Registrar total de questões.
* [ ] Registrar acertos.
* [ ] Registrar erros.
* [ ] Calcular percentual.
* [ ] Registrar por disciplina.
* [ ] Registrar assuntos problemáticos.
* [ ] Registrar observação.
* [ ] Atualizar domínio.
* [ ] Atualizar prioridade.
* [ ] Atualizar Dashboard.

## 7.3 Dashboard final

Cards:

* [ ] Dias até a prova.
* [ ] Bloco atual.
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
* [ ] Índice geral.

Gráficos:

* [ ] Evolução de acertos.
* [ ] Questões por semana.
* [ ] Horas por semana.
* [ ] Desempenho por disciplina.
* [ ] Evolução dos simulados.
* [ ] Erros por causa raiz.
* [ ] Assuntos com menor domínio.
* [ ] Assuntos com maior prioridade.

## 7.4 Estatísticas

* [ ] Filtro por período.
* [ ] Filtro por disciplina.
* [ ] Filtro por assunto.
* [ ] Filtro por tipo de atividade.
* [ ] Tendência de desempenho.
* [ ] Total de questões.
* [ ] Total de horas.
* [ ] Aproveitamento por disciplina.
* [ ] Aproveitamento por assunto.
* [ ] Erros recorrentes.
* [ ] Causas de erro.
* [ ] Revisões.
* [ ] Simulados.
* [ ] Metas semanais.

## 7.5 UX e mensagens

* [ ] Iniciar estudo em menos de 30 segundos.
* [ ] Reduzir quantidade de cliques.
* [ ] Evitar caixas de diálogo excessivas.
* [ ] Usar Sidebars.
* [ ] Exibir mensagens claras.
* [ ] Não exibir stack trace ao usuário.
* [ ] Mostrar resumo do bloco concluído.
* [ ] Mostrar resumo da sessão.
* [ ] Perguntar se ainda possui tempo.
* [ ] Informar progresso salvo.
* [ ] Validar legibilidade.

## 7.6 Testes completos

* [ ] Instalação em planilha vazia.
* [ ] Reinstalação segura.
* [ ] Importação.
* [ ] Menu.
* [ ] Sidebars.
* [ ] Ciclo.
* [ ] Blocos.
* [ ] Sessões.
* [ ] Aproveitar Tempo.
* [ ] Barra de Energia.
* [ ] Questões.
* [ ] Erros.
* [ ] Revisões.
* [ ] Simulados.
* [ ] Prioridade.
* [ ] Domínio.
* [ ] Métricas.
* [ ] Dashboard.
* [ ] Estatísticas.
* [ ] Histórico.
* [ ] Logs.
* [ ] Backup.
* [ ] Recuperação.
* [ ] Performance.
* [ ] Acesso em computadores diferentes.

## 7.7 Bugs

### Críticos

* [ ] Nenhum bug crítico conhecido na entrega.

### Altos

* [ ] Registrar e corrigir todos os bugs de alto impacto.

### Médios

* [ ] Corrigir os que afetarem o fluxo de estudos.
* [ ] Registrar os demais.

### Baixos

* [ ] Registrar no `TODO.md`.
* [ ] Adiar apenas quando não prejudicarem o uso.

## 7.8 Performance

* [ ] Revisar leituras.
* [ ] Revisar escritas.
* [ ] Implementar operações em lote.
* [ ] Evitar chamadas dentro de loops.
* [ ] Revisar caches.
* [ ] Revisar locks.
* [ ] Revisar gatilhos.
* [ ] Revisar backups.
* [ ] Medir tempo das principais operações.

## 7.9 README

* [ ] Explicar objetivo.
* [ ] Explicar requisitos.
* [ ] Explicar criação da planilha.
* [ ] Explicar acesso ao Apps Script.
* [ ] Explicar autorização.
* [ ] Explicar setup.
* [ ] Explicar Continuar Ciclo.
* [ ] Explicar Aproveitar Tempo.
* [ ] Explicar questões.
* [ ] Explicar Banco de Erros.
* [ ] Explicar revisões.
* [ ] Explicar simulados.
* [ ] Explicar Dashboard.
* [ ] Explicar configurações.
* [ ] Explicar backup.
* [ ] Explicar restauração.
* [ ] Incluir perguntas frequentes.
* [ ] Incluir solução de problemas.
* [ ] Incluir limitações da versão 1.0.

## 7.10 Entrega

* [ ] Atualizar `ROADMAP.md`.
* [ ] Atualizar `CHANGELOG.md`.
* [ ] Atualizar este `TODO.md`.
* [ ] Criar `REVIEW.md` final.
* [ ] Marcar versão `SOEA v1.0`.
* [ ] Garantir ausência de pendência crítica.
* [ ] Registrar pendências futuras.
* [ ] Entregar instruções de uso.
* [ ] Parar e aguardar aprovação final.

---

# 8. TESTES DE ACEITAÇÃO DO PRODUCT OWNER

## Fase 1

* [ ] Conferir disciplinas.
* [ ] Conferir assuntos.
* [ ] Conferir pesos.
* [ ] Conferir matriz de cobertura.
* [ ] Conferir lacunas.
* [ ] Aprovar dados de importação.

## Fase 2

* [ ] Executar setup.
* [ ] Conferir abas.
* [ ] Conferir cabeçalhos.
* [ ] Conferir dados importados.
* [ ] Conferir menu.
* [ ] Abrir Sidebars.
* [ ] Conferir Dashboard básico.
* [ ] Aprovar estrutura.

## Fase 3

* [ ] Iniciar bloco.
* [ ] Interromper bloco.
* [ ] Retomar bloco.
* [ ] Usar Aproveitar Tempo.
* [ ] Concluir bloco.
* [ ] Registrar questões.
* [ ] Registrar erros.
* [ ] Conferir revisões.
* [ ] Conferir prioridade.
* [ ] Conferir domínio.
* [ ] Conferir salvamento.
* [ ] Aprovar Motor do SOEA.

## Fase 4

* [ ] Registrar simulado.
* [ ] Conferir Dashboard.
* [ ] Conferir gráficos.
* [ ] Conferir estatísticas.
* [ ] Conferir README.
* [ ] Executar fluxo completo.
* [ ] Aprovar versão 1.0.

---

# 9. BUGS E BLOQUEIOS

## Bugs abertos

Nenhum registrado.

## Bloqueios abertos

Nenhum registrado.

## Formato para novos registros

```text
[!] Identificador:
Fase:
Funcionalidade:
Descrição:
Impacto:
Forma de reprodução:
Solução proposta:
Status:
```

---

# 10. ITENS ADIADOS PARA VERSÃO FUTURA

* [~] Aplicação web.
* [~] Aplicativo mobile.
* [~] Multiusuário.
* [~] Múltiplos concursos.
* [~] Integração com o Estratégia.
* [~] Integração com plataformas de questões.
* [~] Importação automática do edital.
* [~] IA integrada à planilha.
* [~] Google Calendar.
* [~] Sincronização entre contas.
* [~] Notificações externas.
* [~] Gamificação avançada.

Esses itens não deverão ser implementados na versão 1.0.

---

# 11. ESTADO ATUAL

```text
FASE 0 — DOCUMENTAÇÃO
Em validação final

FASE 1 — ANÁLISE
Não iniciada

FASE 2 — ESTRUTURA
Não iniciada

FASE 3 — MOTOR DO SOEA
Não iniciada

FASE 4 — FINALIZAÇÃO
Não iniciada
```

## Próxima tarefa

```text
Criar CHANGELOG.md e REVIEW.md iniciais.

Depois executar o Prompt da Fase 1.
```

---

# 12. ENCERRAMENTO

O objetivo deste documento é manter o desenvolvimento controlado, verificável e alinhado ao escopo.

A prioridade da versão 1.0 é entregar uma planilha funcional e estável com rapidez suficiente para apoiar os estudos para a DATAPREV 2026.

Itens cosméticos ou evoluções que não sejam essenciais deverão ser adiados, evitando que o desenvolvimento consuma o tempo destinado à preparação para a prova.
