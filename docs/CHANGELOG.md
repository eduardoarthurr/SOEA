# CHANGELOG.md

# SOEA — Sistema Operacional de Estudos Adaptativo

Todas as alterações relevantes realizadas na Planilha Inteligente SOEA deverão ser registradas neste documento.

O formato deste arquivo segue, de maneira simplificada, o padrão de changelog por versões.

---

# Regras de atualização

O Codex deverá atualizar este documento sempre que:

* uma fase for concluída;
* uma funcionalidade for criada;
* uma funcionalidade for alterada;
* um bug for corrigido;
* uma limitação for identificada;
* uma decisão técnica relevante for tomada;
* uma versão for preparada para entrega.

Cada registro deverá informar:

* versão;
* data;
* fase;
* tipo de alteração;
* descrição;
* arquivos criados ou alterados;
* observações ou limitações.

O Codex não deverá apagar registros antigos.

---

# Tipos de alteração

Utilizar preferencialmente as categorias abaixo:

## Adicionado

Para novas funcionalidades, arquivos, abas ou recursos.

## Alterado

Para mudanças em funcionalidades ou estruturas existentes.

## Corrigido

Para bugs e comportamentos incorretos.

## Removido

Para itens retirados do projeto.

## Segurança

Para correções relacionadas à integridade ou proteção dos dados.

## Documentação

Para alterações em documentos do projeto.

## Conhecido

Para bugs ou limitações ainda não corrigidos.

---

# Formato padrão

```md
## [versão] — AAAA-MM-DD

### Fase

Nome da fase.

### Adicionado

- Item criado.

### Alterado

- Item modificado.

### Corrigido

- Erro corrigido.

### Arquivos criados

- `Arquivo.gs`

### Arquivos alterados

- `ArquivoExistente.gs`

### Limitações conhecidas

- Limitação identificada.

### Observações

- Informação adicional.
```

Se alguma categoria não possuir alterações, ela poderá ser omitida.

---

# [0.0.1] — Planejamento inicial

## Fase

Fase 0 — Documentação e preparação.

## Adicionado

* Definição inicial da Planilha Inteligente SOEA.
* Definição do método híbrido de estudos.
* Definição da funcionalidade Continuar Ciclo.
* Definição da funcionalidade Retomar Ciclo.
* Definição da funcionalidade Aproveitar Tempo.
* Definição da Barra de Energia.
* Definição dos blocos e sessões de estudo.
* Definição do Banco de Questões.
* Definição do Banco de Erros.
* Definição das revisões automáticas.
* Definição dos simulados.
* Definição do Índice de Prioridade.
* Definição do Índice de Domínio.
* Definição do Tempo Estimado Inteligente.
* Definição do salvamento automático.
* Definição das abas visíveis e ocultas.
* Definição da arquitetura Google Sheets + Google Apps Script.

## Documentação

* Criado o `PRD.md`.
* Criado o `ARQUITETURA.md`.
* Criado o `ROADMAP.md`.
* Criado o `TODO.md`.
* Criado o `CHANGELOG.md`.

## Decisões técnicas

* A versão 1.0 será implementada exclusivamente com Google Sheets e Google Apps Script.
* Não serão utilizados servidores, hospedagem ou banco de dados externo.
* As abas ocultas serão a fonte oficial dos dados.
* Toda lógica de negócio será centralizada no Google Apps Script.
* O desenvolvimento será dividido em fases e dependerá da aprovação do Product Owner.
* O projeto continuará sendo uma planilha inteligente, não uma aplicação web.

## Limitações conhecidas

* Nenhuma implementação foi iniciada.
* A análise do edital e do pacote do Estratégia ainda não foi executada.
* As fórmulas dos Índices de Prioridade e Domínio ainda serão definidas durante a implementação.
* O acesso ao conteúdo do pacote do Estratégia poderá depender da disponibilidade pública da página.

## Próxima etapa

* Criar o `REVIEW.md` inicial.
* Executar a Fase 1: análise do edital e do curso preparatório.

---

# Versões planejadas

## [0.1.0] — Análise concluída

Prevista para o encerramento da Fase 1.

Deverá registrar:

* análise do edital;
* análise do pacote do Estratégia;
* disciplinas extraídas;
* assuntos extraídos;
* matriz de cobertura;
* lacunas encontradas;
* dados preparados para importação.

---

## [0.2.0] — Estrutura da planilha

Prevista para o encerramento da Fase 2.

Deverá registrar:

* abas criadas;
* cabeçalhos;
* validações;
* dados importados;
* menu personalizado;
* Sidebars iniciais;
* Dashboard básico;
* função de instalação.

---

## [0.3.0] — Motor do SOEA

Prevista para o encerramento da Fase 3.

Deverá registrar:

* Continuar Ciclo;
* Retomar Ciclo;
* Aproveitar Tempo;
* sessões;
* blocos;
* questões;
* Banco de Erros;
* revisões;
* Índice de Prioridade;
* Índice de Domínio;
* Tempo Estimado Inteligente;
* integridade;
* histórico;
* backup.

---

## [1.0.0] — Primeira versão estável

Prevista para o encerramento da Fase 4.

Deverá registrar:

* Dashboard final;
* simulados;
* estatísticas;
* testes;
* correções;
* documentação final;
* README;
* bugs conhecidos;
* instruções de instalação e uso;
* aprovação final do Product Owner.

---

# Registro de bugs

Quando um bug for corrigido, utilizar o seguinte formato:

```md
### Corrigido

- **BUG-001 — Título do problema**
  - Causa: descrição da causa.
  - Correção: descrição da solução.
  - Arquivos afetados: `Arquivo.gs`.
  - Teste realizado: descrição do cenário validado.
```

---

# Registro de limitações

Quando uma limitação não puder ser corrigida na versão atual:

```md
### Conhecido

- **LIM-001 — Título da limitação**
  - Descrição: detalhe da limitação.
  - Impacto: baixo, médio, alto ou crítico.
  - Alternativa disponível: solução temporária.
  - Versão sugerida para correção: versão futura.
```

---

# Controle atual

**Versão atual:** `0.0.1`
**Fase atual:** Fase 0 — Documentação
**Situação:** documentação-base em validação final
**Próxima versão planejada:** `0.1.0`
**Próxima fase:** análise do edital e do curso do Estratégia
**Última atualização:** a preencher
