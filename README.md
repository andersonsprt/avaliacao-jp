# avaliacao-jp

Avaliação dia 22/08

COMANDOS DE GIT

branch --> ramificações, situações para adicionar um novo recurso ou corrigir um erro gerando uma nova ramificação garantindo qu eo código instável não seja mesclado nos arquivos do projeto principal. Tipos de branchs (main/master/prod, release/hml, dev, bugfix, feature).

merge --> usado para integrar as mudanças de um branch em outro. É uma operação essencial para combinar o trabalho de diferentes branches, como quando você está desenvolvendo uma nova funcionalidade em um branch separado e deseja incorporar essas mudanças ao branch principal (geralmente chamado de main ou master).

commit --> operação que registra mudanças no repositório Git. Cada commit tem um identificador único (hash) e pode incluir uma mensagem descritiva que explica as alterações feitas. Nunca commitar na main/master/prod, para isso abrimos branchs.

feat --> algo relacionado com features que você adicionar.

fix --> algo para corrigir.

docs --> algo relacionado a documentações, README e afins.

style --> algo relacionado com estilização.

refactor --> algo relacionado com refatorção (refazer).

perf --> algo relacionado a performace.

test --> algo com testes.

chore --> algo para coisas relacionados a build, configs e afins. Exemplo: use esse, seja utilizando a versão do pacote ou instalando novas dependências.

Verificação de comando --> abra o terminal, digite git --version.

Configuração --> configurar git local com os comandos:
    >git config --global user.name "Seu nome"
    >git config --global user.email "seuEmail@email.com"

git init : Inicializa um novo repositório Git em um diretório existente. Cria um subdiretório .git que contém todos os arquivos necessários para o repositório. Para desfazer a inicialização, exclua o diretório .git.

git status : Exibe o estado atual do repositório.
Mostra arquivos modificados, novos arquivos e arquivos
preparados para commit. Não há necessidade de reverter, pois apenas exibe informações.

git add <filename ou . > : Adiciona arquivos ao índice (staging area).Prepara os arquivos especificados para o próximo commit. Use git rm --cached <file> para remover os arquivos da staging area.

git rm --cached <file> : Remove arquivos do índice (staging area). Os arquivos são removidos da staging area, mas não do diretório de trabalho. Adicione novamente os arquivos com git add <filename ou . >.

git branch : Lista todas as branchs locais existentes git branch -r Lista todas as branchs remotas git branch -a Lista todas as branchs remotas e locais.

git checkout <branchname> : Muda para a branch especificada. O diretório de trabalho é atualizado para refletir o estado da branch. Para voltar à branch anterior, use git checkout <previous- branchname>.

git checkout -b <branchname> : Cria uma nova branch e muda para ela. Uma nova branch é criada e você é movido para essa nova branch. Use git branch -D <branchname> para excluir a branch e git checkout <previous-branchname> para voltar à branch anterior.

git commit -m "<description>" : Faz um commit das mudanças no índice com uma mensagem descritiva. As mudanças na staging area são salvas no repositório com a mensagem fornecida.

Use git reset --soft HEAD~1 para desfazer o último commit mantendo as mudanças no índice, ou git reset --hard HEAD~1 para desfazer o commit e as mudanças.

git merge <branch> : Realiza o merge da branch ATUAL na Branch informada

git push : Envia commits do repositório local para o repositório remoto. Os commits locais são enviados para a branch correspondente no repositório remoto. Use git revert <commit-hash> para criar um novo commit que desfaz as mudanças do commit específico.

git branch -D <branchname> : Exclui a branch especificada. A branch é removida do repositório local. Não há como reverter diretamente. Se necessário, crie a branch novamente a partir de um commit específico.

git fetch : Baixa objetos e referências do repositório remoto. Atualiza o repositório local com informações do repositório remoto sem mesclar. Não há necessidade de reverter, pois apenas atualiza as referências locais.

git pull : Baixa objetos e referências do repositório remoto e mescla com a branch atual. Mescla as mudanças do repositório remoto na branch local. Use git reset --hard <commit-hash> para reverter o estado da branch local ao commit anterior ao pull.