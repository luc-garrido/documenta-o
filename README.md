## 🌱 `git init`
**Descrição:**

Inicializa um novo repositório Git no diretório atual.

**Exemplo de uso:**

```python
git init
```
## ➕ `git add`
**Descrição:**
Adiciona arquivos ao staging area (preparando para o commit).

**Parâmetros:**

`arquivo (str):` caminho do arquivo ou . para todos.

**Retorno:**

Arquivo(s) preparado(s) para commit.

**Exemplo de uso:**
```python
git add.
```
## 💾 `git commit -m "mensagem"`
**Descrição:**
Cria um commit com as alterações que estão no staging area.

**Parâmetros:**

`-m (str):` mensagem de commit.

**Retorno:**

Histórico salvo com as mudanças.

**Exemplo de uso:**
```python
git commit -m
```
"Adiciona função de limpeza de texto"


## ⬇️ `git pull`
**Descrição:**
Atualiza o repositório local com as últimas mudanças do repositório remoto.

**Parâmetros:**

`remoto (opcional):` nome do remoto (ex: origin).

`branch (opcional):` nome da branch (ex: main).

**Retorno:**

Baixa e integra alterações remotas.

**Exemplo de uso:**

```python
git pull origin main
```
## ⬆️ `git push`
**Descrição:**
Envia commits locais para o repositório remoto.

**Parâmetros:**

`remoto (str):` nome do remoto.

`branch (str):` nome da branch.

**Retorno:**

Atualiza o repositório remoto com seus commits.

**Exemplo de uso:**

```python
git push origin main
```
## 🔀 `git merge`
**Descrição:**
Mescla outra branch com a branch atual.

**Parâmetros:**

`branch (str):` nome da branch que será mesclada.

**Retorno:**

Aplica as alterações da outra branch na atual.

**Exemplo de uso:**

```python
git merge feature-xyz
```
## 🌳 `git branch`
**Descrição:**
Lista, cria ou deleta branches.

**Parâmetros:**

`branch (str, opcional):` nome da nova branch.

**Retorno:**

Exibe lista de branches ou cria/deleta.

**Exemplo de uso:**

```python
git branch nova-feature
```
## 🔁 `git checkout`
**Descrição:**
Alterna entre branches ou restaura arquivos.

**Parâmetros:**

`branch/commit/arquivo (str):` o que deseja acessar.

**Retorno:**

Altera o HEAD ou recupera um arquivo.

**Exemplo de uso:**

```python
git checkout main
```
## 🧼 `git clean`
**Descrição:**
Remove arquivos não monitorados do diretório de trabalho.

**Parâmetros:**

`-f:` força a remoção.

**Retorno:**
Remove arquivos temporários.

**Exemplo de uso:**

```python
git clean -f
```

## 🔄 `git fetch`
**Descrição:**
Baixa as atualizações do repositório remoto sem aplicar.

**Parâmetros:**

`remoto (opcional):` nome do repositório remoto.

**Retorno:**
Atualizações locais do repositório remoto.

**Exemplo de uso:**

```python
git fetch origin
```
## 🧭 `git status`
**Descrição:**
Exibe o estado atual do repositório.

**Parâmetros:**
Nenhum.

**Retorno:**
Mostra arquivos modificados e pendentes.

Exemplo de uso:
```python
git status
```
## 📜 `git log`
**Descrição:**
Exibe o histórico de commits.

**Parâmetros:**

`--oneline (opcional):` exibe resumo.

**Retorno:**
Histórico de commits.

**Exemplo de uso:**

```python
git log --oneline
```
## 🧪 `git diff`
**Descrição:**
Mostra as diferenças entre arquivos.

**Parâmetros:**
Nenhum ou nome de arquivos específicos.

**Retorno:**
Alterações não commitadas.

**Exemplo de uso:**

```python
git diff
```
## 🗑️ `git reset`
**Descrição:**
Desfaz commits ou alterações no staging.

**Parâmetros:**

`--soft, --mixed, --hard:` nível de reset.

**Retorno:**
Volta o estado do repositório.

**Exemplo de uso:**

```python
git reset --hard HEAD~1
```
## 🗃️ `git clone`
**Descrição:**
Clona um repositório remoto para a máquina local.

**Parâmetros:**

`url (str):` URL do repositório.

**Retorno:**
Copia todos os arquivos e histórico.

**Exemplo de uso:**

```python
git clone https://github.com/usuario/repositorio.git
```
