# Git

Ferramenta de versionamento de código.

Guia prático para a utilização da ferramenta.

# Scenes ( Casos de uso )

- [ ] Criar pontos na história da produção do projeto, de acordo com as funcionalidades desenvolvidas.

- [ ] Verificar mudanças feitas no projeto.

- [ ] Começar uma nova funcionalidade no projeto, sem estragar o que já foi feito.
- [ ] Adicionar as novas funcionalidades ao projeto em produção.
- [ ] Deletar a branch da nova funcionalidade, depois de aplicar no projeto.

- [ ] Querer colocar o projeto na nuvem.

- [ ] Pegar um projeto já iniciado, para se trabalhar com o time.
- [ ] Resolver conflitos.
- [ ] Antes de enviar a resulução, precisa-se atualizar o projeto local.

- [ ] Voltar um arquivo para um determinado momento da linha do tempo.

- [ ] Recuperar algo deletado.

# Comandos

- `git init` \\ Inicia a linha do tempo.
- `git remote` \\ Adiciona um repositório remoto.
- `git add` \\ Adiciona ou atualiza mudanças para irem para a linha do tempo.
- `git commit` \\ Adiciona um ponto na linha do tempo.
- `git log` \\ Visualiza os pontos na linha do tempo / commit.
- `git status` \\ Informa o estado das alterações do projeto.
- `git show` \\ Apresenta determinado ponto na história.
- `git branch` \\ Gerencia novas linhas do tempo.
- `git checkout` \\ Manipula as linhas do tempo.
- `git merge` \\ Une as linhas do tempo.
- `git push` \\ Envia as alterações locais para o repositório remoto.
- `git clone` \\ Clonar um projeto / repositório.
- `git pull` \\ Puxa do repositório remoto.

# Comandos mais detalhados

### Obtendo & Criação projetos

| Comando                                                           | Descrição                                     |
| ----------------------------------------------------------------- | --------------------------------------------- |
| `git init`                                                        | Inicializa um repositório Git local           |
| `git clone ssh://git@github.com/[usuario]/[nome-repositorio].git` | Cria uma cópia local de um repositório remoto |

### Básicos

| Comando                                | Descrição                                                            |
| -------------------------------------- | -------------------------------------------------------------------- |
| `git status`                           | Checa o status                                                       |
| `git add [nome-arquivo.txt]`           | Adiciona um arquivo para área de stage                               |
| `git add -A`                           | Adiciona todos os arquivos novos ou modificados para a área de stage |
| `git commit -m "[Mensagem de Commit]"` | Comita as alterações                                                 |
| `git rm -r [nome-arquivo.txt]`         | Remove um arquivo (ou pasta)                                         |

### Ramificação e União/fusão

| Comando                                                    | Descrição                                             |
| ---------------------------------------------------------- | ----------------------------------------------------- |
| `git branch`                                               | Lista as branches (o asterisco denota a branch atual) |
| `git branch -a`                                            | Lista todas as branches (local e remoto)              |
| `git branch [nome da branch]`                              | Cria uma nova branch                                  |
| `git branch -d [nome da branch]`                           | Deleta uma branch                                     |
| `git push origin --delete [nome da branch]`                | Deleta uma branch remota                              |
| `git checkout -b [nome da branch]`                         | Cria uma nova branch e muda para ela                  |
| `git checkout -b [nome da branch] origin/[nome da branch]` | Clona uma branch remota e muda para ela               |
| `git checkout [nome da branch]`                            | Seleciona uma branch                                  |
| `git checkout -`                                           | Muda para a última branch                             |
| `git checkout -- [nome-arquivo.txt]`                       | Descarta modificações de um arquivo                   |
| `git merge [nome da branch]`                               | Faz um merge de uma branch na branch atual            |
| `git merge [source branch] [branch alvo]`                  | Faz um merge de uma branch em outra branch            |
| `git stash`                                                | Tirar o estado sujo do seu diretório de trabalho      |
| `git stash clear`                                          | Remove todas as entradas 'stash'                      |

### Compartilhando e atualizando projetos

| Comando                                                                           | Descrição                                                                                    |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `git push origin [nome da branch]`                                                | Enviar uma branch para seu repositório remoto                                                |
| `git push -u origin [nome da branch]`                                             | Envia as alterações da branch informada para um repositório remoto (and selecionar a branch) |
| `git push`                                                                        | Envia as alterações para o repositório remoto (branch atual)                                 |
| `git push origin --delete [nome da branch]`                                       | Deletar uma branch remota                                                                    |
| `git pull`                                                                        | Atualiza o repositório local para o último commit                                            |
| `git pull origin [nome da branch]`                                                | Recebe alterações do repositório remoto                                                      |
| `git remote add origin ssh://git@github.com/[usuario]/[nome-repositorio].git`     | Adicionar um repositório remoto                                                              |
| `git remote set-url origin ssh://git@github.com/[usuario]/[nome-repositorio].git` | Seta um repositório da origin branch para o SSH                                              |

### Inspeção & Comparação

| Comando                                    | Descrição                              |
| ------------------------------------------ | -------------------------------------- |
| `git log`                                  | Ver modificações                       |
| `git log --summary`                        | Ver modificações (detalhadas)          |
| `git diff [branch original] [branch alvo]` | Visualizar alterações antes de mesclar |
