# Aprendendo Git e Gitflow

Repositório voltado ao aprendizado de versionamento de código utilizando a tecnologia git. Dessa forma, pode ser utilizado tanto para aprendizado como para consulta.

Atualmente possuo algumas certificações sobre a tecnologia, caso queira consultar [clique aqui](#certificacoes).

#### Como principais fontes bibliográficas foi utilizado:

* [Documentação oficial (PT-BR)](https://git-scm.com/docs/git/pt_BR)
* [Livro: Controlando versões com Git e GitHub](https://www.casadocodigo.com.br/products/livro-git-github)

## Indíces

#### Conceitos

* [1. O que é git?](#oqueegit)
* [2. O que é gitflow?](#oqueegitflow)
* [3. O que é desenvolvimento baseado em troncos?](#oqueetroncos)

#### Principais comandos
| <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | 
| :------:|:-----:| :------:| :-------:|:------:|:-----:| :------:| :-------:|
| [git init](#gitinit) | [git config](#gitconfig) 	| [git status](#gitstatus) |  [git log](#gitlog) |  [git add](#gitadd) |  [git rm](#gitrm) | [git mv](#gitmv) | [git commit](#gitcommit) |
| [git reset](#gitreset) | [git revert](#gitrevert) | [git push](#gitpush) | [git remote](#gitremote) | [git pull](#gitpull) | [git branch](#gitbranch) | [git checkout](#gitcheckout) | [git switch](#gitswitch) |
| [git restore](#gitrestore) | [git merge](#gitmerge) | [git rebase](#gitrebase) | [git diff](#gitdiff) | [git clone](#gitclone) |
 
<div id='oqueegit'/>

## 1. O que é git? 

O Git possui a função de registrar quaisquer alterações realizadas em um código, armazenando essas informações e permitindo que, caso necessário, um(a) programador(a) possa recuperar a versão anterior de uma aplicação de modo simples e rápido. Além disso, o Git facilita o processo de compartilhamento de código entre um time, e aliado a seu desempenho, segurança e flexbilidade, se tornou atualmente o sistema de controle de versão mais usado no mundo.

Dado que o git possui uma arquitetura distribuída, ele é um exemplo de DVCS (Sistema de Controle de Versão Distribuída). Portanto, em vez de possuir apenas um único local para o histórico completo da versão do software, como era comum em sistemas de controle de versão antes populares, a cópia de trabalho de todo desenvolvedor do código também é um repositório que pode conter o histórico completo de todas as alterações do projeto.



<div id='oqueegitflow'/>

## 2. O que é gitflow? 

<div id='oqueetroncos'/>

## 3. O que é desenvolvimento baseado em troncos?

## Comandos

<div id='gitinit'/>

### git init
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Este comando cria um repositório Git vazio, basicamente um diretório .git com subdiretórios para os arquivos objects, refs/heads, refs/tags e arquivos modelo. Também é criado um arquivo inicial HEAD que tem como referencia o HEAD do ramo principal.*

Assim, esse comando possibilita o uso de git no respectivo diretório e seus subdiretórios. 

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-init/pt_BR)

#### Parâmetros do git init
| Código     | Resultado |
| ------|:-----:| 
| git init | Cria um repositório do Git com funcionalidade completa. 	|
| git init &lt;Diretório&gt; | Cria um repositório do Git vazio no diretório especificado.	|

</details>

<div id='gitconfig'/>

### git config
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Você pode consultar, definir, substituir e remover opções com este comando. Na verdade o nome é a seção e a chave são separadas por um ponto, e seu valor será escapado.*

Esse comando do git permite alterar as configurações do Git na máquina. Por exemplo: fazer o login na sua conta GitHub, permitindo você acessar repositórios que seu usuário tenha permissão.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-config/pt_BR)

#### Parâmetros do git config
| Código     | Resultado |
| ------|:-----:| 
| git config &lt;Chave de Parâmetro&gt; | Permite verificar qual o valor do parâmetro no repositório atual, como por exemplo: user.name .	|
| git config --global &lt;Parâmetro&gt; | Altera o arquivo global ~/.gitconfig em vez do repositório .git/config, ou seja, a mudança nos parâmetros será padrão do Git na máquina.	|
| git config --global user.name &lt;Usuário&gt;| Adiciona seu nome de usuário globalmente, ou seja, altera o usuário padrão do Git na máquina. 	|
| git config --global user.email &lt;Email&gt; | Adiciona seu email de usuário globalmente, ou seja, altera o email de usuário padrão do Git na máquina. 	|

</details>

<div id='gitstatus'/>

### git status
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Exibe os caminhos que têm diferenças entre o arquivo do índice e o commit atual no HEAD, os caminhos que têm diferenças entre a árvore de trabalho e o arquivo do índice, os caminhos na árvore de trabalho que não são rastreados pelo Git (e não foram ignorados pelo gitignore).*

Comando que exibe o estado atual do diretório de trabalho e a área de stage. 

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-status/pt_BR)

#### Parâmetros do git status
| Código     | Resultado |
| ------|:-----:| 
| git status | Exibe a condição da árvore de trabalho. 	|
| git status -s | Saída em formato curto. 	|

</details>

<div id='gitlog'/>

### git log
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Exibe os registros log do commit.*

Comando que exibe o histórico de alterações (commits), apresentando o *hash do commit* e a mensagem do commit. 

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-log/pt_BR)

#### Parâmetros do git log
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git log | Exibe histórico de alterações padrão. 	| |
| git log --oneline | Informação de cada commit ocupa uma linha. 	| |
| git log --parents| Adiciona o hash do commit pai na exibição. 	| Commits gerados pelo comando merge possuem dois commits pais. |
| git log --decorate| Exibe histórico de alterações padrão. 	| Exibe quais commits as branches e a HEAD estão apontando (padrão desde a versão 2.12.2 do git). |

</details>

<div id='gitadd'/>

### git add
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Este comando atualiza o índice utilizando o conteúdo atual encontrado na árvore de trabalho para preparar o conteúdo para o próximo commit. Em geral ele adiciona o conteúdo atual dos caminhos existentes como um todo, mas com algumas opções ele também pode ser utilizado para adicionar o conteúdo com apenas a parte das alterações aplicadas nos arquivos da árvore de trabalho ou remover os caminhos que não existam mais na árvore de trabalho.
O "index" (ou índice) contém um instantâneo do conteúdo da árvore de trabalho que é tomado como o conteúdo do próximo commit. Portanto, depois de fazer alterações na árvore de trabalho e antes de executar o comando commit, você deve utilizar o comando add para adicionar qualquer aquivo novo ou que foi modificado ao índice.*

Comando utilizado para adicionar arquivos ao stage, preparando-os para o commit. Além disso, começa a rastrear alterações no arquivo a partir da sua primeira execução no arquivo. 

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-add/pt_BR)

#### Parâmetros do git add
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git add . | Adiciona todos os arquivos com alteração ao stage 	| Na primeira execução inicia o rastreio dos arquivos |
| git add &lt;Arquivo&gt; | Adiciona o arquivo ao stage 	| Na primeira execução inicia o rastreio do arquivo |

</details>

<div id='gitrm'/>

### git rm
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Remove os arquivos correspondentes ao pathspec do índice, ou da árvore de trabalho e do índice. O comando git rm não removerá um arquivo apenas do seu diretório de trabalho.*

Comando utilizado para remover o arquivo do diretório, e consequentemente, parar de ser rastreado. No entanto, cabe ressaltar que é possível obter o mesmo arquivo através do versionamento, caso o mesmo esteja contido em algum commit anterior.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-rm/pt_BR)

#### Parâmetros do git rm
| Código     | Resultado | 
| ------|:-----:|
| git rm &lt;Arquivo&gt; | Remove o arquivo do diretório. 	|
 
</details> 
 
<div id='gitmv'/>

### git mv
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Mova ou renomeie um arquivo, diretório ou link simbólico.*

Comando utilizado para mover ou renomear um arquivo, diretório e link simbólico. O comando diferencia a renomeação e movimentação dependendo do modo como é definido os parâmetros.

Para renomear basta introduzir seu nome original e o esperado. Por exemplo: 

```
git mv inicial.css final.css
```

No entanto, para mover você deve introduzir como primeiro parâmetro o arquivo/diretório/link e como segundo parâmetro o diretório de destino considerando o arquivo já movido. Por exemplo:

```
git mv inicial.css styles/inicial.css
```

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-mv/pt_BR)

#### Parâmetros do git mv
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git mv &lt;Arquivo Renomear&gt; &lt;Arquivo Renomeado&gt; | Renomea o arquivo, diretório ou link 	| |
| git mv &lt;Origem&gt; &lt;Destino&gt; | Move o arquivo, diretório ou link 	| O parâmetro de origem deve conter o que será movido, e o parâmetro de destino deve conter o parâmetro de origem |

</details>

<div id='gitcommit'/>

### git commit
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Cria um novo commit que tenha todos os conteúdos atuais do índice e a mensagem informada no registro log descrevendo as alterações. Um novo commit é um herdeiro direto do HEAD que em geral é o topo do ramo atual e o ramo é atualizado para apontar para ele.*

Esse comando captura um instantâneo das alterações que atualmente estão no stage do projeto. Os commits podem ser considerado as versões "seguras" de um projeto, pois o Git nunca irá alterá-los sem a requisição explicita. Cabe ressaltar, que devido o instântaneo ser da área de stage, é necessário utilizar o *git add* antes para adicionar as diferenças ao stage.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-commit/pt_BR)

#### Parâmetros do git commit
| Código     | Resultado | Observações
| ------|:-----:|:-----:|
| git commit -m "mensagem" | Cria um instantâneo das alterações que estão na área de stage. 	| |
| git commit . -m "mensagem" | Adiciona todas as alterações rastreadas pelo Git à área de stage e cria um instantâneo.	| Portanto, substitui a utilização do git add previamente ao commit. |
| git commit &lt;Arquivo&gt; -m "mensagem" | Cria um instantâneo com as alterações do respectivo arquivo. 	| As alterações do arquivo não precisa estar na área de stage mas é necessário que o arquivo seja rastreado pelo Git.  |
| git commit -a -m "mensagem" | Permite commitar as alterações que ainda não estão na área de stage. 	| |

</details>

<div id='gitreset'/>

### git reset
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Esses formulários redefinem as entradas do índice para todos os caminhos correspondentes ao &lt;pathspec&gt; à sua condição em &lt;tree-ish&gt;. (Isso não afeta a árvore de trabalho ou a ramificação atual.)
Isto significa que git reset &lt;pathspec&gt; é o oposto de git add &lt;pathspec&gt;. Este comando é equivalente a git restore [--source=&lt;tree-ish&gt;] --staged &lt;pathspec&gt;...*

Esse comando é utilizado para retirar arquivos da área de stage.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-reset/pt_BR)

#### Parâmetros do git reset
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git reset | Retira todos os arquivos da área de stage. 	| |
| git reset --&lt;Arquivo&gt; | Retira o arquivo em específico da área de stage. 	| |
| git reset --hard | Descarta todas as mudanças nos arquivos, retira todos os arquivos da área de stage e desfaz todas as alterações nesses arquivos. 	|   |
| git reset --hard HEAD| Além de reverter as alterações, retorna aos arquivos que tinha no HEAD. 	| Recomendo fortemente a leitura do [seguinte artigo](https://devconnected.com/how-to-git-reset-to-head/#:~:text=To%20hard%20reset%20files%20to,option%20and%20specify%20the%20HEAD.&text=The%20purpose%20of%20the%20%E2%80%9Cgit,before%20HEAD%20and%20so%20on).  |

</details>

<div id='gitrevert'/>

### git revert
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Dado um ou mais commits já existentes, reverta as alterações introduzidas pelos patches relacionados e registre alguns novos commits que registram neles. Isso requer que a sua árvore de trabalho esteja limpa (nenhuma alteração a partir do commit HEAD).*

Desfaz as alterações no repositório. Cabe ressaltar que o processo é feito através de um novo commit com a versão anterior dos arquivos.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-revert/pt_BR)

#### Parâmetros do git revert
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git revert | Desfaz todas as alterações no repositório. 	| | 
| git revert --no-edit | Desfaz todas as alterações no repositório. 	| Não inicia o editor de mensagens do commit. | 
 
</details> 
 
<div id='gitpush'/>

### git push
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Atualiza as refs remotas utilizando as refs locais, enquanto envia os objetos necessários para que seja concluída as refs informadas.*

Esse comando é utilizado para enviar o conteúdo do repositório local para o repositório remoto.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-push/pt_BR)

#### Parâmetros do git push
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git push &lt;Nome Conexão&gt; &lt;Nome Branch&gt; | Envia o conteúdo da branch para o repositório da conexão. 	| Cria a branch caso não exista no repositório remoto. |

</details>

 <div id='gitremote'/>

### git remote
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Gerencie o conjunto de repositórios ("remotos") cujos ramos você monitora.*

Esse comando é utilizado para gerenciar os repositórios remotos que o projeto está inserido.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-remote/pt_BR)

#### Parâmetros do git remote
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git remote | Exibe os nomes dos repositórios remotos adicionados. 	| |
| git remote add &lt;Nome Conexão&gt; &lt;URL Repositório&gt; | Adiciona um repositório remoto 	| Todo repositório remoto precisa possuir um nome distinto dos demais. |
| git remote -v | Exibe os nomes e URL's dos repositórios remotos adicionados. 	| O Git separa em duas URL's: leitura (fetch) e escrita (push). Sendo útil quando se utiliza protocolos diferentes para leitura e escrita. |
| git remote rename &lt;Nome Atual&gt; &lt;Nome Atualizado&gt; | Altera o nome do repositório remoto. 	| |
| git remote set-url &lt;Nome Conexão&gt; &lt;URL&gt; | Altera a URL de conexão. 	| |
| git remote -r | Exibe as branches remotas. 	| |
| git remote -a | Exibe as branches remotas e locais. 	| |
| git remote -r -v | Lista para quais commits as branches remotas estão apontando. 	| |

</details>
 
<div id='gitpull'/>

### git pull
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Incorpora as alterações de um repositório remoto no ramo atual. Em seu modo predefinido, o comando git pull é uma abreviação do comando git fetch seguido por git merge FETCH_HEAD.
Mais precisamente, o comando git pull executa o git fetch com os parâmetros informados e chama o git merge para mesclar os cabeçalhos recuperados da ramificação no ramo atual. Com --rebase, ele executa o comando git rebase em vez do git merge.*

Esse comando é utilizado para buscar e baixar o conteúdo de repositórios remotos, além de fazer a atualização imediata do repositório local para que os conteúdos sejam iguais. Portanto, é o mesmo que git fetch ＜remote＞ seguido de git merge origin/＜current-branch＞.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-pull/pt_BR)

#### Parâmetros do git pull
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git pull &lt;Nome Conexão&gt; &lt;Nome Branch&gt; | Baixa e atualiza a branch especificada no repositório local. 	| |
| git pull &lt;Nome Conexão&gt;  | Baixa e atualiza a branch atual no repositório local. 	| |
| git pull --no-commit &lt;Nome Conexão&gt;  | Baixa e atualiza a branch atual no repositório local. 	| Não cria um commit de merge |
| git pull --rebase &lt;Nome Conexão&gt;  | Baixa e atualiza a branch atual no repositório local. 	| Em vez de usar git merge para a atualização do repositório local, utiliza o git rebase. |
 
 </details>
 
 <div id='gitbranch'/>

### git branch
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Lista, cria ou exclui ramificações.*

Comando utilizado para exibir, criar ou excluir branches. As branches permitem trabalhar distintamente utilizando um commit em especifíco como base, ou seja, pode-se trabalhar a parte à partir do código sem afetar o código de origem (normalmente a master).

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-branch/pt_BR)

#### Parâmetros do git branch
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git branch | Exibe as branches do nosso repositório local. 	| |
| git branch -v | Exibe as branches do nosso repositório local com seus commits associados.	| |
| git branch &lt;Nome Branch&gt; | Cria uma nova branch. 	| |
| git branch -d &lt;Nome Branch&gt; | Excluí a branch informada. 	| Não é possível excluir com -d uma branch que possua commits não aplicados em outras branches. |
 
</details> 
 
<div id='gitcheckout'/>

### git checkout
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Atualiza os arquivos na árvore de trabalho para coincidir com a versão no índice ou na árvore informada. Se nenhum "pathspec" seja utilizado, o comando git checkout também atualizará o HEAD para definir o ramo informado como o ramo atual.*

Esse comando é utilizado para alterar entre as branches ou restaurar arquivos.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-checkout/pt_BR)

#### Parâmetros do git checkout
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git checkout &lt;Nome Branch&gt; | Muda a branch atual para a especificada. 	| |
| git checkout -b &lt;Nome Branch&gt; | Cria e muda a branch atual para a especificada.	| |
| git checkout -- &lt;Arquivo&gt; | Restaura o arquivo. 	| Desfaz somente as alterações que não estão na área de stage. Caso exista alguma alteração dentro da área de stage, essa alteração não será desfeita. |
 
</details> 
 
<div id='gitswitch'/>

### git switch
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Alterna para um ramo específico. A árvore de trabalho e o índice são atualizados para coincidir com o ramo. Todos os novos commits serão adicionadas ao cume deste ramo.*

Esse comando é utilizado para alterar entre as branches. Cabe ressaltar que o comando git checkout, a partir da versão 2.23.0 do Git, foi separado em dois comandos: git switch e git restore. Essa divisão visa diminuir as confusões pelo fato do git checkout possuir duas responsabilidades distintas.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-switch/pt_BR)

#### Parâmetros do git switch
| Código     | Resultado | 
| ------|:-----:|
| git switch &lt;Nome Branch&gt; | Muda a branch atual para a especificada. 	|
| git switch -c &lt;Nome Branch&gt; | Cria e muda a branch atual para a especificada. 	|

</details>

<div id='gitrestore'/>

### git restore
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Restaure os caminhos definidos na árvore de trabalho com algum conteúdo de uma fonte de restauração. Se um caminho for monitorado, porém não existir na fonte de restauração, ele será removido para coincidir com a fonte.*

Esse comando é utilizado para restaurar arquivos. Cabe ressaltar que o comando git checkout, a partir da versão 2.23.0 do Git, foi separado em dois comandos: git switch e git restore. Essa divisão visa diminuir as confusões pelo fato do git checkout possuir duas responsabilidades distintas.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-restore/pt_BR)

#### Parâmetros do git restore
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git restore --source &lt;Hash Commit&gt; . | Restaura todo o projeto até o commit especificado. 	| |
| git restore -- &lt;Nome Arquivo&gt; | Restaura o arquivo que está visível (working tree) para o do commit apontado pelo HEAD. 	|  |
| git restore -- &lt;Nome Arquivo1&gt; &lt;Nome Arquivo2&gt; | Restaura os arquivos que está visível (working tree) para o do commit apontado pelo HEAD. 	| Quantidade de arquivos indefinidos.  |

</details>

<div id='gitmerge'/>

### git merge
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Incorpora as alterações dos commits citados (desde o momento em que os seus históricos divergirem do ramo atual) para dentro do ramo atual. Este comando é utilizado pelo git pull para incorporar as alterações vindos de outro repositório e pode ser utilizado manualmente para mesclar as alterações do outro ramo para um outro.*

Esse comando une dois ou mais históricos de desenvolvimento (branches). Assim, permite que você pegue as linhas de desenvolvimento independentes e integre em uma ramificação única. Além disso, a branch atual é atualizada para refletir a mesclagem, no entanto, o branch alvo não sofre alterações.

Cabe ressaltar que normalmente é gerado um commit de mesclage, no entanto, caso ocorra uma mesclagem de avanço rápido (a branch atual não recebeu commits posteriores a criação da branch alvo) não ocorrerá a criação de um commit de mesclagem.

Recomendo fortemente a leitura do seguinte [artigo.](https://www.atlassian.com/br/git/tutorials/using-branches/git-merge) 

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-merge/pt_BR)

#### Parâmetros do git merge
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git merge &lt;Branch Alvo&gt; | Mescla os commits da branch especificada na branch atual. 	| A branch especificada não sofre alterações. |
| git merge --no-ff &lt;Branch Alvo&gt; | Mescla os commits da branch especificada na branch atual.	| Obrigatoriamente gera um commit de mesclagem. |

</details>

<div id='gitrebase'/>

### git rebase
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Caso o &lt;ramo&gt; seja utilizado, o comando git rebase executará um git switch &lt;ramo&gt; automaticamente antes de fazer qualquer outra coisa. Caso contrário, ele permanecerá no ramo atual.*

Esse comando reaplica os commits da branch alvo na branch atual. Dessa forma, faz parecer que a branch atual foi recriada a partir de um commit diferente (o commit HEAD da branch alvo). O Git faz isso criando novos commits e aplicando-os à base especificada.

Recomendo fortemente a leitura do seguinte [artigo.](https://www.atlassian.com/br/git/tutorials/rewriting-history/git-rebase) 

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-rebase/pt_BR)

#### Parâmetros do git rebase
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git rebase &lt;Branch alvo&gt; | Reaplica os commits da branch alvo na branch atual. 	| A branch alvo se mantém intacta. |
| git rebase --interactive &lt;Branch alvo&gt; | Reaplica os commits da branch alvo na branch atual. 	| Abre uma sessão interativa com mais opções de configurações do rebase. |
 
</details> 
 
<div id='gitdiff'/>

### git diff
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Exibe as alterações entre a árvore de trabalho, o índice ou uma árvore, as alterações entre o índice e uma árvore, as alterações entre as duas árvores, nas alterações resultantes de uma mesclagem, nas alterações entre dois objetos gota ou nas alterações entre dois arquivos no disco.*

Esse comando é utilizado para exibir as mudanças entre commits, o commit, os repositórios etc.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-diff/pt_BR)

#### Parâmetros do git diff
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git diff | Exibe a diferença entre os arquivos do diretório local e a área de stage. 	| | 
| git diff &lt;Arquivo&gt; | Exibe a diferença entre o arquivo do diretório local e a área de stage. 	| | 
| git diff --staged | Exibe a diferença entre os arquivos da área de stage e o último commit. 	| | 
| git diff --cached | Mesmo efeito de git diff --staged. 	| Única opção antes da versão 1.6.1 do Git | 
| git diff &lt;Commit&gt; | Exibe as alterações dentro e fora do stage com relação ao commit especificado. 	| | 
| git diff HEAD | Exibe as alterações dentro e fora do stage com relação ao commit que o HEAD está apontando.	| | 
| git diff &lt;Commit1&gt;..&lt;Commit2&gt; | Exibe as mudanças comitadas realizadas a partir do commit1 até o commit2. 	| Dado que é mostrado as linhas (-) e (+) necessárias para converter o commit1 no próximo commit, e assim sucessivamente até o commit2, a inversão da ordem dos commits gera a inversão dos sinais (-) e (+) dos resultados. | 
| git diff &lt;Commit&gt;~n | Exibe as mudanças nos arquivos do commit inserido como parâmetro em relação aos n commits realizados imediatamente antes. 	| Inclui mudanças não comitadas, sejam elas fora ou dentro da área de stage. | 
 
</details> 
 
<div id='gitclone'/>

### git clone
<details>

<summary> Conteúdo: </summary>
De acordo com a documentação do git :

>*Clona um repositório em um diretório recém-criado, cria o monitoramento remoto dos ramos para cada ramo no repositório clonado (visível utilizando git branch --remotes), cria e verifica um ramo inicial que é bifurcado do ramo ativo atualmente do repositório clonado.*

Clona um repositório a partir de sua URL, criando um repositório local idêntico ao especificado.

Caso queira consultar a documentação (PT-BR) [clique aqui.](https://git-scm.com/docs/git-clone/pt_BR)

#### Parâmetros do git clone
| Código     | Resultado | Observações
| ------|:-----:| :-----:|
| git pull &lt;URL&gt; | Cria um repositório local idêntico ao repositório da URL especificada 	| |

</details>

<div id='certificacoes'/>

## Minhas certificações sobre o assunto
[Git e GitHub: Repositório, Commit e Versões (Alura)](https://cursos.alura.com.br/certificate/6f31f8d1-9769-4d4b-996f-034822ac0407)
