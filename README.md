# desafio.dio-introducao-ao-git-github
Projeto era criar um novo repositório aqui no GitHub e aqui está.

Tipos de Comandos:

GIT CONFIG
Este comando é essencial, pois nos permite ter acesso a diversas configurações da ferramenta que serão essenciais no início dos trabalhos, como as funções a seguir:

1. git config --global user.name “nome_de_usuário”
Este comando permite que o usuário defina o nome de usuário que será usado para identificar quem fez as alterações e edições ao longo do versionamento do código. O nome de usuário e o e-mail (que será citado no tópico à seguir) são exibidos ao lado do commit feito pelo usuário.

1.2 git config --global user.email <email_do_usuário>
Este comando é muito semelhante ao comando anterior. A única coisa que muda é que aqui o usuário precisa informar o e-mail ao invés do nome de usuário.

2. GIT INIT
Este comando é usado para iniciar um novo repositório do Git. Caso a pessoa possua um projeto que ainda não seja versionado, basta acessar a pasta raiz local do projeto no prompt de comando (caso a opção de compatibilidade tenha sido selecionada durante a instalação) ou no Bash do próprio Git e digitar o comando “git init” que um subdiretório chamado .git será criado e nele haverão todos os arquivos responsáveis pelos metadados e arquivos de configuração do repositório. Caso não exista nenhum projeto, basta criar uma nova pasta, acessá-la pelo Bash ou pelo Prompt (caso a opção de compatibilidade tenha sido selecionada durante a instalação) e digitar o comando que, a partir daquele momento, o diretório passará a ser versionado.

3. GIT CLONE
O comando git clone <REPOSITÓRIO> é usado para criar uma cópia local de um repositório remoto (do GitHub, por exemplo).

4. GIT ADD
Este comando serve para adicionar os arquivos que foram modificados à área de “Staging” do Git, antes de serem “commitados”. Existem algumas possibilidades de execução deste comando, que são:

4.1 git add <PATH>
Nesta versão do comando é possível adicionar um arquivo específico ou um diretório específico à área de Staging.

4.2 git add .
Este comando adiciona todos os arquivos que foram editados (exceto os listados no arquivo .gitignore) à área de staging.

5. GIT COMMIT
O comando “commit” também possui algumas variações, mas o que geralmente é mais usado está relatado a seguir:

5.1 git commit -m “MESSAGE”
Aqui o usuário “junta todos os arquivos” que foram adicionados à área de “staging” (mencionada no comando anterior) a um pacote e deixa um comentário falando o que foi alterado / editado / incluído no código.

6. BRANCHES, MERGES, CHECKOUT E REBASE
  
6.1 git branch
O comando git branch lista todas as branches / ramificações locais do repositório. O asterisco (*) simboliza a branch atual em que o usuário está.

6.2 git branch -a
O comando lista todas as branches / ramificações do projeto, incluindo as locais e as remotas.

6.3 git branch <NOME_DA_BRANCH>
Este comando cria uma nova branch no repositório.

6.4 git branch -d <NOME_DA_BRANCH>
Este comando deleta uma branch do repositório.

6.5 git push origin --delete <NOME_DA_BRANCH>
Este comando deleta uma branch no repositório remoto.

6.6 git checkout -b <NOME_DA_BRANCH>
Cria uma nova branch e muda imediatamente para ela.

6.7 git branch -m <NOME_ANTIGO_BRANCH> <NOVO_NOME>
Renomeia uma branch.

6.8 git checkout <NOME_DA_BRANCH>
Muda o HEAD para a branch citada no comando.

6.9 git checkout <HASH_DO_COMMIT>
Muda o HEAD para a posição do commit mencionado no comando.

6.10 git merge <NOME_DA_BRANCH>
Executa o merge da branch citada no comando com a branch atual. Por exemplo: se o usuário estiver na branch MASTER e executar o comando “git merge develop” a branch “develop” será “merged” na branch “MASTER”.

6.11 git rebase <NOME_DA_BRANCH_DESTINO>
Neste caso o comando “copia” os commits da branch ativa e os despeja na branch de destino, mencionada no comando. Este comando funciona como o “merge”, mas neste caso a linha do tempo é perdida.

7. RESET E REVERT
  
7.1 git reset HEAD~1
Este comando “apaga” uma parte da linha do tempo. Recomendado usar apenas na branch de feature ou na branch local. O comando apaga os arquivos a partir do commit mencionado, mantendo uma cópia no diretório local.

7.2 git revert <HASH_DO_COMMIT>
Este comando cria um novo commit na linha do tempo do repositório revertendo as alterações que foram feitas no commit mencionado no comando.

8. PULL E PUSH
  
8.1 git pull
Atualiza o repositório local com o último commit do repositório remoto.

8.2 git push
Faz o “upload” das alterações dos arquivos locais para o repositório remoto.
