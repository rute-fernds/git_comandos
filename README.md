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
git pull origin nome_da_branch
```

## ⚠️ Fiz alterações sem atualizar a branch, o que fazer?

Nessa situação, podem ter ocorrido dois cenários. Siga as instruções conforme o seu caso:

### 1. Ainda não fiz commit (apenas editei os arquivos)
Se você fez alterações locais, mas percebeu que a branch remota está à frente, o Git permite “guardar” temporariamente seu trabalho para atualizar a branch com segurança.

```bash
# Guarda suas alterações temporariamente
git stash

# Atualiza a branch local com a versão remota
git pull origin nome_da_branch

# Restaura suas alterações
git stash pop
```

Se houver conflitos durante o git stash pop, o Git irá avisar e você precisará resolvê-los manualmente.

Após resolver ou se não houver conflitos, finalize normalmente:

```bash
git add .
git commit -m "Descrição das alterações"
git push origin nome_da_branch
```

### 2. Já fiz commit local, mas não consigo dar push

Se você já fez commit, mas o git push foi rejeitado (geralmente porque a branch remota está à frente), você precisa integrar as mudanças remotas antes de enviar as suas.

A forma mais recomendada é usar rebase:

```bash
# Atualiza sua branch aplicando seus commits por cima da versão remota
git pull --rebase origin nome_da_branch
```

Se não houver conflito, após o processo de rebase rode:
```bash
git pull origin nome_da_branch
```
Se houver conflitos, o Git irá interromper o processo e você deverá resolvê-los manualmente.

Depois de resolver:

```bash
git add .
git rebase --continue
git pull origin nome_da_branch
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

