# docker-in-slackware
SlackBuilds do Docker 20.10.21 para instalação em Slackware 15.

####################################
##### Docker (Community Edition)
##########################

Procedimentos adaptados do <https://slackbuilds.org>.

Necessário realizar o download de todos os pacotes deste repositório, inclusive já consta o ".tgz" da versão "20.10.21".

Após realizar o download, precisará criar o grupo 'docker' por meio de um usuário com super privilégios: 

sudo groupadd -r -g 281 docker

Feito isso, adicionar o usuário corrente no grupo 'docker', pois dessa não precisará executar o docker com um usuário admin:

usermod -a -G docker <your_username>


Ao descompactar o pacote contendo todos os arquivos necessários à instalação é somente executar o script abaixo para gerar o ".txz": 
 
./docker-ce.SlackBuild

Por padrão, o arquivo é gerado no diretório "/tmp". Para concluir o processo de instalação, executar o comando seguinte:

upgradepkg --install-new /tmp/docker-ce-20.10.21-x86_64-jspinho.txz

(...) divirta-se!!!
