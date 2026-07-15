# PROMPT 04 — FASE 4: FINALIZAÇÃO E ENTREGA DA VERSÃO 1.0

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
* `docs/FORMULAS_SOEA.md`
* `docs/TESTES_FASE_3.md`

Leia também todos os arquivos existentes nas pastas:

```text
analises/
dados/
fontes/
apps-script/
```

Leia o `README.md`, caso ele já exista.

Confirme no `ROADMAP.md`, no `TODO.md` e no `REVIEW.md` que:

1. a Fase 3 foi executada;
2. o Motor do SOEA foi implantado na planilha real;
3. Continuar Ciclo foi testado;
4. Retomar Ciclo foi testado;
5. Aproveitar Tempo foi testado;
6. sessões parciais foram testadas;
7. questões foram testadas;
8. Banco de Erros foi testado;
9. revisões foram testadas;
10. Índice de Prioridade foi testado;
11. Índice de Domínio foi testado;
12. integridade, recuperação e backup foram testados;
13. os dados de teste da Fase 3 foram removidos;
14. os bugs críticos e altos impeditivos da Fase 3 foram corrigidos;
15. o Product Owner aprovou explicitamente a Fase 3;
16. a fase atual é a Fase 4.

A aprovação deverá estar registrada de forma equivalente a:

```text
Fase 3 aprovada.

Pode iniciar a Fase 4.
```

Caso a Fase 3 não esteja aprovada:

1. não execute esta fase;
2. registre o bloqueio no `REVIEW.md`;
3. preserve todos os arquivos e dados;
4. informe o Product Owner;
5. pare.

---

# 2. Verificação obrigatória do ambiente autônomo

Leia:

```text
docs/AMBIENTE_AUTONOMO.md
```

A Fase 4 somente poderá continuar quando o status for:

```text
PRONTO_COMPLETO
```

Confirme novamente:

* Node.js compatível;
* npm;
* `clasp`;
* autenticação do `clasp`;
* API do Google Apps Script;
* projeto Apps Script correto;
* planilha principal correta;
* arquivo `.clasp.json`;
* envio com `clasp push`;
* Chrome conectado;
* acesso ao editor do Apps Script;
* acesso à planilha;
* execução remota de funções;
* Computer Use ou ferramenta visual equivalente.

Execute:

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

Abra o projeto remoto e confirme que ele corresponde ao projeto aprovado na Fase 3.

Caso o ambiente não esteja `PRONTO_COMPLETO`:

1. não entregue apenas arquivos locais;
2. não declare a Fase 4 como executada;
3. tente restaurar o ambiente autonomamente;
4. solicite intervenção humana apenas para autenticação, segurança ou decisão pessoal;
5. continue após a intervenção;
6. só prossiga quando o status voltar a `PRONTO_COMPLETO`.

---

# 3. Objetivo da fase

Finalizar, implantar, testar e preparar para uso real a versão:

```text
SOEA v1.0.0
```

Esta fase deverá:

* revisar o Motor implementado na Fase 3;
* corrigir bugs pendentes;
* implementar o sistema de simulados;
* implementar a agenda de simulados;
* implementar a correção dos simulados;
* finalizar o Dashboard;
* finalizar a aba Estatísticas;
* finalizar as abas visíveis;
* revisar as Configurações;
* revisar a experiência de uso;
* revisar acessibilidade;
* revisar mensagens;
* revisar performance;
* revisar segurança;
* revisar permissões;
* revisar backup e recuperação;
* executar testes de instalação;
* executar testes de atualização;
* executar testes de regressão;
* executar testes de simulados;
* executar testes de Dashboard;
* executar testes de Estatísticas;
* corrigir os problemas encontrados;
* limpar os dados de teste;
* preparar a documentação final;
* preparar a versão estável.

Não será suficiente alterar o código localmente.

O fluxo obrigatório será:

```text
Revisar implementação atual
↓
Criar ambiente controlado de teste
↓
Implementar localmente
↓
Validar localmente
↓
Executar clasp push
↓
Executar na planilha de teste
↓
Executar testes completos
↓
Corrigir falhas
↓
Executar novo clasp push
↓
Executar regressão
↓
Limpar dados de teste
↓
Implantar na planilha principal
↓
Executar validação final
↓
Atualizar documentação
↓
Aguardar aprovação final
```

---

# 4. Limites da Fase 4

Esta fase é de finalização.

Não aumentar o escopo.

Não implementar:

* aplicação web;
* aplicativo mobile;
* Firebase;
* servidor externo;
* banco de dados externo;
* API externa;
* integração automática com o Estratégia;
* integração automática com plataformas de questões;
* sistema multiusuário;
* suporte a múltiplos concursos;
* inteligência artificial integrada;
* notificações externas;
* gamificação avançada;
* versão comercial;
* sistema de assinatura;
* funcionalidades não previstas no PRD.

Qualquer melhoria não essencial deverá ser registrada no `TODO.md` como:

```text
[~] Adiada para versão futura
```

A ordem de prioridade deverá ser:

```text
Integridade dos dados
↓
Estabilidade
↓
Fluxo principal
↓
Usabilidade
↓
Performance
↓
Aparência
```

Não atrasar a entrega por melhorias puramente cosméticas.

---

# 5. Preservação da implementação existente

Não reconstruir o projeto do zero.

Antes de alterar qualquer arquivo:

1. analisar o código aprovado na Fase 3;
2. identificar os fluxos funcionais;
3. preservar a arquitetura;
4. preservar a planilha principal;
5. preservar disciplinas;
6. preservar assuntos;
7. preservar configurações;
8. preservar ciclos;
9. preservar blocos;
10. preservar sessões;
11. preservar questões;
12. preservar erros;
13. preservar revisões;
14. preservar métricas;
15. preservar histórico;
16. preservar logs;
17. preservar backups;
18. preservar IDs;
19. preservar fórmulas aprovadas.

Não alterar:

* `docs/PRD.md`;
* `docs/ARQUITETURA.md`;
* `docs/INSTRUCOES.md`;
* conteúdo oficial do edital;
* nomes oficiais das disciplinas;
* textos oficiais dos assuntos;
* decisões aprovadas nas fases anteriores.

Caso seja necessária uma alteração estrutural:

1. identificar o problema;
2. justificar a alteração;
3. criar backup;
4. planejar a migração;
5. preservar dados existentes;
6. atualizar `Setup.gs`;
7. testar instalação limpa;
8. testar atualização da instalação existente;
9. executar regressão;
10. documentar a alteração.

---

# 6. Ambiente controlado de testes

Os testes finais não deverão contaminar os dados reais.

Preferir:

```text
Planilha principal
↓
Cópia controlada para testes
↓
Testes completos
↓
Correções
↓
Regressão
↓
Limpeza
↓
Implantação final na planilha principal
```

O Codex deverá verificar se a cópia da planilha mantém corretamente o projeto Apps Script vinculado.

Não presumir que o vínculo foi copiado.

Caso a cópia possua um projeto Apps Script próprio:

* registrar o ID da planilha de teste;
* registrar o ID do projeto de teste;
* não alterar o `.clasp.json` principal de forma definitiva;
* utilizar configuração temporária segura;
* restaurar o vínculo principal ao final.

Caso a cópia não possua o projeto necessário:

* criar um projeto de teste vinculado;
* enviar o código para o projeto de teste;
* não sobrescrever o projeto principal durante testes destrutivos;
* documentar o procedimento.

Caso não seja viável manter um projeto separado:

* criar backup;
* utilizar registros identificados como teste;
* evitar testes destrutivos;
* limpar somente registros de teste;
* validar novamente a integridade.

---

# 7. Identificação dos dados de teste

Todos os registros de teste deverão ser identificados.

Utilizar, quando houver suporte:

```text
origem = TESTE_FASE_4
```

ou:

```text
is_test = true
```

Também poderão ser utilizados:

* prefixos nos nomes;
* observações padronizadas;
* IDs de execução de teste;
* planilha separada.

Exemplo:

```text
TESTE_FASE_4_SIMULADO_001
```

Não alterar a arquitetura apenas para criar um campo de teste quando houver alternativa segura.

Registrar no `TESTES_FASE_4.md` a estratégia utilizada.

---

# 8. Backup antes da finalização

Antes de qualquer alteração estrutural ou teste destrutivo:

* executar `criarBackupSOEA()`;
* registrar o tipo como `PRE_FASE_4`;
* registrar data e hora;
* registrar versão;
* registrar planilha;
* registrar entidades incluídas;
* validar que o backup não está vazio;
* registrar no histórico.

Criar também uma referência local da versão anterior.

Caso o projeto utilize Git:

* verificar o status;
* não incluir credenciais;
* registrar um commit de segurança quando apropriado;
* não executar `push --force`;
* não apagar histórico.

O uso do Git é auxiliar e não substitui o backup dos dados da planilha.

---

# 9. Revisão inicial dos bugs e pendências

Antes de implementar novas funcionalidades, consultar:

* `docs/TODO.md`;
* `docs/REVIEW.md`;
* `docs/TESTES_FASE_3.md`;
* `docs/CHANGELOG.md`;
* `_db_Logs`;
* resultados de `verificarIntegridadeSOEA()`.

Classificar as pendências em:

```text
Crítica
Alta
Média
Baixa
Melhoria futura
```

Corrigir primeiro:

1. risco de perda de dados;
2. corrupção de dados;
3. duplicidade;
4. fluxo principal quebrado;
5. recuperação incorreta;
6. métricas incorretas;
7. problemas de interface;
8. problemas visuais.

Não iniciar refinamentos visuais enquanto houver bug crítico.

---

# 10. Classificação oficial de bugs

## Crítico

Exemplos:

* perda de dados;
* corrupção;
* duplicidade grave;
* projeto não executa;
* ciclo inutilizável;
* recuperação destrutiva;
* setup apaga dados.

Nenhum bug crítico poderá permanecer na versão 1.0.

## Alto

Exemplos:

* Continuar Ciclo não funciona;
* sessão não salva;
* revisão não é criada;
* bloco não retoma;
* simulado não registra;
* métricas importantes incorretas.

Nenhum bug alto impeditivo poderá permanecer sem decisão explícita do Product Owner.

## Médio

Exemplos:

* filtro incorreto;
* mensagem confusa;
* gráfico com problema;
* comportamento com alternativa segura.

Corrigir os que afetarem o estudo cotidiano.

## Baixo

Exemplos:

* alinhamento;
* detalhe visual;
* texto secundário;
* ajuste cosmético.

Poderão ser adiados.

---

# 11. Registro de bugs

Utilizar IDs:

```text
BUG-001
BUG-002
BUG-003
```

Cada bug deverá registrar:

* título;
* severidade;
* fase;
* cenário;
* comportamento esperado;
* comportamento obtido;
* causa;
* correção;
* arquivos afetados;
* teste de regressão;
* status.

Registrar em:

* `docs/TODO.md`;
* `docs/TESTES_FASE_4.md`;
* `docs/REVIEW.md`;
* `docs/CHANGELOG.md`, após a correção.

---

# 12. Sistema de simulados

Finalizar `SimulationService.gs`.

O sistema deverá permitir:

* criar simulado planejado;
* criar simulado manual;
* registrar simulado realizado;
* editar registro incompleto;
* corrigir simulado;
* cancelar simulado;
* consultar simulados;
* filtrar simulados;
* atualizar métricas;
* atualizar prioridade;
* atualizar domínio;
* atualizar Dashboard;
* impedir duplicidade.

Cada simulado deverá possuir, conforme o modelo aprovado:

* ID;
* nome;
* data planejada;
* data realizada;
* duração prevista;
* duração real;
* total de questões;
* acertos;
* erros;
* percentual;
* status;
* origem;
* observação;
* assuntos problemáticos;
* data de criação;
* data de atualização;
* identificação de teste.

Utilizar os cabeçalhos aprovados no PRD.

---

# 13. Status dos simulados

Centralizar em `Constants.gs`.

Estados esperados:

```text
PLANEJADO
REALIZADO
EM_CORRECAO
CORRIGIDO
CANCELADO
ATRASADO
```

Utilizar os valores já aprovados no projeto quando houver diferença.

Não espalhar textos de status diretamente pelo código.

---

# 14. Validação dos simulados

Validar:

* ID único;
* nome obrigatório;
* data válida;
* duração não negativa;
* total de questões maior que zero;
* acertos maiores ou iguais a zero;
* acertos menores ou iguais ao total;
* erros calculados automaticamente;
* percentual entre 0 e 100;
* status permitido;
* ausência de duplicidade;
* origem válida.

Não considerar um simulado realizado apenas porque a data passou.

Quando a data prevista passar sem resultado:

* utilizar status `ATRASADO`;
* não inventar desempenho;
* não preencher data realizada;
* não criar questões fictícias.

---

# 15. Agenda automática de simulados

Implementar agenda baseada na data da prova armazenada em `_db_Config`.

Não fixar a data diretamente no código.

Planejamento inicial aprovado:

## Julho de 2026

* segundo sábado;
* quarto sábado.

## Agosto de 2026

* todos os sábados.

## Setembro de 2026

* todos os sábados.

## Últimos 15 dias antes da prova

* permitir mini simulados em dias úteis;
* não substituir o simulado principal;
* evitar sobrecarga;
* respeitar revisões finais.

## Domingos

* priorizar correção;
* Banco de Erros;
* revisão de assuntos problemáticos.

Criar ou utilizar:

```javascript
gerarAgendaSimuladosSOEA()
```

---

# 16. Regras da agenda

A agenda deverá:

* considerar a data real de instalação;
* considerar a data atual;
* criar somente datas futuras;
* não criar simulado após a prova;
* não criar pendências retroativas;
* impedir duplicidade;
* permitir edição manual;
* permitir cancelamento;
* registrar origem automática ou manual;
* não recriar simulado cancelado sem confirmação;
* ser idempotente.

Exemplo:

```text
Data do simulado: 11/07/2026
Início de uso: 20/07/2026

Resultado:
O simulado de 11/07/2026 não deverá ser criado como pendência.
```

---

# 17. Correção dos simulados

Após registrar um simulado, permitir etapa de correção.

Registrar:

* desempenho geral;
* desempenho por disciplina;
* assuntos problemáticos;
* erros de conteúdo;
* erros de interpretação;
* erros de atenção;
* problemas de tempo;
* observações;
* ações recomendadas.

Quando permitido pelo modelo, permitir transformar erros selecionados em registros do Banco de Erros.

Evitar preenchimento duplicado de:

* disciplina;
* assunto;
* data;
* simulado;
* percentual.

A correção deverá atualizar:

* métricas;
* Índice de Prioridade;
* Índice de Domínio;
* Estatísticas;
* Dashboard.

---

# 18. Desempenho por disciplina no simulado

Quando o modelo aprovado permitir, registrar para cada disciplina:

* questões;
* acertos;
* erros;
* percentual;
* assuntos problemáticos;
* observação.

Caso seja necessária uma estrutura adicional:

1. verificar o PRD;
2. verificar a Arquitetura;
3. utilizar a menor alteração possível;
4. criar backup;
5. atualizar o setup;
6. testar migração;
7. documentar.

Não criar uma nova arquitetura silenciosamente.

---

# 19. Sidebar de simulados

Finalizar `SidebarSimulation.html`.

Permitir:

* visualizar simulado planejado;
* registrar realização;
* informar duração;
* informar questões;
* informar acertos;
* registrar observação;
* iniciar correção;
* cancelar;
* editar registro incompleto.

A Sidebar deverá:

* validar campos;
* impedir clique repetido;
* mostrar carregamento;
* preservar dados em caso de erro;
* mostrar resumo;
* não fechar antes da confirmação.

---

# 20. Dashboard final

Finalizar `DashboardService.gs`.

Cards obrigatórios:

* dias até a prova;
* ciclo ativo;
* bloco atual;
* etapa atual;
* horas totais;
* horas da semana;
* questões totais;
* questões da semana;
* aproveitamento geral;
* revisões pendentes;
* revisões atrasadas;
* erros pendentes;
* percentual do edital;
* sequência de estudos;
* próximo simulado;
* último simulado;
* resultado do último simulado;
* meta semanal;
* domínio geral, quando previsto.

Todos os valores deverão vir de dados reais.

Quando não houver dados:

```text
Ainda sem dados
```

Não exibir zero quando zero puder ser confundido com ausência de dados.

---

# 21. Gráficos finais

Criar ou finalizar:

* evolução do aproveitamento;
* questões por semana;
* horas por semana;
* desempenho por disciplina;
* evolução dos simulados.

Gráficos complementares permitidos:

* erros por causa-raiz;
* revisões concluídas e atrasadas;
* assuntos com menor domínio;
* assuntos com maior prioridade.

Não criar excesso de gráficos.

Todos os gráficos deverão:

* possuir título;
* utilizar dados reais;
* utilizar intervalos dinâmicos;
* atualizar corretamente;
* funcionar sem dados;
* evitar `#N/A`;
* evitar `#REF!`;
* evitar intervalos vazios inválidos;
* possuir legibilidade.

---

# 22. Layout final do Dashboard

Revisar:

* hierarquia;
* alinhamento;
* espaçamento;
* contraste;
* títulos;
* números;
* percentuais;
* datas;
* largura de colunas;
* altura de linhas;
* tamanho dos gráficos;
* áreas vazias;
* estados sem dados.

Evitar:

* excesso de cores;
* textos cortados;
* gráficos pequenos;
* informações duplicadas;
* cards sem utilidade;
* células mescladas desnecessárias.

O Dashboard deverá ser painel de acompanhamento.

Não deverá ser fonte oficial de dados nem local principal de edição.

---

# 23. Aba Estatísticas final

Finalizar a aba `Estatísticas`.

Implementar filtros ou seletores para:

* período;
* disciplina;
* assunto;
* tipo de atividade;
* status;
* fonte das questões;
* simulados.

Apresentar:

* horas estudadas;
* questões realizadas;
* acertos;
* erros;
* aproveitamento;
* desempenho por disciplina;
* desempenho por assunto;
* revisões;
* erros recorrentes;
* causas-raiz;
* simulados;
* assuntos com menor domínio;
* assuntos com maior prioridade;
* evolução no período;
* metas semanais.

O Dashboard mostra resumo.

A aba Estatísticas deverá mostrar detalhamento.

---

# 24. Aba Banco de Erros final

Revisar:

* filtros;
* status;
* recorrência;
* disciplina;
* assunto;
* causa-raiz;
* data;
* observação;
* atualização de status;
* sincronização;
* proteção contra edição destrutiva.

Destacar:

* erros novos;
* erros recorrentes;
* erros antigos;
* erros resolvidos;
* erros relacionados a assuntos de alta prioridade.

O usuário não deverá precisar abrir `_db_Erros`.

---

# 25. Aba Ciclo final

A aba `Ciclo` deverá mostrar:

* ciclo ativo;
* bloco atual;
* disciplina;
* assunto;
* etapa;
* progresso;
* tempo previsto;
* tempo realizado;
* questões previstas;
* questões realizadas;
* sessão;
* próxima revisão;
* justificativa;
* próxima ação.

Evitar controles duplicados entre a aba e as Sidebars.

As ações principais continuarão no menu `SOEA`.

---

# 26. Aba Configurações final

Garantir que:

* somente configurações editáveis possam ser alteradas;
* tipos sejam validados;
* datas sejam válidas;
* números possuam limites;
* listas utilizem valores permitidos;
* configurações técnicas não sejam expostas;
* alterações sejam registradas;
* alterações relevantes atualizem o sistema.

Implementar opção segura para restaurar configurações editáveis aos padrões.

Essa opção não poderá:

* apagar ciclos;
* apagar blocos;
* apagar sessões;
* apagar questões;
* apagar erros;
* apagar revisões;
* apagar simulados;
* apagar histórico;
* alterar IDs.

Solicitar confirmação antes da restauração.

---

# 27. Experiência de uso

Revisar o fluxo completo.

Objetivo:

```text
Iniciar uma sessão em menos de 30 segundos
```

Revisar:

* quantidade de cliques;
* quantidade de campos;
* ordem das perguntas;
* mensagens;
* confirmações;
* cancelamentos;
* carregamentos;
* resumo das sessões;
* resumo dos blocos;
* resumo das revisões;
* resumo dos simulados.

Remover campos que possam ser calculados automaticamente.

Não solicitar repetidamente:

* disciplina;
* assunto;
* bloco;
* sessão;
* data;
* erros calculáveis;
* percentual;
* tempo médio.

---

# 28. Mensagens finais

Padronizar mensagens.

## Sucesso

```text
Sessão concluída.

Tempo estudado: 45 minutos
Questões realizadas: 20
Aproveitamento: 80%
Progresso salvo com sucesso.
```

## Erro recuperável

```text
Não foi possível concluir esta ação.

Seu progresso foi preservado.
Revise os dados e tente novamente.
```

## Integridade

```text
Foi encontrada uma inconsistência no estado da sessão.

Nenhum dado foi apagado.
Utilize “Verificar Integridade” para consultar os detalhes.
```

## Sem dados

```text
Ainda não há dados suficientes para gerar esta análise.
```

Não exibir:

* stack trace;
* JSON;
* nome interno de intervalo;
* detalhes de exceção;
* IDs desnecessários;
* nomes técnicos desnecessários.

---

# 29. Acessibilidade e legibilidade

Revisar:

* contraste;
* tamanho dos textos;
* labels;
* textos dos botões;
* campos obrigatórios;
* mensagens de validação;
* estados de carregamento;
* estados de erro;
* estados de sucesso;
* navegação por teclado quando possível.

Não utilizar somente cores para representar:

* status;
* domínio;
* prioridade;
* erro;
* sucesso.

Sempre combinar cor com:

* texto;
* símbolo;
* rótulo.

---

# 30. Performance

Revisar:

* leituras repetidas;
* escritas célula por célula;
* loops com acesso à planilha;
* atualizações completas desnecessárias;
* recálculos;
* criação repetida de gráficos;
* triggers;
* backups;
* locks;
* cache;
* leitura de configurações;
* atualização do Dashboard.

Priorizar:

* `getValues()`;
* `setValues()`;
* mapas de cabeçalhos;
* operações em lote;
* atualização somente do necessário;
* cache seguro;
* invalidação correta.

Não sacrificar a integridade por ganho pequeno de velocidade.

---

# 31. Medição de performance

Medir as operações principais quando possível:

* abrir menu;
* abrir Sidebar;
* executar setup;
* Continuar Ciclo;
* Aproveitar Tempo;
* concluir sessão;
* concluir bloco;
* registrar questões;
* registrar erro;
* realizar revisão;
* registrar simulado;
* atualizar Dashboard;
* atualizar Estatísticas;
* verificar integridade;
* criar backup;
* recuperar estado.

Registrar:

* operação;
* volume de dados;
* tempo observado;
* resultado;
* necessidade de otimização.

Não inventar tempos.

Quando uma medição não puder ser realizada, registrar o motivo.

---

# 32. Segurança e privacidade

Verificar ausência de:

* senhas;
* tokens;
* cookies;
* credenciais;
* chaves privadas;
* dados bancários;
* conteúdo protegido;
* PDFs protegidos;
* enunciados completos de questões;
* informações pessoais desnecessárias.

Confirmar:

* ausência de APIs externas;
* ausência de CDN;
* ausência de bibliotecas externas;
* permissões mínimas;
* abas ocultas protegidas;
* IDs únicos;
* locks;
* validações;
* backups;
* logs sem credenciais.

---

# 33. Manifesto e permissões

Revisar `appsscript.json`.

Confirmar:

* runtime V8;
* fuso `America/Sao_Paulo`;
* exceções configuradas;
* ausência de escopos desnecessários;
* ausência de integrações externas;
* sintaxe válida.

Documentar no README:

* quais permissões são solicitadas;
* por que são necessárias;
* que nenhum acesso externo é utilizado.

---

# 34. Backup final

Validar `BackupService.gs`.

Confirmar:

* backup manual;
* backup antes de operações críticas;
* ID;
* data;
* motivo;
* tipo;
* versão;
* entidades;
* retenção;
* remoção segura de backups antigos;
* consulta a backups;
* ausência de registros vazios.

Não considerar uma linha vazia como backup válido.

---

# 35. Recuperação e restauração

Validar `RecoveryService.gs`.

Testar:

* sessão órfã;
* dois ciclos ativos;
* dois blocos ativos;
* duas sessões abertas;
* registro órfão;
* revisão duplicada;
* progresso inválido;
* cabeçalho ausente;
* configuração ausente.

Quando a correção automática for segura:

* criar backup;
* corrigir;
* registrar log;
* registrar histórico;
* mostrar resumo.

Quando puder apagar ou substituir dados:

* não executar automaticamente;
* apresentar alternativas;
* registrar bloqueio;
* aguardar autorização.

---

# 36. Funções públicas finais

Verificar se todas as funções usadas pela interface existem.

Exemplos:

```javascript
setupSOEA()
continuarCicloSOEA()
aproveitarTempoSOEA()
iniciarSessaoSOEA(payload)
concluirSessaoSOEA(payload)
registrarQuestoesSOEA(payload)
registrarErroSOEA(payload)
concluirBlocoSOEA(payload)
realizarRevisaoSOEA(payload)
registrarSimuladoSOEA(payload)
corrigirSimuladoSOEA(payload)
gerarAgendaSimuladosSOEA()
atualizarDashboardSOEA()
verificarIntegridadeSOEA()
criarBackupSOEA()
```

Os nomes poderão variar, mas deverão:

* ser claros;
* existir;
* estar vinculados corretamente;
* retornar respostas estruturadas;
* tratar erros;
* não conter toda a regra de negócio.

---

# 37. Limpeza do código

Antes dos testes finais:

* remover código morto;
* remover funções duplicadas;
* remover comentários temporários;
* remover dados fictícios;
* remover logs de depuração;
* remover arquivos não utilizados;
* remover respostas `FEATURE_NOT_AVAILABLE` de funções concluídas;
* preservar diagnósticos úteis;
* preservar testes auxiliares seguros;
* validar includes;
* validar nomes;
* validar referências.

Não apagar documentos históricos.

Não apagar análises.

Não apagar CSVs.

---

# 38. Validação local antes do envio

Antes de `clasp push`, verificar:

* sintaxe;
* manifesto;
* funções duplicadas;
* constantes;
* referências;
* funções do menu;
* includes HTML;
* arquivos faltantes;
* respostas estruturadas;
* ausência de credenciais;
* ausência de código sabidamente inválido.

Não enviar código inválido.

---

# 39. Implantação no ambiente de teste

Dentro da pasta correta, executar:

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

* projeto de teste correto;
* arquivos reconhecidos;
* envio concluído;
* ausência de erro.

Abrir:

```bash
clasp open-script
```

ou:

```bash
npx clasp open-script
```

Confirmar os arquivos no editor remoto.

---

# 40. Execução real no ambiente de teste

Executar as funções necessárias:

* migração;
* setup;
* geração de agenda;
* atualização do Dashboard;
* atualização das Estatísticas;
* integridade;
* backup;
* testes auxiliares.

Abrir a planilha de teste.

Confirmar os resultados reais.

Não considerar a execução aprovada apenas por ausência de erro de sintaxe.

---

# 41. Documento de testes finais

Criar:

```text
docs/TESTES_FASE_4.md
```

Registrar:

* ambiente;
* versão;
* data;
* planilha;
* projeto;
* responsável;
* dados de teste;
* testes de instalação;
* testes de atualização;
* testes de regressão;
* testes de simulados;
* testes do Dashboard;
* testes das Estatísticas;
* testes de integridade;
* testes de backup;
* testes de recuperação;
* testes de performance;
* testes de segurança;
* bugs;
* correções;
* regressões;
* limpeza;
* resultado final.

Status:

```text
Aprovado
Reprovado
Bloqueado
Pendente do Product Owner
Não aplicável
```

Com ambiente `PRONTO_COMPLETO`, testes técnicos não poderão ser transferidos ao Product Owner.

---

# 42. Teste de instalação limpa

Em uma planilha de teste vazia:

1. vincular o projeto;
2. executar `setupSOEA()`;
3. autorizar permissões;
4. verificar abas;
5. verificar cabeçalhos;
6. verificar seeds;
7. verificar menu;
8. verificar Sidebars;
9. verificar Dashboard;
10. verificar Configurações;
11. executar integridade;
12. criar backup.

Resultado esperado:

* instalação concluída;
* nenhuma exceção crítica;
* dados importados;
* estrutura funcional.

---

# 43. Teste de segunda instalação

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
* valores preservados;
* ciclos preservados;
* blocos preservados;
* sessões preservadas;
* questões preservadas;
* erros preservados;
* revisões preservadas;
* simulados preservados;
* ausência de erro.

A idempotência deverá ser comprovada por execução real.

---

# 44. Teste de atualização da Fase 3

Executar a versão final sobre uma cópia da planilha da Fase 3.

Confirmar:

* migração segura;
* criação somente de campos ausentes;
* preservação dos dados;
* preservação de IDs;
* preservação das configurações;
* preservação do ciclo;
* preservação dos blocos;
* preservação das sessões;
* preservação das questões;
* preservação dos erros;
* preservação das revisões;
* atualização da versão;
* ausência de corrupção.

---

# 45. Testes de regressão do Motor

Reexecutar:

* criação do ciclo;
* Continuar Ciclo sem bloco;
* interrupção;
* retomada;
* registro de questões;
* registro de erro;
* conclusão do bloco;
* criação de revisões;
* prevenção de revisão duplicada;
* revisão com desempenho alto;
* revisão com desempenho intermediário;
* revisão com desempenho baixo;
* Aproveitar Tempo parcial;
* Aproveitar Tempo concluindo bloco;
* Modo Emergência;
* energia muito baixa;
* clique duplicado;
* duas sessões abertas;
* dois blocos ativos;
* persistência;
* Dashboard;
* prioridade;
* domínio;
* amostra pequena;
* integridade;
* backup;
* recuperação.

Nenhuma alteração da Fase 4 poderá quebrar a Fase 3.

---

# 46. Testes da agenda de simulados

## Teste 1 — Geração inicial

Confirmar:

* datas corretas;
* somente datas futuras;
* nenhum simulado após a prova;
* origem automática;
* status planejado.

## Teste 2 — Segunda execução

Executar novamente e confirmar ausência de duplicidade.

## Teste 3 — Instalação após data planejada

Confirmar que não cria simulado retroativo.

## Teste 4 — Cancelamento

Cancelar um simulado e confirmar que ele não reaparece automaticamente.

## Teste 5 — Edição

Alterar uma data planejada e confirmar preservação.

## Teste 6 — Últimos 15 dias

Confirmar mini simulados dentro das regras.

---

# 47. Testes de registro de simulado

Registrar um simulado válido.

Confirmar:

* ID;
* data;
* duração;
* questões;
* acertos;
* erros;
* percentual;
* status;
* métricas;
* Dashboard;
* prioridade;
* domínio.

Registrar dados inválidos:

* acertos maiores que questões;
* duração negativa;
* zero questões;
* data inválida.

Confirmar rejeição.

---

# 48. Testes de correção de simulado

Registrar:

* disciplinas;
* assuntos problemáticos;
* causas de erro;
* observações;
* problemas de tempo.

Confirmar:

* atualização das métricas;
* atualização da prioridade;
* atualização do domínio;
* atualização do Banco de Erros, quando selecionado;
* atualização das Estatísticas;
* atualização do Dashboard.

---

# 49. Testes do Dashboard

Validar:

* sem dados;
* poucos dados;
* grande volume;
* datas;
* percentuais;
* totais;
* cards;
* gráficos;
* atualização após sessão;
* atualização após questões;
* atualização após erro;
* atualização após revisão;
* atualização após simulado;
* atualização após limpeza de testes.

Confirmar ausência de:

* `#N/A`;
* `#REF!`;
* valores fictícios;
* intervalos quebrados;
* gráficos vazios inválidos.

---

# 50. Testes da aba Estatísticas

Validar filtros por:

* período;
* disciplina;
* assunto;
* tipo;
* status;
* fonte;
* simulado.

Confirmar:

* cálculos corretos;
* totais;
* percentuais;
* ausência de duplicidade;
* atualização;
* estados vazios;
* legibilidade.

---

# 51. Testes de experiência

O Codex deverá verificar autonomamente:

* menu visível;
* Sidebars abrindo;
* campos claros;
* botões funcionando;
* mensagens;
* carregamentos;
* cancelamentos;
* resumos;
* quantidade de cliques;
* ausência de erros técnicos visíveis.

O Product Owner ficará responsável apenas pela avaliação subjetiva:

* preferência visual;
* conforto;
* clareza percebida;
* utilidade;
* facilidade de uso cotidiano.

---

# 52. Testes de performance

Executar medições reais quando possível.

Registrar:

* operação;
* quantidade de registros;
* tempo;
* resultado.

Verificar especialmente:

* setup;
* Continuar Ciclo;
* Aproveitar Tempo;
* conclusão de sessão;
* conclusão de bloco;
* atualização do Dashboard;
* atualização das Estatísticas;
* geração de agenda;
* integridade;
* backup.

Corrigir operações excessivamente lentas quando houver solução segura.

---

# 53. Testes de segurança

Confirmar:

* ausência de credenciais;
* ausência de conteúdo protegido;
* ausência de API externa;
* ausência de CDN;
* permissões mínimas;
* proteções;
* locks;
* IDs;
* validações;
* backups;
* logs sem dados sensíveis.

---

# 54. Ciclo autônomo de correção

Quando um teste falhar:

```text
Registrar falha
↓
Criar ou atualizar BUG
↓
Analisar causa
↓
Corrigir localmente
↓
Validar localmente
↓
Executar clasp push
↓
Executar na planilha de teste
↓
Repetir o teste
↓
Executar regressão
↓
Atualizar TESTES_FASE_4.md
```

Não solicitar ao Product Owner que corrija código.

Não apresentar a versão 1.0 com bug crítico aberto.

---

# 55. Limpeza dos dados de teste

Após os testes:

1. identificar todos os registros de teste;
2. criar backup;
3. remover somente dados marcados;
4. preservar dados oficiais;
5. preservar configurações;
6. preservar disciplinas;
7. preservar assuntos;
8. executar integridade;
9. atualizar Dashboard;
10. atualizar Estatísticas;
11. confirmar ausência de resíduos;
12. registrar a limpeza.

Não apagar:

* dados reais;
* registros sem identificação de teste;
* documentos;
* backups válidos;
* histórico oficial.

---

# 56. Implantação na planilha principal

Após a aprovação técnica no ambiente de teste:

1. confirmar `.clasp.json` principal;
2. confirmar planilha principal;
3. criar backup `PRE_V1_FINAL`;
4. validar arquivos locais;
5. executar `clasp status`;
6. executar `clasp push`;
7. abrir o Apps Script principal;
8. executar migração ou setup seguro;
9. abrir a planilha principal;
10. validar estrutura;
11. executar integridade;
12. validar menu;
13. validar Sidebars;
14. validar Dashboard;
15. validar Estatísticas;
16. validar simulados;
17. executar teste rápido de regressão;
18. confirmar ausência de dados de teste.

Não enviar para o projeto errado.

Não utilizar `--force` sem análise.

---

# 57. Teste rápido final na planilha principal

Executar um teste controlado e reversível:

* abrir menu;
* abrir Configurações;
* atualizar Dashboard;
* executar integridade;
* criar backup;
* abrir Sidebars;
* validar agenda;
* validar leitura dos dados existentes.

Não criar um ciclo, bloco ou simulado real sem necessidade.

Caso seja necessário criar dado de teste:

* identificá-lo;
* removê-lo;
* executar integridade novamente.

---

# 58. README final

Criar ou finalizar na raiz:

```text
README.md
```

O README deverá conter:

## Apresentação

* nome;
* objetivo;
* concurso;
* tecnologias;
* versão.

## Funcionalidades

* Continuar Ciclo;
* Retomar Ciclo;
* Aproveitar Tempo;
* Barra de Energia;
* Modo Emergência;
* questões;
* Banco de Erros;
* revisões;
* simulados;
* Dashboard;
* Estatísticas;
* backup;
* integridade.

## Requisitos

* conta Google;
* Google Sheets;
* Apps Script;
* permissões necessárias.

## Instalação

Passo a passo.

## Comece em 5 minutos

1. abrir planilha;
2. executar setup;
3. recarregar;
4. abrir menu;
5. configurar;
6. clicar em Continuar Ciclo;
7. informar tempo e energia;
8. iniciar.

## Como usar

Explicar o fluxo cotidiano.

## Questões e erros

Passo a passo.

## Revisões

Passo a passo.

## Simulados

Passo a passo.

## Dashboard e Estatísticas

Explicar indicadores.

## Backup e recuperação

Passo a passo.

## Integridade

Passo a passo.

## Solução de problemas

Problemas comuns.

## Limitações da versão 1.0

Ser transparente.

## Estrutura do projeto

Explicar pastas e arquivos.

## Segurança

Explicar o que não é armazenado.

## Versão

```text
SOEA v1.0.0
```

O README deverá ser compreensível para uma pessoa sem experiência com Apps Script.

---

# 59. Revisão da documentação

Verificar coerência entre:

* `PRD.md`;
* `ARQUITETURA.md`;
* `INSTRUCOES.md`;
* `AMBIENTE_AUTONOMO.md`;
* `ROADMAP.md`;
* `TODO.md`;
* `CHANGELOG.md`;
* `REVIEW.md`;
* `README.md`;
* `FORMULAS_SOEA.md`;
* `TESTES_FASE_2.md`;
* `TESTES_FASE_3.md`;
* `TESTES_FASE_4.md`.

Não modificar o PRD ou a Arquitetura para justificar implementação incorreta.

Em caso de divergência:

1. corrigir a implementação;
2. registrar o problema;
3. solicitar decisão quando necessário.

---

# 60. Identificação da versão

Preparar:

```text
SOEA v1.0.0
```

Atualizar a versão em:

* `Constants.gs`;
* Configurações internas;
* Sidebar Sobre;
* `README.md`;
* `CHANGELOG.md`;
* `REVIEW.md`;
* relatórios;
* locais visíveis apropriados.

Não marcar como estável enquanto houver:

* bug crítico;
* bug alto impeditivo;
* teste principal reprovado;
* risco de perda de dados;
* instalação não validada;
* atualização não validada;
* regressão não validada.

---

# 61. Controle de versão com Git

Caso o projeto utilize Git:

1. executar `git status`;
2. verificar arquivos sensíveis;
3. confirmar `.gitignore`;
4. revisar as alterações;
5. não incluir credenciais;
6. criar commit final quando apropriado;
7. utilizar mensagem clara;
8. criar tag `v1.0.0` somente após aprovação final do Product Owner.

Antes da aprovação final, não criar tag estável definitiva.

Poderá ser utilizado estado candidato, como:

```text
v1.0.0-rc1
```

somente se fizer sentido para o projeto e for documentado.

Não executar `push --force`.

---

# 62. Critérios de aceite técnico

A Fase 4 somente poderá ser apresentada para revisão quando:

* ambiente estiver `PRONTO_COMPLETO`;
* bugs críticos abertos forem zero;
* bugs altos impeditivos forem zero;
* instalação limpa estiver aprovada;
* segunda instalação estiver aprovada;
* atualização da Fase 3 estiver aprovada;
* regressão do Motor estiver aprovada;
* sistema de simulados estiver funcional;
* agenda estiver funcional;
* agenda for idempotente;
* não existirem simulados retroativos indevidos;
* simulados atualizarem métricas;
* Dashboard estiver finalizado;
* Estatísticas estiverem funcionais;
* Banco de Erros estiver utilizável;
* Configurações estiverem seguras;
* backup estiver validado;
* recuperação estiver validada;
* integridade estiver aprovada;
* performance tiver sido revisada;
* segurança tiver sido revisada;
* dados de teste tiverem sido removidos;
* planilha principal tiver sido atualizada;
* validação final tiver sido realizada;
* README estiver concluído;
* documentação estiver atualizada;
* versão `1.0.0` estiver preparada;
* nenhuma fase posterior tiver sido criada.

---

# 63. Atualização do ROADMAP

Atualizar `docs/ROADMAP.md`.

Registrar:

* Fase 4 implementada;
* percentual;
* implantação;
* testes;
* regressão;
* bugs;
* correções;
* limitações;
* situação da versão;
* aprovação pendente.

Utilizar estado semelhante a:

```text
Fase 4 — 100% implementada e testada

Versão — SOEA v1.0.0

Status — Aguardando aprovação final do Product Owner
```

Não marcar o projeto como definitivamente concluído antes da aprovação.

---

# 64. Atualização do TODO

Atualizar `docs/TODO.md`.

Separar:

* tarefas concluídas;
* pendências críticas;
* pendências não críticas;
* testes pendentes;
* bugs;
* limitações;
* melhorias futuras;
* itens adiados.

Para apresentação da versão:

```text
Pendências críticas: 0
```

Não apagar o histórico.

---

# 65. Atualização do CHANGELOG

Preparar:

```text
## [1.0.0] — AAAA-MM-DD
```

Registrar:

## Adicionado

* simulados;
* agenda;
* correção de simulados;
* Dashboard final;
* Estatísticas;
* documentação final;
* testes finais.

## Alterado

* experiência de uso;
* mensagens;
* performance;
* abas visíveis;
* Sidebars;
* Configurações;
* backup;
* recuperação.

## Corrigido

* bugs da Fase 3;
* duplicidades;
* problemas de métricas;
* problemas de gráficos;
* problemas de interface;
* problemas de instalação.

## Segurança

* preservação de dados;
* permissões;
* locks;
* validações;
* backups;
* remoção de credenciais.

## Conhecido

* limitações não impeditivas;
* itens adiados.

A versão deverá permanecer aguardando aprovação final.

---

# 66. Atualização do REVIEW

Criar ou atualizar:

```text
REVISÃO DA FASE 4 — FINALIZAÇÃO E ENTREGA DA VERSÃO 1.0
```

Incluir:

* objetivo;
* ambiente;
* planilha de teste;
* planilha principal;
* projeto Apps Script;
* entregas;
* arquivos criados;
* arquivos alterados;
* testes;
* regressões;
* bugs;
* correções;
* performance;
* segurança;
* dados de teste;
* limpeza;
* implantação final;
* limitações;
* instruções de validação;
* critérios de aceite;
* situação da versão.

Adicionar checklist:

* [ ] Instalação validada.
* [ ] Segunda instalação validada.
* [ ] Atualização validada.
* [ ] Menu validado.
* [ ] Continuar Ciclo validado.
* [ ] Retomar Ciclo validado.
* [ ] Aproveitar Tempo validado.
* [ ] Questões validadas.
* [ ] Banco de Erros validado.
* [ ] Revisões validadas.
* [ ] Simulados validados.
* [ ] Dashboard validado.
* [ ] Estatísticas validadas.
* [ ] Backup validado.
* [ ] Recuperação validada.
* [ ] Integridade validada.
* [ ] Dados de teste removidos.
* [ ] README validado.
* [ ] Versão 1.0 aprovada.

Não incluir credenciais.

---

# 67. Intervenções humanas permitidas

Solicitar intervenção apenas para:

* autenticação;
* conta Google;
* CAPTCHA;
* OAuth;
* confirmação sensível;
* decisão de produto;
* risco real de perda de dados;
* avaliação subjetiva;
* aprovação final.

Não solicitar que o Product Owner:

* execute `clasp`;
* copie código;
* execute funções técnicas;
* procure logs;
* teste idempotência;
* crie planilha de teste manualmente, quando o Codex puder criar;
* corrija código;
* limpe dados;
* atualize documentos;
* valide cálculos técnicos.

---

# 68. Pontos para avaliação do Product Owner

O Product Owner deverá avaliar principalmente:

* aparência;
* conforto visual;
* clareza;
* utilidade;
* sequência das ações;
* quantidade de cliques;
* coerência da estratégia;
* clareza das justificativas;
* facilidade de uso diário;
* confiança para iniciar os estudos.

Os testes técnicos executados pelo Codex não precisarão ser repetidos integralmente.

---

# 69. Saída final no chat

Ao concluir, responder:

```text
Fase 4 executada.

Versão preparada:
- SOEA v1.0.0.

Ambiente:
- status PRONTO_COMPLETO;
- projeto Apps Script validado;
- planilha de teste validada;
- planilha principal validada.

Implantação:
- alterações enviadas com clasp;
- testes executados na planilha de teste;
- correções reenviadas;
- regressões executadas;
- versão final enviada à planilha principal;
- validação final concluída.

Entregas:
- sistema de simulados;
- agenda de simulados;
- correção de simulados;
- Dashboard final;
- Estatísticas;
- melhorias de experiência;
- melhorias de performance;
- documentação final.

Testes:
- aprovados: quantidade;
- reprovados: quantidade;
- bloqueados: quantidade.

Bugs abertos:
- críticos: quantidade;
- altos: quantidade;
- médios: quantidade;
- baixos: quantidade.

Dados de teste:
- estratégia utilizada;
- limpeza concluída;
- integridade confirmada.

Documentação atualizada:
- README.md;
- TESTES_FASE_4.md;
- ROADMAP.md;
- TODO.md;
- CHANGELOG.md;
- REVIEW.md.

Limitações:
- lista ou “Nenhuma limitação impeditiva”.

Nenhuma funcionalidade fora do escopo foi adicionada.

A versão ainda depende da aprovação final do Product Owner.

Aguardando revisão final.
```

Não declarar o projeto definitivamente aprovado.

Não criar uma Fase 5.

Não iniciar versão 2.0.

Não implementar melhorias futuras após apresentar a entrega.

Aguardar aprovação explícita.

---

# 70. Aprovação final

Somente após o Product Owner responder de forma equivalente a:

```text
Fase 4 aprovada.

A versão SOEA v1.0.0 está aprovada para uso.
```

o Codex poderá:

1. atualizar `ROADMAP.md` para concluído;
2. atualizar `REVIEW.md` para aprovado;
3. atualizar `CHANGELOG.md` com a data final;
4. marcar `SOEA v1.0.0` como versão estável;
5. criar a tag `v1.0.0`, caso Git esteja sendo utilizado;
6. confirmar a conclusão do projeto.

Nesse momento:

* não alterar funcionalidades;
* não adicionar melhorias;
* não mudar requisitos;
* não iniciar nova versão;
* não apagar históricos;
* não remover documentos de teste.

Responder apenas com um resumo final da entrega.
