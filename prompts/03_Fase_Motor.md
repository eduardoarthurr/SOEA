# PROMPT 03 — FASE 3: MOTOR DO SOEA

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
* `docs/INSTALACAO_FASE_2.md`
* `docs/TESTES_FASE_2.md`

Leia também todos os arquivos existentes nas pastas:

```text
analises/
dados/
fontes/
apps-script/
```

Confirme no `ROADMAP.md`, no `TODO.md` e no `REVIEW.md` que:

1. a Fase 2 foi executada;
2. a estrutura do Google Sheets foi implantada na planilha real;
3. o `setupSOEA()` foi executado;
4. a segunda execução do setup foi testada;
5. a idempotência estrutural foi confirmada;
6. as abas, cabeçalhos, menu e Sidebars foram validados;
7. os bugs críticos e altos da Fase 2 foram corrigidos;
8. o Product Owner aprovou explicitamente a Fase 2;
9. a fase atual é a Fase 3.

A aprovação deverá estar registrada de forma equivalente a:

```text
Fase 2 aprovada.

Pode iniciar a Fase 3.
```

Caso a Fase 2 não esteja aprovada:

1. não execute esta fase;
2. registre o bloqueio no `REVIEW.md`;
3. preserve todos os arquivos e dados;
4. informe o Product Owner;
5. pare.

---

# 2. Verificação obrigatória do ambiente autônomo

Leia o status registrado em:

```text
docs/AMBIENTE_AUTONOMO.md
```

A Fase 3 somente poderá continuar quando o status for:

```text
PRONTO_COMPLETO
```

Confirme que estão realmente funcionais:

* Node.js compatível;
* npm;
* `clasp`;
* autenticação do `clasp`;
* API do Google Apps Script;
* projeto Apps Script correto;
* planilha Google Sheets vinculada;
* arquivo `.clasp.json`;
* envio com `clasp push`;
* Chrome conectado;
* acesso ao editor do Apps Script;
* acesso à planilha real;
* execução remota de funções;
* Computer Use ou ferramenta visual equivalente.

Execute uma verificação curta:

```bash
node --version
npm --version
clasp --version
```

Caso o `clasp` esteja instalado localmente:

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

Confirme que o projeto remoto e a planilha vinculada são os mesmos aprovados na Fase 2.

Caso o ambiente não esteja `PRONTO_COMPLETO`:

1. não entregue somente arquivos locais;
2. não declare a fase como executada;
3. tente corrigir autonomamente;
4. solicite intervenção humana apenas para autenticação, segurança ou decisão pessoal;
5. continue após a intervenção;
6. só prossiga quando o ambiente voltar a `PRONTO_COMPLETO`.

---

# 3. Objetivo da fase

Implementar, implantar e testar o Motor do SOEA.

Ao final desta fase, a planilha real deverá ser capaz de:

* criar e manter um ciclo ativo;
* selecionar o próximo assunto;
* criar blocos de estudo;
* iniciar sessões;
* interromper sessões;
* retomar sessões;
* preservar progresso parcial;
* executar Continuar Ciclo;
* executar Retomar Ciclo;
* executar Aproveitar Tempo;
* ajustar a carga conforme tempo e energia;
* ativar Modo Emergência;
* registrar questões;
* registrar erros;
* concluir blocos;
* criar revisões automáticas;
* realizar revisões;
* calcular Índice de Prioridade;
* calcular Índice de Domínio;
* estimar tempos com base no histórico;
* atualizar métricas;
* atualizar o Dashboard;
* atualizar a aba Ciclo;
* registrar histórico;
* registrar logs;
* verificar integridade;
* recuperar estados inconsistentes;
* criar backups antes de operações críticas.

Não será suficiente escrever o código.

O fluxo obrigatório será:

```text
Implementar localmente
↓
Validar localmente
↓
Executar clasp push
↓
Executar na planilha real
↓
Criar dados controlados de teste
↓
Testar os fluxos
↓
Corrigir os problemas
↓
Executar novo clasp push
↓
Repetir os testes
↓
Executar testes de regressão
↓
Limpar os dados de teste
↓
Atualizar a documentação
```

---

# 4. Limites da Fase 3

Implementar completamente nesta fase:

* IDs únicos;
* ciclo;
* blocos;
* etapas;
* sessões;
* Continuar Ciclo;
* Retomar Ciclo;
* Aproveitar Tempo;
* Barra de Energia;
* Modo Emergência;
* registro de questões;
* Banco de Erros;
* conclusão de bloco;
* revisões;
* Índice de Prioridade;
* Índice de Domínio;
* Tempo Estimado Inteligente;
* métricas funcionais;
* Dashboard funcional básico;
* aba Ciclo funcional;
* histórico;
* logs;
* integridade avançada;
* recuperação de estado;
* backup de operações críticas;
* testes reais;
* documentação das fórmulas;
* documentação dos testes.

Não finalizar nesta fase:

* agenda definitiva de simulados;
* análise detalhada dos simulados;
* Dashboard visual definitivo;
* todos os gráficos finais;
* Estatísticas finais;
* refinamentos estéticos finais;
* testes finais de instalação da versão 1.0;
* README definitivo;
* preparação da versão estável `1.0.0`.

Esses itens pertencem à Fase 4.

---

# 5. Preservação do projeto existente

Não reconstruir o projeto do zero.

Antes de alterar qualquer arquivo:

1. analisar a implementação da Fase 2;
2. identificar os componentes já funcionais;
3. preservar a arquitetura aprovada;
4. preservar a planilha vinculada;
5. preservar disciplinas;
6. preservar assuntos;
7. preservar configurações;
8. preservar IDs existentes;
9. preservar proteções;
10. preservar formatações;
11. preservar histórico;
12. preservar backups.

Não alterar:

* `docs/PRD.md`;
* `docs/ARQUITETURA.md`;
* `docs/INSTRUCOES.md`;
* dados oficiais do edital;
* nomes oficiais das disciplinas;
* textos oficiais dos assuntos;
* valores aprovados na Fase 1.

Caso seja necessária uma alteração estrutural:

1. identificar o motivo;
2. criar backup;
3. planejar migração;
4. adicionar somente campos ausentes;
5. preservar os dados existentes;
6. atualizar o `Setup.gs`;
7. testar instalação nova;
8. testar atualização da planilha existente;
9. documentar a alteração.

---

# 6. Cópia de teste e proteção dos dados reais

Antes dos testes do Motor, preferir uma cópia controlada da planilha.

A estratégia recomendada é:

```text
Planilha principal do SOEA
↓
Criar cópia de teste
↓
Executar implementação e testes
↓
Corrigir
↓
Validar regressão
↓
Enviar versão estável ao projeto principal
```

Caso a arquitetura do projeto utilize um único projeto Apps Script vinculado:

* criar uma cópia segura antes dos testes destrutivos;
* utilizar registros identificados como teste;
* não alterar dados oficiais;
* não limpar registros que não estejam marcados como teste.

Todo dado de teste deverá possuir identificação clara, por exemplo:

```text
origem = TESTE_FASE_3
```

ou:

```text
is_test = true
```

Caso o modelo de dados não possua campo de origem:

1. utilizar observação padronizada;
2. utilizar IDs ou prefixos de teste;
3. documentar a estratégia;
4. não alterar a arquitetura silenciosamente.

Antes de operações críticas:

* criar backup;
* registrar o motivo;
* registrar a versão;
* confirmar a planilha utilizada.

---

# 7. Revisão inicial da implementação

Antes de programar, revisar:

* `Main.gs`;
* `Setup.gs`;
* `Constants.gs`;
* `SeedData.gs`;
* `Repository.gs`;
* `MenuController.gs`;
* `SidebarController.gs`;
* `SoeaEngine.gs`;
* todos os serviços;
* todas as Sidebars;
* `appsscript.json`.

Verificar:

* funções vazias;
* respostas `FEATURE_NOT_AVAILABLE`;
* funções associadas ao menu;
* cabeçalhos atuais;
* formato dos registros;
* constantes;
* validações;
* logs;
* backups;
* configurações;
* limitações registradas na Fase 2.

Criar um plano interno de implementação coerente com o `TODO.md`.

Não criar uma arquitetura paralela.

---

# 8. Estados oficiais do domínio

Centralizar em `Constants.gs` os estados utilizados.

Utilizar os nomes definidos no PRD.

Quando o PRD não definir o texto exato, utilizar convenção consistente em maiúsculas e sem acentos.

## Ciclo

```text
PLANEJADO
ATIVO
CONCLUIDO
ARQUIVADO
```

Deverá existir no máximo um ciclo `ATIVO`.

## Bloco

```text
PENDENTE
EM_ANDAMENTO
PAUSADO
CONCLUIDO
CANCELADO
```

Deverá existir no máximo um bloco principal com status `EM_ANDAMENTO` ou `PAUSADO`.

## Sessão

```text
ABERTA
PAUSADA
CONCLUIDA
CANCELADA
RECUPERADA
```

Deverá existir no máximo uma sessão `ABERTA`.

## Revisão

```text
PENDENTE
ATRASADA
EM_ANDAMENTO
CONCLUIDA
CANCELADA
```

## Erro

```text
NOVO
EM_REVISAO
REVISADO
RESOLVIDO
```

## Etapa de bloco

Utilizar etapas compatíveis com o PRD, como:

```text
TEORIA
QUESTOES
CORRECAO
BANCO_DE_ERROS
CONCLUSAO
```

Não espalhar valores de status diretamente pelo código.

---

# 9. IDs únicos

Implementar ou concluir `IdService.gs`.

Formatos:

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
```

Regras:

* utilizar `LockService`;
* consultar os IDs existentes;
* não depender somente da última linha;
* não reutilizar IDs apagados;
* suportar linhas vazias;
* validar o prefixo;
* validar a quantidade de dígitos;
* impedir duplicidade;
* liberar o lock em `finally`;
* registrar falhas no log técnico.

Não alterar IDs de disciplinas e assuntos.

Criar testes para:

* primeiro ID;
* IDs sequenciais;
* linhas apagadas;
* registros fora de ordem;
* clique duplicado;
* chamadas simultâneas.

---

# 10. Operações críticas

Utilizar `LockService` em:

* criação de ciclo;
* criação de bloco;
* criação de sessão;
* geração de IDs;
* conclusão de bloco;
* criação de revisões;
* atualização global de métricas;
* recuperação;
* backup;
* migração estrutural;
* limpeza de dados de teste.

Fluxo:

```text
Adquirir lock
↓
Validar estado
↓
Criar backup quando necessário
↓
Preparar alterações
↓
Executar escrita em lote
↓
Validar resultado
↓
Registrar histórico
↓
Liberar lock
```

Não manter o lock durante interações longas com o usuário.

---

# 11. Ciclo ativo

Implementar em `CycleService.gs` funções equivalentes a:

```javascript
getActiveCycle()
createInitialCycle()
ensureActiveCycle()
updateCycleProgress()
completeCycle()
validateSingleActiveCycle()
```

O primeiro ciclo deverá utilizar:

```text
CYC-001
```

O ciclo deverá registrar:

* ID;
* status;
* data de criação;
* data de início;
* data de conclusão;
* quantidade total de assuntos;
* quantidade iniciada;
* quantidade concluída;
* quantidade de blocos;
* progresso;
* observação.

Regras:

* criar somente quando não houver ciclo ativo;
* não recriar a cada sessão;
* não apagar durante setup;
* não criar dois ciclos ativos;
* preservar ciclos concluídos;
* atualizar progresso com dados reais.

Caso existam dois ciclos ativos:

1. bloquear criação de bloco;
2. registrar erro crítico;
3. criar backup;
4. executar verificação de integridade;
5. não escolher um ciclo silenciosamente.

---

# 12. Estrutura dos blocos

O bloco deverá representar uma unidade de estudo vinculada a:

* ciclo;
* disciplina;
* assunto.

Campos mínimos:

* ID;
* ID do ciclo;
* ID da disciplina;
* ID do assunto;
* tipo;
* origem;
* status;
* etapa atual;
* data de criação;
* data de início;
* data de conclusão;
* tempo previsto;
* tempo realizado;
* quantidade prevista de questões;
* quantidade realizada;
* prioridade no momento da criação;
* progresso;
* observação.

O PRD permanece como fonte oficial dos cabeçalhos.

Implementar em `BlockService.gs` funções equivalentes a:

```javascript
getActiveBlock()
createBlock()
resumeBlock()
pauseBlock()
updateBlockProgress()
completeBlock()
validateSingleActiveBlock()
getNextBlockStep()
```

---

# 13. Etapas do bloco

Fluxo principal:

```text
Teoria
↓
Questões
↓
Correção
↓
Banco de Erros
↓
Conclusão
↓
Revisões
```

Nem todas as etapas precisam ocorrer na mesma sessão.

Cada etapa deverá registrar ou permitir calcular:

* status;
* tempo previsto;
* tempo realizado;
* quantidade prevista;
* quantidade realizada;
* data de início;
* data de conclusão.

A etapa atual deverá ser calculada pelos dados persistidos.

Não depender somente da Sidebar aberta.

Não marcar etapa como concluída apenas porque a sessão terminou.

---

# 14. Progresso parcial

O sistema deverá preservar o progresso parcial.

Exemplo:

```text
Teoria prevista: 60 minutos
Teoria realizada: 25 minutos
Tempo restante: 35 minutos
```

Resultado:

* bloco permanece em andamento;
* sessão é encerrada;
* etapa continua como teoria;
* próxima sessão retoma os 35 minutos restantes.

Não:

* reiniciar a etapa;
* duplicar tempo;
* considerar a etapa concluída;
* criar novo bloco.

O progresso deverá ser calculado de forma coerente com as etapas.

Documentar o método utilizado em `FORMULAS_SOEA.md`.

---

# 15. Sessões

Implementar em `SessionService.gs` funções equivalentes a:

```javascript
getOpenSession()
createSession()
pauseSession()
completeSession()
cancelSession()
recoverOrphanSession()
validateSingleOpenSession()
calculateSessionDuration()
```

Campos mínimos:

* ID;
* ID do bloco;
* tipo;
* origem;
* tempo disponível;
* energia;
* horário inicial;
* horário final;
* duração real;
* status;
* progresso realizado;
* observação;
* identificação de teste, quando aplicável.

Regras:

* um bloco poderá possuir várias sessões;
* uma sessão encerrada não conclui automaticamente o bloco;
* no máximo uma sessão poderá estar aberta;
* a duração deverá ser calculada com dados reais;
* tempos negativos deverão ser rejeitados;
* sessões órfãs deverão ser detectadas.

---

# 16. Fluxo Continuar Ciclo

Implementar o item:

```text
SOEA → Continuar Ciclo
```

Criar ou utilizar função pública:

```javascript
continuarCicloSOEA()
```

Fluxo:

```text
Usuário seleciona Continuar Ciclo
↓
Validar integridade mínima
↓
Garantir ciclo ativo
↓
Verificar sessão aberta
↓
Verificar bloco ativo
↓
Solicitar tempo disponível
↓
Solicitar energia
↓
Calcular carga
↓
Retomar bloco ou selecionar assunto
↓
Apresentar atividade
↓
Solicitar confirmação
↓
Criar sessão
↓
Iniciar atividade
```

Não criar a sessão antes da confirmação final.

A Sidebar deverá mostrar:

* disciplina;
* assunto;
* etapa;
* justificativa;
* tempo estimado;
* quantidade de questões;
* energia;
* progresso atual;
* botão iniciar;
* botão cancelar.

---

# 17. Retomar Ciclo

Quando existir bloco incompleto:

* carregar o mesmo bloco;
* carregar a mesma disciplina;
* carregar o mesmo assunto;
* identificar a etapa;
* identificar o progresso;
* calcular o restante;
* adaptar ao tempo disponível;
* não criar novo bloco;
* não repetir etapa concluída;
* preservar o histórico;
* informar o ponto de retomada.

Exemplo:

```text
Você possui um bloco em andamento.

Disciplina: Banco de Dados
Assunto: Normalização
Etapa: Teoria
Realizado: 25 de 60 minutos
Restante estimado: 35 minutos
```

Se houver sessão aberta válida, o sistema deverá oferecer retomada da sessão ou recuperação segura.

---

# 18. Seleção do próximo assunto

Implementar no `SoeaEngine.gs`.

Ordem de decisão:

```text
1. Sessão aberta válida
2. Bloco ativo ou pausado
3. Revisão prioritária
4. Assunto pelo Índice de Prioridade
5. Criação de novo bloco
```

Regras:

* não criar bloco quando houver bloco retomável;
* não selecionar assunto inativo;
* respeitar assuntos bloqueados;
* considerar peso;
* considerar domínio;
* considerar revisões;
* considerar erros;
* considerar tempo sem contato;
* considerar quantidade de questões;
* considerar proximidade da prova;
* considerar frequência mínima;
* evitar repetição excessiva da mesma disciplina;
* registrar a justificativa.

Retornar objeto estruturado:

```javascript
{
  success: true,
  action: 'RESUME_BLOCK',
  reason: 'Existe um bloco em andamento.',
  cycleId: 'CYC-001',
  blockId: 'BLK-000001',
  disciplineId: 'DSC-001',
  subjectId: 'ASU-0001'
}
```

Não retornar somente textos soltos.

---

# 19. Criação de blocos

Ao criar bloco:

* associar ao ciclo;
* associar à disciplina;
* associar ao assunto;
* registrar origem;
* registrar prioridade;
* registrar domínio;
* registrar tempo previsto;
* registrar questões previstas;
* definir etapa inicial;
* validar ausência de bloco ativo;
* registrar histórico;
* atualizar aba Ciclo;
* atualizar Dashboard.

A criação deverá ser idempotente para a mesma operação.

Clique repetido não poderá criar dois blocos.

---

# 20. Fluxo Aproveitar Tempo

Implementar:

```text
SOEA → Aproveitar Tempo
```

Criar ou utilizar função:

```javascript
aproveitarTempoSOEA()
```

Solicitar:

* tempo disponível;
* objetivo;
* energia, quando necessário.

Objetivos:

```text
QUESTOES
REVISAO
BANCO_DE_ERROS
TANTO_FAZ
```

Ordem de decisão:

1. etapa compatível do bloco atual;
2. revisão pendente compatível;
3. erros pendentes;
4. questões de assunto prioritário;
5. melhor atividade compatível.

Regras:

* não criar ciclo paralelo;
* não criar dois blocos principais;
* não apagar progresso;
* não reiniciar etapa;
* não criar tarefa maior que o tempo disponível;
* não concluir atividade incompleta;
* registrar origem `APROVEITAR_TEMPO`;
* vincular ao ciclo;
* atualizar o progresso imediatamente.

Caso conclua o bloco:

* marcar como concluído;
* criar revisões;
* atualizar domínio;
* atualizar prioridade;
* atualizar métricas;
* atualizar Dashboard;
* permitir avanço no próximo Continuar Ciclo.

---

# 21. Barra de Energia

Implementar os níveis definidos no PRD:

```text
Excelente
Boa
Cansado
Muito cansado
```

## Excelente

Poderá permitir:

* teoria mais longa;
* maior volume de questões;
* conteúdo novo;
* assunto complexo.

## Boa

Utilizar carga normal.

## Cansado

Priorizar:

* bloco menor;
* questões reduzidas;
* correção;
* revisão;
* Banco de Erros.

## Muito cansado

Priorizar:

* Modo Emergência;
* revisão curta;
* poucos erros;
* pequeno lote de questões;
* continuação de etapa curta.

A energia deverá ajustar a carga.

Não deverá:

* cancelar automaticamente o estudo;
* considerar atividade como concluída;
* registrar tempo inexistente.

---

# 22. Modo Emergência

Ativar quando:

* o tempo estiver abaixo do limite configurado;
* a energia estiver muito baixa;
* a combinação tempo e energia impedir um bloco normal.

Atividades permitidas:

* revisar poucos erros;
* resolver pequeno lote de questões;
* concluir parte de etapa;
* realizar revisão curta;
* corrigir questões pendentes.

Não deverá:

* concluir bloco inteiro sem execução;
* criar dados fictícios;
* ignorar revisão urgente compatível;
* criar ciclo separado;
* apagar progresso.

Os parâmetros deverão vir de `_db_Config`.

---

# 23. Início e encerramento da sessão

Ao iniciar:

* validar payload;
* validar bloco;
* validar sessão aberta;
* adquirir lock;
* criar ID;
* registrar horário;
* registrar energia;
* registrar tempo disponível;
* atualizar bloco;
* registrar histórico;
* retornar resposta estruturada.

Ao encerrar:

* registrar horário final;
* calcular duração;
* solicitar apenas resultados necessários;
* atualizar progresso;
* concluir ou pausar etapa;
* atualizar bloco;
* atualizar métricas;
* atualizar Dashboard;
* registrar histórico;
* retornar resumo.

Exemplo:

```text
Sessão concluída.

Tempo estudado: 42 minutos
Etapa: Questões
Questões realizadas: 20
Acertos: 15
Progresso do bloco: 70%

Seu progresso foi salvo.
```

---

# 24. Registro de questões

Implementar completamente `QuestionService.gs`.

Funções esperadas:

* abrir formulário;
* validar payload;
* registrar lote;
* consultar por bloco;
* consultar por disciplina;
* consultar por assunto;
* calcular desempenho;
* calcular tempo médio;
* atualizar métricas.

Campos mínimos:

* ID;
* data;
* bloco;
* sessão;
* disciplina;
* assunto;
* fonte;
* quantidade;
* acertos;
* erros;
* percentual;
* tempo total;
* tempo médio;
* tipo;
* observação;
* identificação de teste.

Validações:

* quantidade maior que zero;
* acertos maiores ou iguais a zero;
* acertos menores ou iguais à quantidade;
* erros calculados;
* percentual entre 0 e 100;
* tempo não negativo;
* bloco existente;
* sessão existente, quando obrigatória;
* disciplina existente;
* assunto existente.

Não armazenar enunciados completos protegidos.

---

# 25. Banco de Erros

Implementar completamente `ErrorBankService.gs`.

Preencher automaticamente:

* bloco;
* sessão;
* disciplina;
* assunto;
* data.

Solicitar:

* motivo;
* causa-raiz;
* observação;
* referência opcional;
* status inicial.

Utilizar as categorias aprovadas no PRD.

Implementar:

* criação;
* atualização;
* mudança de status;
* consulta;
* filtros;
* recorrência;
* seleção para revisão;
* vínculo com assunto;
* vínculo com bloco;
* impacto na prioridade;
* atualização da aba visível.

Não exigir que o usuário digite novamente informações já conhecidas.

---

# 26. Conclusão de bloco

Implementar como operação crítica.

Fluxo:

```text
Validar bloco
↓
Validar etapas
↓
Validar sessão
↓
Registrar resultados
↓
Atualizar tempos
↓
Atualizar questões
↓
Atualizar erros
↓
Marcar bloco concluído
↓
Criar revisões
↓
Atualizar assunto
↓
Recalcular domínio
↓
Recalcular prioridade
↓
Atualizar ciclo
↓
Atualizar métricas
↓
Atualizar Dashboard
↓
Registrar histórico
↓
Exibir resumo
```

Regras:

* não concluir com dados inválidos;
* não concluir duas vezes;
* não duplicar revisões;
* não perder resultados;
* não deixar sessão aberta;
* não criar novo bloco automaticamente sem confirmação.

---

# 27. Revisões automáticas

Implementar em `ReviewService.gs`.

Criar após a conclusão do bloco:

```text
D+1
D+7
D+15
D+30
```

Campos:

* ID;
* bloco de origem;
* disciplina;
* assunto;
* tipo;
* data prevista;
* status;
* data realizada;
* resultado;
* quantidade de questões;
* acertos;
* observação;
* identificação de teste.

Utilizar chave lógica:

```text
bloco de origem + tipo
```

para evitar duplicidade.

Atualizar para `ATRASADA` quando:

* a data prevista passou;
* não estiver concluída;
* não estiver cancelada.

---

# 28. Resultado das revisões

Aplicar:

## 90% ou mais

* concluir;
* considerar consolidada;
* não criar revisão extra;
* manter ou reduzir levemente prioridade.

## 70% a 89%

* concluir;
* aumentar levemente prioridade;
* manter revisões futuras.

## Abaixo de 70%

* marcar como não consolidada;
* aumentar prioridade;
* criar revisão extra;
* destacar assunto;
* considerar erros recorrentes.

O prazo da revisão extra deverá vir de `_db_Config`.

Caso a configuração não exista:

1. verificar PRD e documentos;
2. adicionar configuração documentada;
3. utilizar padrão apenas quando permitido;
4. manter valor editável;
5. registrar no `REVIEW.md`.

---

# 29. Índice de Prioridade

Implementar em `PriorityService.gs`.

Resultado:

```text
0 a 100
```

Considerar:

* peso da disciplina;
* baixo domínio;
* desempenho em questões;
* volume insuficiente de questões;
* erros pendentes;
* recorrência;
* revisões atrasadas;
* tempo desde o último contato;
* proximidade da prova;
* simulados, quando houver;
* frequência mínima.

Requisitos:

* pesos em `_db_Config`;
* pesos normalizados;
* resultado limitado;
* tratamento sem histórico;
* sem divisão por zero;
* justificativa da pontuação;
* cálculo reproduzível.

Retorno esperado:

```javascript
{
  subjectId: 'ASU-0001',
  priority: 82.5,
  components: {
    examWeight: 20,
    lowMastery: 25,
    overdueReviews: 15,
    pendingErrors: 12,
    timeWithoutContact: 10
  },
  reason: 'Baixo domínio e revisão atrasada.'
}
```

Os valores são ilustrativos.

---

# 30. Índice de Domínio

Implementar em `MasteryService.gs`.

Resultado:

```text
0 a 100
```

Classificação:

```text
0–59: Vermelho
60–79: Amarelo
80–100: Verde
```

Considerar:

* questões;
* volume de questões;
* revisões;
* erros recorrentes;
* simulados, quando houver;
* tempo sem contato;
* confiança da amostra.

Amostra pequena não poderá gerar domínio artificialmente alto.

Exemplo:

```text
1 questão
1 acerto

Resultado:
Não considerar domínio de 100%.
Aplicar baixa confiança.
```

A fórmula deverá ser:

* documentada;
* reproduzível;
* configurável;
* limitada;
* resistente a valores extremos.

---

# 31. Documento das fórmulas

Criar:

```text
docs/FORMULAS_SOEA.md
```

Documentar:

* fórmula de prioridade;
* componentes;
* pesos;
* normalização;
* tratamento sem histórico;
* exemplos;
* fórmula de domínio;
* confiança da amostra;
* cores;
* fórmula de progresso;
* estimativa de tempo;
* regras de energia;
* Modo Emergência;
* parâmetros editáveis.

O Product Owner deverá conseguir entender por que um assunto foi selecionado.

---

# 32. Tempo Estimado Inteligente

Implementar com:

1. valores padrão;
2. histórico real;
3. amostra mínima;
4. limites mínimos;
5. limites máximos;
6. tratamento de valores extremos.

Considerar:

* disciplina;
* assunto;
* etapa;
* tempo por questão;
* tempo de teoria;
* tempo de correção;
* tempo de revisão;
* energia;
* tempo disponível.

Preferir:

* mediana;
* média aparada;
* limite configurável.

Não permitir que um único registro distorça permanentemente as estimativas.

Documentar o método.

---

# 33. Métricas

Implementar em `MetricsService.gs`:

* horas totais;
* horas diárias;
* horas semanais;
* horas mensais;
* questões totais;
* questões diárias;
* questões semanais;
* questões mensais;
* acertos;
* erros;
* aproveitamento;
* blocos concluídos;
* assuntos iniciados;
* assuntos concluídos;
* revisões pendentes;
* revisões atrasadas;
* revisões concluídas;
* erros pendentes;
* percentual do edital;
* sequência de estudos;
* metas semanais.

Utilizar leitura e escrita em lote.

Não recalcular toda a planilha desnecessariamente.

---

# 34. Dashboard funcional

Atualizar `DashboardService.gs`.

Tornar funcionais:

* dias até a prova;
* ciclo ativo;
* bloco atual;
* etapa;
* horas totais;
* horas da semana;
* questões totais;
* questões da semana;
* aproveitamento;
* revisões pendentes;
* revisões atrasadas;
* erros pendentes;
* percentual do edital;
* sequência;
* próximo simulado, quando houver.

Os gráficos finais permanecem para a Fase 4.

Não exibir valores fictícios.

Utilizar:

```text
Ainda sem dados
```

quando necessário.

---

# 35. Aba Ciclo funcional

Atualizar a aba `Ciclo` com:

* ciclo ativo;
* bloco;
* disciplina;
* assunto;
* etapa;
* tempo previsto;
* tempo realizado;
* progresso;
* sessão;
* próxima revisão;
* justificativa da seleção;
* próxima ação.

Os dados deverão vir das abas ocultas.

A aba não deverá ser fonte oficial.

---

# 36. Histórico funcional

Implementar em `HistoryService.gs` registros para:

* ciclo criado;
* bloco criado;
* bloco iniciado;
* bloco pausado;
* bloco retomado;
* bloco concluído;
* sessão criada;
* sessão concluída;
* sessão recuperada;
* questões registradas;
* erro registrado;
* erro atualizado;
* revisão criada;
* revisão concluída;
* prioridade calculada;
* domínio calculado;
* backup criado;
* recuperação executada.

Campos:

* ID;
* data;
* tipo;
* entidade;
* ID da entidade;
* resumo;
* origem;
* resultado;
* indicação de teste.

Não armazenar stack trace no histórico funcional.

---

# 37. Logs técnicos

Registrar em `_db_Logs`:

* exceções;
* erros de validação;
* tentativas de duplicidade;
* falhas de escrita;
* aba ausente;
* cabeçalho incorreto;
* inconsistência;
* recuperação necessária.

Campos:

* data;
* nível;
* função;
* código;
* mensagem;
* contexto;
* ação sugerida.

Não exibir o log técnico completo ao usuário.

---

# 38. Integridade avançada

Expandir:

```javascript
verificarIntegridadeSOEA()
```

Verificar:

* abas;
* cabeçalhos;
* IDs duplicados;
* relacionamentos;
* ciclos ativos;
* blocos ativos;
* sessões abertas;
* sessões sem bloco;
* blocos sem ciclo;
* blocos sem assunto;
* assuntos sem disciplina;
* revisões sem bloco;
* revisões duplicadas;
* questões sem bloco;
* erros sem assunto;
* tempos negativos;
* percentuais inválidos;
* acertos maiores que questões;
* progresso inválido;
* configurações ausentes;
* configurações duplicadas.

Classificar:

```text
Aprovado
Aviso
Erro
Crítico
```

Não corrigir automaticamente problemas destrutivos.

---

# 39. Recuperação de estado

Implementar em `RecoveryService.gs`:

* detectar sessão antiga;
* detectar sessão órfã;
* localizar bloco ativo;
* reconstruir etapa;
* encerrar sessão órfã com segurança;
* preservar progresso;
* registrar recuperação;
* orientar o usuário.

Preferir:

```text
Preservar dados
```

em vez de:

```text
Apagar e recriar
```

Caso não seja possível decidir com segurança:

1. criar backup;
2. registrar bloqueio;
3. apresentar opções;
4. aguardar decisão.

---

# 40. Backup da Fase 3

Expandir `BackupService.gs`.

Criar backup antes de:

* migração;
* recuperação;
* correção de inconsistência;
* alteração em massa;
* limpeza de testes;
* restauração.

Registrar:

* ID;
* data;
* tipo;
* motivo;
* entidades;
* origem;
* versão.

Evitar backup excessivo.

Não declarar restauração automática quando não estiver validada.

---

# 41. Tratamento das Sidebars

Todas as Sidebars deverão:

* impedir clique repetido;
* desabilitar botões durante processamento;
* mostrar carregamento;
* tratar sucesso;
* tratar falha;
* preservar campos em caso de erro;
* não fechar antes da confirmação;
* exibir mensagens claras.

Exemplo:

```text
Não foi possível salvar esta sessão.

Seu bloco continua preservado.
Revise os dados e tente novamente.
```

---

# 42. Funções públicas

As funções de interface deverão ficar nos controladores.

Exemplos:

```javascript
continuarCicloSOEA()
aproveitarTempoSOEA()
iniciarSessaoSOEA(payload)
concluirSessaoSOEA(payload)
registrarQuestoesSOEA(payload)
registrarErroSOEA(payload)
concluirBlocoSOEA(payload)
realizarRevisaoSOEA(payload)
atualizarDashboardSOEA()
verificarIntegridadeSOEA()
criarBackupSOEA()
```

Retornar respostas estruturadas:

```javascript
{
  success: true,
  code: 'SESSION_CREATED',
  message: 'Sessão iniciada.',
  data: {}
}
```

Não colocar toda a regra de negócio nos controladores.

---

# 43. Testes auxiliares

Criar, caso seja útil:

```text
apps-script/TestRunner.gs
```

Utilizar para testes seguros de:

* percentuais;
* normalização;
* prioridade;
* domínio;
* datas;
* IDs;
* energia;
* tempo;
* payloads;
* decisões do Motor.

Não criar testes destrutivos.

Documentar a existência no `REVIEW.md`.

---

# 44. Documento de testes

Criar:

```text
docs/TESTES_FASE_3.md
```

Para cada teste, registrar:

* ID;
* data;
* ambiente;
* planilha utilizada;
* pré-condições;
* dados de teste;
* passos;
* resultado esperado;
* resultado obtido;
* status;
* evidência;
* correções;
* regressão;
* limpeza.

Status:

```text
Aprovado
Reprovado
Bloqueado
Pendente do Product Owner
Não aplicável
```

Com ambiente `PRONTO_COMPLETO`, testes técnicos não poderão ser classificados como pendentes do Product Owner.

---

# 45. Validação local antes do envio

Antes de `clasp push`, verificar:

* sintaxe;
* funções duplicadas;
* constantes;
* includes HTML;
* referências;
* nomes das funções públicas;
* menu;
* manifesto;
* ausência de credenciais;
* ausência de código morto evidente;
* respostas estruturadas.

Não enviar código sabidamente inválido.

---

# 46. Implantação inicial da Fase 3

Dentro de `apps-script/`, executar:

```bash
clasp status
clasp push
```

Ou:

```bash
npx clasp status
npx clasp push
```

Confirmar:

* projeto correto;
* arquivos reconhecidos;
* envio concluído;
* ausência de erros.

Depois:

```bash
clasp open-script
```

ou:

```bash
npx clasp open-script
```

Confirmar os arquivos no editor remoto.

---

# 47. Execução real

Executar no Apps Script as funções necessárias de:

* instalação ou migração;
* criação do ciclo;
* atualização do Dashboard;
* integridade;
* backup;
* testes auxiliares.

Abrir a planilha e validar os resultados reais.

Não considerar a função testada apenas porque não apresentou erro de sintaxe.

---

# 48. Testes obrigatórios

## Teste 1 — Criação do ciclo

Confirmar:

* `CYC-001`;
* status ativo;
* ausência de duplicidade;
* registro no histórico.

## Teste 2 — Continuar Ciclo sem bloco

Confirmar:

* tempo;
* energia;
* seleção;
* justificativa;
* bloco;
* sessão.

## Teste 3 — Interrupção na teoria

Realizar parte e confirmar:

* tempo parcial;
* sessão concluída;
* bloco ativo;
* etapa preservada.

## Teste 4 — Retomada

Confirmar:

* mesmo bloco;
* mesmo assunto;
* tempo restante;
* nenhuma repetição.

## Teste 5 — Questões

Registrar lote e confirmar:

* quantidade;
* acertos;
* erros;
* percentual;
* tempo médio;
* métricas.

## Teste 6 — Banco de Erros

Registrar erro e confirmar:

* bloco;
* sessão;
* assunto;
* status;
* prioridade.

## Teste 7 — Conclusão de bloco

Confirmar:

* bloco concluído;
* sessão encerrada;
* ciclo atualizado;
* métricas;
* Dashboard.

## Teste 8 — Revisões

Confirmar criação de:

* D+1;
* D+7;
* D+15;
* D+30.

Reexecutar conclusão e confirmar ausência de duplicidade.

## Teste 9 — Revisão com 95%

Confirmar consolidação.

## Teste 10 — Revisão com 80%

Confirmar ajuste leve de prioridade.

## Teste 11 — Revisão com 60%

Confirmar:

* não consolidação;
* aumento de prioridade;
* revisão extra.

## Teste 12 — Aproveitar Tempo parcial

Confirmar:

* atividade compatível;
* sessão;
* progresso;
* nenhum ciclo paralelo.

## Teste 13 — Aproveitar Tempo concluindo bloco

Confirmar:

* mesmo bloco concluído;
* revisões;
* próximo ciclo avança.

## Teste 14 — Energia muito baixa

Confirmar Modo Emergência.

## Teste 15 — Clique duplicado

Confirmar:

* um ID;
* um bloco;
* uma sessão;
* uma escrita.

## Teste 16 — Duas sessões abertas

Simular e confirmar bloqueio ou recuperação.

## Teste 17 — Dois blocos ativos

Simular e confirmar bloqueio.

## Teste 18 — Fechar e abrir

Confirmar persistência.

## Teste 19 — Outro computador ou nova sessão

Confirmar que o estado vem da planilha.

## Teste 20 — Dashboard

Confirmar indicadores reais.

## Teste 21 — Integridade

Confirmar relatório.

## Teste 22 — Backup

Confirmar registro.

## Teste 23 — Amostra pequena

Uma questão e um acerto não poderão gerar domínio integral.

## Teste 24 — Prioridade

Testar:

* revisão atrasada;
* baixo desempenho;
* erros recorrentes;
* tempo sem contato.

## Teste 25 — Idempotência do setup

Executar novamente e confirmar preservação do Motor e dos dados.

## Teste 26 — Atualização da versão existente

Confirmar que dados da Fase 2 foram preservados.

---

# 49. Ciclo autônomo de correção

Quando um teste falhar:

```text
Registrar falha
↓
Criar BUG
↓
Analisar causa
↓
Corrigir localmente
↓
Validar localmente
↓
Executar clasp push
↓
Executar na planilha
↓
Repetir o teste
↓
Executar regressão
↓
Atualizar TESTES_FASE_3.md
```

Não solicitar ao Product Owner que corrija código.

Não encerrar com fluxo principal reprovado.

---

# 50. Limpeza dos dados de teste

Após a validação:

1. identificar registros de teste;
2. criar backup;
3. remover somente registros marcados;
4. preservar disciplinas;
5. preservar assuntos;
6. preservar configurações;
7. preservar dados reais;
8. executar integridade;
9. atualizar Dashboard;
10. registrar a limpeza.

Não utilizar exclusão genérica.

Não apagar dados sem marcação de teste.

---

# 51. Intervenções humanas permitidas

Solicitar intervenção apenas para:

* autenticação;
* escolha de conta;
* CAPTCHA;
* OAuth;
* confirmação sensível;
* decisão de produto;
* risco de perda de dados;
* avaliação subjetiva de usabilidade.

Não solicitar que o Product Owner:

* execute funções técnicas;
* copie código;
* execute `clasp`;
* procure logs;
* teste duplicidade;
* crie dados técnicos;
* limpe dados;
* corrija erros;
* atualize documentos.

---

# 52. Critérios de aceite técnico

A Fase 3 somente poderá ser apresentada quando:

* ambiente estiver `PRONTO_COMPLETO`;
* ciclo estiver funcional;
* blocos estiverem funcionais;
* sessões estiverem funcionais;
* Continuar Ciclo estiver funcional;
* Retomar Ciclo estiver funcional;
* Aproveitar Tempo estiver funcional;
* energia ajustar a carga;
* Modo Emergência estiver funcional;
* progresso parcial estiver preservado;
* questões forem registradas;
* erros forem registrados;
* blocos forem concluídos;
* revisões forem criadas;
* revisões não forem duplicadas;
* prioridade for calculada;
* domínio for calculado;
* amostra pequena for tratada;
* métricas forem atualizadas;
* Dashboard usar dados reais;
* aba Ciclo estiver funcional;
* integridade avançada estiver funcional;
* recuperação estiver funcional;
* backup estiver funcional;
* locks estiverem aplicados;
* testes reais tiverem sido executados;
* bugs críticos tiverem sido corrigidos;
* bugs altos impeditivos tiverem sido corrigidos;
* dados de teste tiverem sido limpos;
* documentação tiver sido atualizada;
* a Fase 4 não tiver sido iniciada.

---

# 53. Atualização do ROADMAP

Atualizar `docs/ROADMAP.md`.

Registrar:

* percentual da Fase 3;
* funcionalidades;
* implantação real;
* testes;
* correções;
* bugs;
* limitações;
* próximo marco.

Não marcar como aprovada.

Utilizar:

```text
Fase 3 — 100% implementada e testada

Status — Aguardando revisão do Product Owner
```

---

# 54. Atualização do TODO

Atualizar `docs/TODO.md`.

Marcar somente tarefas executadas.

Registrar:

* ciclo;
* blocos;
* sessões;
* Continuar Ciclo;
* Retomar Ciclo;
* Aproveitar Tempo;
* energia;
* Modo Emergência;
* questões;
* erros;
* revisões;
* prioridade;
* domínio;
* métricas;
* Dashboard;
* integridade;
* recuperação;
* backup;
* implantação;
* testes;
* bugs;
* correções;
* limpeza dos dados de teste.

Não iniciar tarefas da Fase 4.

---

# 55. Atualização do CHANGELOG

Preparar:

```text
## [0.3.0] — AAAA-MM-DD
```

Registrar:

## Adicionado

* ciclo;
* blocos;
* sessões;
* Continuar Ciclo;
* Retomar Ciclo;
* Aproveitar Tempo;
* energia;
* Modo Emergência;
* questões;
* Banco de Erros;
* revisões;
* prioridade;
* domínio;
* tempo inteligente;
* métricas;
* integridade;
* recuperação;
* backups;
* testes.

## Alterado

* Sidebars;
* Dashboard;
* aba Ciclo;
* serviços;
* repositórios;
* configurações.

## Corrigido

* bugs;
* problemas de duplicidade;
* problemas de persistência;
* problemas de interface;
* problemas de métricas.

## Conhecido

* agenda de simulados;
* Dashboard final;
* Estatísticas finais;
* limitações reais.

A versão permanecerá aguardando aprovação.

---

# 56. Atualização do REVIEW

Criar ou atualizar:

```text
REVISÃO DA FASE 3 — MOTOR DO SOEA
```

Incluir:

* objetivo;
* ambiente;
* planilha;
* implantação;
* entregas;
* arquivos criados;
* arquivos alterados;
* funções públicas;
* fórmulas;
* testes;
* bugs;
* correções;
* limitações;
* dados de teste;
* limpeza;
* evidências;
* pontos para avaliação do Product Owner;
* critérios de aceite;
* status.

Não incluir credenciais.

---

# 57. Pontos para revisão do Product Owner

O Product Owner deverá avaliar principalmente:

* se a escolha dos assuntos parece coerente;
* se as justificativas são compreensíveis;
* se o fluxo é intuitivo;
* se as cargas de energia fazem sentido;
* se o Aproveitar Tempo atende ao uso real;
* se as mensagens são claras;
* se a quantidade de cliques é adequada;
* se o Dashboard é útil.

Os testes técnicos já executados pelo Codex não precisarão ser repetidos integralmente.

---

# 58. Saída final no chat

Ao concluir, responder:

```text
Fase 3 executada.

Ambiente:
- status PRONTO_COMPLETO;
- projeto Apps Script validado;
- planilha real validada.

Implantação:
- arquivos enviados com clasp;
- Motor executado na planilha;
- testes reais concluídos;
- correções reenviadas;
- regressões executadas.

Motor implementado:
- ciclo;
- blocos;
- sessões;
- Continuar Ciclo;
- Retomar Ciclo;
- Aproveitar Tempo;
- Barra de Energia;
- Modo Emergência;
- questões;
- Banco de Erros;
- revisões;
- prioridade;
- domínio;
- métricas;
- integridade;
- recuperação;
- backup.

Testes:
- aprovados: quantidade;
- reprovados: quantidade;
- bloqueados: quantidade.

Bugs corrigidos:
- lista ou “Nenhum”.

Dados de teste:
- estratégia utilizada;
- limpeza concluída;
- integridade após limpeza.

Limitações:
- lista ou “Nenhuma limitação impeditiva”.

Documentação atualizada:
- FORMULAS_SOEA.md;
- TESTES_FASE_3.md;
- ROADMAP.md;
- TODO.md;
- CHANGELOG.md;
- REVIEW.md.

A agenda definitiva de simulados e os refinamentos finais não foram implementados.
A Fase 4 não foi iniciada.

Aguardando revisão do Product Owner.
```

Não iniciar a Fase 4.

Não declarar a Fase 3 aprovada.

Não implementar tarefas futuras.

Aguardar aprovação explícita do Product Owner.
