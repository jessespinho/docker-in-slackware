# docker-in-slackware
*SlackBuilds* do *Docker* 20.10.21 para instalação em *Slackware* 15.

------------------------------
## *Docker (Community Edition)*
---------------------------

Procedimentos adaptados do [*SlackBuilds*](https://slackbuilds.org).

1. Clonar este repositório para obter os arquivos descritos;

2. Realizar o *download* do pacote ".tgz" da versão "20.10.21" no diretório em que consta o *SlackBuid*: [docker-20.10.21.tgz](https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz).

3. Após realizar o *download*, precisará criar o grupo '*docker*' por meio de um usuário com super privilégios: sudo groupadd -r -g 281 docker

4. Feito isso, adicionar o usuário corrente no grupo '*docker*', pois dessa forma não precisará executar o *docker* com um usuário admin: sudo usermod -a -G docker <your_username>

5. Ao descompactar o pacote contendo todos os arquivos necessários à instalação é somente executar o *script* abaixo para gerar o ".txz": ./docker-ce.SlackBuild

6. Por padrão, o arquivo é gerado no diretório "/tmp". Para concluir o processo de instalação, executar o comando seguinte: sudo upgradepkg --install-new /tmp/docker-ce-20.10.21-x86_64-jspinho.txz

+==============================================================================
| Installing new package /tmp/docker-ce-20.10.21-x86_64-jspinho.txz
+==============================================================================

Verifying package docker-ce-20.10.21-x86_64-jspinho.txz. 
Installing package docker-ce-20.10.21-x86_64-jspinho.txz: 
PACKAGE DESCRIPTION:

docker-ce (manager for applications in Linux containers) 
Docker is an open-source project to easily create lightweight, 
portable, self-sufficient containers from any application. The same 
container that a developer builds and tests on a laptop can run at 
scale, in production, on VMs, bare metal, OpenStack clusters, public 
clouds and more. 

Homepage: https://www.docker.com/products/container-runtime

Executing install script for docker-ce-20.10.21-x86_64-jspinho.txz.
Package docker-ce-20.10.21-x86_64-jspinho.txz installed.

(...) divirta-se!!!
