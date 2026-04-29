# Comandos git

Esse repositório tem o objetivo de ter informações sobre o uso do git, desde comando básicos para um commit quanto de versionamento de código. 

## Como clonar um repositório?

```Bash
git clone link_do_repositório

cd nome_do_repositório

code .

```

## Como fazer um commit?

```Bash
git add .
git commit -m "Descriação das alterações feitas"
git push origin nome_da_branch
```

## Como trazer atualizações do repositório para o meu repo local?
```Bash
git push origin nome_da_branch
```

## Como excluir arquivos da branch
```Bash
git rm nome_do_arquivo

#Para o caso de pastas ou arquivos dentro de pastas
git rm -r nome_da_pasta ou caminho_do_arquivo

# Suba as alteações pro github
git commit -m "Exclusão de arquivos"
git push origin nome_da_branch
```

## Como saber em qual branch eu estou? Como criar uma nova branch?
```Bash

```


## Como criar um ambiente virtual?

```Bash
python3 -m venv "nome do ambiente"

source nome_do_ambiente/bin/activate

```

#
