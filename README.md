# git_commands

# Configuração:

git config: Configura opções do Git.

git config --global user.name "[nome]": Configura o nome do usuário para commits.

git config --global user.email "[email]": Configura o e-mail do usuário para commits.

git config --global color.ui auto: Ativa a colorização da saída do Git.

git config --global alias.[alias] "[comando]": Cria um alias para um comando Git.

# Inicialização e Clonagem:

git init: Inicializa um novo repositório Git na pasta atual.

git clone [URL]: Clona um repositório Git existente para sua máquina local.

# Adicionando e Registrando Alterações:

git add [arquivo]: Adiciona um arquivo específico ou mudanças em um arquivo ao próximo commit.

git add .: Adiciona todas as mudanças na pasta atual ao próximo commit.

git add -A: Adiciona todas as mudanças na pasta atual ao próximo commit, incluindo arquivos removidos.

git commit -m "[mensagem]": Registra as mudanças adicionadas ao repositório Git com uma mensagem de commit.

git commit -am "[mensagem]": Adiciona todas as mudanças e realiza um commit em um único comando.

# Visualização de Status e Histórico:

git status: Exibe o estado atual do repositório, mostrando arquivos modificados, adicionados ou removidos.

git diff: Exibe as diferenças entre os arquivos modificados e a última versão confirmada.

git log: Exibe o histórico de commits.


# Gerenciamento de Ramificações:


git branch: Lista todas as branches locais.

git branch [nome]: Cria uma nova branch com o nome especificado.

git branch -d [nome]: Exclui a branch especificada.

git branch -m [nome]: Renomeia a branch atual.

git checkout [branch]: Muda para a branch especificada.

git checkout -b [nome]: Cria uma nova branch com o nome especificado e muda para ela.

git checkout -: Volta para a branch anteriormente selecionada.

git merge [branch]: Mescla a branch especificada com a branch atual.

git rebase [branch]: Reaplica commits da branch especificada sobre a branch atual.

# Envio e Recebimento de Alterações:

git push: Envia commits locais para um repositório remoto.

git push [remote] [branch]: Envia commits locais para um repositório remoto e branch específicos.

git pull: Puxa as alterações do repositório remoto para o repositório local.

git pull --rebase: Puxa as alterações do repositório remoto para o repositório local e reaplica commits locais por cima.

git fetch: Busca alterações do repositório remoto sem mesclá-las.

# Gerenciamento de Tags e Submódulos:

git tag: Gerencia tags de versão.

git tag [nome]: Cria uma nova tag no commit atual.

git tag -d [nome]: Exclui a tag especificada.

git tag -a [nome] -m "[mensagem]": Cria uma nova tag anotada com uma mensagem.

git tag -l: Lista todas as tags.

git tag -v [nome]: Verifica a assinatura de uma tag.

git submodule: Gerencia submódulos dentro do repositório Git.


# Outros Comandos Úteis:

git stash: Armazena temporariamente mudanças não comprometidas.

git stash list: Lista todas as mudanças armazenadas temporariamente.

git stash apply: Aplica a última mudança armazenada temporariamente.

git stash pop: Aplica e remove a última mudança armazenada temporariamente.

git stash drop: Remove a última mudança armazenada temporariamente.

git remote: Gerencia repositórios remotos.

git blame [arquivo]: Mostra quem modificou cada linha de um arquivo e quando.

git grep [padrão]: Permite pesquisar por padrões em arquivos do repositório.

git bisect: Ajuda a encontrar o commit que introduziu um bug.

git archive: Cria um arquivo zip contendo o conteúdo de uma branch ou commit.

git cherry-pick [commit]: Aplica as mudanças introduzidas por um commit específico.

git revert [commit]: Reverte um commit específico, criando um novo commit que desfaz as mudanças.

git reflog: Registra todos os comandos executados no repositório, útil para recuperar commits perdidos.

git fsck: Verifica a integridade do repositório.

git prune: Remove objetos não referenciados do banco de dados do Git.

git gc: Limpa e otimiza o banco de dados do Git.

git instaweb: Inicia um servidor web para visualizar o repositório Git no navegador.




# Configuração e Inicialização

git init                          # Inicializa um novo repositório Git localmente.

git clone [url]                   # Clona um repositório Git remoto para o seu computador.

git config                        # Configura opções do Git, como nome de usuário, email, cores, etc.

# Exemplo:

git config --global user.name "Seu Nome".

git config --global user.email "seuemail@example.com".

# Básicos de Commit

git add [arquivo(s)]              # Adiciona arquivos ao índice (staging area) para preparar o commit.

# Exemplo:

git add arquivo.txt

git add .                          # Adiciona todos os arquivos modificados.

git commit -m "Mensagem do commit" # Registra as alterações no repositório, com uma mensagem de commit descritiva.

# Exemplo:

git commit -m "Adiciona funcionalidade X"

git commit --amend                 # Altera o commit mais recente.

# Ramificações (Branches)

git branch                         # Lista todas as branches locais.

git branch [nome]                  # Cria uma nova branch com o nome especificado.

# Exemplo:

git branch nova-feature

git checkout [branch]              # Muda para a branch especificada.

# Exemplo:

git checkout main

git checkout -b [nome]             # Cria uma nova branch e muda para ela.

# Exemplo:

git checkout -b nova-feature
git merge [branch]                 # Mescla a branch especificada na branch atual.

# Exemplo:

git merge desenvolvimento

# Sincronização com o Repositório Remoto

git remote add [nome] [url]        # Adiciona um novo repositório remoto.

# Exemplo:

git remote add origin https://github.com/usuario/repositorio.git

git remote -v                      # Lista todos os repositórios remotos configurados.

git fetch [remote]                 # Busca todas as branches e tags de um repositório remoto.

# Exemplo:

git fetch origin

git pull [remote] [branch]         # Obtém e mescla as alterações de um repositório remoto para a branch atual.

# Exemplo:

git pull origin main

git push [remote] [branch]         # Envia os commits locais para o repositório remoto.

# Exemplo:

git push origin main

git push --force                   # Força o push, substituindo o histórico do repositório remoto.

# Visualização e Histórico

git status                         # Mostra o estado atual do repositório.

git log                            # Exibe o histórico de commits.

git diff                           # Mostra as diferenças entre alterações nos arquivos.

git show [commit]                  # Exibe informações sobre um commit específico.

# Exemplo:

git show abc123

# Desfazendo Alterações

git reset [arquivo]                # Remove arquivos do índice (staging area) sem alterar o diretório de trabalho.

git checkout -- [arquivo]          # Descarta alterações em um arquivo específico no diretório de trabalho.

git revert [commit]                # Desfaz um commit específico, adicionando um novo commit com as alterações revertidas.

git reset --hard [commit]          # Reseta o HEAD para um commit específico, desfazendo todos os commits após ele.

# Submódulos

git submodule add [url]            # Adiciona um repositório externo como um submódulo dentro do seu repositório Git.

git submodule init                 # Inicializa os submódulos.

git submodule update               # Atualiza os submódulos para a versão definida no repositório.

# Limpeza

git clean -n                       # Lista arquivos não rastreados que seriam removidos pelo `git clean -f`.

git clean -f                       # Remove arquivos não rastreados do diretório de trabalho.

# Outros

git cherry-pick [commit]           # Aplica as mudanças introduzidas por um commit específico para a branch atual.

git tag [nome]                     # Cria uma tag para um commit específico.

git stash                          # Salva temporariamente alterações não commitadas.

git stash apply                    # Aplica a última entrada do stash ao diretório de trabalho atual.

