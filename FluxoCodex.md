# FLUXO EXATO DE EXECUÇÃO DO PROJETO SOEA NO CODEX

## 1. Estrutura final do projeto

Antes de abrir o projeto no Codex, confirme que a pasta está organizada assim:

```text
SOEA/
├── docs/
│   ├── PRD.md
│   ├── ARQUITETURA.md
│   ├── INSTRUCOES.md
│   ├── ROADMAP.md
│   ├── TODO.md
│   ├── CHANGELOG.md
│   └── REVIEW.md
│
├── fontes/
│   └── edital-dataprev-2026.pdf
│
├── prompts/
│   ├── 00_Configurar_Ambiente_Autonomo.md
│   ├── 01_Fase_Analise.md
│   ├── 02_Fase_Estrutura.md
│   ├── 03_Fase_Motor.md
│   └── 04_Fase_Finalizacao.md
│
└── .gitignore
```

As pastas abaixo ainda não precisam existir inicialmente:

```text
analises/
dados/
apps-script/
```

Elas serão criadas ou completadas durante as fases.

---

# 2. Não envie os prompts separadamente no início

Abra a pasta completa `SOEA` no Codex.

O Codex deverá ter acesso a:

* todos os documentos;
* todos os prompts;
* edital em PDF;
* estrutura de pastas;
* terminal;
* Git, quando disponível;
* Chrome conectado;
* Google Sheets;
* Google Apps Script;
* `clasp`;
* Computer Use ou recurso equivalente.

Não copie apenas o conteúdo de um prompt no chat sem disponibilizar os arquivos do projeto.

A pasta completa será a fonte oficial.

---

# 3. Primeira mensagem ao Codex

Depois de abrir a pasta `SOEA`, envie somente esta mensagem:

```text
Você está trabalhando no projeto SOEA — Sistema Operacional de Estudos Adaptativo.

Leia inicialmente:

- docs/PRD.md
- docs/ARQUITETURA.md
- docs/INSTRUCOES.md
- docs/ROADMAP.md
- docs/TODO.md
- docs/CHANGELOG.md
- docs/REVIEW.md

Depois, leia:

- prompts/00_Configurar_Ambiente_Autonomo.md

Execute somente o Prompt 00.

Não execute os Prompts 01, 02, 03 ou 04.

Siga integralmente as regras do INSTRUCOES.md.

Seu objetivo agora é configurar e validar o ambiente autônomo, incluindo clasp, Google Apps Script, Google Sheets, Chrome conectado e execução real.

Não se limite a criar arquivos locais.

Quando houver uma etapa de autenticação ou segurança do Google, pare somente nesse ponto, explique exatamente a ação que preciso realizar e continue depois da minha confirmação.

Não solicite senhas, códigos ou tokens pelo chat.

Ao terminar, pare e aguarde minha aprovação.
```

---

# 4. Execução do Prompt 00

O Codex deverá:

1. ler os documentos;
2. verificar Node.js;
3. verificar npm;
4. instalar ou validar `clasp`;
5. verificar o acesso à API do Apps Script;
6. executar `clasp login`;
7. criar ou localizar a planilha do SOEA;
8. criar ou localizar o projeto Apps Script vinculado;
9. configurar `.clasp.json`;
10. executar um envio de teste;
11. abrir o Apps Script;
12. executar a função de diagnóstico;
13. abrir a planilha;
14. confirmar escrita e leitura;
15. confirmar limpeza da aba temporária;
16. executar um segundo envio;
17. criar `docs/AMBIENTE_AUTONOMO.md`;
18. atualizar `TODO.md`, `CHANGELOG.md` e `REVIEW.md`;
19. parar.

O resultado obrigatório deverá ser:

```text
PRONTO_COMPLETO
```

---

# 5. Quando o Codex pedir autenticação

Durante o Prompt 00, o Codex poderá parar e apresentar uma mensagem equivalente a:

```text
Intervenção de segurança necessária.

Ação:
Autorize o acesso do clasp à sua conta Google.

Conclua diretamente na página oficial do Google.

Não envie senha, código ou token no chat.

Depois responda:
“Autorização concluída. Continue.”
```

Nesse momento:

1. confira se a página é realmente do Google;
2. selecione sua conta;
3. digite sua senha diretamente no Google, se necessário;
4. conclua a autenticação em dois fatores;
5. aprove as permissões necessárias;
6. volte ao Codex.

Responda:

```text
Autorização concluída. Continue do ponto em que parou.
```

Não envie ao Codex:

* senha;
* código de autenticação;
* token;
* cookie;
* conteúdo de arquivo de credenciais.

---

# 6. Revisão do Prompt 00

Quando o Codex concluir, confira se informou:

* status `PRONTO_COMPLETO`;
* `clasp` instalado;
* `clasp` autenticado;
* planilha criada ou vinculada;
* projeto Apps Script vinculado;
* `clasp push` executado;
* função real executada;
* Chrome conectado;
* planilha aberta;
* segundo envio validado;
* `AMBIENTE_AUTONOMO.md` criado.

Caso algo esteja faltando, envie:

```text
O Prompt 00 ainda não está aprovado.

Revise os critérios de aceite de prompts/00_Configurar_Ambiente_Autonomo.md e conclua os itens pendentes.

Não inicie o Prompt 01.
```

Quando estiver correto, envie:

```text
Configuração do ambiente autônomo aprovada.

Registre a aprovação no ROADMAP.md e no REVIEW.md, caso ainda não esteja registrada.

Pode encerrar o Prompt 00.

Não execute o Prompt 01 ainda.
```

---

# 7. Execução do Prompt 01

Depois da aprovação do ambiente, envie:

```text
Leia novamente os documentos obrigatórios do projeto e execute somente:

prompts/01_Fase_Analise.md

A configuração do ambiente autônomo está aprovada.

Não execute os Prompts 02, 03 ou 04.

Analise o edital oficial e a página pública do curso conforme as regras do prompt.

Crie as pastas analises/ e dados/ e todos os arquivos exigidos.

Não implemente Google Apps Script nesta fase.

Atualize ROADMAP.md, TODO.md, CHANGELOG.md e REVIEW.md.

Ao concluir, pare e aguarde minha revisão.
```

---

# 8. Resultado esperado do Prompt 01

O Codex deverá criar:

```text
analises/
├── 00_Resumo_Fase_1.md
├── 01_Estrutura_Prova.md
├── 02_Analise_Estrategia.md
├── 03_Matriz_Cobertura.md
├── 04_Lacunas_Materiais.md
├── 05_Estrategia_Inicial.md
└── 06_Validacao_Dados.md
```

E:

```text
dados/
├── disciplinas.csv
├── assuntos.csv
└── config_inicial.csv
```

Também deverá atualizar:

```text
docs/ROADMAP.md
docs/TODO.md
docs/CHANGELOG.md
docs/REVIEW.md
```

---

# 9. Revisão do Prompt 01

Leia principalmente:

```text
analises/00_Resumo_Fase_1.md
analises/01_Estrutura_Prova.md
analises/03_Matriz_Cobertura.md
analises/04_Lacunas_Materiais.md
analises/05_Estrategia_Inicial.md
analises/06_Validacao_Dados.md
```

Confira os CSVs.

Caso haja correções,envie:

```text
A Fase 1 ainda não está aprovada.

Corrija os seguintes pontos:

- [descreva o problema];
- [descreva o problema].

Reexecute as validações afetadas.

Atualize ROADMAP.md, TODO.md, CHANGELOG.md e REVIEW.md.

Não inicie a Fase 2.
```

Quando estiver correto, envie:

```text
Fase 1 aprovada.

Pode registrar a aprovação no ROADMAP.md e no REVIEW.md.

Não execute a Fase 2 ainda.
```

---

# 10. Execução do Prompt 02

Depois da aprovação da Fase 1, envie:

```text
Leia novamente todos os documentos obrigatórios e execute somente:

prompts/02_Fase_Estrutura.md

A Fase 1 está aprovada.

Confirme que docs/AMBIENTE_AUTONOMO.md está com status PRONTO_COMPLETO.

Implemente a estrutura local, envie com clasp, execute setupSOEA() no projeto real, abra a planilha vinculada e realize todos os testes obrigatórios.

Não se limite a criar arquivos locais.

Corrija autonomamente os problemas encontrados, execute novo clasp push e repita os testes.

Não implemente o Motor da Fase 3.

Atualize toda a documentação exigida.

Ao concluir, pare e aguarde minha revisão.
```

---

# 11. Resultado esperado do Prompt 02

O Codex deverá criar ou completar:

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

Também deverá criar:

```text
docs/INSTALACAO_FASE_2.md
docs/TESTES_FASE_2.md
```

E implantar na planilha real:

* abas visíveis;
* abas ocultas;
* menu;
* Sidebars;
* Dashboard estrutural;
* Configurações;
* dados iniciais;
* proteções;
* integridade;
* backup.

---

# 12. Revisão do Prompt 02

Você deverá abrir a planilha e avaliar principalmente:

* aparência;
* organização das abas;
* clareza dos títulos;
* menu `SOEA`;
* abertura das Sidebars;
* Configurações;
* Dashboard;
* mensagens apresentadas.

O Codex já deverá ter executado os testes técnicos.

Caso encontre problema, envie:

```text
A Fase 2 ainda não está aprovada.

Problemas encontrados:

- [problema];
- [problema].

Corrija os arquivos localmente, execute clasp push, teste novamente na planilha real e atualize TESTES_FASE_2.md, TODO.md, CHANGELOG.md e REVIEW.md.

Não inicie a Fase 3.
```

Quando estiver correto, envie:

```text
Fase 2 aprovada.

Pode registrar a aprovação no ROADMAP.md e no REVIEW.md.

Não execute a Fase 3 ainda.
```

---

# 13. Execução do Prompt 03

Depois da aprovação da Fase 2, envie:

```text
Leia novamente todos os documentos obrigatórios e execute somente:

prompts/03_Fase_Motor.md

A Fase 2 está aprovada.

Confirme o ambiente PRONTO_COMPLETO e utilize a planilha e o projeto Apps Script aprovados.

Implemente o Motor do SOEA, envie as alterações com clasp e execute os testes reais na planilha.

Crie dados controlados de teste, identifique-os claramente, corrija autonomamente os problemas, execute regressões e remova somente os dados de teste ao final.

Não se limite a validações estáticas.

Não implemente a agenda final de simulados nem os refinamentos da Fase 4.

Atualize toda a documentação exigida.

Ao concluir, pare e aguarde minha revisão.
```

---

# 14. Resultado esperado do Prompt 03

O Codex deverá implantar e testar:

* ciclo;
* blocos;
* sessões;
* Continuar Ciclo;
* Retomar Ciclo;
* Aproveitar Tempo;
* Barra de Energia;
* Modo Emergência;
* questões;
* Banco de Erros;
* conclusão de blocos;
* revisões;
* Índice de Prioridade;
* Índice de Domínio;
* Tempo Estimado Inteligente;
* métricas;
* Dashboard funcional;
* aba Ciclo;
* integridade;
* recuperação;
* backup.

Também deverá criar:

```text
docs/FORMULAS_SOEA.md
docs/TESTES_FASE_3.md
```

E, opcionalmente:

```text
apps-script/TestRunner.gs
```

---

# 15. Revisão do Prompt 03

Teste a planilha como usuário.

Avalie principalmente:

* coerência dos assuntos escolhidos;
* justificativa da escolha;
* facilidade de iniciar sessão;
* retomada;
* Aproveitar Tempo;
* quantidade de cliques;
* mensagens;
* carga por energia;
* clareza do Dashboard.

Caso encontre problema:

```text
A Fase 3 ainda não está aprovada.

Problemas encontrados:

- [problema];
- [problema].

Corrija localmente, execute clasp push, teste novamente na planilha real, execute regressões e atualize a documentação.

Não inicie a Fase 4.
```

Quando estiver correto:

```text
Fase 3 aprovada.

Pode registrar a aprovação no ROADMAP.md e no REVIEW.md.

Não execute a Fase 4 ainda.
```

---

# 16. Execução do Prompt 04

Depois da aprovação da Fase 3, envie:

```text
Leia novamente todos os documentos obrigatórios e execute somente:

prompts/04_Fase_Finalizacao.md

A Fase 3 está aprovada.

Confirme o ambiente PRONTO_COMPLETO.

Crie ou utilize um ambiente controlado de testes, sem contaminar os dados reais.

Implemente os simulados, agenda, Dashboard final, Estatísticas e refinamentos finais.

Execute instalação limpa, reinstalação, atualização da Fase 3, regressão completa, testes de simulados, Dashboard, Estatísticas, backup, recuperação, integridade, segurança e performance.

Corrija autonomamente os problemas encontrados, execute novos clasp push e repita os testes.

Remova somente os dados identificados como teste.

Depois de aprovar tecnicamente o ambiente de teste, implante a versão final na planilha principal e execute a validação final.

Prepare a versão SOEA v1.0.0, mas não a declare definitivamente aprovada.

Atualize toda a documentação exigida.

Ao concluir, pare e aguarde minha aprovação final.
```

---

# 17. Resultado esperado do Prompt 04

O Codex deverá entregar:

* simulados;
* agenda de simulados;
* correção de simulados;
* Dashboard final;
* Estatísticas;
* Configurações finais;
* revisão de experiência;
* revisão de acessibilidade;
* revisão de performance;
* revisão de segurança;
* testes de instalação;
* testes de atualização;
* regressão;
* limpeza dos dados de teste;
* implantação na planilha principal.

Também deverá criar:

```text
README.md
docs/TESTES_FASE_4.md
```

E atualizar:

```text
docs/ROADMAP.md
docs/TODO.md
docs/CHANGELOG.md
docs/REVIEW.md
```

---

# 18. Revisão final da versão 1.0

Antes de aprovar, confira:

* a planilha principal abre;
* o menu aparece;
* Continuar Ciclo funciona;
* Retomar Ciclo funciona;
* Aproveitar Tempo funciona;
* questões funcionam;
* Banco de Erros funciona;
* revisões funcionam;
* simulados funcionam;
* Dashboard está correto;
* Estatísticas estão corretas;
* Configurações estão corretas;
* integridade não apresenta erro crítico;
* backup funciona;
* não existem dados de teste;
* nenhum bug crítico está aberto;
* nenhum bug alto impeditivo está aberto;
* README está compreensível.

Caso encontre problema:

```text
A Fase 4 ainda não está aprovada.

Problemas encontrados:

- [problema];
- [problema].

Corrija na planilha de teste, execute regressões, implante novamente na planilha principal e atualize TESTES_FASE_4.md, TODO.md, CHANGELOG.md e REVIEW.md.

Não marque a versão 1.0.0 como estável.
```

---

# 19. Aprovação final

Quando tudo estiver correto, envie:

```text
Fase 4 aprovada.

A versão SOEA v1.0.0 está aprovada para uso.

Atualize ROADMAP.md, REVIEW.md e CHANGELOG.md com a aprovação final.

Marque a versão 1.0.0 como estável.

Caso o projeto utilize Git, crie a tag v1.0.0 sem utilizar push forçado.

Não implemente novas funcionalidades e não inicie uma versão 2.0.

Apresente apenas o resumo final da entrega.
```

---

# 20. Regra para todas as fases

Nunca envie uma mensagem como:

```text
Execute todos os prompts.
```

Nunca peça:

```text
Faça o projeto inteiro.
```

Sempre execute uma etapa por vez.

A ordem obrigatória é:

```text
Prompt 00
↓
Revisão e aprovação
↓
Prompt 01
↓
Revisão e aprovação
↓
Prompt 02
↓
Revisão e aprovação
↓
Prompt 03
↓
Revisão e aprovação
↓
Prompt 04
↓
Revisão e aprovação final
```

---

# 21. Intervenções que poderão depender de você

Você poderá precisar agir somente em:

* login no Google;
* senha;
* autenticação em dois fatores;
* CAPTCHA;
* consentimento OAuth;
* confirmação de permissões;
* escolha entre duas planilhas;
* escolha entre dois projetos;
* decisão sobre risco de perda de dados;
* avaliação visual;
* aprovação de cada fase.

O Codex deverá executar sozinho:

* comandos;
* criação de arquivos;
* criação da planilha;
* criação do Apps Script;
* `clasp push`;
* execução das funções;
* criação das abas;
* testes técnicos;
* correções;
* regressões;
* limpeza dos dados de teste;
* documentação.

---

# 22. Resumo operacional

## Antes de começar

```text
Organizar a pasta SOEA
Abrir a pasta completa no Codex
Garantir Chrome conectado
Garantir conta Google acessível
```

## Execução

```text
Enviar mensagem do Prompt 00
Autorizar Google quando solicitado
Aprovar Prompt 00

Enviar mensagem do Prompt 01
Revisar análise
Aprovar Fase 1

Enviar mensagem do Prompt 02
Revisar estrutura visual
Aprovar Fase 2

Enviar mensagem do Prompt 03
Revisar uso do Motor
Aprovar Fase 3

Enviar mensagem do Prompt 04
Revisar versão final
Aprovar SOEA v1.0.0
```

## Resultado

```text
Planilha SOEA criada
Apps Script vinculado
Código versionado localmente
Implantação automatizada por clasp
Testes reais executados
Dados preservados
Documentação concluída
Versão SOEA v1.0.0 pronta para uso
```
