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