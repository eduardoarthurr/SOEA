# ===================================================================
# PRD - SOEA
# Sistema Operacional de Estudos Adaptativo
# PARTE 3B
#
# Motor do SOEA, Regras de Negócio e Inteligência da Planilha
# ===================================================================

# 49. MOTOR DO SOEA

## Objetivo

O Motor do SOEA representa o núcleo inteligente da planilha.

Toda decisão deverá ser tomada exclusivamente por ele.

Nenhuma aba visível deverá possuir lógica de decisão.

Toda regra deverá permanecer centralizada no Google Apps Script.

---

## Responsabilidades

O Motor deverá ser responsável por:

• localizar o estado atual do ciclo;

• localizar o bloco ativo;

• verificar revisões pendentes;

• verificar Banco de Erros;

• calcular o Índice de Prioridade;

• calcular o Índice de Domínio;

• gerar o próximo bloco;

• registrar sessões;

• atualizar métricas;

• atualizar Dashboard;

• salvar automaticamente o progresso.

---

# 50. FLUXO DE DECISÃO

Sempre que o usuário clicar em:

CONTINUAR CICLO

o Motor deverá executar obrigatoriamente a sequência abaixo.

PASSO 1

Verificar existência de bloco em andamento.

↓

SIM

↓

Retomar exatamente esse bloco.

↓

NÃO

↓

PASSO 2

Existem revisões pendentes?

↓

SIM

↓

Inserir revisão no próximo bloco.

↓

NÃO

↓

PASSO 3

Calcular Índice de Prioridade.

↓

Selecionar assunto.

↓

Gerar novo bloco.

---

Nenhuma etapa poderá ser ignorada.

---

# 51. GERAÇÃO DE BLOCOS

Todo bloco deverá ser criado automaticamente.

Jamais manualmente.

O Motor deverá utilizar:

• disciplina;

• assunto;

• prioridade;

• tempo disponível;

• energia;

• histórico;

• proximidade da prova.

---

Todo bloco deverá possuir.

ID

Disciplina

Assunto

Tempo previsto

Questões

Objetivo

Status

---

# 52. APROVEITAR TEMPO

A funcionalidade Aproveitar Tempo nunca criará um novo bloco.

Ela apenas consumirá parte do bloco atual.

Fluxo.

Usuário informa.

Tempo disponível.

↓

Motor identifica.

Bloco atual.

↓

Seleciona parte do bloco.

↓

Atualiza progresso.

↓

Salvar automaticamente.

---

Caso todo o bloco seja concluído.

O sistema deverá marcá-lo como concluído.

Gerar revisões.

E atualizar o Dashboard.

---

# 53. ALGORITMO DO ÍNDICE DE PRIORIDADE

O Índice de Prioridade deverá ser recalculado sempre que:

• uma sessão terminar;

• uma revisão for concluída;

• um simulado for registrado;

• um erro for registrado;

• um bloco for concluído.

---

O cálculo deverá considerar.

Peso do edital.

+

Desempenho.

+

Quantidade de erros.

+

Revisões atrasadas.

+

Tempo sem estudar.

+

Proximidade da prova.

---

Quanto maior.

Maior prioridade.

---

# 54. ALGORITMO DO ÍNDICE DE DOMÍNIO

Representa o domínio do usuário sobre determinado assunto.

Deverá considerar.

Acertos.

↓

Revisões.

↓

Simulados.

↓

Reincidência de erros.

---

Quanto maior.

Maior domínio.

---

Nunca deverá diminuir por ausência de estudo.

Apenas por desempenho.

---

# 55. GERAÇÃO DAS REVISÕES

As revisões nunca serão cadastradas manualmente.

Ao concluir um bloco.

O Motor deverá criar automaticamente.

D+1

D+7

D+15

D+30

---

Cada revisão deverá permanecer vinculada ao bloco que a originou.

---

Caso uma revisão atrase.

Ela nunca será excluída.

Seu estado passará para:

ATRASADA.

---

# 56. BANCO DE ERROS

Sempre que uma questão for registrada como incorreta.

O usuário poderá informar.

Motivo.

↓

O Motor registrará automaticamente.

Disciplina.

Assunto.

Bloco.

Data.

Motivo.

---

O Banco de Erros será utilizado para.

• Revisões.

• Índice de Prioridade.

• Estatísticas.

• Dashboard.

---

# 57. TEMPO ESTIMADO INTELIGENTE

Durante os primeiros blocos.

A planilha utilizará tempos padrão.

Após existir histórico suficiente.

O Motor deverá calcular automaticamente.

Tempo médio de teoria.

Tempo médio por questão.

Tempo médio de revisão.

Tempo médio por bloco.

---

As estimativas deverão tornar-se personalizadas.

---

# 58. DASHBOARD

O Dashboard nunca armazenará informações.

Ele será apenas uma camada de visualização.

Todos os dados deverão ser obtidos automaticamente das abas ocultas.

---

O Dashboard deverá apresentar.

• Próximo bloco.

• Revisões pendentes.

• Questões realizadas.

• Horas estudadas.

• Blocos concluídos.

• Simulados.

• Banco de Erros.

• Evolução.

• Percentual do edital.

---

# 59. SINCRONIZAÇÃO

Toda alteração deverá ser salva automaticamente.

Jamais deverá existir botão:

Salvar.

O usuário nunca deverá preocupar-se com sincronização.

Toda alteração será imediatamente persistida.

---

# 60. PERFORMANCE

O Motor deverá evitar:

Leituras desnecessárias.

Atualizações repetidas.

Recalcular indicadores sem necessidade.

---

Sempre que possível.

Os cálculos deverão utilizar apenas os registros alterados.

---

# 61. BACKUP

Toda alteração crítica deverá gerar um registro.

Caso ocorra falha.

O Google Apps Script deverá permitir restaurar o último estado consistente.

---

# 62. REGRAS DE INTEGRIDADE

Jamais poderá existir.

• bloco sem assunto;

• bloco sem disciplina;

• sessão sem bloco;

• revisão sem bloco;

• erro sem bloco;

• questão sem bloco.

---

Nunca poderá existir.

Mais de um bloco "Em andamento".

Mais de um ciclo ativo.

---

Toda inconsistência deverá ser corrigida automaticamente.

---

# 63. CRITÉRIOS GERAIS DE ACEITAÇÃO

O SOEA será considerado corretamente implementado quando:

✔ O usuário nunca precisar decidir o que estudar.

✔ O progresso nunca for perdido.

✔ O Dashboard for atualizado automaticamente.

✔ O ciclo continuar exatamente do ponto onde foi interrompido.

✔ As revisões forem geradas automaticamente.

✔ O Banco de Erros funcionar automaticamente.

✔ Os Índices forem recalculados automaticamente.

✔ Nenhuma aba oculta precisar de edição manual.

✔ Toda lógica permanecer centralizada no Google Apps Script.

✔ A planilha funcionar integralmente dentro do Google Sheets.

---

# 64. EVOLUÇÕES FUTURAS

Os itens abaixo estão fora do escopo da versão 1.0.

• Multiusuário.

• Multi-concurso.

• Aplicação Web.

• Aplicativo Mobile.

• Integração com APIs externas.

• Inteligência Artificial para geração de questões.

• Integração automática com plataformas de questões.

• Sincronização entre diferentes contas Google.

---

# 65. ENCERRAMENTO DA ESPECIFICAÇÃO

Com a conclusão das Partes 1, 2, 3A e 3B, considera-se encerrada a especificação funcional da versão 1.0 da Planilha Inteligente SOEA.

Todo o desenvolvimento deverá seguir rigorosamente este PRD.

Caso seja identificada qualquer necessidade de alteração de requisitos durante a implementação, o PRD deverá ser atualizado antes da implementação.

Qualquer funcionalidade que não esteja prevista neste documento deverá ser considerada fora do escopo da versão 1.0 até aprovação do Product Owner.