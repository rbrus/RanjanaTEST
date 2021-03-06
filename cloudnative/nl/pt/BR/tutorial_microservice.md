---

copyright:
  years: 2016, 2017
lastupdated: "2017-03-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Tutorial de ponta a ponta do Iniciador Microservice Basic
{: #tutorial}

O tutorial de ponta a ponta a seguir percorre as etapas para criar um projeto por meio do Iniciador Microservice Basic, incluindo as ferramentas que devem ser instaladas e, subsequentemente, as etapas para executar o código do projeto.

## Instalando ferramentas do desenvolvedor
{: #dev_tools}

Assegure-se de que você tenha instalado as [ferramentas do desenvolvedor de pré-requisito ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](get_code.html#prereq-dev-tools){: new_window}.


## Criando um projeto usando o {{site.data.keyword.dev_console}}
{: #create-devex}

1. Crie um projeto no {{site.data.keyword.Bluemix}} {{site.data.keyword.dev_console}}.

	1. Na página **Introdução** no {{site.data.keyword.dev_console}}, clique em **Criar projeto**.

		Como alternativa, clique em **Criar projeto** na página **Projetos**.

	2. Selecione **Microservice** e clique em **Avançar**.

	3. Selecione **Basic** e clique em **Avançar**.

	4. Insira o nome do projeto. Para este tutorial, use `MicroserviceProject`.   

	5. Insira um nome do host. Para este tutorial, use `devhost`. 
   
	6. Clique em **Criar**.

2. Opcional: inclua o recurso Dados.

	1. Clique em **Visualizar** para **Dados** na página **Visão geral do projeto**.

      Como alternativa, é possível selecionar **Criar** ou **Incluir existente** na página **Recursos > Dados**.

   2. Insira o nome do serviço e clique em **Criar**.

3. Gere seu código do projeto.

	1. Clique em **Obter o código** na página **Visão geral do projeto** para selecionar sua linguagem.
   
		Como alternativa, é possível clicar na página **Código**.
      
	2. Clique em **Gerar código**.
   
	3. Quando o código do projeto concluir a geração, clique
em **Fazer download do código** para fazer
download do seu archive de projeto.

4. Opcional: [atualize seu projeto](project_overview_page.html#update_language) para gerar uma nova linguagem.


## Criando um projeto usando a {{site.data.keyword.dev_cli_notm}}
{: #create-cli}

1. Assegure-se de que tenha instalado a [{{site.data.keyword.dev_cli_short}}](dev_cli.html).

2. No prompt do Terminal, navegue para um diretório local de sua preferência e execute o comando a seguir.
  
	```
	bx dev create
	```
	{: codeblock}

3. Forneça os valores a seguir quando solicitado:

	* Selecione um padrão: 4 (para Microservices)
	* Selecione um iniciador: 1 (para Basic)
	* Selecione uma plataforma: 3 (para Java)
	* Insira um nome para seu projeto: `MicroserviceProjectCLI`

4. Se desejar incluir serviços no projeto, digite `y` no prompt de pergunta e responda às perguntas restantes.

5. Quando o `MicroserviceProjectCLI` tiver sido salvo com sucesso, navegue para a pasta `MicroserviceProjectCLI`.

6. Nesse ponto será possível incluir seu próprio código, construir ou executar o projeto.
 
 
## Executando o projeto usando a {{site.data.keyword.dev_cli_notm}}
{: #running-dev-plugin}

1. Para construir o projeto no diretório de projeto atual, insira o comando a seguir:

	```
	bx dev build
	```     
	{: codeblock}

2. Para construir e executar o projeto no diretório de projeto atual, insira o comando a seguir:

	```
	bx dev run
	```
	{: codeblock}	

3. É possível acessar o aplicativo usando curl no servidor:

	```
	curl http://localhost:8080	
	```
	{: codeblock}
