<h2>GETTING AN IMAGE TO DOCKER HUB</h2>

- Click on Create Repository.
- Choose a name (e.g. verse_gapminder) and a description for your repository and click Create.
- Log into the Docker Hub from the command line docker login --username=yourhubusername --email=youremail@company.com. ...
- Check the image ID using docker images


**COMANDOS:**
* _CTRL + pq_:
    + Sai do container sem finalizar o container
* _CTRL + d:_
    + Sai do container e finaliza o mesmo

* Criar um container:
    <pre> docker create -v VOLUME --name NOME_CONTAINER IMAGE_BASE </pre>
    Ex: docker create -v /data --name dbdados debian
* terminal interativo
	<pre> docker run --ti </pre> 

* mostrar todas os containners
	<pre>docker ps -a </pre>

* mostrar todas as imagens
	<pre>docker images</pre>

* Gerenciamento de memoria de um container
	<pre>docker run --ti --memory 512m --name teste debian</pre>
* Mudar/Atualizar quantidade de memória de um container ativo/existente
    <pre>docker update -m 512m ID_CONTAINER ou NOME_CONTAINER </pre>
* Gerenciamento de CPU de um container
    <pre>docker run -ti --cpu-share QTDE --name NOME_CONTAINER debian </pre>
* Mudar/Atualizar quantidade de cpu de um container ativo/existente
    <pre> docker update --cpu-share QTDE ID_CONTAINER ou NOME_CONTAINER </pre>

* Montar volumes:
    <pre> docker run --ti -v NOME_VOLUME CONTAINER COMANDO </pre>
        Ex: docker run --ti -v /teste ubuntu /bin/bash   