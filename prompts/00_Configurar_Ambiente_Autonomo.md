# PROMPT 00 — CONFIGURAÇÃO DO AMBIENTE AUTÔNOMO

## 1. Objetivo

Configurar e validar o ambiente necessário para que o Codex consiga desenvolver, enviar, executar, testar e corrigir autonomamente o projeto SOEA no Google Sheets e no Google Apps Script.

Esta etapa deverá criar a ponte entre:

```text
Arquivos locais do projeto
↓
clasp
↓
Google Apps Script
↓
Google Sheets
↓
Chrome conectado
↓
Testes visuais e funcionais
```

Ao final, o Codex deverá ser capaz de:

* editar os arquivos locais;
* enviar alterações com `clasp push`;
* acessar o projeto real do Google Apps Script;
* acessar a planilha vinculada;
* executar funções no Apps Script;
* autorizar o script quando necessário;
* verificar visualmente a planilha;
* identificar erros;
* corrigir os arquivos;
* enviar novamente as correções;
* repetir os testes.

Esta etapa não deverá implementar funcionalidades do SOEA.

---

# 2. Escopo desta etapa

Executar somente:

* diagnóstico do ambiente;
* validação do sistema operacional;
* validação do Node.js;
* instalação ou validação do `clasp`;
* ativação do acesso à API do Apps Script;
* autenticação do `clasp`;
* validação do Chrome conectado;
* validação do Computer Use;
* criação da planilha do SOEA;
* criação do projeto Apps Script vinculado;
* configuração local do projeto;
* envio de um script mínimo;
* execução de um teste controlado;
* validação da comunicação local → Google;
* documentação do ambiente.

Não executar:

* análise do edital;
* análise do Estratégia;
* criação das disciplinas;
* criação das abas definitivas;
* criação do Dashboard;
* criação do Motor do SOEA;
* criação de ciclos;
* criação de blocos;
* criação de sessões;
* criação de revisões;
* execução dos Prompts 1, 2, 3 ou 4.

---

# 3. Documentos que deverão ser lidos

Antes de iniciar, leia:

* `docs/PRD.md`
* `docs/ARQUITETURA.md`
* `docs/INSTRUCOES.md`
* `docs/ROADMAP.md`
* `docs/TODO.md`
* `docs/CHANGELOG.md`
* `docs/REVIEW.md`

Utilize esses documentos apenas para compreender o projeto.

Não altere:

* `PRD.md`;
* `ARQUITETURA.md`;
* requisitos funcionais;
* decisões de arquitetura;
* conteúdo oficial do concurso.

Esta etapa é apenas de preparação do ambiente.

---

# 4. Regra de autonomia

Não transfira ao Product Owner tarefas técnicas que possam ser executadas pelo Codex.

O Codex deverá executar autonomamente:

* comandos no terminal;
* criação de pastas;
* criação de arquivos;
* instalação de dependências sem privilégios administrativos, quando possível;
* configuração do `clasp`;
* criação do projeto remoto;
* envio dos arquivos;
* abertura do Apps Script;
* abertura do Google Sheets;
* execução do teste;
* verificação dos resultados;
* correção de problemas técnicos.

Solicite intervenção do Product Owner somente quando houver:

* escolha ou confirmação da conta Google;
* digitação de senha;
* autenticação em dois fatores;
* CAPTCHA;
* consentimento OAuth;
* confirmação de uma permissão sensível;
* aprovação de acesso a um aplicativo ou site;
* decisão que envolva segurança da conta;
* bloqueio que realmente não possa ser resolvido pelo Codex.

Nunca solicite:

* senha;
* código de autenticação;
* código de recuperação;
* token OAuth;
* cookie;
* arquivo de sessão;
* credencial copiada no chat.

Quando uma dessas etapas aparecer, pare apenas naquele ponto e informe claramente:

```text
Intervenção de segurança necessária.

Ação:
Explique exatamente o que deve ser confirmado.

Não envie sua senha ou código no chat.
Conclua diretamente na página oficial do Google e informe quando terminar.
```

Depois da confirmação, continue a execução do ponto em que parou.

---

# 5. Separação entre terminal e interface gráfica

Utilize o terminal normal do ambiente Codex para:

* verificar versões;
* instalar pacotes;
* executar `npm`;
* executar `clasp`;
* criar arquivos;
* editar arquivos;
* executar verificações locais;
* consultar status;
* enviar alterações.

Não utilize Computer Use para digitar comandos em terminal.

Utilize o Chrome conectado ou o Computer Use para:

* abrir páginas autenticadas;
* acessar a conta Google já conectada;
* acessar o Apps Script;
* acessar o Google Sheets;
* conceder acesso a sites;
* selecionar funções no editor;
* executar funções;
* conferir abas;
* conferir menus;
* conferir Sidebars;
* consultar execuções e erros visuais.

Utilize a ferramenta mais estruturada disponível.

Não use cliques no navegador para tarefas que o `clasp` possa executar com segurança.

---

# 6. Diagnóstico inicial

Antes de instalar qualquer coisa, verificar:

## Sistema

Registrar:

* sistema operacional;
* versão do sistema;
* diretório do projeto;
* shell disponível;
* permissões de escrita;
* espaço básico disponível;
* existência de Git, quando aplicável.

## Node.js

Executar:

```bash
node --version
```

Registrar a versão.

A versão deverá ser igual ou superior a:

```text
20.0.0
```

## npm

Executar:

```bash
npm --version
```

## clasp

Executar:

```bash
clasp --version
```

Caso o comando não exista, verificar também:

```bash
npx clasp --version
```

## Chrome conectado

Verificar se:

* o Chrome está instalado;
* o plugin do Chrome está conectado ao Codex;
* a extensão aparece como conectada;
* o perfil correto do Chrome está em uso;
* a conta Google necessária está autenticada.

## Computer Use

Verificar se:

* o recurso está instalado;
* está habilitado;
* possui permissão para usar o Chrome;
* consegue visualizar a janela do navegador;
* consegue operar o navegador quando autorizado.

Não presumir que uma ferramenta está disponível apenas porque foi mencionada no prompt.

---

# 7. Classificação inicial do ambiente

Classifique o ambiente em um dos estados:

## `PRONTO_COMPLETO`

Utilizar quando houver:

* Node.js compatível;
* npm funcional;
* `clasp` funcional;
* autenticação Google válida;
* API do Apps Script habilitada;
* Chrome conectado;
* Computer Use funcional;
* projeto remoto criado;
* envio testado;
* execução real testada;
* planilha real acessível.

## `PRONTO_PARA_ENVIO`

Utilizar quando:

* o `clasp` consegue enviar arquivos;
* mas a execução ou validação visual ainda não funciona.

Esse estado não é suficiente para as Fases 2, 3 e 4.

## `INTERVENCAO_NECESSARIA`

Utilizar quando falta apenas uma ação de segurança do Product Owner, como autorização Google.

## `BLOQUEADO`

Utilizar quando existe impedimento técnico que não pode ser corrigido nesta etapa.

O objetivo obrigatório é alcançar:

```text
PRONTO_COMPLETO
```

Não declarar autonomia total com o estado `PRONTO_PARA_ENVIO`.

---

# 8. Instalação do clasp

Caso o `clasp` não esteja instalado, tentar primeiro:

```bash
npm install --global @google/clasp
```

Se a instalação global falhar por falta de permissão administrativa, não interromper imediatamente.

Utilizar instalação local:

```bash
npm install --save-dev @google/clasp
```

Nesse caso, executar os comandos com:

```bash
npx clasp
```

Definir uma forma única de execução para as próximas fases:

## Instalação global

```text
CLASP_COMMAND=clasp
```

## Instalação local

```text
CLASP_COMMAND=npx clasp
```

Registrar a opção utilizada no relatório do ambiente.

Não exigir privilégio administrativo quando a instalação local resolver o problema.

---

# 9. Proteção de credenciais

Verificar e atualizar o `.gitignore` da raiz.

Garantir que não sejam enviados ao repositório:

```gitignore
.clasprc.json
**/.clasprc.json
credentials.json
client_secret*.json
token.json
tokens/
.env
.env.*
```

Adicionar também, caso a decisão do projeto seja manter o vínculo do Apps Script apenas localmente:

```gitignore
apps-script/.clasp.json
```

Não apagar regras existentes do `.gitignore`.

Não criar credenciais dentro da pasta do projeto.

Não copiar arquivos de autenticação para o repositório.

Não imprimir tokens no terminal, documentos ou chat.

A autenticação padrão do `clasp` deverá ser utilizada sempre que possível.

---

# 10. Ativação do acesso ao Apps Script

Verificar se o acesso de aplicações externas aos projetos do Apps Script está habilitado na conta Google.

Utilizar Chrome conectado para abrir a página oficial de configurações do Google Apps Script.

Caso o acesso esteja desabilitado:

1. navegar até a configuração correta;
2. explicar ao Product Owner o que será habilitado;
3. solicitar confirmação somente se a interface ou política exigir;
4. não solicitar credenciais;
5. habilitar o acesso após a autorização;
6. registrar a alteração.

Não habilitar APIs, serviços ou permissões não relacionados ao projeto.

Não criar um projeto Google Cloud separado sem necessidade.

O objetivo desta etapa é permitir que o `clasp` gerencie o projeto Apps Script.

---

# 11. Autenticação do clasp

Executar:

```bash
clasp login
```

Ou, se estiver usando instalação local:

```bash
npx clasp login
```

O comando deverá abrir o fluxo oficial de autenticação do Google.

Quando a página de login ou consentimento aparecer:

* utilize o Chrome conectado;
* não digite senhas;
* não aprove autenticação em dois fatores;
* não copie códigos;
* solicite intervenção do Product Owner somente para a etapa de segurança;
* continue após a autorização.

Depois da autenticação, verificar:

```bash
clasp list
```

ou:

```bash
npx clasp list
```

Não considerar a autenticação concluída apenas porque o navegador mostrou uma mensagem de sucesso.

Confirmar pelo resultado do terminal.

---

# 12. Verificação de projeto existente

Antes de criar uma nova planilha, verificar se já existe no projeto local:

```text
apps-script/.clasp.json
```

Verificar também se há uma planilha ou projeto Apps Script já criado para o SOEA.

Utilizar:

```bash
clasp list
```

e, quando necessário, o Google Drive pelo Chrome conectado.

Procurar por nomes como:

```text
SOEA
SOEA — Sistema Operacional de Estudos Adaptativo
Planilha Inteligente SOEA
```

Caso exista um projeto válido:

* não criar duplicata;
* confirmar se ele pertence ao projeto atual;
* confirmar se está vinculado a uma planilha;
* utilizar o projeto existente;
* registrar o ID localmente;
* preservar arquivos remotos;
* criar backup antes de sobrescrever conteúdo.

Caso existam vários projetos semelhantes e não seja possível determinar qual é o correto, pare e solicite uma decisão do Product Owner.

---

# 13. Criação da pasta local

Caso ainda não exista, criar:

```text
apps-script/
```

Todos os comandos do `clasp` deverão ser executados dentro dessa pasta.

Estrutura inicial:

```text
SOEA/
├── apps-script/
├── docs/
├── fontes/
└── prompts/
```

Não criar as funcionalidades finais nesta etapa.

---

# 14. Criação da planilha e do projeto vinculado

Caso não exista um projeto válido, entre na pasta:

```bash
cd apps-script
```

Criar uma nova planilha com projeto Apps Script vinculado.

Utilizar:

```bash
clasp create "SOEA — Sistema Operacional de Estudos Adaptativo" --type sheets
```

Ou, com instalação local:

```bash
npx clasp create "SOEA — Sistema Operacional de Estudos Adaptativo" --type sheets
```

O resultado deverá criar:

```text
apps-script/.clasp.json
apps-script/appsscript.json
```

Confirmar que:

* o arquivo `.clasp.json` existe;
* o `scriptId` está preenchido;
* o manifesto existe;
* o projeto remoto aparece na conta Google;
* uma planilha vinculada foi criada.

Não criar um projeto `standalone`.

O projeto deverá ser vinculado ao Google Sheets.

---

# 15. Vinculação a uma planilha já existente

Caso o Product Owner tenha criado previamente a planilha correta, utilizar o ID dela.

Executar dentro de `apps-script/`:

```bash
clasp create "SOEA — Sistema Operacional de Estudos Adaptativo" --type sheets --parentId ID_DA_PLANILHA
```

Ou:

```bash
npx clasp create "SOEA — Sistema Operacional de Estudos Adaptativo" --type sheets --parentId ID_DA_PLANILHA
```

Não inventar o ID.

Obter o ID pela URL oficial da planilha ou pelo contexto fornecido.

Não criar uma segunda planilha quando uma planilha correta já estiver disponível.

---

# 16. Manifesto mínimo

Validar o `appsscript.json`.

Garantir inicialmente:

```json
{
  "timeZone": "America/Sao_Paulo",
  "exceptionLogging": "STACKDRIVER",
  "runtimeVersion": "V8"
}
```

Preservar outros campos válidos criados automaticamente.

Não adicionar escopos OAuth manualmente sem necessidade.

Não adicionar:

* APIs externas;
* serviços avançados;
* bibliotecas externas;
* implantação web;
* permissões desnecessárias.

---

# 17. Script mínimo de diagnóstico

Criar temporariamente:

```text
apps-script/EnvironmentCheck.gs
```

Implementar uma função semelhante a:

```javascript
function validarAmbienteSOEA() {
  const spreadsheet = SpreadsheetApp.getActiveSpreadsheet();

  if (!spreadsheet) {
    throw new Error('O projeto não está vinculado a uma planilha.');
  }

  const timestamp = new Date();
  const temporarySheetName = `_SOEA_ENV_TEST_${timestamp.getTime()}`;

  const temporarySheet = spreadsheet.insertSheet(temporarySheetName);

  try {
    temporarySheet.getRange('A1:B3').setValues([
      ['Teste', 'Resultado'],
      ['Projeto vinculado', 'OK'],
      ['Data', timestamp]
    ]);

    SpreadsheetApp.flush();

    const writtenValue = temporarySheet.getRange('B2').getValue();

    if (writtenValue !== 'OK') {
      throw new Error('A escrita na planilha não foi confirmada.');
    }

    const result = {
      success: true,
      spreadsheetId: spreadsheet.getId(),
      spreadsheetName: spreadsheet.getName(),
      spreadsheetUrl: spreadsheet.getUrl(),
      testedAt: timestamp.toISOString()
    };

    console.log(JSON.stringify(result));

    return result;
  } finally {
    spreadsheet.deleteSheet(temporarySheet);
  }
}
```

A função deverá:

* acessar a planilha vinculada;
* criar uma aba temporária;
* escrever dados;
* ler os dados;
* confirmar o valor;
* excluir a aba temporária;
* retornar um resultado estruturado;
* não deixar dados de teste permanentes;
* não alterar abas reais.

A função poderá ser ajustada para respeitar limitações reais do Apps Script, mas não deverá implementar funcionalidades do SOEA.

---

# 18. Envio inicial com clasp

Dentro da pasta `apps-script`, executar:

```bash
clasp status
```

Depois:

```bash
clasp push
```

Ou os equivalentes com `npx`.

Confirmar pelo terminal:

* arquivos reconhecidos;
* manifesto reconhecido;
* envio concluído;
* ausência de erro de autenticação;
* ausência de erro da API;
* ausência de projeto inválido.

Se houver conflito com arquivos remotos:

1. não utilizar `--force` imediatamente;
2. executar `clasp pull` em uma pasta temporária ou criar cópia de segurança;
3. comparar os arquivos;
4. preservar conteúdo relevante;
5. somente sobrescrever após confirmar que o projeto remoto é o correto.

Não destruir código remoto sem análise.

---

# 19. Abertura do projeto remoto

Executar:

```bash
clasp open-script
```

Ou:

```bash
npx clasp open-script
```

Utilizar o Chrome conectado para verificar:

* o projeto correto foi aberto;
* o arquivo `EnvironmentCheck.gs` está presente;
* o manifesto foi enviado;
* o projeto está vinculado à planilha correta.

Não considerar o teste concluído apenas porque o editor abriu.

---

# 20. Execução real da função

No editor oficial do Google Apps Script:

1. selecionar `validarAmbienteSOEA`;
2. executar a função;
3. aguardar a autorização do Google, se solicitada;
4. solicitar intervenção do Product Owner apenas nas confirmações de segurança;
5. não digitar senha ou código;
6. continuar após a autorização;
7. verificar o resultado da execução;
8. verificar os logs;
9. confirmar que a função terminou sem erro.

Depois, abrir a planilha vinculada e confirmar:

* a planilha está acessível;
* nenhuma aba temporária permaneceu;
* nenhuma aba legítima foi alterada;
* o projeto realmente está vinculado à planilha.

---

# 21. Teste de correção e novo envio

Para confirmar que o ciclo de desenvolvimento funciona:

1. adicionar ao `EnvironmentCheck.gs` um campo de versão do teste;
2. executar novo `clasp push`;
3. confirmar o envio;
4. abrir novamente o projeto;
5. confirmar que a alteração apareceu;
6. executar novamente a função;
7. confirmar sucesso;
8. não deixar dados temporários.

Exemplo de versão:

```javascript
const SOEA_ENVIRONMENT_CHECK_VERSION = '1.0.0';
```

Esse teste deverá comprovar o ciclo:

```text
Editar localmente
↓
Enviar com clasp
↓
Executar remotamente
↓
Verificar o resultado
↓
Corrigir localmente
↓
Enviar novamente
```

---

# 22. Teste do Chrome conectado

Utilizando Chrome conectado ou Computer Use, confirmar que o Codex consegue:

* abrir o projeto Apps Script;
* abrir a planilha vinculada;
* alternar entre as duas páginas;
* visualizar o resultado de uma execução;
* consultar a página de execuções;
* localizar mensagens de erro;
* recarregar a planilha;
* manter a sessão autenticada.

Não realizar alterações em outros arquivos do Google Drive.

Não acessar Gmail, documentos pessoais ou outras áreas não relacionadas.

Limitar o acesso aos domínios e páginas necessários ao projeto.

---

# 23. Condição operacional no Windows

Registrar que, durante testes visuais no Windows:

* a máquina deverá permanecer ligada;
* a sessão deverá permanecer desbloqueada;
* a conexão com a internet deverá permanecer ativa;
* o Chrome deverá permanecer acessível;
* o Computer Use trabalhará na área de trabalho ativa;
* o Product Owner não deverá disputar mouse e teclado durante a operação.

Isso não deverá impedir o Codex de executar operações de terminal normalmente.

Caso a interface gráfica seja necessária e o computador esteja bloqueado, registrar a interrupção sem declarar falha do código.

---

# 24. Verificação de erros comuns

Tratar, quando possível:

## Node incompatível

* informar versão encontrada;
* atualizar apenas se houver autorização e método seguro;
* preferir solução sem privilégios administrativos;
* não alterar instalações corporativas sem permissão.

## `clasp` não encontrado

* tentar instalação global;
* tentar instalação local;
* registrar o método escolhido.

## API do Apps Script desabilitada

* abrir configuração oficial;
* orientar a ativação;
* solicitar confirmação de segurança;
* repetir o comando.

## Não autenticado

* executar `clasp login`;
* concluir fluxo oficial;
* confirmar no terminal.

## Projeto não vinculado

* validar `.clasp.json`;
* confirmar `scriptId`;
* criar ou vincular corretamente.

## Erro no `clasp push`

* ler a mensagem;
* corrigir a causa;
* não utilizar força sem análise;
* repetir o envio.

## Função não encontrada

* confirmar arquivo enviado;
* confirmar nome;
* salvar;
* recarregar o editor;
* repetir.

## Autorização pendente

* orientar o Product Owner;
* não solicitar credenciais;
* continuar depois da autorização.

## Chrome desconectado

* confirmar perfil correto;
* confirmar extensão;
* reconectar o plugin;
* abrir uma nova tarefa quando necessário.

---

# 25. Arquivo de configuração local

Ao final, a pasta `apps-script` deverá conter, no mínimo:

```text
apps-script/
├── .clasp.json
├── appsscript.json
└── EnvironmentCheck.gs
```

O `.clasp.json` deverá apontar para o projeto real.

Não mostrar o conteúdo completo do arquivo em relatórios públicos.

Registrar apenas:

* existência;
* validade;
* projeto vinculado;
* status.

---

# 26. Relatório do ambiente

Criar:

```text
docs/AMBIENTE_AUTONOMO.md
```

O documento deverá conter:

## Informações gerais

* data;
* sistema operacional;
* diretório do projeto;
* versão do Node.js;
* versão do npm;
* versão do `clasp`;
* forma de instalação do `clasp`;
* comando utilizado.

## Integração Google

* API do Apps Script habilitada;
* autenticação concluída;
* projeto criado ou reutilizado;
* planilha criada ou reutilizada;
* projeto vinculado;
* envio com `clasp push`;
* editor aberto;
* execução real concluída;
* planilha acessada.

## Ferramentas visuais

* Chrome conectado;
* Computer Use habilitado;
* acesso ao Apps Script validado;
* acesso ao Google Sheets validado.

## Testes

* envio inicial;
* execução;
* escrita temporária;
* leitura;
* exclusão da aba temporária;
* segundo envio;
* segunda execução.

## Intervenções humanas necessárias

Registrar somente as intervenções realmente solicitadas.

## Limitações

Registrar qualquer limitação encontrada.

## Status final

Utilizar somente:

```text
PRONTO_COMPLETO
PRONTO_PARA_ENVIO
INTERVENCAO_NECESSARIA
BLOQUEADO
```

## Próxima ação

Quando o resultado for `PRONTO_COMPLETO`:

```text
O ambiente está pronto para a execução autônoma das fases do projeto.
```

---

# 27. Atualização do TODO

Atualizar `docs/TODO.md` com uma seção:

```md
## Configuração do ambiente autônomo

- [ ] Node.js 20 ou superior validado.
- [ ] npm validado.
- [ ] clasp instalado.
- [ ] API do Apps Script habilitada.
- [ ] clasp autenticado.
- [ ] Chrome conectado.
- [ ] Computer Use habilitado.
- [ ] Planilha criada ou vinculada.
- [ ] Projeto Apps Script criado.
- [ ] clasp push validado.
- [ ] Execução real validada.
- [ ] Teste de escrita e leitura validado.
- [ ] Segundo envio validado.
- [ ] Ambiente classificado como PRONTO_COMPLETO.
```

Marcar apenas os itens realmente validados.

Não marcar como concluído com base apenas em análise de arquivos.

---

# 28. Atualização do CHANGELOG

Atualizar `docs/CHANGELOG.md`.

Registrar uma entrada de preparação, sem alterar as versões funcionais das fases.

Exemplo:

```md
## [ambiente-autonomo] — AAAA-MM-DD

### Adicionado

- Configuração do clasp.
- Projeto Apps Script vinculado ao Google Sheets.
- Script de verificação do ambiente.
- Relatório AMBIENTE_AUTONOMO.md.

### Validado

- Envio local para o Apps Script.
- Execução real no Google.
- Acesso visual pelo Chrome conectado.

### Limitações

- Listar apenas limitações reais.
```

Não marcar a Fase 1 como concluída.

---

# 29. Atualização do REVIEW

Adicionar ao `docs/REVIEW.md` uma seção:

```md
# REVISÃO DA CONFIGURAÇÃO DO AMBIENTE AUTÔNOMO
```

Incluir:

* objetivo;
* verificações executadas;
* comandos utilizados;
* projeto criado ou reutilizado;
* planilha vinculada;
* testes executados;
* intervenções solicitadas;
* erros encontrados;
* correções;
* limitações;
* status final.

Essa configuração não constitui uma fase funcional do produto.

Não alterar a aprovação da Fase 0.

---

# 30. Critérios de aceite

A configuração somente será considerada concluída quando:

* Node.js 20 ou superior estiver disponível;
* npm estiver funcional;
* `clasp` estiver funcional;
* acesso à API do Apps Script estiver habilitado;
* `clasp login` estiver concluído;
* o projeto estiver vinculado a uma planilha;
* `.clasp.json` estiver válido;
* `clasp push` tiver sido executado com sucesso;
* o script enviado aparecer no editor remoto;
* uma função real tiver sido executada;
* a função tiver criado, escrito, lido e removido uma aba temporária;
* a planilha puder ser aberta pelo Codex;
* o projeto Apps Script puder ser aberto pelo Codex;
* uma alteração local adicional puder ser enviada;
* a segunda execução tiver sido validada;
* nenhuma credencial tiver sido armazenada no projeto;
* o relatório tiver sido criado;
* o status final for `PRONTO_COMPLETO`.

---

# 31. Condições que impedem a conclusão

Não declarar `PRONTO_COMPLETO` quando:

* apenas arquivos locais foram criados;
* o `clasp` não está autenticado;
* o envio não foi realizado;
* a planilha não existe;
* o projeto não está vinculado;
* a função não foi executada;
* a execução foi apenas simulada;
* o Chrome não consegue acessar a planilha;
* o Computer Use não consegue verificar a interface;
* existem erros de autorização;
* o teste deixou dados temporários;
* o Codex depende do Product Owner para copiar códigos;
* o Product Owner precisaria executar manualmente as tarefas técnicas das próximas fases.

---

# 32. Saída em caso de intervenção

Quando for necessária uma ação humana, responder somente com o necessário:

```text
Configuração pausada em uma etapa de segurança.

Ação necessária:
[descrição exata]

Página:
[nome da página oficial, sem solicitar credenciais no chat]

Não envie senha, código ou token.

Depois de concluir diretamente no Google, responda:
“Autorização concluída. Continue.”
```

Não encerrar a configuração.

Não reiniciar do zero depois da autorização.

---

# 33. Saída em caso de bloqueio

Caso o ambiente não possa atingir `PRONTO_COMPLETO`, responder:

```text
Configuração do ambiente bloqueada.

Etapa:
[etapa]

Problema:
[descrição]

Tentativas realizadas:
- tentativa;
- tentativa.

Impacto:
[explicar o que o Codex não conseguirá fazer autonomamente]

Ação necessária:
[menor ação possível]

Status registrado:
BLOQUEADO
```

Não afirmar que as fases seguintes poderão ser autônomas.

---

# 34. Saída final

Quando tudo estiver validado, responder:

```text
Ambiente autônomo configurado.

Status:
PRONTO_COMPLETO

Validações:
- Node.js compatível;
- clasp instalado e autenticado;
- API do Apps Script habilitada;
- planilha criada ou vinculada;
- projeto Apps Script vinculado;
- clasp push executado;
- função real executada;
- escrita, leitura e limpeza validadas;
- Chrome conectado;
- acesso visual ao Apps Script validado;
- acesso visual ao Google Sheets validado;
- segundo envio e segunda execução validados.

Documentação atualizada:
- AMBIENTE_AUTONOMO.md;
- TODO.md;
- CHANGELOG.md;
- REVIEW.md.

Nenhuma funcionalidade do SOEA foi implementada.
Nenhuma fase funcional foi iniciada.

O ambiente está pronto para a execução do Prompt 1.
```

Não executar o Prompt 1 automaticamente.

Aguardar autorização explícita do Product Owner.
