# ARQUITETURA.md

# SOEA — Sistema Operacional de Estudos Adaptativo

**Versão:** 1.0
**Status:** Arquitetura inicial aprovada
**Tecnologias obrigatórias:** Google Sheets + Google Apps Script
**Documento relacionado:** `PRD.md`

---

# 1. OBJETIVO DESTE DOCUMENTO

Este documento define como a versão 1.0 da Planilha Inteligente SOEA deverá ser organizada e implementada.

O `PRD.md` define **o que deve ser construído**.

O `ARQUITETURA.md` define **como a implementação deve ser estruturada**.

Em caso de conflito:

1. O `PRD.md` prevalece sobre o `ARQUITETURA.md`.
2. O `ARQUITETURA.md` prevalece sobre decisões improvisadas durante a implementação.
3. Nenhuma alteração de requisito poderá ser realizada sem aprovação do Product Owner.

O projeto deverá permanecer uma planilha inteligente.

Não deverá ser convertido em aplicação web, aplicativo mobile, API ou sistema hospedado durante a versão 1.0.

---

# 2. PAPEL DO CODEX

O Codex atuará como Engenheiro de Software responsável pela implementação da versão 1.0 da Planilha Inteligente SOEA.

Suas responsabilidades são:

* ler e respeitar o `PRD.md`;
* ler e respeitar este documento;
* implementar exclusivamente com Google Sheets e Google Apps Script;
* manter o código modular;
* evitar duplicação;
* preservar os dados;
* manter a documentação atualizada;
* interromper o desenvolvimento ao final de cada fase;
* aguardar a aprovação do Product Owner antes de prosseguir.

O Codex poderá sugerir melhorias.

Entretanto, não poderá implementar mudanças de requisito sem aprovação explícita.

---

# 3. PRINCÍPIOS ARQUITETURAIS

Toda implementação deverá respeitar os princípios abaixo.

## 3.1 Planilha antes de software web

O SOEA é uma planilha inteligente.

A solução deverá aproveitar os recursos nativos do Google Sheets e do Google Apps Script.

Não utilizar tecnologias externas quando houver solução viável dentro do ecossistema Google.

---

## 3.2 Simplicidade

A solução mais simples e estável deverá ser priorizada.

Evitar abstrações desnecessárias.

Evitar criar infraestrutura que não seja necessária para a versão 1.0.

---

## 3.3 Separação de responsabilidades

Cada arquivo do Google Apps Script deverá possuir responsabilidade clara.

Não concentrar toda a implementação em um único arquivo `.gs`.

---

## 3.4 Fonte única de verdade

As abas ocultas serão a fonte oficial dos dados.

As abas visíveis serão apenas interfaces e relatórios.

O Dashboard nunca deverá armazenar dados permanentes.

---

## 3.5 Salvamento automático

O usuário nunca deverá clicar em “Salvar”.

Todas as alterações deverão ser persistidas automaticamente.

---

## 3.6 Continuidade

A planilha deverá sempre conseguir identificar:

* o ciclo ativo;
* o bloco ativo;
* a etapa atual do bloco;
* as revisões pendentes;
* o progresso já realizado.

---

## 3.7 Não duplicidade

Nunca deverão existir simultaneamente:

* dois ciclos ativos;
* dois blocos em andamento;
* duas sessões abertas;
* revisões duplicadas do mesmo tipo e bloco;
* IDs duplicados.

---

## 3.8 Baixa manutenção

A planilha deverá exigir o mínimo possível de manutenção manual.

O usuário nunca deverá editar diretamente as abas ocultas.

---

# 4. STACK TECNOLÓGICA

A versão 1.0 utilizará exclusivamente:

## Interface e visualização

* Google Sheets
* Gráficos nativos do Google Sheets
* Formatação condicional
* Validação de dados
* Menus personalizados

## Lógica e automação

* Google Apps Script
* HTML Service do Google Apps Script para Sidebars
* Properties Service para estados técnicos simples, quando necessário
* Lock Service para prevenir execuções simultâneas
* Cache Service apenas quando trouxer ganho real de desempenho

## Persistência

* Abas ocultas do Google Sheets

## Documentação

* Markdown

## Arquivos obrigatórios

* `PRD.md`
* `ARQUITETURA.md`
* `ROADMAP.md`
* `TODO.md`
* `CHANGELOG.md`
* `REVIEW.md`
* `README.md`

---

# 5. TECNOLOGIAS FORA DO ESCOPO

Não utilizar na versão 1.0:

* React;
* Next.js;
* Angular;
* Vue;
* Node.js;
* Python;
* Firebase;
* bancos de dados externos;
* APIs externas;
* Docker;
* hospedagem;
* servidor próprio;
* aplicação web independente;
* autenticação adicional;
* integração automática com o Estratégia;
* integração automática com plataformas de questões.

Caso algum requisito pareça depender de uma dessas tecnologias, o Codex deverá:

1. não implementar a dependência externa;
2. registrar a limitação no `TODO.md`;
3. explicar a alternativa possível dentro do Google Sheets;
4. aguardar decisão do Product Owner.

---

# 6. ARQUITETURA GERAL

A arquitetura deverá seguir este fluxo:

```text
Usuário
   ↓
Abas Visíveis / Menu SOEA / Sidebar
   ↓
Controladores do Apps Script
   ↓
Motor do SOEA
   ↓
Serviços de domínio
   ↓
Repositórios de acesso às abas ocultas
   ↓
Abas ocultas
   ↓
Métricas e atualização do Dashboard
```

Nenhuma aba visível deverá tomar decisões.

Toda decisão deverá passar pelo Google Apps Script.

---

# 7. ABAS VISÍVEIS

A versão 1.0 deverá possuir apenas estas abas visíveis:

## 7.1 Dashboard

Função:

* apresentar indicadores;
* mostrar o próximo bloco;
* mostrar revisões pendentes;
* mostrar questões totais;
* mostrar horas estudadas;
* mostrar percentual do edital;
* mostrar informações de simulados;
* mostrar erros pendentes;
* oferecer acesso rápido às ações principais.

O Dashboard não deverá armazenar dados permanentes.

---

## 7.2 Ciclo

Função:

* exibir o bloco atual;
* exibir a etapa atual;
* exibir tempo previsto;
* permitir iniciar ou continuar a sessão;
* permitir usar “Aproveitar Tempo”;
* permitir registrar resultados;
* permitir concluir o bloco.

---

## 7.3 Banco de Erros

Função:

* exibir erros registrados;
* permitir filtros;
* permitir atualização de status;
* apresentar motivo, causa raiz e observação;
* mostrar assuntos com maior recorrência.

---

## 7.4 Simulados

Função:

* registrar simulados;
* consultar resultados;
* comparar desempenho;
* mostrar evolução histórica.

---

## 7.5 Estatísticas

Função:

* apresentar métricas detalhadas;
* desempenho por disciplina;
* desempenho por assunto;
* questões por período;
* horas por período;
* domínio;
* prioridade;
* evolução.

---

## 7.6 Configurações

Função:

* editar preferências;
* alterar tempos padrão;
* alterar quantidade padrão de questões;
* alterar metas;
* alterar regras de revisão permitidas;
* refletir os dados armazenados em `_db_Config`.

A aba Configurações não será a fonte oficial dos dados.

---

# 8. ABAS OCULTAS

As seguintes abas serão utilizadas como persistência interna:

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
* `_db_Backup`

Essas abas deverão:

* ser criadas automaticamente;
* ser ocultadas;
* possuir cabeçalhos fixos;
* ser manipuladas apenas por funções do Apps Script;
* utilizar IDs únicos;
* possuir validação mínima de integridade;
* manter histórico consistente.

---

# 9. ORGANIZAÇÃO DOS ARQUIVOS APPS SCRIPT

A implementação deverá ser dividida em arquivos com responsabilidades claras.

## 9.1 `Main.gs`

Responsável por:

* função `onOpen`;
* criação do menu SOEA;
* inicialização geral;
* chamadas de alto nível;
* verificação de instalação.

Não deve conter regras complexas de negócio.

---

## 9.2 `Setup.gs`

Responsável por:

* criar as abas;
* criar cabeçalhos;
* aplicar formatação inicial;
* criar validações;
* ocultar abas internas;
* popular configurações padrão;
* verificar estrutura;
* executar instalação inicial;
* permitir reinstalação segura sem apagar dados.

---

## 9.3 `MenuController.gs`

Responsável por:

* ações do menu;
* abrir Sidebars;
* redirecionar comandos;
* exibir mensagens de sucesso ou erro.

---

## 9.4 `SidebarController.gs`

Responsável por:

* enviar dados às Sidebars;
* receber respostas do usuário;
* validar entradas;
* chamar o Motor do SOEA;
* retornar a próxima etapa da interface.

---

## 9.5 `SoeaEngine.gs`

Representa o Motor do SOEA.

Responsável por:

* identificar o ciclo ativo;
* identificar o bloco ativo;
* localizar revisões pendentes;
* calcular prioridades;
* decidir a próxima ação;
* gerar novos blocos;
* retomar blocos;
* controlar “Continuar Ciclo”;
* controlar “Aproveitar Tempo”;
* impedir duplicidade.

Este arquivo não deverá acessar células diretamente.

Ele deverá utilizar serviços e repositórios.

---

## 9.6 `CycleService.gs`

Responsável por:

* consultar o ciclo ativo;
* criar ciclo quando permitido;
* atualizar progresso do ciclo;
* concluir ciclo;
* calcular percentual do edital.

Na versão 1.0 deverá existir apenas um ciclo ativo.

---

## 9.7 `BlockService.gs`

Responsável por:

* criar blocos;
* atualizar blocos;
* retomar blocos;
* concluir blocos;
* controlar etapas;
* impedir múltiplos blocos em andamento;
* calcular progresso do bloco;
* vincular bloco a disciplina, assunto e ciclo.

---

## 9.8 `SessionService.gs`

Responsável por:

* criar sessões;
* encerrar sessões;
* registrar tempo;
* registrar energia;
* controlar sessão ativa;
* calcular duração;
* vincular sessões a blocos.

---

## 9.9 `QuestionService.gs`

Responsável por:

* registrar lotes de questões;
* calcular acertos;
* calcular erros;
* calcular percentual;
* calcular tempo médio;
* atualizar métricas;
* alimentar Índice de Domínio e Índice de Prioridade.

A versão 1.0 não armazenará o enunciado das questões.

---

## 9.10 `ReviewService.gs`

Responsável por:

* criar revisões D+1, D+7, D+15 e D+30;
* impedir revisões duplicadas;
* localizar revisões pendentes;
* marcar revisões atrasadas;
* registrar desempenho;
* reagendar revisão extra quando necessário;
* atualizar prioridade e domínio.

---

## 9.11 `ErrorBankService.gs`

Responsável por:

* registrar erros;
* atualizar erros;
* alterar status;
* localizar erros por disciplina e assunto;
* classificar motivo;
* classificar causa raiz;
* selecionar erros para revisão.

---

## 9.12 `SimulationService.gs`

Responsável por:

* registrar simulados;
* calcular desempenho;
* registrar duração;
* registrar resultados;
* fornecer dados para gráficos;
* atualizar domínio e prioridade.

---

## 9.13 `PriorityService.gs`

Responsável por:

* calcular Índice de Prioridade;
* normalizar valores entre 0 e 100;
* ordenar assuntos;
* considerar pesos do edital;
* considerar erros;
* considerar revisões;
* considerar desempenho;
* considerar tempo sem contato;
* considerar proximidade da prova.

A fórmula deverá ser configurável e documentada.

---

## 9.14 `MasteryService.gs`

Responsável por:

* calcular Índice de Domínio;
* classificar assuntos;
* combinar questões, revisões, simulados e erros;
* fornecer estado vermelho, amarelo ou verde;
* recalcular somente quando necessário.

---

## 9.15 `DashboardService.gs`

Responsável por:

* reunir métricas;
* atualizar cards;
* atualizar tabelas;
* atualizar gráficos;
* mostrar próximo bloco;
* mostrar revisões pendentes;
* não armazenar dados permanentes.

---

## 9.16 `MetricsService.gs`

Responsável por:

* consolidar horas;
* consolidar questões;
* consolidar acertos;
* consolidar erros;
* consolidar revisões;
* consolidar simulados;
* calcular sequência de estudos;
* calcular metas semanais.

---

## 9.17 `HistoryService.gs`

Responsável por:

* registrar eventos relevantes;
* manter rastreabilidade;
* registrar ações do usuário;
* registrar alterações automáticas;
* ajudar na reconstrução de estado.

---

## 9.18 `BackupService.gs`

Responsável por:

* criar backups;
* manter política de retenção;
* restaurar último estado consistente;
* registrar restaurações;
* evitar backup excessivo.

---

## 9.19 `ConfigService.gs`

Responsável por:

* ler configurações;
* validar configurações;
* aplicar valores padrão;
* atualizar `_db_Config`;
* impedir valores inválidos.

---

## 9.20 `Repository.gs`

Responsável por:

* leitura padronizada das abas;
* escrita padronizada;
* busca por ID;
* inserção;
* atualização;
* validação de cabeçalhos;
* conversão de linhas em objetos;
* conversão de objetos em linhas.

Não deverá conter regras de negócio.

Caso o tamanho cresça demais, poderá ser dividido em:

* `DisciplineRepository.gs`
* `SubjectRepository.gs`
* `CycleRepository.gs`
* `BlockRepository.gs`
* `SessionRepository.gs`
* `ReviewRepository.gs`
* `ErrorRepository.gs`
* `SimulationRepository.gs`

---

## 9.21 `IdService.gs`

Responsável por gerar IDs únicos.

Formatos previstos:

```text
CYC-001
BLK-000001
SES-000001
QST-000001
REV-000001
ERR-000001
SIM-000001
HIS-000001
BKP-000001
DSC-000001
ASU-000001
```

A geração deverá ser segura contra duplicidade.

---

## 9.22 `ValidationService.gs`

Responsável por:

* validar entradas;
* validar relacionamentos;
* validar estado do ciclo;
* validar bloco ativo;
* validar sessão ativa;
* detectar inconsistências;
* impedir operações inválidas.

---

## 9.23 `RecoveryService.gs`

Responsável por:

* detectar inconsistências;
* reconstruir estado;
* recuperar bloco ativo;
* encerrar sessões órfãs;
* restaurar dados quando necessário;
* registrar ações de recuperação.

---

## 9.24 `Utils.gs`

Responsável apenas por funções genéricas e reutilizáveis:

* datas;
* horários;
* arredondamentos;
* textos;
* conversões;
* normalizações;
* cálculos auxiliares.

Não deverá possuir regras de negócio.

---

## 9.25 `Constants.gs`

Responsável por armazenar constantes:

* nomes de abas;
* cabeçalhos;
* status;
* tipos de sessão;
* tipos de revisão;
* mensagens;
* formatos de ID;
* valores padrão.

Evitar strings repetidas diretamente no código.

---

# 10. ARQUIVOS HTML DAS SIDEBARS

As Sidebars deverão ser simples e responsivas dentro do limite do Google Sheets.

Arquivos sugeridos:

* `SidebarSession.html`
* `SidebarOpportunity.html`
* `SidebarQuestionResult.html`
* `SidebarErrorEntry.html`
* `SidebarReview.html`
* `SidebarSimulation.html`
* `SidebarSettings.html`
* `SidebarAbout.html`

Poderão existir arquivos compartilhados:

* `Styles.html`
* `Scripts.html`
* `Components.html`

Não utilizar frameworks externos.

---

# 11. SIDEBAR DE SESSÃO

A Sidebar principal deverá controlar:

1. tempo disponível;
2. nível de energia;
3. bloco atual;
4. etapa atual;
5. tempo estimado;
6. quantidade de questões;
7. registro de resultado;
8. conclusão do bloco;
9. pergunta “Ainda possui tempo?”;
10. geração do próximo bloco.

A Sidebar deverá permanecer simples.

Evitar abrir várias janelas consecutivas.

---

# 12. MENU PERSONALIZADO

O menu `SOEA` deverá ser criado automaticamente por `onOpen`.

Itens:

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

Os itens mais importantes deverão aparecer primeiro.

---

# 13. FLUXO DO “CONTINUAR CICLO”

O fluxo deverá ser implementado desta forma:

```text
Usuário clica em Continuar Ciclo
   ↓
Validar estrutura da planilha
   ↓
Verificar ciclo ativo
   ↓
Verificar sessão aberta
   ↓
Verificar bloco em andamento
   ↓
Se existir, retomar
   ↓
Se não existir, verificar revisões pendentes
   ↓
Se houver revisão prioritária, gerar bloco de revisão
   ↓
Se não houver, calcular Índice de Prioridade
   ↓
Selecionar assunto
   ↓
Criar bloco
   ↓
Abrir Sidebar
```

O usuário deverá informar tempo e energia antes da geração final da carga.

---

# 14. FLUXO DO “APROVEITAR TEMPO”

```text
Usuário clica em Aproveitar Tempo
   ↓
Informa tempo disponível
   ↓
Informa objetivo:
- Questões
- Revisão
- Banco de Erros
- Tanto faz
   ↓
Motor verifica bloco atual
   ↓
Motor escolhe atividade compatível
   ↓
Não criar ciclo paralelo
   ↓
Não criar bloco duplicado
   ↓
Atualizar o mesmo progresso
```

Caso o bloco seja concluído, deverá:

* marcá-lo como concluído;
* criar revisões;
* atualizar histórico;
* atualizar métricas;
* permitir que o próximo “Continuar Ciclo” avance normalmente.

---

# 15. FLUXO DE CONCLUSÃO DE BLOCO

```text
Usuário conclui todas as etapas
   ↓
Validar resultados
   ↓
Atualizar bloco
   ↓
Registrar tempo real
   ↓
Registrar questões
   ↓
Registrar erros, quando informado
   ↓
Marcar bloco como concluído
   ↓
Criar revisões
   ↓
Recalcular domínio
   ↓
Recalcular prioridade
   ↓
Atualizar métricas
   ↓
Atualizar Dashboard
   ↓
Registrar histórico
   ↓
Mostrar resumo da sessão
   ↓
Perguntar se ainda possui tempo
```

---

# 16. MODELO DE ACESSO A DADOS

Nenhum serviço deverá usar diretamente chamadas espalhadas como:

```javascript
SpreadsheetApp.getActive().getSheetByName(...)
```

Essas chamadas deverão ser centralizadas no repositório ou em um serviço de planilha.

Isso permitirá:

* padronização;
* tratamento de erro;
* testes;
* manutenção;
* redução de duplicação.

---

# 17. LEITURA E ESCRITA EM LOTE

Evitar operações célula por célula.

Priorizar:

* `getValues()`;
* `setValues()`;
* leitura em lote;
* escrita em lote;
* atualização apenas das linhas necessárias.

Não chamar `getRange()` repetidamente dentro de loops quando puder ser evitado.

---

# 18. CONCORRÊNCIA

Antes de operações críticas, utilizar `LockService`.

Operações críticas incluem:

* criação de ID;
* criação de bloco;
* conclusão de bloco;
* criação de revisões;
* criação de backup;
* restauração;
* atualização de métricas globais.

Isso impedirá duplicidades causadas por cliques repetidos ou execuções simultâneas.

---

# 19. TRATAMENTO DE ERROS

Toda função pública deverá possuir tratamento adequado de erros.

O padrão esperado:

1. capturar a exceção;
2. registrar em `_db_Historico` ou `_db_Logs`;
3. preservar o estado;
4. exibir mensagem simples ao usuário;
5. evitar exposição de detalhes técnicos;
6. permitir recuperação.

Mensagens ao usuário:

```text
Não foi possível concluir esta ação.
Seu progresso foi preservado.
Tente novamente ou use “Verificar Integridade”.
```

Detalhes técnicos deverão ficar apenas nos logs.

---

# 20. LOGS

A arquitetura deverá diferenciar:

## Histórico funcional

Exemplos:

* bloco iniciado;
* sessão concluída;
* revisão criada;
* erro registrado.

## Log técnico

Exemplos:

* exceção;
* falha de validação;
* aba ausente;
* cabeçalho incorreto;
* tentativa de duplicidade.

Caso necessário, criar `_db_Logs` separada de `_db_Historico`.

---

# 21. BACKUP

O backup não deverá copiar a planilha inteira após cada alteração pequena.

Deverá existir uma política equilibrada.

Sugestão:

* backup antes de operações críticas;
* backup diário;
* backup antes de restauração;
* retenção limitada;
* remoção automática de backups antigos.

A política final deverá ser configurável em `_db_Config`.

---

# 22. CONFIGURAÇÕES PADRÃO

As configurações iniciais deverão incluir:

* data da prova: `11/10/2026`;
* duração padrão de teoria;
* tempo padrão por questão;
* quantidade padrão de questões;
* revisões: D+1, D+7, D+15 e D+30;
* metas semanais;
* pesos dos componentes do Índice de Prioridade;
* pesos dos componentes do Índice de Domínio;
* limite de backups;
* tempo mínimo para Modo Emergência.

Nenhuma configuração importante deverá ficar fixa dentro das funções.

---

# 23. ÍNDICE DE PRIORIDADE

O cálculo deverá ficar isolado em `PriorityService.gs`.

O resultado deverá variar de 0 a 100.

Componentes esperados:

* peso da disciplina;
* baixo desempenho;
* erros pendentes;
* revisões atrasadas;
* tempo desde o último contato;
* proximidade da prova;
* desempenho em simulados;
* quantidade insuficiente de questões.

A fórmula exata deverá:

* ser documentada;
* ser configurável;
* possuir limites;
* evitar valores acima de 100 ou abaixo de 0.

---

# 24. ÍNDICE DE DOMÍNIO

O cálculo deverá ficar isolado em `MasteryService.gs`.

Resultado entre 0 e 100.

Classificação:

```text
0–59: Vermelho
60–79: Amarelo
80–100: Verde
```

Componentes:

* desempenho em questões;
* desempenho nas revisões;
* desempenho em simulados;
* reincidência de erros;
* volume mínimo de questões.

O domínio não deverá ser considerado alto com amostra muito pequena.

---

# 25. TEMPO ESTIMADO INTELIGENTE

Durante a fase inicial, utilizar valores padrão.

Quando houver histórico suficiente, considerar:

* tempo médio por questão;
* tempo médio de teoria;
* tempo médio de correção;
* tempo médio de revisão;
* disciplina;
* assunto;
* tipo de sessão.

A estimativa personalizada deverá substituir gradualmente o valor padrão.

---

# 26. REVISÕES

As revisões deverão ser criadas após a conclusão de um bloco.

Cada revisão deverá possuir:

* ID;
* bloco de origem;
* tipo;
* data prevista;
* status;
* resultado;
* data realizada.

A revisão não deverá reabrir o bloco original.

Ela será uma nova atividade vinculada ao bloco de origem.

---

# 27. BANCO DE ERROS

O cadastro deverá ser rápido.

Campos sugeridos:

* disciplina;
* assunto;
* bloco;
* motivo;
* causa raiz;
* observação;
* status.

Disciplina, assunto e bloco deverão ser preenchidos automaticamente sempre que possível.

Evitar exigir preenchimento repetitivo.

---

# 28. DASHBOARD

O Dashboard deverá ser atualizado por serviço específico.

Cards mínimos:

* dias até a prova;
* bloco atual;
* horas totais;
* horas da semana;
* questões totais;
* questões da semana;
* aproveitamento;
* revisões pendentes;
* erros pendentes;
* percentual do edital;
* sequência de estudos;
* próximo simulado.

Gráficos mínimos:

* evolução de acertos;
* questões por semana;
* horas por semana;
* desempenho por disciplina;
* evolução dos simulados.

Evitar excesso de gráficos.

---

# 29. SEGURANÇA DE DADOS

Não armazenar:

* senhas;
* dados bancários;
* tokens externos;
* credenciais do Estratégia;
* conteúdo protegido do curso;
* enunciados completos de questões protegidas.

A planilha deverá armazenar apenas dados de acompanhamento.

---

# 30. DOCUMENTAÇÃO OBRIGATÓRIA

Ao final de cada fase, o Codex deverá atualizar:

## `ROADMAP.md`

* fase atual;
* percentual;
* entregas concluídas;
* próximo marco.

## `TODO.md`

* tarefas concluídas;
* tarefas pendentes;
* bugs;
* melhorias futuras.

## `CHANGELOG.md`

* arquivos criados;
* arquivos alterados;
* funcionalidades entregues;
* correções realizadas.

## `REVIEW.md`

* resumo da fase;
* itens implementados;
* arquivos modificados;
* testes realizados;
* pendências;
* bugs conhecidos;
* instruções para validação do Product Owner.

O `PRD.md` e o `ARQUITETURA.md` só deverão ser alterados quando houver requisito ou decisão arquitetural aprovada.

---

# 31. PROCESSO DE APROVAÇÃO

Ao concluir cada fase, o Codex deverá parar.

Não iniciar a fase seguinte automaticamente.

Deverá apresentar:

```text
Fase concluída.

ROADMAP atualizado.
TODO atualizado.
CHANGELOG atualizado.
REVIEW.md criado ou atualizado.

Aguardando validação do Product Owner.
```

Somente após aprovação explícita poderá prosseguir.

---

# 32. CRITÉRIOS ARQUITETURAIS DE ACEITE

A arquitetura será considerada respeitada quando:

* toda lógica estiver no Apps Script;
* nenhuma lógica crítica depender de fórmulas espalhadas;
* as abas ocultas forem a fonte oficial dos dados;
* serviços não acessarem células diretamente de forma desorganizada;
* o Motor do SOEA centralizar decisões;
* o código estiver dividido por responsabilidade;
* IDs forem únicos;
* operações críticas utilizarem Lock Service;
* erros forem registrados;
* o usuário nunca editar abas ocultas;
* o projeto não depender de hospedagem;
* a planilha puder ser acessada por qualquer computador com a conta Google;
* a documentação for atualizada ao final de cada fase.

---

# 33. DEFINIÇÃO DE PRONTO ARQUITETURAL

Uma funcionalidade somente será considerada pronta quando:

1. estiver implementada;
2. respeitar o PRD;
3. respeitar esta arquitetura;
4. possuir validações;
5. possuir tratamento de erro;
6. atualizar os dados corretos;
7. atualizar histórico;
8. não gerar duplicidade;
9. possuir cenário de teste;
10. estiver registrada no `CHANGELOG.md`;
11. estiver marcada no `TODO.md`;
12. estiver descrita no `REVIEW.md`.

---

# 34. ENCERRAMENTO

Este documento representa a arquitetura oficial da versão 1.0 da Planilha Inteligente SOEA.

O foco desta versão é:

* entregar rapidamente;
* reduzir riscos;
* evitar infraestrutura externa;
* permitir acesso de qualquer lugar;
* garantir estabilidade;
* apoiar os estudos para a DATAPREV 2026.

Nenhuma decisão técnica deverá transformar o projeto em um desenvolvimento maior do que o necessário para cumprir esse objetivo.
