---
aliases: [TF-IDF, Vetorização, Bag of Words, Embeddings]
tags: [data-science, nlp, tf-idf, text-mining]
area: Data Science
status: Pendente
data: 2026-04-30
---
## Resumo (TL;DR)

Para que um computador analise textos, precisamos da **Vetorização**, o processo de transformar documentos em representações numéricas[cite: 37]. A evolução mais importante do método simples de contagem de palavras (*Bag of Words*) é o **TF-IDF (Term Frequency - Inverse Document Frequency)**, que calcula a importância de um termo baseando-se na sua frequência no documento contra a sua raridade no conjunto total[cite: 38, 39]. Palavras que aparecem muito, mas em todos os documentos, perdem peso, enquanto termos específicos que diferenciam uma reunião da outra ganham relevância[cite: 39].

## Conceitos Principais

- **Limitações do Bag of Words:**
    - Conta apenas as ocorrências, ignorando o contexto e a importância relativa das palavras[cite: 38].
- **A Mecânica do TF-IDF:**
    - **TF (Term Frequency):** Mede quantas vezes o termo aparece no documento específico[cite: 39].
    - **IDF (Inverse Document Frequency):** Penaliza palavras muito comuns no conjunto total e valoriza as raras[cite: 39].
    - *Intuição:* "Quais palavras realmente diferenciam uma transcrição das outras?"[cite: 39].
- **Análise Exploratória Textual:**
    - Após a vetorização, busca-se ir além da simples contagem para gerar interpretação[cite: 41].
    - Em vez de "A palavra suporte apareceu 15 vezes" (fraco), o insight deve ser "A palavra suporte aparece associada a termos como demora, indicando risco de retenção" (forte)[cite: 41].
- **Embeddings (Evolução):**
    - Enquanto o TF-IDF foca em frequência, os Embeddings (representações vetoriais densas) capturam o **contexto e a similaridade semântica**[cite: 45].
    - Frases como "cancelar contrato" e "encerrar parceria" podem ser identificadas como similares mesmo usando palavras diferentes[cite: 45].

## Exemplos Práticos / Código
```python
import pandas as pd
from sklearn.feature_extraction.text import TfidfVectorizer

# Textos já limpos
textos = ["suporte demorou avaliando cancelar", "gostamos erp queremos proposta"]

# Inicializando o TF-IDF
# max_features: limita o vocabulário; ngram_range=(1,2): pega palavras isoladas e pares
tfidf = TfidfVectorizer(max_features=100, ngram_range=(1,2))

# Gerando a matriz
matriz_tfidf = tfidf.fit_transform(textos)

# Convertendo para DataFrame para visualização
df_tfidf = pd.DataFrame(
    matriz_tfidf.toarray(),
    columns=tfidf.get_feature_names_out()
)
print(df_tfidf.head())
```
## 🔗 Conexões
- [[08 - NLP aplicado à Inteligência de Negócio]]

- [[10 - ANOVA e Tamanho de Efeito]]