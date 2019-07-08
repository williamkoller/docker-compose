docker run -it -v /data --name web03 nginx /bin/bash

cria um container com volume no diretório /data com imagem do nginx e abre direto no /bin/bash no modo interativo

docker inspect <nomedocontainer>

mostra os dados do container

 docker run -d -p 8084:80 -v /home/william/dev-studies/docker-course/:/usr/share/nginx --name web05 nginx

 docker run -d -p 8280:80 --volumes-from web01 --name web06 nginx 

 utiliza o mesmo volume para um novo container

 docker run --name dbserver1 -e MYSQL_ROOT_PASSWORD=1234 -e MYSQL_DATABASE=wordpress -d mysql:5.7

 sobre o container do mysl 

 docker run --name wordpress --link dbserver1:mysql -d -p 8088:80 wordpress

 sobre container do wordpress linkando o banco de dados

 docker build -t williamkoller/nginx .

 cria a imagem 
 
 docker run -d -p 8001:8080 williamckoller/nginx
 
 rodando uma imagem depois de criada e passando a porta do nginx

 