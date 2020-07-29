![Magento 2](https://cdn.rawgit.com/rafaelstz/magento2-snippets-visualstudio/master/images/icon.png)

#  Docker para ambiente de desenvolvimento do Magento 2

### Apache 2.4 + PHP 7.1 + MariaDB + N98 Magerun 2 + XDebug + Redis

### Requisitos de sistema

[MacOS, Linux e Windows](https://github.com/lucasapoena/docker-dev-magento2/wiki/requisitos)

### Como utiliizar?

Execute o comando abaixo no seu terminal. Mude o nome **DOCKER_MAGENTO2** para o nome de sua escolha.
Execute in your terminal, change the *MYMAGENTO2* to use the name of your project:

```
curl -s https://raw.githubusercontent.com/lucasapoena/docker-dev-magento2/master/init | bash -s DOCKER_MAGENTO2 clone
```

Se você desejar instalar o Magento, basta executar os comandos abaixo:

```
cd DOCKER_MAGENTO2
./shell
rm index.php
install-magento2
```

Você pode especificar qual versão deseja instalar bastando informa-la ao final do comando install. (Ex.: `install-magento2 2.2`).

### Paineis de Controle

**Web server:** http://localhost/

**PHPMyAdmin:** http://localhost:8080

**Servidor de E-mails:** http://localhost:8025

### Comandos

| Comandos  | Descrição  | Opções e Exemplos |
|---|---|---|
| `./init`  | Se você não usou o comando de instalação CURL acima, use este comando alterando o nome do projeto.  | `./init MYMAGENTO2` |
| `./start`  | 
Se você não continuar usando o CURL, poderá iniciar seu contêiner manualmente  | |
| `./stop`  | Pare os contêineres do seu projeto  | |
| `./kill`  | 
Interrompe contêineres e remove contêineres, redes, volumes e imagens criados para o projeto específico  | |
| `./shell`  | Acesse seu contêiner
  | `./shell root` | |
| `./magento`  | Utilizar o Magento CLI  | |
| `./n98`  | Utilizar os comandos do Magerun | |
| `./grunt-init`  | Inicializar o Grunt  | |
| `./grunt`  | Use o Grunt especificamente em seu tema ou completamente, ele fará a implantação e ficará observando  | `./grunt luma` |
| `./xdebug`  |  Enable / Disable o XDebug | |
| `./composer`  |  Utilizar os comandos do Composer | `./composer update` |

### Informações Gerais
Projeto adaptado do [Rafael Corrêa Gomes](https://github.com/rafaelstz/)

