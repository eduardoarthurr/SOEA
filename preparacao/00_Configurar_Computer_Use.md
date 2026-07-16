# PREPARAÇÃO 00 — CONFIGURAÇÃO DO COMPUTER USE E DO CHROME

## 1. Objetivo

Preparar e validar o Computer Use e a integração com o Google Chrome para permitir que o Codex opere visualmente:

* aplicativos do Windows;
* Google Chrome;
* Google Sheets;
* Google Apps Script;
* telas de execução;
* menus;
* Sidebars;
* células;
* gráficos;
* mensagens de erro.

Esta preparação acontece antes do fluxo oficial do SOEA.

Ela não faz parte das Fases 0, 1, 2, 3 ou 4 do produto.

Ela também não substitui:

```text
prompts/00_Configurar_Ambiente_Autonomo.md
```

A ordem correta será:

```text
Preparação do Computer Use
↓
Validação do Computer Use
↓
Validação do Chrome
↓
Validação do Google Sheets
↓
Execução do Prompt 00 do SOEA
```

---

# 2. Limite de autonomia

O Codex deverá conduzir toda a preparação que estiver tecnicamente ao seu alcance.

Entretanto, o Computer Use não poderá instalar ou autorizar a si próprio controlando a interface do ChatGPT.

O Product Owner precisará realizar manualmente somente as ações iniciais dentro do aplicativo oficial:

* abrir a área de Plugins;
* selecionar Computer Use;
* clicar em instalar ou habilitar;
* ativar os componentes solicitados;
* aprovar permissões do aplicativo;
* instalar a extensão oficial do Chrome;
* aprovar permissões da extensão;
* fazer login em contas;
* realizar autenticação em dois fatores;
* resolver CAPTCHA;
* confirmar consentimentos de segurança.

O Codex não deverá solicitar:

* senha;
* código de autenticação;
* código de recuperação;
* token;
* cookie;
* arquivo de sessão;
* credencial;
* chave privada.

Esses dados deverão ser inseridos somente nas páginas oficiais correspondentes.

---

# 3. Resultado esperado

Ao final, o ambiente deverá alcançar:

```text
COMPUTER_USE_PRONTO
```

Esse estado somente poderá ser declarado quando:

* o aplicativo desktop oficial estiver instalado;
* a área Codex ou Work estiver acessível;
* o plugin Computer Use estiver instalado;
* o servidor do Computer Use estiver habilitado;
* a skill do Computer Use estiver habilitada;
* o Computer Use conseguir operar um aplicativo simples;
* o plugin Chrome estiver instalado;
* a extensão oficial estiver instalada no perfil correto;
* a extensão mostrar `Connected`;
* o Codex conseguir abrir o Chrome;
* o Codex conseguir acessar o Google Sheets;
* o Codex conseguir criar uma planilha de teste;
* o Codex conseguir escrever em uma célula;
* o Codex conseguir ler o resultado;
* o Codex conseguir acessar o Google Apps Script;
* as permissões mínimas estiverem configuradas;
* os testes temporários tiverem sido removidos ou identificados.

---

# 4. Estados permitidos

Utilizar somente:

```text
NAO_INICIADO
INTERVENCAO_NECESSARIA
EM_CONFIGURACAO
COMPUTER_USE_PRONTO
BLOQUEADO
```

## `NAO_INICIADO`

Nenhuma verificação foi executada.

## `INTERVENCAO_NECESSARIA`

Existe uma ação que somente o Product Owner pode realizar.

## `EM_CONFIGURACAO`

A instalação foi iniciada, mas os testes ainda não foram concluídos.

## `COMPUTER_USE_PRONTO`

Todos os critérios de aceite foram comprovados.

## `BLOQUEADO`

Existe uma limitação técnica que impede a utilização necessária para o SOEA.

Não utilizar `COMPUTER_USE_PRONTO` apenas porque o plugin aparece instalado.

---

# 5. Instrução inicial ao Codex

Ao receber este documento, o Codex deverá:

1. ler integralmente este arquivo;
2. executar somente esta preparação;
3. não executar os prompts da pasta `prompts/`;
4. não analisar o edital;
5. não instalar o `clasp`;
6. não criar a planilha oficial do SOEA;
7. não criar o projeto oficial Apps Script;
8. não modificar o PRD, a Arquitetura ou o Roadmap;
9. não iniciar nenhuma fase do produto;
10. parar após validar o Computer Use e o Chrome.

---

# 6. Verificação do aplicativo desktop

Verificar se a tarefa está sendo executada no aplicativo desktop oficial para Windows.

Confirmar:

* o aplicativo está instalado;
* o aplicativo está atualizado;
* a conta ChatGPT está conectada;
* a área Codex ou Work está disponível;
* o repositório SOEA está aberto;
* a pasta do projeto pode ser lida;
* o sistema operacional é Windows.

Caso a tarefa esteja sendo executada somente:

* no navegador;
* no Codex Web;
* em uma IDE sem acesso ao aplicativo desktop;
* na CLI isolada;
* em um ambiente remoto sem área de trabalho;

não prosseguir com a validação visual.

Registrar:

```text
BLOQUEADO
```

e explicar que esta preparação exige o aplicativo desktop com suporte a Plugins e Computer Use.

---

# 7. Instalação manual mínima do Computer Use

O Codex deverá orientar o Product Owner a realizar as ações abaixo no aplicativo desktop:

```text
Abrir Codex ou Work
↓
Abrir Plugins
↓
Localizar Computer Use
↓
Selecionar Install plugin, se disponível
↓
Selecionar Enable, se disponível
↓
Ativar o servidor Computer Use
↓
Ativar a skill Computer Use
↓
Selecionar Try now
```

Como o Computer Use não poderá controlar a própria interface do ChatGPT para instalar a si mesmo, esta etapa será manual.

O Codex deverá apresentar:

```text
Intervenção necessária para instalar o Computer Use.

No aplicativo desktop:

1. Abra Codex ou Work.
2. Abra Plugins.
3. Localize Computer Use.
4. Clique em Install plugin ou Enable.
5. Ative o servidor e a skill do Computer Use.
6. Clique em Try now.

Não envie senhas ou códigos no chat.

Depois responda:
“Computer Use instalado e habilitado. Continue.”
```

Depois da confirmação, continuar do ponto em que parou.

Não reiniciar a preparação.

---

# 8. Verificação das configurações do Computer Use

Após a instalação, orientar o Product Owner a abrir:

```text
Settings
↓
Computer Use
```

Verificar:

* controle de aplicativos habilitado;
* Computer Use ativo;
* lista de aplicativos autorizados;
* Chrome conectado ou ainda pendente;
* ausência de bloqueio administrativo;
* política de acesso compatível.

Não habilitar acesso permanente a todos os aplicativos.

Utilizar permissões restritas inicialmente.

---

# 9. Política inicial de permissões

Durante os primeiros testes, utilizar:

```text
Permitir somente nesta tarefa
```

ou opção equivalente.

Não utilizar inicialmente:

```text
Sempre permitir qualquer aplicativo
```

O acesso permanente poderá ser concedido posteriormente somente para aplicativos necessários e confiáveis.

Aplicativos esperados:

* Bloco de Notas;
* Google Chrome.

Não autorizar durante esta preparação:

* Gmail;
* Outlook;
* gerenciadores de senha;
* aplicativos bancários;
* aplicativos corporativos;
* pastas pessoais não relacionadas;
* mensageiros;
* outros navegadores com sessões sensíveis.

---

# 10. Teste básico do Computer Use

Após o plugin estar instalado, iniciar um teste explícito com:

```text
@Computer abra o Bloco de Notas do Windows, digite
“Teste do Computer Use do SOEA concluído”
e pare sem salvar o arquivo.
```

O Codex deverá verificar:

* o Bloco de Notas foi aberto;
* a janela correta foi selecionada;
* o texto foi digitado;
* nenhum arquivo foi salvo;
* nenhum outro aplicativo foi alterado;
* a tarefa parou após o teste.

O Product Owner poderá precisar aprovar o acesso ao Bloco de Notas.

Depois do teste:

* fechar o Bloco de Notas;
* descartar o conteúdo;
* não salvar arquivo temporário.

Caso funcione, registrar:

```text
TESTE-CU-001: APROVADO
```

Caso não funcione:

1. verificar se o plugin está habilitado;
2. verificar se o aplicativo está visível;
3. verificar se existe uma permissão pendente;
4. iniciar uma nova tarefa;
5. repetir uma vez;
6. registrar o erro real.

---

# 11. Condição operacional no Windows

Durante tarefas de Computer Use no Windows:

* manter o computador ligado;
* manter o Windows desbloqueado;
* manter a internet ativa;
* manter o aplicativo-alvo visível;
* não disputar mouse e teclado;
* não executar duas tarefas contra o mesmo aplicativo;
* não cobrir a janela-alvo;
* não alternar de usuário;
* não bloquear a sessão;
* não minimizar o aplicativo necessário durante a ação.

O Computer Use deverá trabalhar na área de trabalho ativa.

O Product Owner poderá interromper a tarefa a qualquer momento caso o Codex selecione uma janela incorreta.

---

# 12. Configuração do plugin Chrome

Depois do teste básico, orientar o Product Owner a configurar o Chrome:

```text
Abrir Codex ou Work
↓
Abrir Plugins
↓
Adicionar o plugin Chrome
↓
Seguir o assistente
↓
Instalar a extensão oficial
↓
Aprovar as permissões exibidas pelo Chrome
↓
Abrir o perfil correto
↓
Confirmar Connected
```

O Codex deverá apresentar:

```text
Intervenção necessária para conectar o Chrome.

1. Abra Codex ou Work.
2. Abra Plugins.
3. Adicione o plugin Chrome.
4. Siga o assistente oficial.
5. Instale a extensão aberta pelo próprio aplicativo.
6. Aprove as permissões diretamente no Chrome.
7. Abra a extensão e confirme que aparece Connected.

Depois responda:
“Chrome conectado. Continue.”
```

Não solicitar que o usuário envie captura contendo dados pessoais ou credenciais.

---

# 13. Perfil do Chrome

Recomendar um perfil dedicado:

```text
Nome do perfil: SOEA
Finalidade: Google Sheets e Google Apps Script
```

O perfil deverá conter somente o necessário para o projeto.

Antes dos testes, confirmar:

* a extensão está instalada nesse perfil;
* o perfil está ativo;
* a extensão mostra `Connected`;
* a conta Google correta está conectada;
* não existem múltiplas contas causando ambiguidade;
* outras abas sensíveis estão fechadas.

Não acessar:

* Gmail;
* histórico de navegação;
* favoritos;
* outros arquivos do Drive;
* documentos pessoais não relacionados;
* dados de outras contas.

---

# 14. Acesso a sites

Durante os testes, autorizar apenas os domínios necessários ao fluxo:

* Google Sheets;
* Google Drive, somente quando necessário para localizar a planilha de teste;
* Google Apps Script;
* páginas oficiais de autenticação do Google, com presença do Product Owner.

Começar com autorização somente para a tarefa atual.

Não habilitar acesso irrestrito a todos os sites.

Não habilitar acesso ao histórico do Chrome sem necessidade.

---

# 15. Teste de conexão do Chrome

Executar:

```text
@Chrome abra uma nova aba, acesse o Google Sheets
e pare quando a página inicial estiver carregada.

Não crie, altere, compartilhe ou exclua nenhum arquivo.
```

Verificar:

* o Chrome correto foi aberto;
* o perfil correto foi utilizado;
* o Google Sheets carregou;
* a conta correta aparece conectada;
* nenhuma senha foi solicitada pelo chat;
* nenhuma ação além da navegação foi realizada.

Registrar:

```text
TESTE-CU-002: APROVADO
```

Caso a extensão apareça desconectada:

1. abrir a extensão no Chrome;
2. verificar `Connected`;
3. confirmar o plugin Chrome habilitado;
4. confirmar o perfil correto;
5. reiniciar o Chrome;
6. reiniciar o aplicativo desktop;
7. remover e adicionar novamente o plugin, se necessário;
8. iniciar uma nova tarefa;
9. repetir o teste.

---

# 16. Login na conta Google

Caso a conta Google ainda não esteja conectada, solicitar intervenção:

```text
Intervenção de segurança necessária.

Entre na conta Google diretamente no Chrome.

Conclua senha, autenticação em dois fatores e qualquer
confirmação somente nas páginas oficiais do Google.

Não envie senha, código ou token no chat.

Depois responda:
“Conta Google conectada. Continue.”
```

O Codex não deverá:

* digitar senha;
* armazenar senha;
* copiar código de autenticação;
* tentar contornar CAPTCHA;
* alterar configurações de segurança;
* adicionar telefone;
* alterar e-mail de recuperação.

---

# 17. Teste de criação no Google Sheets

Executar:

```text
@Chrome abra o Google Sheets e crie uma planilha vazia chamada
“TESTE COMPUTER USE SOEA”.

Na célula A1, escreva:
“Computer Use funcionando”.

Na célula A2, escreva a data e a hora atuais.

Depois leia novamente A1 e confirme o conteúdo.

Não compartilhe a planilha.
Não altere permissões.
Não abra outros arquivos.
Pare ao concluir.
```

Verificar:

* uma nova planilha foi criada;
* o nome está correto;
* A1 foi preenchida;
* A2 foi preenchida;
* A1 foi lida novamente;
* o conteúdo foi confirmado;
* nenhuma outra planilha foi alterada;
* nenhuma permissão foi modificada.

Registrar:

```text
TESTE-CU-003: APROVADO
```

---

# 18. Teste do Google Apps Script

Na planilha de teste, executar:

```text
@Chrome abra Extensões → Apps Script na planilha
“TESTE COMPUTER USE SOEA”.

Confirme que o editor foi aberto e que existe um projeto
vinculado à planilha.

Não escreva código.
Não execute funções.
Não altere o manifesto.
Pare depois da confirmação.
```

Verificar:

* o menu correto foi utilizado;
* o editor Apps Script foi aberto;
* o projeto está vinculado à planilha de teste;
* o Codex consegue visualizar o editor;
* nenhuma alteração foi realizada.

Registrar:

```text
TESTE-CU-004: APROVADO
```

---

# 19. Teste de navegação entre as interfaces

Executar um teste controlado:

```text
@Chrome alterne entre a planilha de teste e o editor Apps Script.

Confirme o nome da planilha e o título do projeto.

Não altere código ou células.

Pare depois de confirmar as duas interfaces.
```

Verificar:

* o Codex mantém o contexto da planilha;
* o Codex mantém o contexto do Apps Script;
* as abas corretas são utilizadas;
* nenhuma página incorreta foi aberta.

Registrar:

```text
TESTE-CU-005: APROVADO
```

---

# 20. Limpeza do teste

Após os testes, o Codex deverá orientar a remoção ou preservação segura da planilha temporária.

Ação recomendada:

```text
Mover “TESTE COMPUTER USE SOEA” para a lixeira
```

Como exclusão é uma ação potencialmente destrutiva, solicitar confirmação antes de executá-la.

Mensagem:

```text
Os testes do Computer Use foram concluídos.

Posso mover a planilha temporária
“TESTE COMPUTER USE SOEA” para a lixeira.

Essa ação não afetará nenhum arquivo do projeto SOEA.

Confirme explicitamente para continuar.
```

Somente após confirmação:

* mover a planilha temporária para a lixeira;
* confirmar que o arquivo correto foi removido;
* não esvaziar a lixeira;
* não excluir permanentemente;
* não tocar em outros arquivos.

Caso o Product Owner prefira manter a planilha, registrar que ela permanece como artefato de teste.

---

# 21. Aplicativos sempre permitidos

Depois que todos os testes forem aprovados, o Product Owner poderá adicionar à lista de aplicativos sempre permitidos apenas:

* Google Chrome, quando necessário;
* outros aplicativos estritamente necessários ao projeto.

Não é necessário manter o Bloco de Notas permanentemente autorizado.

Não utilizar política ampla de qualquer aplicativo sem necessidade.

---

# 22. Teste de segurança

Confirmar:

* nenhuma senha foi enviada pelo chat;
* nenhum código foi enviado pelo chat;
* nenhum token foi registrado;
* nenhuma credencial foi criada no projeto;
* nenhuma extensão não oficial foi instalada;
* nenhum outro arquivo do Drive foi alterado;
* nenhum e-mail foi aberto;
* nenhuma permissão de compartilhamento foi modificada;
* nenhum histórico do Chrome foi acessado;
* nenhuma ação destrutiva foi realizada sem confirmação.

Registrar:

```text
TESTE-CU-006: APROVADO
```

---

# 23. Diagnóstico de problemas

## Computer Use não aparece em Plugins

* confirmar aplicativo desktop oficial;
* confirmar aplicativo atualizado;
* confirmar conta correta;
* confirmar acesso ao recurso no plano ou workspace;
* reiniciar o aplicativo;
* registrar a indisponibilidade real;
* não inventar que está instalado.

## Plugin aparece, mas não instala

* fechar e abrir o aplicativo;
* verificar atualizações;
* verificar política do workspace;
* verificar bloqueios corporativos;
* tentar novamente;
* registrar a mensagem apresentada.

## Computer Use não controla o aplicativo

* manter a janela visível;
* confirmar permissão;
* confirmar que a tarefa usou `@Computer`;
* iniciar uma nova tarefa;
* não usar duas tarefas simultâneas;
* verificar configurações de Computer Use.

## Chrome mostra `Disconnected`

* confirmar plugin Chrome habilitado;
* confirmar extensão instalada;
* confirmar perfil correto;
* remover e adicionar novamente o plugin;
* reiniciar Chrome;
* reiniciar o aplicativo;
* iniciar nova tarefa.

## Chrome mostra host nativo ausente

* remover o plugin Chrome do aplicativo;
* adicionar novamente;
* seguir todo o assistente;
* confirmar `Connected`.

## Google Sheets pede login

* pausar;
* solicitar login manual;
* não solicitar credenciais;
* continuar após confirmação.

## Codex abre a janela errada

* interromper imediatamente;
* fechar aplicativos sensíveis;
* reabrir somente o aplicativo necessário;
* iniciar tarefa mais específica;
* repetir o teste.

---

# 24. Critérios de aceite

A preparação somente será aprovada quando:

* [ ] Aplicativo desktop oficial validado.
* [ ] Área Codex ou Work validada.
* [ ] Plugin Computer Use instalado.
* [ ] Plugin Computer Use habilitado.
* [ ] Servidor Computer Use habilitado.
* [ ] Skill Computer Use habilitada.
* [ ] Configurações acessíveis.
* [ ] Teste com Bloco de Notas aprovado.
* [ ] Plugin Chrome instalado.
* [ ] Extensão oficial instalada.
* [ ] Perfil correto do Chrome validado.
* [ ] Extensão mostrando `Connected`.
* [ ] Conta Google conectada.
* [ ] Google Sheets acessível.
* [ ] Planilha temporária criada.
* [ ] Célula A1 preenchida.
* [ ] Conteúdo de A1 relido e confirmado.
* [ ] Google Apps Script acessível.
* [ ] Navegação Sheets ↔ Apps Script aprovada.
* [ ] Teste de segurança aprovado.
* [ ] Planilha de teste removida ou registrada.
* [ ] Nenhuma credencial exposta.
* [ ] Nenhum arquivo real alterado.
* [ ] Status final `COMPUTER_USE_PRONTO`.

---

# 25. Relatório final no chat

Quando todos os testes forem aprovados, responder:

```text
Preparação do Computer Use concluída.

Status:
COMPUTER_USE_PRONTO

Validações:
- aplicativo desktop validado;
- Computer Use instalado e habilitado;
- servidor habilitado;
- skill habilitada;
- operação de aplicativo Windows validada;
- plugin Chrome instalado;
- extensão Chrome conectada;
- perfil correto validado;
- conta Google conectada;
- Google Sheets acessível;
- criação e leitura de célula validadas;
- Google Apps Script acessível;
- navegação entre Sheets e Apps Script validada;
- segurança validada.

Intervenções realizadas pelo Product Owner:
- listar somente as ações realmente necessárias.

Artefato temporário:
- removido ou mantido, conforme decisão.

Nenhuma fase do SOEA foi iniciada.
Nenhum arquivo oficial do SOEA foi alterado.
Nenhum prompt da pasta prompts/ foi executado.

O ambiente está pronto para iniciar:
prompts/00_Configurar_Ambiente_Autonomo.md
```

Depois disso, parar.

Não executar o Prompt 00 automaticamente.

Aguardar autorização explícita do Product Owner.

---

# 26. Saída em caso de bloqueio

Caso não seja possível concluir:

```text
Preparação do Computer Use bloqueada.

Status:
BLOQUEADO

Etapa:
[etapa em que ocorreu]

Problema:
[mensagem objetiva]

Tentativas realizadas:
- tentativa;
- tentativa.

Impacto:
O Codex não poderá operar e validar autonomamente
o Google Sheets e o Google Apps Script pela interface.

Ação necessária:
[menor ação possível]

Nenhuma fase do SOEA foi iniciada.
```

Não declarar `COMPUTER_USE_PRONTO`.

---

# 27. Próxima etapa

Depois da aprovação desta preparação, executar somente:

```text
prompts/00_Configurar_Ambiente_Autonomo.md
```

Esse prompt cuidará de:

* Node.js;
* npm;
* `clasp`;
* autenticação do `clasp`;
* criação ou vínculo da planilha oficial;
* criação ou vínculo do projeto Apps Script;
* primeiro envio;
* execução real;
* relatório `AMBIENTE_AUTONOMO.md`;
* classificação `PRONTO_COMPLETO`.

A preparação atual não deverá executar essas tarefas antecipadamente.