# 📘 Documentação de Funções

Este arquivo tem como objetivo documentar funções utilizadas no projeto, explicando sua finalidade, parâmetros, retorno e exemplos de uso.

---

## 🧠 `nomeDaFuncao(param1, param2)`

**Descrição:**  
Explica de forma breve e clara o que a função faz.

**Parâmetros:**
- `param1` (*tipo*): descrição do parâmetro.
- `param2` (*tipo*): descrição do parâmetro.

**Retorno:**
- *tipo*: descrição do que é retornado pela função.

**Exemplo de uso:**
```python
resultado = nomeDaFuncao(valor1, valor2)
print(resultado)
```
## 🔠 `capitalize_words(text)`
**Descrição:**
Capitaliza a primeira letra de cada palavra em uma string.

**Parâmetros:**

- `text (str):` texto a ser capitalizado.

**Retorno:**

`str:` texto com as palavras iniciadas em letra maiúscula.

**Exemplo de uso:**
```python
resultado = capitalize_words("documentação de funções")
print(resultado)  # Saída: "Documentação De Funções"
```
## 🔢 `is_prime(n)`
**Descrição:**
Verifica se um número é primo.

**Parâmetros:**

`n (int):` número inteiro positivo.

**Retorno:**

`bool:` True se for primo, False caso contrário.

**Exemplo de uso:**

```python
resultado = is_prime(7)
print(resultado)  # Saída: True
```
## 🔁 `reverse_list(lista)`
**Descrição:**
Inverte a ordem dos elementos de uma lista.

**Parâmetros:**

lista (list): lista com qualquer tipo de elementos.

**Retorno:**

`list:` lista invertida.

**Exemplo de uso:**

```python
resultado = reverse_list([1, 2, 3])
print(resultado)  # Saída: [3, 2, 1]
```
## 📏 `count_vowels(text)`
**Descrição:**
Conta quantas vogais existem em uma string.

**Parâmetros:**

`text (str):` texto de entrada.

**Retorno:**

`int:` quantidade de vogais encontradas.

**Exemplo de uso:**

```python
resultado = count_vowels("Python é divertido")
print(resultado)  # Saída: 6
```
## ✂️ `clean_text(text)`
**Descrição:**
Realiza limpeza de texto removendo pontuações, espaços extras e convertendo para minúsculas.

**Parâmetros:**

`text (str):` texto bruto.

**Retorno:**

`str:` texto limpo e padronizado.

**Exemplo de uso:**

```python
resultado = clean_text("Olá, Mundo!  ")
print(resultado)  # Saída: "olá mundo"
```
# 🔡 `tokenize_text(text)`
**Descrição:**
Divide o texto em tokens (palavras).

**Parâmetros:**

`text (str):` texto a ser tokenizado.

**Retorno:**

`list[str]:` lista de tokens.

Exemplo de uso:

```python
resultado = tokenize_text("machine learning é poderoso")
print(resultado)  # Saída: ['machine', 'learning', 'é', 'poderoso']
```
## 📦 `text_to_vector(text, model)`
**Descrição:**
Transforma um texto em vetor numérico usando um modelo de embedding (ex: Word2Vec, BERT, etc).

**Parâmetros:**

`text (str):` texto de entrada.

model: modelo pré-treinado de embeddings.

**Retorno:**

`np.ndarray:` vetor que representa semanticamente o texto.

**Exemplo de uso:**

```python
vector = text_to_vector("exemplo de texto", embedding_model)
```
## 🔍 `cosine_similarity(vec1, vec2)`
**Descrição:**
Calcula a similaridade do cosseno entre dois vetores.

**Parâmetros:**

`vec1 (np.ndarray):` primeiro vetor.

`vec2 (np.ndarray):` segundo vetor.

**Retorno:**

`float:` valor de similaridade (entre -1 e 1).

**Exemplo de uso:**

```python
similaridade = cosine_similarity(vec1, vec2)
print(similaridade)  # Saída: 0.87 (por exemplo)
```
## 🧠 `generate_text(prompt, model, max_tokens=50)`
**Descrição:**
Gera texto com base em um prompt usando um modelo de linguagem (como GPT, LLaMA, etc).

**Parâmetros:**

`prompt (str):` texto de entrada.

`model:` modelo de linguagem.

`max_tokens (int):` limite de geração.

**Retorno:**

`str:` texto gerado pelo modelo.

**Exemplo de uso:**

```python
resposta = generate_text("Explique redes neurais:", modelo)
print(resposta)
```
## 🧹 `remove_stopwords(tokens, stopwords)`
**Descrição:**
Remove palavras irrelevantes ("stopwords") de uma lista de tokens.

**Parâmetros:**

`tokens (list[str]):` lista de palavras/tokenizadas.

`stopwords (set[str]):` conjunto de palavras a serem removidas.

**Retorno:**

`list[str]:` lista de tokens sem as stopwords.

**Exemplo de uso:**

```python
resultado = remove_stopwords(['isso', 'é', 'um', 'teste'], {'é', 'um'})
print(resultado)  # Saída: ['isso', 'teste']
```
## 🌱 `stem_tokens(tokens)`
**Descrição:**
Aplica stemming nos tokens, reduzindo as palavras às suas raízes.

**Parâmetros:**

`tokens (list[str]):` lista de palavras.

**Retorno:**

`list[str]:` lista com as palavras stemmed.

**Exemplo de uso:**

```python
from nltk.stem import PorterStemmer
stemmer = PorterStemmer()
```
```python
resultado = stem_tokens(['running', 'flies', 'easily'])
print(resultado)  # Saída: ['run', 'fli', 'eas']
```
## 🍃 `lemmatize_tokens(tokens, lemmatizer)`
**Descrição:**
Aplica lematização nos tokens usando um lematizador.

**Parâmetros:**

`tokens (list[str]):` lista de palavras.

`lemmatizer:` objeto lematizador (ex: WordNetLemmatizer).

**Retorno:**

`list[str]:` lista com os lemas das palavras.

**Exemplo de uso:**

```python
from nltk.stem import WordNetLemmatizer
lemmatizer = WordNetLemmatizer()
```
```python
resultado = lemmatize_tokens(['running', 'flies'], lemmatizer)
print(resultado)  # Saída: ['running', 'fly']
```

## 🌐 `generate_embedding(text, tokenizer, model)`
**Descrição:**
Gera um embedding vetorial para um texto usando um modelo e tokenizador.

**Parâmetros:**

`text (str):` texto a ser convertido.

`tokenizer:` tokenizador do modelo (ex: da HuggingFace).

`model:` modelo de linguagem pré-treinado.

**Retorno:**

`np.ndarray:` vetor numérico representando o texto.

**Exemplo de uso:**

```python
inputs = tokenizer("Exemplo", return_tensors="pt")
outputs = model(**inputs)
embedding = outputs.last_hidden_state.mean(dim=1).squeeze()
```
## 📊 `plot_word_frequency(tokens, top_n=20)`
**Descrição:**
Plota as top_n palavras mais frequentes em um gráfico de barras.

**Parâmetros:**

`tokens (list[str]):` lista de tokens.

`top_n (int):` número de palavras a exibir.

**Retorno:**

`None:` exibe um gráfico matplotlib.

**Exemplo de uso:**

```python
plot_word_frequency(['ai', 'é', 'incrível', 'ai', 'ai', 'incrível'], top_n=2)
```
## ☁️ `generate_wordcloud(text)`
**Descrição:**
Gera uma nuvem de palavras visual a partir do texto.

**Parâmetros:**

`text (str):` texto de entrada.

**Retorno:**

`None:` exibe a nuvem de palavras.

**Exemplo de uso:**

```python
generate_wordcloud("inteligência artificial é incrível e poderosa")
```
