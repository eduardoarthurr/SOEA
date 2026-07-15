# PROMPT 02 — FASE 2: ESTRUTURA DO GOOGLE SHEETS

## 1. Instrução inicial

Antes de criar, alterar, enviar ou executar qualquer arquivo, leia integralmente:

* `docs/PRD.md`
* `docs/ARQUITETURA.md`
* `docs/INSTRUCOES.md`
* `docs/AMBIENTE_AUTONOMO.md`
* `docs/ROADMAP.md`
* `docs/TODO.md`
* `docs/CHANGELOG.md`
* `docs/REVIEW.md`

Leia também todos os arquivos existentes nas pastas:

```text
analises/
dados/
fontes/
apps-script/
```

Confirme no `ROADMAP.md`, no `TODO.md` e no `REVIEW.md` que:

1. a Fase 1 foi executada;
2. a análise do edital foi concluída;
3. os dados de disciplinas, assuntos e configurações foram produzidos;
4. o Product Owner aprovou explicitamente a Fase 1;
5. a fase atual é a Fase 2.

A aprovação deverá estar registrada de forma equivalente a:

```text
Fase 1 aprovada.

Pode iniciar a Fase 2.
```

Caso a Fase 1 não esteja aprovada:

1. não execute esta fase;
2. registre o bloqueio no `REVIEW.md`;
3. preserve todos os arquivos;
4. informe o Product Owner;
5. pare.

---

# 2. Verificação obrigatória do ambiente autônomo

Antes da implementação, leia o status registrado em:

```text
docs/AMBIENTE_AUTONOMO.md
```

A Fase 2 somente poderá continuar quando o status for:

```text
PRONTO_COMPLETO
```

Confirme que estão realmente funcionais:

* Node.js compatível;
* npm;
* `clasp`;
* autenticação do `clasp`;
* API do Google Apps Script;
* projeto Apps Script vinculado;
* planilha Google Sheets vinculada;
* arquivo `.clasp.json`;
* `clasp push`;
* Chrome conectado;
* acesso ao editor do Apps Script;
* acesso à planilha;
* execução real de função;
* Computer Use ou ferramenta visual equivalente.

Não presuma que o ambiente continua funcional apenas porque foi configurado anteriormente.

Execute uma verificação curta antes de iniciar:

```bash
node --version
npm --version
clasp --version
```

Caso a instalação do `clasp` seja local, utilize:

```bash
npx clasp --version
```

Dentro de `apps-script/`, execute:

```bash
clasp status
```

ou:

```bash
npx clasp status
```

Confirme também que o projeto remoto correto pode ser aberto.

Caso o ambiente não esteja `PRONTO_COMPLETO`:

1. não produza uma entrega somente local;
2. não declare que a fase foi executada;
3. registre o bloqueio;
4. tente corrigir autonomamente o problema;
5. solicite intervenção do Product Owner apenas quando houver autenticação, segurança ou decisão pessoal;
6. continue após a intervenção;
7. só prossiga quando o ambiente voltar a `PRONTO_COMPLETO`.

---

# 3. Objetivo da fase

Criar, implantar e testar a estrutura funcional inicial da Planilha Inteligente SOEA utilizando:

* Google Sheets;
* Google Apps Script;
* HTML Service;
* menus nativos;
* Sidebars;
* validações de dados;
* formatação condicional;
* abas visíveis;
* abas ocultas;
* gráficos nativos;
* `clasp`;
* execução real na planilha vinculada.

Ao final desta fase, deverá existir uma planilha real capaz de:

* instalar a estrutura do SOEA;
* criar todas as abas;
* criar e validar os cabeçalhos;
* importar disciplinas;
* importar assuntos;
* importar configurações;
* aplicar formatações;
* aplicar validações;
* ocultar e proteger abas internas;
* criar o menu `SOEA`;
* abrir as Sidebars iniciais;
* montar o Dashboard estrutural;
* alterar configurações simples;
* verificar a integridade estrutural;
* criar um backup estrutural;
* preservar os dados em novas execuções do setup.

Não será suficiente criar os arquivos localmente.

A implementação deverá ser:

```text
Criada localmente
↓
Enviada com clasp
↓
Executada no Apps Script real
↓
Validada no Google Sheets real
↓
Testada
↓
Corrigida
↓
Testada novamente
```

---

# 4. Limites da Fase 2

Implementar completamente nesta fase:

* estrutura de arquivos;
* manifesto;
* constantes;
* dados iniciais;
* setup;
* reinstalação segura;
* criação das abas;
* cabeçalhos;
* formatações;
* validações;
* proteção;
* ocultação;
* menu;
* Sidebars iniciais;
* interface de configurações;
* Dashboard estrutural;
* métricas estruturais básicas;
* verificação de integridade estrutural;
* histórico e logs iniciais;
* backup estrutural;
* documentação de instalação;
* implantação e testes reais.

Não implementar completamente nesta fase:

* seleção adaptativa do próximo assunto;
* criação real de ciclos de estudo;
* criação adaptativa de blocos;
* retomada inteligente;
* sessões funcionais;
* Aproveitar Tempo funcional;
* registro definitivo de questões;
* Banco de Erros totalmente funcional;
* geração automática de revisões;
* Índice de Prioridade;
* Índice de Domínio;
* Tempo Estimado Inteligente;
* recuperação avançada;
* agenda automática de simulados;
* Dashboard analítico final;
* Estatísticas finais.

Esses itens pertencem às Fases 3 e 4.

Não apresentar uma funcionalidade futura como concluída.

---

# 5. Preservação do projeto remoto

Antes de enviar qualquer alteração:

1. confirmar que o `.clasp.json` aponta para o projeto correto;
2. confirmar que a planilha vinculada é a planilha do SOEA;
3. abrir o projeto remoto;
4. verificar se existem arquivos remotos não presentes localmente;
5. preservar qualquer arquivo relevante;
6. criar cópia de segurança antes de sobrescrever conteúdo existente.

Se houver código remoto:

* não executar `clasp push --force` imediatamente;
* executar `clasp pull` em uma pasta temporária ou criar um backup;
* comparar os arquivos;
* preservar conteúdo válido;
* documentar conflitos;
* só substituir depois de confirmar que é seguro.

Não apagar código remoto sem análise.

---

# 6. Verificação dos dados da Fase 1

Antes de criar `SeedData.gs`, verificar a existência de:

```text
dados/disciplinas.csv
dados/assuntos.csv
dados/config_inicial.csv
```

Consultar especialmente:

```text
analises/00_Resumo_Fase_1.md
analises/03_Matriz_Cobertura.md
analises/06_Validacao_Dados.md
```

Validar:

* codificação UTF-8;
* existência dos cabeçalhos;
* ausência de IDs duplicados;
* ausência de disciplinas duplicadas;
* ausência de assuntos duplicados;
* relacionamento entre assuntos e disciplinas;
* ausência de registros órfãos;
* valores de cobertura permitidos;
* campos obrigatórios;
* caracteres especiais;
* datas;
* números;
* campos `Não verificado`;
* ausência de linhas totalmente vazias.

Caso um erro impeça a importação segura:

1. não corrigir silenciosamente informações oficiais;
2. registrar o problema;
3. identificar o arquivo e a linha;
4. explicar o impacto;
5. corrigir apenas erros técnicos evidentes que não alterem o conteúdo oficial;
6. solicitar decisão do Product Owner quando houver dúvida de conteúdo;
7. não prosseguir com dados inconsistentes.

---

# 7. Estrutura local do Apps Script

Utilizar a pasta:

```text
apps-script/
```

Criar ou completar:

```text
apps-script/
├── .clasp.json
├── appsscript.json
├── Main.gs
├── Setup.gs
├── Constants.gs
├── SeedData.gs
├── Repository.gs
├── MenuController.gs
├── SidebarController.gs
├── SoeaEngine.gs
├── CycleService.gs
├── BlockService.gs
├── SessionService.gs
├── QuestionService.gs
├── ReviewService.gs
├── ErrorBankService.gs
├── SimulationService.gs
├── PriorityService.gs
├── MasteryService.gs
├── DashboardService.gs
├── MetricsService.gs
├── HistoryService.gs
├── BackupService.gs
├── ConfigService.gs
├── IdService.gs
├── ValidationService.gs
├── RecoveryService.gs
├── Utils.gs
├── SidebarSession.html
├── SidebarOpportunity.html
├── SidebarQuestionResult.html
├── SidebarErrorEntry.html
├── SidebarReview.html
├── SidebarSimulation.html
├── SidebarSettings.html
├── SidebarAbout.html
├── Styles.html
├── Scripts.html
└── Components.html
```

O arquivo `EnvironmentCheck.gs`, criado pelo Prompt 00, poderá:

* permanecer temporariamente durante os testes;
* ser removido ao final da fase, caso não seja mais necessário;
* ou permanecer como diagnóstico seguro, desde que seja documentado.

Caso seja necessário criar outro arquivo:

1. utilizar nome claro;
2. definir responsabilidade única;
3. justificar no `REVIEW.md`;
4. manter compatibilidade com a arquitetura;
5. não criar arquivos redundantes.

---

# 8. Manifesto

Validar `appsscript.json`.

Garantir:

```json
{
  "timeZone": "America/Sao_Paulo",
  "exceptionLogging": "STACKDRIVER",
  "runtimeVersion": "V8"
}
```

Preservar outros campos válidos já existentes.

Não adicionar:

* APIs externas;
* bibliotecas externas;
* web app;
* escopos desnecessários;
* serviços avançados sem necessidade;
* permissões não relacionadas ao Google Sheets e Apps Script.

Caso o Google adicione escopos automaticamente após a execução, documentar quais permissões foram solicitadas e por quê.

---

# 9. Arquivo `Constants.gs`

Centralizar em `Constants.gs`:

* nomes das abas;
* nomes dos arquivos;
* cabeçalhos;
* status;
* tipos de sessão;
* níveis de energia;
* tipos de revisão;
* motivos de erro;
* causas-raiz;
* textos do menu;
* títulos das Sidebars;
* formatos de ID;
* formatos de data;
* formatos de hora;
* formatos de percentual;
* mensagens;
* valores padrão;
* versão do projeto.

Exemplo ilustrativo:

```javascript
const SOEA_SHEETS = Object.freeze({
  DASHBOARD: 'Dashboard',
  CYCLE: 'Ciclo',
  ERROR_BANK: 'Banco de Erros',
  SIMULATIONS: 'Simulados',
  STATISTICS: 'Estatísticas',
  SETTINGS: 'Configurações',
  DB_DISCIPLINES: '_db_Disciplinas'
});
```

Utilizar os nomes oficiais definidos no PRD e na Arquitetura.

Não espalhar strings estruturais pelo código.

---

# 10. Arquivo `SeedData.gs`

Converter:

```text
dados/disciplinas.csv
dados/assuntos.csv
dados/config_inicial.csv
```

em estruturas JavaScript válidas.

Criar constantes semelhantes a:

```javascript
const SOEA_SEED_DISCIPLINES = [];
const SOEA_SEED_SUBJECTS = [];
const SOEA_SEED_CONFIG = [];
```

Regras:

* preservar IDs;
* preservar acentos;
* preservar textos oficiais;
* preservar campos `Não verificado`;
* escapar aspas;
* tratar quebras de linha;
* não incluir fórmulas;
* não incluir credenciais;
* não alterar valores silenciosamente;
* manter compatibilidade com V8;
* registrar no cabeçalho a origem dos dados;
* registrar a data de geração;
* incluir contagens esperadas.

Criar validação interna que compare:

* quantidade do CSV;
* quantidade convertida;
* IDs;
* relacionamentos.

---

# 11. Repositório de dados

Implementar em `Repository.gs` funções reutilizáveis para:

* obter planilha ativa;
* localizar aba;
* exigir aba;
* criar mapa de cabeçalhos;
* validar cabeçalhos;
* ler linhas em lote;
* converter linha em objeto;
* converter objeto em linha;
* buscar registro por ID;
* verificar existência;
* inserir registro;
* inserir registros em lote;
* atualizar registro;
* localizar linha por ID;
* comparar registros;
* evitar duplicidade.

O repositório não deverá conter regras de negócio.

Evitar chamadas repetidas como:

```javascript
SpreadsheetApp.getActive().getSheetByName(...)
```

Não depender silenciosamente da posição fixa das colunas.

---

# 12. Função principal de instalação

Implementar em `Setup.gs`:

```javascript
function setupSOEA() {
  // implementação
}
```

O fluxo deverá ser:

```text
Adquirir Lock
↓
Validar planilha vinculada
↓
Verificar versão estrutural
↓
Criar backup quando necessário
↓
Criar abas inexistentes
↓
Validar abas existentes
↓
Criar ou validar cabeçalhos
↓
Aplicar formatações
↓
Aplicar validações
↓
Importar disciplinas ausentes
↓
Importar assuntos ausentes
↓
Importar configurações ausentes
↓
Montar abas visíveis
↓
Montar Dashboard estrutural
↓
Ocultar abas internas
↓
Aplicar proteções
↓
Registrar histórico
↓
Executar verificação estrutural
↓
Liberar Lock
↓
Exibir resumo
```

Utilizar `try`, `catch` e `finally`.

O lock deverá sempre ser liberado.

Em caso de falha:

* preservar dados;
* registrar log;
* informar qual etapa falhou;
* não continuar silenciosamente;
* não apagar a estrutura parcial sem análise.

---

# 13. Idempotência obrigatória

O `setupSOEA()` deverá ser idempotente.

Executá-lo novamente não poderá:

* duplicar abas;
* duplicar cabeçalhos;
* duplicar disciplinas;
* duplicar assuntos;
* duplicar configurações;
* apagar dados;
* alterar IDs;
* apagar progresso futuro;
* apagar configurações editadas;
* recriar ciclo;
* remover colunas válidas;
* substituir registros reais por seeds;
* destruir formatação permitida.

A importação deverá comparar registros por ID.

Quando um ID já existir:

* não duplicar;
* não apagar;
* não alterar dados de acompanhamento;
* atualizar somente campos estruturais seguros;
* registrar divergências;
* preservar campos editáveis pelo usuário.

---

# 14. Abas visíveis

Criar:

```text
Dashboard
Ciclo
Banco de Erros
Simulados
Estatísticas
Configurações
```

Para cada aba:

* aplicar título;
* criar estrutura visual;
* definir larguras;
* definir alturas;
* congelar áreas necessárias;
* utilizar contraste adequado;
* evitar excesso de cores;
* evitar células mescladas desnecessárias;
* aplicar formatos;
* exibir estado vazio;
* não incluir dados fictícios permanentes.

---

# 15. Aba `Dashboard`

Criar a estrutura para os cards:

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

Criar áreas para:

* evolução do aproveitamento;
* questões por semana;
* horas por semana;
* desempenho por disciplina;
* evolução dos simulados.

Nesta fase:

* dias até a prova deverá utilizar a configuração real;
* total de disciplinas deverá ser real;
* total de assuntos deverá ser real;
* outros indicadores poderão apresentar `Ainda sem dados`;
* gráficos deverão funcionar com estado vazio;
* nenhum histórico fictício deverá ser criado.

O Dashboard não deverá armazenar dados permanentes.

---

# 16. Aba `Ciclo`

Criar estrutura visual para:

* ciclo ativo;
* bloco atual;
* disciplina;
* assunto;
* etapa;
* tempo estimado;
* tempo realizado;
* progresso;
* quantidade de questões;
* sessão;
* próxima ação.

Exibir:

```text
Utilize o menu SOEA para iniciar ou continuar seus estudos.
```

Como o Motor ainda não estará implementado, não criar ciclo ou bloco fictício.

---

# 17. Aba `Banco de Erros`

Criar estrutura compatível com `_db_Erros`.

Preparar:

* cabeçalhos;
* filtros;
* listas suspensas;
* formatos;
* status;
* destaque para erros novos;
* destaque para recorrência;
* estado vazio.

Não criar erros fictícios.

O funcionamento completo será implementado na Fase 3.

---

# 18. Aba `Simulados`

Criar estrutura para:

* ID;
* nome;
* data planejada;
* data realizada;
* duração;
* questões;
* acertos;
* erros;
* percentual;
* status;
* observações.

Criar espaços futuros para evolução e desempenho.

A agenda automática será implementada na Fase 4.

---

# 19. Aba `Estatísticas`

Criar estrutura para:

* horas;
* questões;
* aproveitamento;
* disciplinas;
* assuntos;
* revisões;
* erros;
* simulados;
* domínio;
* prioridade.

Exibir:

```text
As estatísticas aparecerão após o início dos estudos.
```

Não implementar cálculos avançados nesta fase.

---

# 20. Aba `Configurações`

Criar interface baseada em `_db_Config`.

Exibir configurações como:

* data da prova;
* tempos padrão;
* quantidade padrão de questões;
* revisões;
* metas;
* parâmetros de energia;
* limites de backup;
* demais valores aprovados.

A aba visível será uma interface.

A fonte oficial continuará sendo `_db_Config`.

Permitir alteração apenas de configurações marcadas como editáveis.

Não permitir edição de:

* IDs;
* nomes das abas;
* cabeçalhos;
* chaves técnicas;
* formatos internos;
* versão estrutural;
* configurações não editáveis.

---

# 21. Abas ocultas

Criar:

```text
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
_db_Logs
_db_Backup
```

Utilizar os cabeçalhos definidos no PRD.

Caso um cabeçalho não esteja suficientemente definido:

1. consultar a Arquitetura;
2. consultar o TODO;
3. criar somente o mínimo necessário;
4. documentar a decisão;
5. não inventar campos sem justificativa.

Todas as abas internas deverão:

* possuir cabeçalhos;
* congelar a primeira linha;
* utilizar formatos adequados;
* possuir filtros quando úteis;
* possuir validação estrutural;
* ser ocultadas;
* ser protegidas;
* permanecer acessíveis ao script;
* utilizar IDs;
* não depender de posição visual fixa sem validação.

---

# 22. Proteção das abas internas

Aplicar proteção de forma que:

* o usuário seja desencorajado a editar manualmente;
* o próprio script continue funcionando;
* a proteção não bloqueie o Product Owner permanentemente;
* seja possível realizar manutenção autorizada;
* nenhuma aba visível seja protegida de maneira que impeça o uso normal.

Registrar no `REVIEW.md` como a proteção foi aplicada.

---

# 23. Configurações

Implementar em `ConfigService.gs`:

* leitura por chave;
* leitura de todas as configurações;
* validação de existência;
* atualização de valor editável;
* validação de tipo;
* aplicação de padrão;
* prevenção de duplicidade;
* sincronização com a aba visível.

Tipos previstos:

```text
texto
numero
booleano
data
lista
```

Não transformar valor ausente em zero.

Não aceitar datas ou números inválidos.

---

# 24. Menu `SOEA`

Implementar em `Main.gs`:

```javascript
function onOpen() {
  // menu
}
```

Criar:

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

Nesta fase:

* `Atualizar Dashboard` deverá funcionar;
* `Configurações` deverá abrir;
* `Verificar Integridade` deverá funcionar estruturalmente;
* `Criar Backup` deverá criar backup estrutural;
* `Ajuda` deverá abrir orientação;
* `Sobre` deverá abrir informações;
* as ações das Fases 3 e 4 poderão abrir Sidebars estruturais;
* ações futuras deverão informar claramente que ainda não estão ativas.

Nenhum item do menu poderá apontar para uma função inexistente.

Nenhum clique deverá gerar stack trace visível ao usuário.

---

# 25. Sidebars

Criar:

```text
SidebarSession.html
SidebarOpportunity.html
SidebarQuestionResult.html
SidebarErrorEntry.html
SidebarReview.html
SidebarSimulation.html
SidebarSettings.html
SidebarAbout.html
```

Todas deverão:

* utilizar HTML, CSS e JavaScript simples;
* não utilizar framework;
* não utilizar CDN;
* não utilizar biblioteca externa;
* ser legíveis;
* possuir labels;
* validar campos;
* possuir botão de cancelar;
* possuir estado de carregamento;
* impedir clique repetido;
* utilizar `google.script.run`;
* tratar sucesso;
* tratar erro;
* preservar dados digitados em caso de erro;
* não exibir detalhes técnicos.

---

# 26. Sidebar de sessão

`SidebarSession.html` deverá preparar:

* tempo disponível;
* energia;
* bloco atual;
* etapa atual;
* carga sugerida;
* botão de iniciar;
* botão de cancelar.

Nesta fase, deverá informar:

```text
A estrutura desta funcionalidade está pronta.

O funcionamento completo será ativado na Fase 3.
```

Não criar bloco fictício.

---

# 27. Sidebar Aproveitar Tempo

`SidebarOpportunity.html` deverá preparar:

* tempo disponível;
* objetivo;
* Questões;
* Revisão;
* Banco de Erros;
* Tanto faz.

Não implementar a decisão adaptativa.

---

# 28. Sidebars de registro

Preparar:

## Questões

* quantidade;
* acertos;
* tempo;
* fonte;
* observações.

## Erro

* disciplina;
* assunto;
* motivo;
* causa-raiz;
* observação.

## Revisão

* revisão;
* resultado;
* questões;
* acertos;
* conclusão.

## Simulado

* nome;
* data;
* duração;
* questões;
* acertos;
* observação.

Nesta fase, os formulários deverão abrir e validar a interface, mas não registrar dados de domínio como se a funcionalidade estivesse pronta.

---

# 29. Sidebar de configurações

`SidebarSettings.html` deverá:

* ler configurações reais;
* exibir somente valores permitidos;
* permitir alteração de campos editáveis;
* validar dados;
* salvar em `_db_Config`;
* atualizar a aba visível;
* registrar histórico;
* mostrar confirmação.

Esse fluxo deverá ser funcional nesta fase.

---

# 30. Sidebar Sobre e Ajuda

A interface deverá apresentar:

* nome do projeto;
* versão;
* objetivo;
* tecnologias;
* fase atual;
* instruções iniciais;
* aviso de uso pessoal;
* indicação de funcionalidades ainda em desenvolvimento.

---

# 31. Arquivos HTML compartilhados

Utilizar:

```text
Styles.html
Scripts.html
Components.html
```

Criar função semelhante a:

```javascript
function include(filename) {
  return HtmlService
    .createHtmlOutputFromFile(filename)
    .getContent();
}
```

Evitar duplicar CSS e JavaScript.

---

# 32. Serviços das fases futuras

Criar os arquivos de serviço previstos na arquitetura.

Nesta fase, serviços futuros poderão conter:

* documentação da responsabilidade;
* assinaturas iniciais;
* validações básicas;
* respostas estruturadas de indisponibilidade.

Exemplo:

```javascript
return {
  success: false,
  code: 'FEATURE_NOT_AVAILABLE',
  message: 'Esta funcionalidade será ativada na Fase 3.'
};
```

Não:

* criar blocos fictícios;
* criar sessões fictícias;
* retornar prioridade inventada;
* retornar domínio inventado;
* criar revisões fictícias;
* gerar métricas falsas.

---

# 33. DashboardService

Implementar nesta fase:

* leitura da data da prova;
* cálculo de dias até a prova;
* total de disciplinas;
* total de assuntos;
* total real de registros;
* atualização dos cards básicos;
* estados vazios;
* estrutura dos gráficos.

Não implementar:

* domínio;
* prioridade;
* recomendações;
* previsões;
* tendências avançadas.

---

# 34. Histórico e logs

Implementar estrutura mínima em:

```text
HistoryService.gs
_db_Historico
_db_Logs
```

Registrar eventos como:

* setup iniciado;
* setup concluído;
* setup falhou;
* aba criada;
* cabeçalho criado;
* dado importado;
* configuração alterada;
* Dashboard atualizado;
* verificação executada;
* backup criado;
* erro técnico.

O histórico funcional não deverá armazenar stack trace.

Os detalhes técnicos deverão ficar em `_db_Logs`.

---

# 35. Backup estrutural

Implementar em `BackupService.gs` uma função pública:

```javascript
function criarBackupSOEA() {
  // implementação
}
```

Nesta fase, o backup deverá preservar:

* configurações;
* disciplinas;
* assuntos;
* estrutura das abas;
* cabeçalhos;
* versão estrutural;
* informações necessárias para diagnóstico.

Não declarar restauração automática completa nesta fase.

O backup deverá:

* possuir ID;
* registrar data;
* registrar tipo;
* registrar motivo;
* registrar versão;
* evitar duplicidade desnecessária;
* não apagar backups válidos.

---

# 36. Verificação estrutural

Implementar:

```javascript
function verificarIntegridadeSOEA() {
  // implementação
}
```

Verificar:

* existência das abas;
* nomes das abas;
* cabeçalhos;
* `_db_Config`;
* disciplinas;
* assuntos;
* IDs duplicados;
* assuntos sem disciplina;
* configurações duplicadas;
* planilha vinculada;
* versão estrutural;
* abas internas visíveis;
* erros estruturais básicos.

Retornar relatório com:

```text
Aprovado
Aviso
Erro
Crítico
```

Não corrigir automaticamente uma falha destrutiva.

---

# 37. Manual de instalação

Criar:

```text
docs/INSTALACAO_FASE_2.md
```

Explicar:

1. estrutura do ambiente;
2. vínculo da planilha;
3. função do `clasp`;
4. como executar `setupSOEA()`;
5. quais permissões o Google solicita;
6. como abrir a planilha;
7. como recarregar;
8. como verificar o menu;
9. como abrir as Sidebars;
10. como executar a integridade;
11. como criar backup;
12. como executar novamente o setup;
13. como interpretar mensagens;
14. como relatar problemas.

Embora o Codex execute autonomamente essas tarefas, o documento deverá permitir reinstalação futura pelo Product Owner.

---

# 38. Documento de testes

Criar:

```text
docs/TESTES_FASE_2.md
```

Registrar para cada teste:

* identificador;
* data;
* ambiente;
* pré-condições;
* passos;
* resultado esperado;
* resultado obtido;
* status;
* evidência;
* correções realizadas;
* teste de regressão.

Status permitidos:

```text
Aprovado
Reprovado
Bloqueado
Pendente do Product Owner
Não aplicável
```

Com o ambiente `PRONTO_COMPLETO`, testes técnicos não deverão ser classificados como pendentes do Product Owner.

---

# 39. Validação local antes do envio

Antes de `clasp push`, verificar:

* sintaxe;
* chaves;
* parênteses;
* nomes de funções;
* funções duplicadas;
* funções do menu;
* constantes;
* includes HTML;
* arquivos inexistentes;
* referências circulares;
* HTML inválido;
* JSON do manifesto;
* ausência de credenciais.

Utilizar ferramentas locais disponíveis.

Não enviar código sabidamente inválido.

---

# 40. Primeiro envio ao Apps Script

Dentro de `apps-script/`, executar:

```bash
clasp status
```

Depois:

```bash
clasp push
```

Caso utilize instalação local:

```bash
npx clasp status
npx clasp push
```

Confirmar pelo terminal:

* arquivos reconhecidos;
* envio concluído;
* ausência de erro;
* projeto correto.

Não considerar a implantação concluída apenas pelo retorno do `clasp`.

---

# 41. Execução real do setup

Abrir o projeto remoto:

```bash
clasp open-script
```

ou:

```bash
npx clasp open-script
```

No editor do Apps Script:

1. confirmar os arquivos;
2. selecionar `setupSOEA`;
3. executar;
4. lidar com autorização oficial do Google;
5. solicitar intervenção humana somente para segurança;
6. aguardar a conclusão;
7. consultar o resultado;
8. consultar logs;
9. confirmar ausência de erro.

Depois, abrir a planilha real vinculada.

---

# 42. Validação visual obrigatória

Na planilha, verificar visualmente:

* nome da planilha;
* abas visíveis;
* abas ocultas;
* ordem das abas;
* cabeçalhos;
* títulos;
* larguras;
* alturas;
* formatação;
* filtros;
* validações;
* proteção;
* dados importados;
* Dashboard;
* Configurações;
* estados vazios.

Confirmar as quantidades reais de:

* disciplinas;
* assuntos;
* configurações.

Comparar com os arquivos da Fase 1.

---

# 43. Teste do menu

Recarregar a planilha.

Confirmar que o menu `SOEA` aparece.

Testar todos os itens:

* Continuar Ciclo;
* Aproveitar Tempo;
* Registrar Questões;
* Registrar Erro;
* Registrar Simulado;
* Atualizar Dashboard;
* Configurações;
* Verificar Integridade;
* Criar Backup;
* Ajuda;
* Sobre.

Confirmar que:

* nenhum item chama função inexistente;
* nenhuma ação gera erro técnico;
* funcionalidades futuras mostram mensagem adequada;
* funcionalidades desta fase funcionam.

---

# 44. Teste das Sidebars

Abrir cada Sidebar.

Verificar:

* renderização;
* CSS;
* títulos;
* campos;
* botões;
* cancelamento;
* mensagens;
* carregamento;
* validação;
* tratamento de erro;
* ausência de dependência externa.

Testar funcionalmente:

* Configurações;
* Ajuda;
* Sobre.

Testar estruturalmente:

* sessão;
* Aproveitar Tempo;
* questões;
* erros;
* revisões;
* simulados.

Não registrar dados fictícios permanentes.

---

# 45. Teste de importação

Confirmar:

* quantidade de disciplinas;
* quantidade de assuntos;
* quantidade de configurações;
* IDs;
* nomes;
* acentos;
* textos;
* relacionamentos;
* cobertura;
* ausência de duplicidade.

Comparar:

```text
CSV
↓
SeedData.gs
↓
Abas ocultas
```

As três etapas deverão possuir valores compatíveis.

---

# 46. Teste de reinstalação

Executar novamente:

```javascript
setupSOEA()
```

Confirmar:

* nenhuma aba duplicada;
* nenhum cabeçalho duplicado;
* nenhuma disciplina duplicada;
* nenhum assunto duplicado;
* nenhuma configuração duplicada;
* valores editáveis preservados;
* dados existentes preservados;
* menu preservado;
* proteções preservadas;
* ausência de erro.

Este teste é obrigatório.

Não declarar idempotência apenas pela leitura do código.

---

# 47. Teste de alteração de configuração

Pela Sidebar ou aba de Configurações:

1. alterar uma configuração editável de teste;
2. salvar;
3. confirmar em `_db_Config`;
4. confirmar na interface;
5. recarregar a planilha;
6. confirmar persistência;
7. executar novamente o setup;
8. confirmar que o valor não foi sobrescrito;
9. restaurar o valor correto.

Não alterar a data da prova permanentemente durante o teste.

---

# 48. Teste do Dashboard

Executar:

```javascript
atualizarDashboardSOEA()
```

Confirmar:

* dias até a prova;
* disciplinas;
* assuntos;
* estados vazios;
* ausência de valores fictícios;
* ausência de erros;
* ausência de `#N/A`;
* ausência de `#REF!`;
* formatação adequada.

---

# 49. Teste de integridade

Executar:

```javascript
verificarIntegridadeSOEA()
```

Confirmar:

* relatório gerado;
* verificações estruturais;
* classificações;
* ausência de falso positivo crítico;
* mensagem compreensível;
* registro em histórico;
* registro técnico quando necessário.

---

# 50. Teste de backup

Executar:

```javascript
criarBackupSOEA()
```

Confirmar:

* registro criado;
* ID único;
* data;
* tipo;
* motivo;
* versão;
* dados estruturais;
* ausência de duplicidade indevida;
* histórico atualizado.

---

# 51. Ciclo autônomo de correção

Quando um teste falhar:

```text
Registrar falha
↓
Identificar causa
↓
Corrigir arquivos locais
↓
Validar localmente
↓
Executar clasp push
↓
Executar novamente no Apps Script
↓
Reabrir ou recarregar a planilha
↓
Repetir o teste
↓
Executar regressão relacionada
↓
Atualizar TESTES_FASE_2.md
```

Não solicitar ao Product Owner que corrija o código.

Não encerrar a fase com erro técnico que possa ser corrigido pelo Codex.

---

# 52. Intervenções humanas permitidas

Solicitar intervenção somente para:

* escolher conta Google;
* digitar senha;
* autenticação em dois fatores;
* CAPTCHA;
* aprovar OAuth;
* confirmar uma permissão sensível;
* decidir entre projetos ou planilhas;
* autorizar uma ação com risco real de perda de dados;
* avaliar visualmente gosto ou preferência pessoal.

Não solicitar que o Product Owner:

* execute `setupSOEA`;
* abra Sidebars;
* copie arquivos;
* execute `clasp`;
* procure logs;
* teste idempotência;
* corrija código;
* crie abas;
* configure cabeçalhos.

Essas tarefas são do Codex.

---

# 53. Critérios de aceite técnico

A Fase 2 somente poderá ser apresentada para revisão quando:

* ambiente estiver `PRONTO_COMPLETO`;
* arquivos da arquitetura existirem;
* manifesto estiver válido;
* `SeedData.gs` estiver validado;
* `setupSOEA()` estiver implementado;
* `clasp push` tiver sido executado;
* setup tiver sido executado na planilha real;
* todas as abas tiverem sido criadas;
* cabeçalhos tiverem sido validados;
* dados tiverem sido importados;
* proteções tiverem sido aplicadas;
* menu tiver sido validado;
* Sidebars tiverem sido abertas;
* Configurações estiver funcional;
* Dashboard estrutural estiver funcional;
* integridade estrutural estiver funcional;
* backup estrutural estiver funcional;
* segunda execução do setup tiver sido testada;
* idempotência tiver sido confirmada;
* testes reprovados tiverem sido corrigidos ou classificados como bloqueios reais;
* documentação tiver sido atualizada;
* nenhuma funcionalidade da Fase 3 tiver sido falsamente declarada como concluída.

---

# 54. Atualização do ROADMAP

Atualizar `docs/ROADMAP.md`.

Registrar:

* percentual da Fase 2;
* estrutura criada;
* implantação real;
* testes executados;
* correções;
* bloqueios;
* itens pendentes de avaliação do Product Owner;
* próximo marco.

Não marcar a Fase 2 como aprovada.

Utilizar estado semelhante a:

```text
Fase 2 — 100% implementada e testada

Status — Aguardando revisão do Product Owner
```

---

# 55. Atualização do TODO

Atualizar `docs/TODO.md`.

Marcar somente tarefas realmente executadas.

Registrar:

* arquivos criados;
* setup;
* implantação;
* abas;
* importação;
* menu;
* Sidebars;
* Dashboard;
* Configurações;
* integridade;
* backup;
* reinstalação;
* testes;
* bugs;
* correções;
* bloqueios.

Não iniciar tarefas da Fase 3.

Testes técnicos executados pelo Codex não deverão permanecer como pendentes.

---

# 56. Atualização do CHANGELOG

Preparar em `docs/CHANGELOG.md`:

```text
## [0.2.0] — AAAA-MM-DD
```

Registrar:

## Adicionado

* arquivos `.gs`;
* arquivos `.html`;
* manifesto;
* setup;
* abas;
* cabeçalhos;
* seeds;
* menu;
* Sidebars;
* Dashboard estrutural;
* Configurações;
* integridade;
* backup;
* documentação de instalação;
* testes.

## Alterado

* estrutura remota do Apps Script;
* planilha vinculada;
* configuração do ambiente, quando aplicável.

## Corrigido

* bugs encontrados durante a implantação;
* problemas de importação;
* problemas de interface;
* problemas de idempotência.

## Conhecido

* funcionalidades ainda destinadas às Fases 3 e 4;
* limitações reais.

A versão deverá permanecer aguardando aprovação.

---

# 57. Atualização do REVIEW

Criar ou atualizar em `docs/REVIEW.md`:

```text
REVISÃO DA FASE 2 — ESTRUTURA DO GOOGLE SHEETS
```

Incluir:

* objetivo;
* ambiente utilizado;
* projeto Apps Script;
* planilha vinculada;
* entregas;
* arquivos criados;
* arquivos alterados;
* total de disciplinas;
* total de assuntos;
* total de configurações;
* implantação executada;
* testes executados;
* testes aprovados;
* testes reprovados;
* correções;
* bugs;
* limitações;
* evidências;
* pontos para avaliação do Product Owner;
* critérios de aceite;
* status.

Não incluir tokens, credenciais ou conteúdo sensível.

---

# 58. Pontos para revisão do Product Owner

O Product Owner deverá avaliar principalmente:

* aparência geral;
* legibilidade;
* organização das abas;
* clareza dos títulos;
* clareza das Sidebars;
* facilidade de localizar o menu;
* clareza das mensagens;
* organização do Dashboard;
* organização das Configurações.

O Product Owner não deverá precisar executar novamente todos os testes técnicos já concluídos.

---

# 59. Saída final no chat

Ao concluir, responder:

```text
Fase 2 executada.

Ambiente:
- status PRONTO_COMPLETO;
- planilha vinculada validada;
- projeto Apps Script validado.

Implantação:
- arquivos enviados com clasp;
- setupSOEA executado;
- planilha real validada;
- segunda execução do setup realizada.

Estrutura criada:
- abas visíveis;
- abas ocultas;
- cabeçalhos;
- dados;
- menu;
- Sidebars;
- Dashboard;
- Configurações;
- integridade;
- backup.

Dados importados:
- disciplinas: quantidade;
- assuntos: quantidade;
- configurações: quantidade.

Testes:
- aprovados: quantidade;
- reprovados: quantidade;
- bloqueados: quantidade.

Bugs corrigidos:
- lista ou “Nenhum”.

Limitações:
- lista ou “Nenhuma limitação impeditiva”.

Documentação atualizada:
- INSTALACAO_FASE_2.md;
- TESTES_FASE_2.md;
- ROADMAP.md;
- TODO.md;
- CHANGELOG.md;
- REVIEW.md.

O Motor Adaptativo não foi implementado.
A Fase 3 não foi iniciada.

Aguardando revisão do Product Owner.
```

Não iniciar a Fase 3.

Não executar tarefas futuras.

Não declarar a Fase 2 aprovada.

Aguardar aprovação explícita do Product Owner.
