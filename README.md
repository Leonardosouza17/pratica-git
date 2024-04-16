# pratica-git

Repositório para práticas dos comandos do Git

~~~bash
git config --global core.editor "code --wait"
~~~

~~~bash
git commit --allow-empty
~~~

o parâmetro `allow-empty` permite a criação de um commit vazio, para fins de testes e práticas do git.

~~~bash
git commit -a
~~~

o parâmetro `-a` adiciona todos os arquivos modificados ou não ignorados ao commit inicial.

~~~bash
git checkout -b novoBranch
~~~

o parâmetro `-b` alterna para ``novoBranch` criando o branch. o mesmo acontece com o comando `git switch` com o parâmetro `-c`.

~~~bash
git branch -D nomeBranch
git push --delete origin nomeBranch
~~~

Para apagar um branch é preciso primeiro apagá-lo localmente (1° comando) e depois  propagar a deleção para o repositório remoto (2° comando).

~~~bash
git log --graph --oneline
~~~

O comando `log` exibe o histórico de commits em detalhes. Com as flags `--graph` e `--oneline` exibe o histórico em um formato mais compreeensivel, através de um grafo (grafo?) 

### Rebase interativo

Para alterar o autor de um commit, você pode utilizar o rebase interativo e o comando `commit --amend` .

**Antes, porém**, verifique se o editor de mensagens do commit está cofigurado para o editor do próprio VS Code

~~~bash
git rebase -i <referenciaCommit>
~~~

A referência do commit deve ser sempre para o commit anterior ao commit que deve ser alterado.

No editor de commits, altere a instrução do commit desejado de `pick` para `edit`. Em seguida grave e feche o editor.

O rebase  fará uma pausa para que você altere as informações do autor.

~~~bash
git commit --amend --reset-author  --no-edit
~~~

Caso você queira especificar o autor, utilize a flag `--author="nome do autor <email@autor>"`, nesse exato formato.

Caso seu commit seja vazio, acrescente ainda a flag `--allow-empty`.

Após o reparo do commit,  continue o processo do rebase com o comando abaixo.

~~~bash
git rebase --continue
~~~

Finalmente, **confira o novo histórico localmente** e envie ao repositório remoto **forçadamente**.

~~~bash
git push --force
~~~~


