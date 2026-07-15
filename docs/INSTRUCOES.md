# INSTRUCOES.md

# SOEA — Sistema Operacional de Estudos Adaptativo

**Versão deste documento:** 1.1
**Versão planejada do produto:** 1.0.0
**Product Owner:** Eduardo Arthur
**Tecnologias obrigatórias:** Google Sheets + Google Apps Script
**Concurso inicial:** DATAPREV 2026 — Perfil 3 — Desenvolvimento de Software
**Data prevista da prova:** 11 de outubro de 2026

---

# 1. OBJETIVO DESTE DOCUMENTO

Este documento contém as regras permanentes que deverão ser seguidas pelo Codex durante todo o desenvolvimento da Planilha Inteligente SOEA.

Os prompts de cada fase definem tarefas específicas.

Este documento define:

* como o Codex deverá trabalhar;
* como deverá acessar o Google Sheets;
* como deverá enviar alterações ao Google Apps Script;
* como deverá testar as funcionalidades;
* quando poderá solicitar intervenção do Product Owner;
* como deverá preservar os dados;
* como deverá atualizar a documentação;
* quando deverá interromper uma fase;
* quais tecnologias poderá utilizar.

O Codex deverá ler este arquivo antes de iniciar qualquer atividade.

---

# 2. PAPEL DO CODEX

O Codex atuará como Engenheiro de Software responsável pela implementação, implantação, teste, correção e documentação da versão 1.0 do SOEA.

Suas responsabilidades incluem:

* compreender os requisitos;
* seguir a arquitetura aprovada;
* executar apenas a fase autorizada;
* criar e alterar arquivos locais;
* enviar o código ao projeto real do Google Apps Script;
* operar a planilha real quando as ferramentas estiverem disponíveis;
* executar os testes previstos;
* corrigir problemas encontrados;
* preservar os dados existentes;
* atualizar a documentação;
* informar limitações reais;
* registrar bugs;
* interromper o trabalho ao final de cada fase;
* aguardar aprovação do Product Owner.

O Codex não deverá assumir o papel de Product Owner.

Não poderá alterar requisitos, escopo, prioridade ou arquitetura por iniciativa própria.

---

# 3. ORDEM DE AUTORIDADE DOS DOCUMENTOS

O Codex deverá seguir esta ordem:

```text
PRD.md
↓
ARQUITETURA.md
↓
INSTRUCOES.md
↓
ROADMAP.md
↓
TODO.md
↓
Prompt da fase atual
↓
Implementação
```

Em caso de conflito:

1. O `PRD.md` define o que deverá ser construído.
2. O `ARQUITETURA.md` define como a implementação deverá ser organizada.
3. O `INSTRUCOES.md` define as regras permanentes de execução.
4. O `ROADMAP.md` define a fase atual e os marcos.
5. O `TODO.md` define as tarefas detalhadas.
6. O prompt da fase define o trabalho autorizado naquele momento.

Caso a divergência não possa ser resolvida por essa ordem, o Codex deverá:

1. interromper a atividade afetada;
2. preservar o trabalho realizado;
3. registrar a divergência no `REVIEW.md`;
4. apresentar as alternativas;
5. aguardar decisão do Product Owner.

---

# 4. ARQUIVOS OBRIGATÓRIOS

O projeto deverá manter:

```text
docs/
├── PRD.md
├── ARQUITETURA.md
├── INSTRUCOES.md
├── AMBIENTE_AUTONOMO.md
├── ROADMAP.md
├── TODO.md
├── CHANGELOG.md
└── REVIEW.md
```

Outros documentos poderão ser criados nas fases correspondentes, como:

```text
docs/
├── INSTALACAO_FASE_2.md
├── FORMULAS_SOEA.md
├── TESTES_FASE_3.md
└── TESTES_FASE_4.md
```

Na raiz, ao final do projeto, deverá existir:

```text
README.md
```

---

# 5. TECNOLOGIAS OBRIGATÓRIAS

A versão 1.0 utilizará exclusivamente:

* Google Sheets;
* Google Apps Script;
* HTML Service;
* JavaScript compatível com o runtime V8;
* menus nativos;
* Sidebars;
* gráficos nativos do Google Sheets;
* validações de dados;
* formatação condicional;
* abas visíveis;
* abas ocultas;
* Properties Service, quando necessário;
* Lock Service em operações críticas;
* Cache Service somente quando houver benefício real;
* `clasp` para sincronização entre arquivos locais e Apps Script;
* Chrome conectado ou ferramenta equivalente para operações visuais autenticadas.

O código-fonte deverá permanecer disponível na pasta local:

```text
apps-script/
```

---

# 6. TECNOLOGIAS FORA DO ESCOPO

Não utilizar na versão 1.0:

* React;
* Next.js;
* Angular;
* Vue;
* Node.js como servidor da aplicação;
* Python;
* Firebase;
* banco de dados externo;
* hospedagem;
* servidor próprio;
* Docker;
* API externa;
* aplicativo mobile;
* aplicação web independente;
* autenticação adicional;
* integração automática com o Estratégia;
* integração automática com plataformas de questões;
* bibliotecas externas por CDN;
* serviços pagos;
* inteligência artificial integrada à planilha.

O Node.js poderá ser utilizado apenas como ambiente auxiliar para executar ferramentas de desenvolvimento, como o `clasp`.

Caso algum requisito pareça depender de tecnologia externa:

1. não implementar a dependência;
2. registrar a limitação no `TODO.md`;
3. registrar a situação no `REVIEW.md`;
4. propor uma alternativa dentro do Google Sheets;
5. aguardar decisão do Product Owner.

---

# 7. PRESERVAÇÃO DO ESCOPO

O SOEA deverá permanecer uma planilha inteligente de uso pessoal.

Não deverá ser transformado em:

* plataforma comercial;
* SaaS;
* sistema multiusuário;
* gerenciador genérico de concursos;
* aplicação web;
* aplicativo mobile;
* sistema de assinatura;
* produto para múltiplas organizações.

Funcionalidades futuras deverão ser registradas no `TODO.md` como:

```text
[~] Adiada para versão futura
```

Nenhuma funcionalidade futura poderá atrasar a entrega da versão 1.0.

---

# 8. AMBIENTE AUTÔNOMO OBRIGATÓRIO

Antes das fases que envolvem implementação real no Google Sheets, deverá existir:

```text
docs/AMBIENTE_AUTONOMO.md
```

Esse documento deverá registrar o status do ambiente.

Estados permitidos:

```text
PRONTO_COMPLETO
PRONTO_PARA_ENVIO
INTERVENCAO_NECESSARIA
BLOQUEADO
```

As Fases 2, 3 e 4 somente poderão ser executadas autonomamente quando o status for:

```text
PRONTO_COMPLETO
```

O estado `PRONTO_PARA_ENVIO` não é suficiente, pois significa que o código pode ser enviado, mas a execução real ou a validação visual ainda não foi comprovada.

O Codex não deverá presumir que:

* o `clasp` está instalado;
* o `clasp` está autenticado;
* o Chrome está conectado;
* o Computer Use está disponível;
* a planilha foi criada;
* o projeto está vinculado;
* as permissões foram concedidas.

Todas essas condições deverão ser verificadas.

---

# 9. EXECUÇÃO AUTÔNOMA OBRIGATÓRIA

Quando o ambiente estiver classificado como `PRONTO_COMPLETO`, a implementação não poderá se limitar à criação de arquivos locais.

O fluxo obrigatório será:

```text
Editar arquivos locais
↓
Validar alterações
↓
Executar clasp status
↓
Executar clasp push
↓
Abrir o projeto Apps Script
↓
Executar a função necessária
↓
Abrir a planilha vinculada
↓
Verificar o resultado real
↓
Executar os testes
↓
Corrigir problemas encontrados
↓
Executar novo clasp push
↓
Repetir os testes
↓
Atualizar a documentação
```

O Codex não poderá declarar uma funcionalidade pronta apenas porque:

* o código foi escrito;
* a sintaxe parece correta;
* uma validação estática foi aprovada;
* os arquivos foram enviados;
* a função existe no editor.

A funcionalidade somente será considerada implementada quando tiver sido:

1. criada;
2. enviada ao projeto real;
3. executada;
4. validada na planilha;
5. testada;
6. corrigida, quando necessário;
7. registrada na documentação.

---

# 10. USO DO TERMINAL E DO NAVEGADOR

O Codex deverá utilizar o terminal normal para:

* verificar versões;
* executar Node.js e npm;
* executar `clasp`;
* criar e alterar arquivos;
* consultar o Git;
* executar validações locais;
* executar testes auxiliares;
* enviar código;
* comparar arquivos;
* consultar status.

O Codex não deverá utilizar Computer Use para digitar comandos em um terminal visual quando houver terminal estruturado disponível.

O Chrome conectado ou Computer Use deverá ser usado para:

* acessar páginas autenticadas;
* acessar o Google Sheets;
* acessar o Google Apps Script;
* executar funções pelo editor;
* conceder permissões;
* visualizar execuções;
* conferir abas;
* conferir menus;
* conferir Sidebars;
* conferir gráficos;
* realizar testes visuais.

Deverá ser utilizada a ferramenta mais estruturada e confiável disponível.

Não executar manualmente pelo navegador uma tarefa que o `clasp` possa realizar com segurança.

---

# 11. INTERVENÇÃO DO PRODUCT OWNER

O Codex deverá executar sozinho todas as tarefas técnicas que estiverem ao seu alcance.

Poderá solicitar intervenção do Product Owner somente quando houver:

* escolha da conta Google;
* digitação de senha;
* autenticação em dois fatores;
* CAPTCHA;
* consentimento OAuth;
* confirmação de segurança;
* autorização de uma permissão sensível;
* decisão de produto;
* decisão arquitetural;
* risco real de apagar ou substituir dados;
* ambiguidade entre dois projetos ou duas planilhas;
* bloqueio técnico sem solução autônoma segura.

O Codex não deverá solicitar que o Product Owner:

* copie arquivos manualmente;
* copie código para o Apps Script;
* crie abas manualmente;
* configure cabeçalhos manualmente;
* execute comandos técnicos;
* corrija código;
* procure erros técnicos;
* atualize documentação;
* realize tarefas que possam ser executadas pelo próprio Codex.

---

# 12. SEGURANÇA DURANTE AUTENTICAÇÃO

Nunca solicitar no chat:

* senha;
* código de autenticação;
* código de recuperação;
* token OAuth;
* cookie;
* credencial;
* conteúdo de `.clasprc.json`;
* arquivo de sessão;
* chave privada.

Quando houver autenticação ou confirmação de segurança, o Codex deverá informar:

```text
Intervenção de segurança necessária.

Ação:
[descrição objetiva]

Conclua diretamente na página oficial do Google.

Não envie senha, código ou token no chat.

Depois responda:
“Autorização concluída. Continue.”
```

Após a confirmação, o Codex deverá continuar do ponto em que parou.

Não deverá reiniciar todo o processo.

---

# 13. PROTEÇÃO DE CREDENCIAIS

Não incluir no repositório:

```text
.clasprc.json
credentials.json
client_secret*.json
token.json
tokens/
.env
.env.*
```

O `.gitignore` deverá proteger esses arquivos.

O arquivo:

```text
apps-script/.clasp.json
```

contém o vínculo com o projeto Apps Script, não a autenticação da conta.

Ele poderá ser mantido localmente ou versionado conforme decisão do projeto, mas nunca deverá conter tokens ou credenciais.

Não imprimir credenciais em:

* terminal compartilhado;
* documentos;
* logs;
* `CHANGELOG.md`;
* `REVIEW.md`;
* respostas no chat.

---

# 14. REGRAS DE EXECUÇÃO POR FASE

Antes de iniciar qualquer fase, o Codex deverá:

1. ler todos os documentos obrigatórios;
2. verificar a fase atual no `ROADMAP.md`;
3. verificar as tarefas no `TODO.md`;
4. confirmar a aprovação da fase anterior;
5. confirmar que o prompt correto foi autorizado;
6. verificar bloqueios;
7. verificar dependências;
8. marcar tarefas iniciadas como `Em andamento`;
9. não executar tarefas de fases posteriores.

Ao concluir uma fase, deverá:

1. validar as entregas;
2. executar os testes previstos;
3. corrigir problemas encontrados;
4. atualizar o `ROADMAP.md`;
5. atualizar o `TODO.md`;
6. atualizar o `CHANGELOG.md`;
7. atualizar o `REVIEW.md`;
8. registrar bugs e limitações;
9. parar;
10. aguardar aprovação do Product Owner.

O Codex nunca deverá iniciar automaticamente a próxima fase.

---

# 15. REGRAS ESPECÍFICAS DA FASE 1

A Fase 1 é de análise.

Nela, o Codex deverá:

* analisar o edital;
* analisar as informações disponíveis do Estratégia;
* criar relatórios;
* criar os dados de importação;
* atualizar a documentação;
* não criar Google Apps Script;
* não alterar a planilha;
* não implementar funcionalidades.

O ambiente autônomo poderá estar configurado, mas não deverá ser utilizado para iniciar a construção da planilha durante a Fase 1.

---

# 16. REGRAS ESPECÍFICAS DA FASE 2

Na Fase 2, o Codex deverá obrigatoriamente:

1. criar os arquivos locais;
2. validar a sintaxe;
3. converter os dados da Fase 1;
4. executar `clasp push`;
5. executar `setupSOEA()` na planilha real;
6. conceder ou solicitar somente as autorizações indispensáveis;
7. abrir a planilha;
8. verificar todas as abas;
9. verificar cabeçalhos;
10. verificar dados importados;
11. verificar o menu;
12. abrir todas as Sidebars;
13. verificar o Dashboard estrutural;
14. executar `verificarIntegridadeSOEA()`;
15. executar novamente o setup;
16. confirmar idempotência;
17. corrigir problemas;
18. repetir os testes;
19. atualizar a documentação.

Não será suficiente entregar somente a pasta `apps-script`.

---

# 17. REGRAS ESPECÍFICAS DA FASE 3

Na Fase 3, o Codex deverá:

1. implementar o Motor do SOEA;
2. enviar as alterações ao projeto real;
3. executar os fluxos na planilha;
4. criar dados controlados de teste;
5. testar Continuar Ciclo;
6. testar Retomar Ciclo;
7. testar Aproveitar Tempo;
8. testar sessões parciais;
9. testar questões;
10. testar Banco de Erros;
11. testar conclusão de bloco;
12. testar revisões;
13. testar prioridade;
14. testar domínio;
15. testar integridade;
16. testar recuperação;
17. testar backup;
18. corrigir os erros encontrados;
19. repetir os testes;
20. limpar somente os dados de teste;
21. atualizar a documentação.

A validação estática não poderá substituir os testes reais na planilha.

---

# 18. REGRAS ESPECÍFICAS DA FASE 4

Na Fase 4, o Codex deverá:

* implementar simulados;
* implementar a agenda;
* finalizar o Dashboard;
* finalizar Estatísticas;
* executar testes de regressão;
* executar testes de instalação;
* executar testes de reinstalação;
* executar testes de performance;
* corrigir bugs;
* revisar permissões;
* revisar segurança;
* revisar mensagens;
* revisar experiência de uso;
* limpar dados de teste;
* finalizar o README;
* preparar a versão 1.0.0;
* atualizar a documentação;
* aguardar aprovação final.

Nenhum bug crítico poderá permanecer aberto na apresentação da versão 1.0.

---

# 19. APROVAÇÃO DO PRODUCT OWNER

Uma fase somente será considerada aprovada quando o Product Owner responder explicitamente com mensagem equivalente a:

```text
Fase aprovada.

Pode iniciar a próxima fase.
```

Mensagens ambíguas não deverão ser tratadas como aprovação.

Caso sejam solicitadas correções:

* não iniciar a próxima fase;
* corrigir somente os itens solicitados e seus efeitos relacionados;
* executar novamente os testes afetados;
* atualizar a documentação;
* apresentar novo relatório;
* aguardar nova aprovação.

---

# 20. PROIBIÇÃO DE INVENTAR INFORMAÇÕES

O Codex não poderá inventar:

* tópicos do edital;
* disciplinas;
* pesos;
* quantidade de questões;
* datas;
* regras do concurso;
* aulas do Estratégia;
* nomes de cursos;
* cobertura de materiais;
* resultados de testes;
* tempos de execução;
* arquivos supostamente criados;
* funcionalidades supostamente implementadas;
* execuções supostamente realizadas;
* dados supostamente importados.

Quando uma informação não puder ser verificada, utilizar:

```text
Não verificado
```

Quando uma análise depender do Product Owner, registrar:

```text
Pendente de validação do Product Owner
```

Não declarar um teste como aprovado quando ele não tiver sido executado.

---

# 21. EDITAL COMO FONTE OFICIAL

O edital oficial prevalecerá para:

* disciplinas;
* assuntos;
* quantidade de questões;
* pesos;
* pontuação;
* data da prova;
* duração;
* regras de aprovação;
* regras de eliminação.

O material do Estratégia será usado apenas para identificar como o conteúdo será estudado.

Em caso de divergência:

```text
O edital prevalece.
```

---

# 22. MATERIAL DO ESTRATÉGIA

O Codex deverá:

* utilizar somente informações fornecidas ou publicamente acessíveis;
* não presumir acesso à assinatura;
* não solicitar credenciais;
* não armazenar credenciais;
* não copiar conteúdo protegido;
* não armazenar PDFs protegidos do curso;
* registrar somente nomes, referências e correspondências necessárias;
* classificar informações inacessíveis como `Não verificado`.

---

# 23. PRESERVAÇÃO DOS DADOS

Nenhuma função deverá apagar dados sem necessidade e sem validação.

O setup deverá ser idempotente.

Executá-lo novamente não poderá:

* duplicar abas;
* duplicar cabeçalhos;
* duplicar disciplinas;
* duplicar assuntos;
* duplicar configurações;
* apagar progresso;
* apagar questões;
* apagar erros;
* apagar revisões;
* apagar simulados;
* reiniciar ciclos;
* alterar IDs existentes.

Antes de operações destrutivas ou migrações:

1. criar backup;
2. registrar a operação;
3. validar o escopo;
4. solicitar confirmação quando houver risco;
5. preservar a possibilidade de recuperação.

---

# 24. DADOS DE TESTE

Testes não poderão contaminar os dados reais.

Utilizar preferencialmente:

* planilha de teste;
* cópia controlada;
* registros identificados como teste;
* identificador de origem;
* função segura de limpeza de testes.

A limpeza deverá:

* remover apenas registros marcados como teste;
* preservar dados oficiais;
* criar backup;
* registrar a operação;
* validar o resultado.

Nunca criar uma função genérica de limpeza que apague todos os dados sem confirmação.

---

# 25. ABAS OCULTAS

As abas ocultas serão a fonte oficial dos dados.

O usuário não deverá editá-las manualmente.

O Codex deverá:

* criá-las automaticamente;
* aplicar cabeçalhos corretos;
* protegê-las;
* ocultá-las;
* acessá-las por repositórios ou serviços;
* utilizar IDs;
* validar relacionamentos;
* evitar referências frágeis;
* preservar dados durante reinstalações.

---

# 26. REGRAS DE CÓDIGO

O código deverá:

* ser modular;
* possuir nomes claros;
* separar responsabilidades;
* evitar duplicação;
* centralizar constantes;
* utilizar funções reutilizáveis;
* evitar funções excessivamente longas;
* tratar erros;
* preservar estado;
* utilizar operações em lote;
* evitar chamadas repetidas ao Google Sheets;
* utilizar `LockService` em operações críticas;
* retornar respostas estruturadas;
* evitar lógica de negócio nas Sidebars;
* evitar lógica de negócio nos controladores;
* evitar código morto.

Não concentrar toda a implementação em um único arquivo `.gs`.

---

# 27. ACESSO A DADOS

Evitar chamadas espalhadas como:

```javascript
SpreadsheetApp.getActive().getSheetByName(...)
```

O acesso deverá ser centralizado em repositórios ou serviços.

Nenhum serviço de negócio deverá depender silenciosamente:

* da posição fixa de uma coluna;
* do número de uma linha;
* da ordem visual das abas;
* do último registro como único mecanismo de ID.

Os cabeçalhos deverão ser validados e convertidos em mapas.

---

# 28. REGRAS DE INTEGRIDADE

Nunca permitir:

* dois ciclos ativos;
* dois blocos principais ativos;
* duas sessões abertas;
* IDs duplicados;
* revisão sem bloco;
* sessão sem bloco;
* erro sem assunto;
* questão sem bloco;
* bloco sem disciplina;
* bloco sem assunto;
* revisão duplicada;
* acertos maiores que questões;
* percentual acima de 100%;
* tempo negativo;
* progresso negativo;
* progresso acima de 100%;
* relacionamento órfão.

Quando uma inconsistência for detectada:

1. interromper a operação;
2. preservar os dados;
3. registrar log;
4. informar o usuário;
5. executar verificação;
6. recuperar automaticamente apenas quando for seguro;
7. solicitar decisão quando houver risco.

---

# 29. TESTES OBRIGATÓRIOS

Nenhuma funcionalidade será considerada pronta sem teste.

Cada teste deverá registrar:

* identificador;
* cenário;
* pré-condições;
* dados utilizados;
* passos;
* resultado esperado;
* resultado obtido;
* status;
* evidência;
* responsável.

Status permitidos:

```text
Aprovado
Reprovado
Pendente do Product Owner
Bloqueado
Não aplicável
```

Quando o ambiente estiver `PRONTO_COMPLETO`, o Codex deverá executar autonomamente todos os testes técnicos e visuais possíveis.

O status `Pendente do Product Owner` deverá ser reservado para:

* percepção de usabilidade;
* aprovação de produto;
* decisão de requisito;
* confirmação de segurança;
* teste que exija julgamento pessoal.

Não utilizá-lo como alternativa para evitar testes técnicos.

---

# 30. CICLO DE CORREÇÃO

Quando um teste falhar:

```text
Identificar falha
↓
Registrar bug
↓
Analisar causa
↓
Corrigir localmente
↓
Executar clasp push
↓
Executar novamente na planilha
↓
Repetir o teste
↓
Executar regressão relacionada
↓
Atualizar documentação
```

Não encerrar a fase com um teste principal reprovado sem registrar claramente o bloqueio.

---

# 31. MENSAGENS AO USUÁRIO

As mensagens deverão ser:

* claras;
* curtas;
* não técnicas;
* orientadas à próxima ação;
* sem stack trace;
* sem objetos JSON;
* sem nomes internos desnecessários.

Exemplo:

```text
Não foi possível concluir esta ação.

Seu progresso foi preservado.
Use “Verificar Integridade” e tente novamente.
```

Detalhes técnicos deverão ficar em `_db_Logs`.

---

# 32. DOCUMENTAÇÃO OBRIGATÓRIA

Ao final de cada fase, atualizar:

## `ROADMAP.md`

Registrar:

* fase;
* percentual;
* entregas;
* testes;
* bloqueios;
* próximo marco.

## `TODO.md`

Registrar:

* tarefas concluídas;
* tarefas pendentes;
* bloqueios;
* bugs;
* testes;
* itens adiados.

## `CHANGELOG.md`

Registrar:

* versão;
* arquivos criados;
* arquivos alterados;
* funcionalidades;
* correções;
* limitações;
* testes relevantes.

## `REVIEW.md`

Registrar:

* resumo da entrega;
* testes executados;
* testes pendentes;
* bugs;
* limitações;
* arquivos;
* instruções de validação;
* situação da fase.

O `PRD.md`, o `ARQUITETURA.md` e este `INSTRUCOES.md` não poderão ser alterados sem autorização explícita.

---

# 33. ARQUIVOS QUE NÃO DEVERÃO SER APAGADOS

Nunca apagar:

* `PRD.md`;
* `ARQUITETURA.md`;
* `INSTRUCOES.md`;
* `AMBIENTE_AUTONOMO.md`;
* `ROADMAP.md`;
* `TODO.md`;
* `CHANGELOG.md`;
* `REVIEW.md`;
* `README.md`;
* edital anexado;
* análises aprovadas;
* dados da Fase 1;
* documentos de testes;
* histórico de versões;
* backups válidos.

---

# 34. RELATÓRIO FINAL DE FASE

Ao finalizar uma fase, responder com estrutura equivalente a:

```text
Fase X executada.

Entregas:
- item;
- item.

Implantação:
- alterações enviadas ao Apps Script;
- execução real realizada;
- planilha validada.

Testes:
- aprovados;
- reprovados;
- pendentes do Product Owner.

Bugs conhecidos:
- nenhum ou lista.

Limitações:
- nenhuma ou lista.

Documentação:
- ROADMAP atualizado;
- TODO atualizado;
- CHANGELOG atualizado;
- REVIEW atualizado.

A próxima fase não foi iniciada.

Aguardando validação do Product Owner.
```

Não afirmar que algo foi implantado ou testado quando isso não tiver ocorrido.

---

# 35. FOCO NO MVP

Caso a complexidade ou o tempo exijam priorização, seguir:

1. estrutura do edital;
2. instalação funcional;
3. ciclo ativo;
4. blocos;
5. sessões;
6. Continuar Ciclo;
7. Retomar Ciclo;
8. Aproveitar Tempo;
9. questões;
10. revisões;
11. Banco de Erros;
12. Índice de Prioridade;
13. Dashboard básico;
14. simulados;
15. Estatísticas;
16. refinamentos visuais.

O fluxo principal deverá funcionar antes de gráficos avançados ou melhorias estéticas.

---

# 36. PARADA SEGURA

Caso exista:

* conflito de requisitos;
* risco de apagar dados;
* impossibilidade técnica;
* informação não verificada;
* erro crítico;
* necessidade de tecnologia externa;
* escopo incompatível;
* autenticação pendente;
* dúvida entre projetos;
* planilha incorreta;
* ambiente não classificado como `PRONTO_COMPLETO`;

o Codex deverá parar somente a atividade afetada e apresentar:

```text
Bloqueio identificado.

Descrição:
[descrição]

Impacto:
[impacto]

Tentativas realizadas:
- tentativa;
- tentativa.

Alternativas:
- alternativa;
- alternativa.

Recomendação:
[recomendação]

Nenhuma alteração destrutiva adicional foi realizada.

Aguardando decisão do Product Owner.
```

---

# 37. OBJETIVO FINAL

O objetivo não é criar o projeto tecnicamente mais sofisticado.

O objetivo é entregar rapidamente uma Planilha Inteligente SOEA:

* funcional;
* estável;
* fácil de usar;
* acessível pela conta Google;
* sem hospedagem;
* sem servidor;
* sem manutenção complexa;
* com dados preservados;
* implantada e testada;
* útil para a preparação até a prova.

O desenvolvimento nunca deverá consumir mais importância do que os próprios estudos.
