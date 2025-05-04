# Documentação para Rodar o Projeto

## Pré-requisitos
Antes de começar, certifique-se de que o computador onde o projeto será configurado possui os seguintes requisitos instalados:
- PHP (versão 7.4 ou superior)
- [Composer](https://getcomposer.org/) (para gerenciar dependências do PHP)
- Servidor Web (como Apache ou Nginx) - Wamp ou Xamp
- Banco de Dados (MySQL)
- Editor de Texto/IDE (como Visual Studio Code)

## Clonar o Projeto
Copie o projeto para o computador de destino. Você pode fazer isso via Git ou manualmente:
### Via Git:
    cd C:\wamp64\www\
    git clone <URL_DO_REPOSITORIO>

## Instalar Dependências Composer
Baixar o [Composer](https://getcomposer.org/Composer-Setup.exe)
- Instale selecionando a versão atual do php.
- Agora, rodar o Composer dentro do projeto.
- Abrir o Prompt de Comando
- Abra o cmd.
- Navegue até o diretório do seu projeto: `cd C:\wamp64\www\web.local`
- Instalar as Dependências: `composer install`

## Crie um banco de dados no MySQL
> Endereço: http://localhost/phpmyadmin
 - user: root -> enter
- Clicar em: Base de dados -> nome da base de dados: sistema_prod -> criar 

## Executar dentro do VSCODE
Execute as migrações dentro do terminal do vscode(ctrl + " e selecionar terminal cmd) (essencial):
	php spark migrate

Execute o servidor(essencial):
	php spark serve

Acesse: http://localhost:8080





## Opcional:
- Configure o arquivo .env na raiz do projeto:
- Renomeie o arquivo env para .env (se ainda não estiver renomeado).
 - Edite as configurações de banco de dados
	|--------------------------------------------------------------------------------------------------|  
 	| database.default.hostname = localhost                                                            | 
	| database.default.database = sistema_prod (altere caso banco tenha sido criado com nome diferente)| 
	| database.default.username = root                                                                 | 
	| database.default.password = <sua_senha>                                                          | 
	| database.default.DBDriver = MySQLi                                                               | 
