# Comandos Git

Este repositório tem como objetivo reunir informações sobre o uso do Git, desde comandos básicos para realizar commits até operações de versionamento de código.


## 📥 Como clonar um repositório? 
```bash
git clone link_do_repositorio
cd nome_do_repositorio

# Abrir a pasta no VS Code
code .
```

## ✅ Como fazer um commit?
```bash
git add .
git commit -m "Descrição das alterações feitas"
git push origin nome_da_branch
```

## 🔄 Como trazer atualizações do repositório remoto?
```bash
git pull --rebase origin nome_da_branch
```

## ⚠️ Fiz alterações sem atualizar a branch, o que fazer?

```bash
# Traga as atualizações do repositório remoto
git pull origin nome_da_branch
```
Se houver conflito o git irá avisar e vc precisará resolver manualmente

Após resolver os conflitos, continue o rebase e envie as alterações pro repositório:

```bash
git add .
git rebase --continue
git push origin nome_da_branch
```

## 🗑️ Como excluir arquivos da branch?
```bash
git rm nome_do_arquivo

# Para pastas ou arquivos dentro de pastas
git rm -r nome_da_pasta_ou_caminho

# Envie as alterações pro repositório
git commit -m "Exclusão de arquivos"
git push origin nome_da_branch
```

## 🌿 Como saber em qual branch estou e criar uma nova?
```Bash
# Ver a branch atual
git branch

# Criar uma nova branch
git branch nome_da_branch

# Trocar para a nova branch
git checkout nome_da_branch

# Para fazer tudo com um único comando
git checkout -b nome_da_branch
```


## 🐍 Como criar um ambiente virtual Python?

```Bash
python3 -m venv "nome do ambiente"

# Ativar ambiente
source nome_do_ambiente/bin/activate

```

