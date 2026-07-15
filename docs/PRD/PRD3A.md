# ===================================================================
# PRD - SOEA
# Sistema Operacional de Estudos Adaptativo
# PARTE 3A
#
# Modelo de Dados e Estrutura da Planilha
# ===================================================================

# 32. MODELO DE DADOS

A Planilha Inteligente SOEA utilizará o Google Sheets como mecanismo de persistência de dados.

Todas as informações utilizadas pelo Motor do SOEA serão armazenadas em abas ocultas da própria planilha.

O usuário jamais deverá manipular essas abas diretamente.

Toda leitura, escrita, atualização e exclusão deverá ocorrer exclusivamente através do Google Apps Script.

O Google Sheets será responsável por:

- Interface
- Armazenamento
- Relatórios
- Dashboard
- Gráficos

O Google Apps Script será responsável por:

- Toda regra de negócio
- Geração dos blocos
- Atualização dos indicadores
- Controle do ciclo
- Controle das revisões
- Banco de erros
- Simulados
- Menus
- Sidebars
- Automação completa da planilha

---

# 33. ESTRUTURA DA PLANILHA

A planilha será dividida em dois grupos.

## Abas Visíveis

Representam a interface utilizada pelo usuário.

São as únicas abas que poderão ser manipuladas manualmente.

## Abas Ocultas

Representam o banco de dados interno da planilha.

Jamais deverão ser editadas manualmente.

Toda manipulação será realizada exclusivamente pelo Google Apps Script.

---

# 34. ABAS VISÍVEIS

A versão 1.0 deverá possuir apenas as seguintes abas.

## Dashboard

Página inicial.

Responsável por apresentar:

• Resumo da preparação.

• Próximo bloco.

• Revisões pendentes.

• Estatísticas.

• Indicadores.

• Simulados.

• Banco de erros.

---

## Ciclo

Exibe exclusivamente o bloco atual.

Também será utilizada para:

• Continuar Ciclo

• Aproveitar Tempo

• Encerrar Sessão

---

## Banco de Erros

Consulta completa dos erros registrados.

Permite filtros por:

Disciplina

Assunto

Data

Motivo

Status

---

## Simulados

Histórico dos simulados.

Registro de desempenho.

Comparação entre simulados.

---

## Estatísticas

Indicadores completos da preparação.

---

## Configurações

Interface para alteração das configurações.

Esta aba nunca armazenará os dados.

Ela apenas editará os registros existentes na aba _db_Config.

---

# 35. ABAS OCULTAS

Todas as abas abaixo serão criadas automaticamente.

Jamais deverão ser editadas manualmente.

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

_db_Backup

---

# 36. _db_Disciplinas

## Objetivo

Armazenar todas as disciplinas presentes no edital.

Esses dados serão criados automaticamente durante a configuração inicial da planilha.

O usuário nunca cadastrará disciplinas manualmente.

---

## Campos

disciplina_id

nome

peso_edital

prioridade_base

ordem

status

ultima_atualizacao

---

## Regras

Cada disciplina deverá possuir um identificador único.

O peso será utilizado pelo Índice de Prioridade.

---

# 37. _db_Assuntos

## Objetivo

Armazenar todos os assuntos do edital.

Esses registros serão gerados automaticamente pelo Codex durante a configuração inicial.

O Codex deverá:

- analisar o edital;

- analisar o curso do Estratégia;

- localizar o conteúdo correspondente;

- criar automaticamente os registros.

---

## Campos

assunto_id

disciplina_id

nome

ordem_estudo

tempo_teoria_padrao

questoes_padrao

possui_correspondencia

status

ultima_atualizacao

---

## Regras

Nenhum assunto será cadastrado manualmente.

Caso não exista conteúdo correspondente no Estratégia.

O campo:

possui_correspondencia

deverá ser marcado como FALSE.

---

# 38. _db_Ciclo

## Objetivo

Representar a preparação atual.

Na versão 1.0 existirá apenas um ciclo ativo.

---

## Campos

ciclo_id

status

data_inicio

data_fim

percentual_edital

total_blocos

blocos_concluidos

ultima_atualizacao

---

## Estados

Ativo

Concluído

Arquivado

---

## Regras

Na versão 1.0 existirá apenas:

CYC-001

O usuário nunca visualizará esse identificador.

---

# 39. _db_Blocos

## Objetivo

Representar cada execução de estudo.

Cada assunto do edital gera exatamente um bloco.

---

## Campos

bloco_id

ciclo_id

disciplina_id

assunto_id

status

tempo_previsto

tempo_real

questoes_previstas

questoes_realizadas

percentual

data_inicio

data_conclusao

ultima_atualizacao

---

## Estados

Não iniciado

Em andamento

Concluído

Cancelado

---

## Regras

Nunca poderão existir dois blocos "Em andamento".

Cada bloco pertence obrigatoriamente a:

- um ciclo;

- uma disciplina;

- um assunto.

---

# 40. _db_Sessoes

## Objetivo

Registrar todas as sessões de estudo.

---

## Campos

sessao_id

bloco_id

tipo

tempo_previsto

tempo_real

energia

hora_inicio

hora_fim

data

status

ultima_atualizacao

---

## Tipos

Continuar Ciclo

Aproveitar Tempo

Modo Emergência

---

## Regras

Toda sessão deverá pertencer a um bloco.

Jamais existirão sessões órfãs.

---

# 41. _db_Questoes

## Objetivo

Registrar apenas indicadores das questões.

A planilha não armazenará os enunciados.

---

## Campos

questao_id

bloco_id

disciplina_id

assunto_id

fonte

quantidade

acertos

erros

percentual

tempo_total

tempo_medio

ultima_atualizacao

---

## Regras

Sempre que uma sessão terminar.

As estatísticas deverão ser atualizadas automaticamente.

---

# 42. _db_Revisoes

## Objetivo

Controlar todas as revisões.

---

## Campos

revisao_id

bloco_id

tipo

data_prevista

data_realizada

status

resultado

ultima_atualizacao

---

## Tipos

D+1

D+7

D+15

D+30

Extra

---

## Estados

Pendente

Concluída

Atrasada

---

## Regras

Ao concluir um bloco.

O Google Apps Script deverá criar automaticamente todas as revisões previstas.

As revisões pertencem ao bloco.

Nunca ao ciclo.

---

# 43. _db_Erros

## Objetivo

Representar o Banco de Erros.

---

## Campos

erro_id

bloco_id

disciplina_id

assunto_id

motivo

causa_raiz

observacao

status

data

ultima_atualizacao

---

## Motivos

Não conhecia

Esqueci

Interpretação

Confusão

Desatenção

Chute

Outro

---

## Estados

Novo

Revisado

Resolvido

---

## Regras

Cada erro pertence obrigatoriamente a um bloco.

---

# 44. _db_Simulados

## Objetivo

Registrar todos os simulados.

---

## Campos

simulado_id

nome

data

tempo

questoes

acertos

erros

percentual

observacoes

ultima_atualizacao

---

# 45. _db_Config

## Objetivo

Centralizar todas as configurações da planilha.

A aba Configurações funcionará apenas como interface.

Os valores reais permanecerão nesta aba.

---

## Campos

tempo_padrao_teoria

tempo_padrao_questao

questoes_padrao

dias_revisao

meta_horas_semana

meta_questoes_semana

peso_desempenho

peso_revisoes

peso_edital

ultima_atualizacao

---

## Regras

Toda alteração realizada pelo usuário deverá atualizar automaticamente esta aba.

---

# 46. _db_Metricas

## Objetivo

Centralizar todos os indicadores utilizados pelo Dashboard.

---

## Campos

horas_estudadas

questoes_realizadas

questoes_corretas

questoes_erradas

blocos_concluidos

revisoes_realizadas

simulados_realizados

percentual_edital

indice_prioridade

indice_dominio

sequencia_dias

ultimo_estudo

ultima_atualizacao

---

## Regras

Todos os indicadores serão atualizados automaticamente pelo Google Apps Script.

---

# 47. _db_Historico

## Objetivo

Registrar todas as ações relevantes realizadas na planilha.

---

## Exemplos

Sessão iniciada

Sessão encerrada

Bloco iniciado

Bloco concluído

Revisão criada

Erro registrado

Simulado registrado

Configuração alterada

---

## Campos

historico_id

tipo

descricao

referencia_id

data

hora

ultima_atualizacao

---

# 48. _db_Backup

## Objetivo

Permitir recuperação dos dados.

---

## Regras

Toda alteração crítica deverá gerar automaticamente um ponto de restauração.

A política de retenção será configurável.

---

# FIM DA PARTE 3A