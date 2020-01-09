#CHEAT SHEET MORE USED

##Git

<addr>git clone url</addr> - clonar a branch para o pc
git checkout nome_branch - entrar numa branch já existente.
git checkout -b name_branch - criar e entrar na branch.
git fetch - sincroniza branchs remotas criadas.
git branch - listagem das branchs do projeto no pc.
git pull origin  name_branch - puxa os dados da branch
git push origin name_branch - envia os dados para a branch remota.
git add . - add todos os arquivos com alteração.
git add name_file  - add arquivos especificos
git log - para ver historico de commits.
git reset  - funciona tanto para o commit quanto para o add
git reset --hard HEAD~n - n diz quantos commits ele irá voltar.
git push origin name_branch --force - será necessária a flah force para o comando do resert hard
git stash - salvar um commit “para depois”. ex: precisa trocar de branch para resolver algo urgente, porém não terminou oq estava fazendo.

git stash apply - para retornar o stash como arquivo para ser commitado
git rm --cache git ls-files -i -X .gitignore - esse comando irá excluir arquivos que foram comitados errado e após o erro foram adicionados no .gitignore. ex: criou a branch e esqueceu de colocar a vendor do projeto no gitignore e acabou comitando tudo. Add ele no gitignore de push e rode o comando.

##Docker
docker-compose  up -d - executa os containers em segundo plano.
docker-compose down - derruba os containers.
docker-compose restart - para e retornar os containers.
docker-compose ps - caso esteja na pasta do projeto, esse comando irá listar apenas os containers do docker-compose.yml atual.
docker-compose exec -T name_container mysqldump -h name_container -u root -proot name_databese name_table > name_file.sql - gera um dump de tabela especifica.

docker network ls - lista as redes
docker network rm name_network - remove rede
docker container ls/ps - lista todos os container da maquina
docker container stop name_container - para o container 
docker container rm name_container - remove o container (lembrando que para remover o container deve estar parado).

os comando ls e rm funcionam no geral igual para todos os contextos : volumes, images, container, networks e etc.



##kubectl

kubectl  get pods -n employees - para listar os logs e o que está executando e parado
kubectl logs nomedopod -n service/alias_service - para ver um log específico e mais recente
kubectl logs nomedopod -n service/alias_service --previous ( só se precisar ver os logs antigos)
restartar um comando
kubectl delete pods nomedopod -n service/alias_service
