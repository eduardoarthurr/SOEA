# PROMPT 01 — FASE 1: ANÁLISE DO EDITAL E DO CURSO

## 1. Instrução inicial

Leia integralmente, antes de executar qualquer tarefa:

* `docs/PRD.md`
* `docs/ARQUITETURA.md`
* `docs/INSTRUCOES.md`
* `docs/ROADMAP.md`
* `docs/TODO.md`
* `docs/CHANGELOG.md`
* `docs/REVIEW.md`

Leia também o edital oficial disponível na pasta:

```text
fontes/
```

Confirme no `ROADMAP.md` e no `TODO.md` que a fase atual é:

```text
Fase 1 — Análise do edital e do curso
```

Caso a Fase 0 não esteja aprovada, não execute esta fase. Registre o bloqueio no `REVIEW.md` e pare.

---

# 2. Objetivo da fase

Transformar o edital oficial da DATAPREV 2026 e as informações disponíveis sobre o pacote do Estratégia Concursos em dados estruturados para a futura construção da Planilha Inteligente SOEA.

Esta fase deve produzir:

* estrutura oficial da prova;
* lista de disciplinas;
* lista de assuntos e subassuntos;
* pesos e quantidades de questões;
* matriz de cobertura do material;
* lacunas do curso;
* estratégia inicial de estudos;
* dados preparados para importação futura.

Esta fase não deve produzir código.

---

# 3. Proibições específicas desta fase

Não:

* criar arquivos `.gs`;
* criar arquivos `.html`;
* implementar Google Apps Script;
* criar ou modificar uma planilha do Google Sheets;
* implementar o Motor do SOEA;
* criar Sidebars;
* criar fórmulas;
* criar o Dashboard;
* iniciar tarefas da Fase 2;
* alterar requisitos do `PRD.md`;
* alterar decisões do `ARQUITETURA.md`;
* inventar dados não encontrados nas fontes.

Arquivos CSV e documentos de análise não são considerados código e podem ser criados nesta fase.

---

# 4. Fontes da análise

## 4.1 Fonte oficial

O edital oficial encontrado na pasta `fontes` é a fonte principal para:

* nome do concurso;
* perfil do cargo;
* banca organizadora;
* data da prova;
* duração;
* quantidade de questões;
* pesos;
* pontuação;
* critérios de aprovação;
* critérios de eliminação;
* disciplinas;
* conteúdo programático;
* demais regras oficiais.

Em caso de divergência com qualquer outra fonte, o edital prevalece.

## 4.2 Material preparatório

Analisar as informações publicamente disponíveis no pacote:

```text
https://www.estrategiaconcursos.com.br/curso/dataprev-perfil-3-desenvolvimento-de-software-pacote-2026-pos-edital/
```

O pacote do Estratégia deve ser usado somente para identificar:

* disciplinas oferecidas;
* cursos incluídos;
* aulas;
* módulos;
* PDFs;
* videoaulas;
* simulados;
* materiais complementares;
* correspondência com o edital.

Não presumir acesso à área de assinantes.

Não solicitar ou utilizar credenciais.

Caso uma informação não esteja publicamente acessível, classificá-la como:

```text
Não verificado
```

---

# 5. Preparação da estrutura de saída

Caso ainda não existam, criar as pastas:

```text
SOEA/
├── analises/
└── dados/
```

Os documentos de análise deverão ser salvos na pasta `analises`.

Os dados estruturados deverão ser salvos na pasta `dados`.

---

# 6. Etapa 1 — Identificação do edital

Antes de extrair o conteúdo, registrar:

* nome completo do concurso;
* número e ano do edital;
* órgão;
* banca organizadora;
* cargo ou perfil analisado;
* localidade considerada, quando aplicável;
* data de publicação;
* eventuais retificações encontradas nos arquivos fornecidos;
* arquivo utilizado como fonte principal.

Verificar se o edital corresponde ao:

```text
Perfil 3 — Desenvolvimento de Software
```

Caso o arquivo não corresponda ao perfil correto, registrar o bloqueio e parar.

---

# 7. Etapa 2 — Estrutura da prova

Extrair e documentar:

* data oficial da prova;
* horário, quando disponível;
* duração;
* quantidade total de questões;
* quantidade por módulo;
* quantidade por disciplina, quando informada;
* peso das questões;
* pontuação máxima;
* nota mínima;
* critérios de eliminação;
* critérios de classificação;
* regra relacionada a zerar disciplina ou módulo;
* formato das questões;
* demais regras que afetem o planejamento dos estudos.

Não calcular ou inferir informações que não estejam previstas no edital sem deixar explícito que se trata de estimativa.

Criar:

```text
analises/01_Estrutura_Prova.md
```

---

# 8. Etapa 3 — Extração das disciplinas

Extrair todas as disciplinas do Perfil 3.

Preservar os nomes oficiais apresentados no edital.

Separar corretamente:

* Conhecimentos Gerais;
* Conhecimentos Específicos;
* módulos ou grupos adicionais, caso existam.

Para cada disciplina, registrar:

* ID;
* nome oficial;
* módulo;
* quantidade de questões;
* peso;
* pontuação máxima;
* prioridade-base;
* ordem inicial;
* status inicial;
* observação.

Utilizar o formato de ID:

```text
DSC-001
DSC-002
DSC-003
```

Não utilizar o nome da disciplina como ID.

---

# 9. Etapa 4 — Extração dos assuntos

Para cada disciplina, extrair:

* assuntos;
* tópicos;
* subtópicos relevantes;
* descrições oficiais do conteúdo programático.

Preservar a redação oficial do edital em um campo próprio.

Quando um tópico for excessivamente amplo, ele poderá ser dividido em unidades de estudo menores, desde que:

* o texto original seja preservado;
* a divisão seja claramente identificada como operacional;
* nenhum conteúdo novo seja inventado;
* a divisão facilite a criação de blocos de estudo;
* a divisão não seja excessivamente granular.

Para cada assunto, registrar:

* ID;
* ID da disciplina;
* disciplina;
* nome operacional;
* texto oficial do edital;
* assunto-pai, quando houver;
* ordem inicial;
* status inicial;
* observação.

Utilizar o formato:

```text
ASU-0001
ASU-0002
ASU-0003
```

---

# 10. Etapa 5 — Análise do pacote do Estratégia

Analisar as informações realmente disponíveis na página do pacote.

Registrar:

* nome do pacote;
* disciplinas;
* cursos incluídos;
* nomes dos professores, quando visíveis e relevantes;
* quantidade de aulas, quando disponível;
* módulos;
* PDFs;
* videoaulas;
* simulados;
* trilhas;
* materiais extras;
* atualizações indicadas;
* conteúdos adicionais que não estejam no edital.

Não copiar conteúdo protegido.

Registrar apenas informações necessárias ao planejamento.

Criar:

```text
analises/02_Analise_Estrategia.md
```

Caso a página não possa ser acessada ou esteja incompleta, documentar exatamente:

* o que foi possível verificar;
* o que não foi possível verificar;
* a razão da limitação;
* quais dados dependem de conferência posterior pelo Product Owner.

---

# 11. Etapa 6 — Matriz edital × Estratégia

Para cada assunto extraído do edital, procurar o material correspondente no pacote do Estratégia.

Utilizar as seguintes classificações:

```text
Completa
Parcial
Ausente
Não verificada
```

## Completa

Utilizar quando houver evidência suficiente de que o material cobre integralmente o assunto do edital.

## Parcial

Utilizar quando o material cobrir apenas parte do tópico ou quando o tópico do edital for mais amplo que a aula encontrada.

## Ausente

Utilizar quando a estrutura disponível do curso indicar que o assunto não possui material correspondente.

## Não verificada

Utilizar quando não houver informação pública suficiente para confirmar ou negar a cobertura.

Para cada correspondência, registrar:

* disciplina;
* ID do assunto;
* assunto do edital;
* texto oficial;
* curso correspondente;
* aula ou módulo correspondente;
* tipo de material;
* classificação da cobertura;
* justificativa da classificação;
* observação;
* necessidade de material complementar.

Criar:

```text
analises/03_Matriz_Cobertura.md
```

A matriz deverá conter todos os assuntos do edital.

Nenhum assunto poderá ficar sem classificação.

---

# 12. Etapa 7 — Identificação de lacunas

Criar uma análise separada contendo:

* assuntos com cobertura ausente;
* assuntos com cobertura parcial;
* assuntos não verificados;
* conteúdos do curso que excedem o edital;
* tópicos que precisam de conferência manual;
* possíveis riscos de preparação;
* necessidades de material complementar.

Não recomendar a compra de produtos ou cursos adicionais sem necessidade concreta.

Quando sugerir uma fonte complementar, explicar:

* qual lacuna ela atende;
* por que o material principal pode ser insuficiente;
* se a recomendação é obrigatória ou opcional.

Criar:

```text
analises/04_Lacunas_Materiais.md
```

---

# 13. Etapa 8 — Estratégia inicial de estudos

Propor os parâmetros iniciais do SOEA considerando:

* peso das disciplinas;
* quantidade de questões;
* pontuação;
* risco de eliminação;
* amplitude do conteúdo;
* prioridade de Conhecimentos Específicos;
* necessidade de não abandonar Conhecimentos Gerais;
* cobertura do curso;
* data da prova;
* metodologia definida no `PRD.md`.

A metodologia-base é:

```text
Teoria
↓
Questões
↓
Correção
↓
Banco de Erros
↓
Revisões
↓
Novo bloco
```

Para cada disciplina, sugerir:

* prioridade inicial de 0 a 100;
* proporção inicial entre teoria e questões;
* tempo inicial recomendado de teoria;
* quantidade inicial de questões por bloco;
* frequência mínima de contato;
* observações metodológicas.

Para cada assunto, sugerir:

* tempo inicial estimado de teoria;
* quantidade inicial de questões;
* ordem sugerida;
* prioridade inicial;
* necessidade de material complementar;
* justificativa resumida.

Esses valores serão parâmetros iniciais e não decisões permanentes.

A planilha poderá ajustá-los futuramente conforme o desempenho do usuário.

Criar:

```text
analises/05_Estrategia_Inicial.md
```

---

# 14. Etapa 9 — Dados de disciplinas

Criar:

```text
dados/disciplinas.csv
```

O arquivo deverá possuir, no mínimo, as colunas:

```text
id_disciplina
nome
modulo
quantidade_questoes
peso
pontuacao_maxima
prioridade_base
ordem_inicial
frequencia_minima
status
observacao
fonte
```

Regras:

* utilizar codificação UTF-8;
* incluir cabeçalho;
* não duplicar disciplinas;
* utilizar ponto como separador decimal, quando necessário;
* não incluir fórmulas;
* manter nomes oficiais;
* utilizar IDs únicos;
* registrar `Não informado` quando o edital não trouxer um valor;
* não preencher com zero quando zero significar uma informação diferente de “não informado”.

---

# 15. Etapa 10 — Dados de assuntos

Criar:

```text
dados/assuntos.csv
```

O arquivo deverá possuir, no mínimo, as colunas:

```text
id_assunto
id_disciplina
disciplina
assunto_operacional
texto_oficial_edital
id_assunto_pai
ordem_inicial
material_correspondente
aula_modulo
tipo_material
cobertura
prioridade_inicial
tempo_teoria_minutos
quantidade_questoes_inicial
material_complementar
status
observacao
fonte
```

Regras:

* utilizar IDs únicos;
* preservar o texto oficial;
* manter o relacionamento com a disciplina;
* não criar registros órfãos;
* não duplicar assuntos;
* validar a classificação de cobertura;
* utilizar `Não verificado` quando necessário.

---

# 16. Etapa 11 — Configurações iniciais

Criar:

```text
dados/config_inicial.csv
```

Utilizar as colunas:

```text
chave
valor
tipo
categoria
descricao
fonte
editavel_usuario
```

Preparar configurações relacionadas a:

* data da prova;
* revisões D+1;
* revisões D+7;
* revisões D+15;
* revisões D+30;
* tempos iniciais;
* quantidade inicial de questões;
* metas semanais, quando definidas no PRD;
* parâmetros iniciais de energia;
* parâmetros iniciais do ciclo;
* pesos iniciais do Índice de Prioridade, apenas se já estiverem definidos;
* pesos iniciais do Índice de Domínio, apenas se já estiverem definidos.

Não inventar as fórmulas finais dos índices.

Caso elas ainda estejam previstas para a Fase 3, registrar a configuração como pendente.

---

# 17. Etapa 12 — Validação dos dados

Antes de concluir, verificar:

* se todas as disciplinas possuem ID;
* se todos os assuntos possuem ID;
* se todo assunto está associado a uma disciplina existente;
* se não existem IDs duplicados;
* se não existem disciplinas duplicadas;
* se não existem assuntos omitidos;
* se todos os assuntos possuem classificação de cobertura;
* se pesos e questões correspondem ao edital;
* se a pontuação calculada é compatível com a estrutura da prova;
* se campos não encontrados foram corretamente identificados;
* se todas as fontes foram registradas;
* se os arquivos estão em UTF-8;
* se os arquivos CSV podem ser importados posteriormente.

Registrar o resultado da validação em:

```text
analises/06_Validacao_Dados.md
```

Não declarar a validação como aprovada quando depender de conferência do Product Owner.

---

# 18. Etapa 13 — Relatório consolidado

Criar:

```text
analises/00_Resumo_Fase_1.md
```

O relatório deverá apresentar:

1. resumo executivo;
2. fonte oficial utilizada;
3. estrutura da prova;
4. total de disciplinas;
5. total de assuntos;
6. quantidade de assuntos com cobertura completa;
7. quantidade com cobertura parcial;
8. quantidade ausente;
9. quantidade não verificada;
10. principais lacunas;
11. prioridades iniciais;
12. arquivos produzidos;
13. limitações;
14. bloqueios;
15. itens que precisam de validação do Product Owner;
16. conclusão da fase.

Não esconder incertezas.

---

# 19. Atualização da documentação

Ao final, atualizar obrigatoriamente:

## `docs/ROADMAP.md`

Registrar:

* andamento da Fase 1;
* percentual concluído;
* entregas realizadas;
* bloqueios;
* próximo marco.

## `docs/TODO.md`

* marcar tarefas realmente concluídas;
* manter pendentes as tarefas não verificadas;
* registrar novos bloqueios;
* registrar verificações que dependem do Product Owner;
* não marcar a Fase 1 inteira como concluída antes da revisão.

## `docs/CHANGELOG.md`

Preparar a versão:

```text
0.1.0
```

Registrar:

* documentos criados;
* dados criados;
* análises realizadas;
* limitações;
* decisões relevantes.

A versão deverá permanecer como candidata à aprovação até a decisão do Product Owner.

## `docs/REVIEW.md`

Criar ou atualizar a seção:

```text
REVISÃO DA FASE 1 — ANÁLISE DO EDITAL E DO CURSO
```

Incluir:

* objetivo;
* entregas;
* arquivos criados;
* arquivos alterados;
* verificações realizadas;
* limitações;
* pendências;
* pontos que o Product Owner deverá conferir;
* critérios de aceite;
* status da fase.

Não alterar:

* `docs/PRD.md`;
* `docs/ARQUITETURA.md`;
* `docs/INSTRUCOES.md`.

---

# 20. Saída final no chat

Ao terminar, responder apenas com um resumo objetivo contendo:

```text
Fase 1 executada.

Entregas produzidas:
- lista dos principais arquivos.

Resultados:
- número de disciplinas;
- número de assuntos;
- resumo da cobertura.

Validações pendentes do Product Owner:
- lista.

Bloqueios ou limitações:
- lista ou “Nenhum”.

Documentação atualizada:
- ROADMAP.md;
- TODO.md;
- CHANGELOG.md;
- REVIEW.md.

Nenhum código foi criado.
A Fase 2 não foi iniciada.

Aguardando revisão do Product Owner.
```

Não iniciar a Fase 2.

Não implementar correções não solicitadas após apresentar a entrega.

Aguardar aprovação explícita do Product Owner.
