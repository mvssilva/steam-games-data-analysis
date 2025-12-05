# Steam Games Text Analytics: Unsupervised Learning

Este projeto aplica técnicas de **Processamento de Linguagem Natural (NLP)** e **Aprendizado Não Supervisionado (Clustering)** para investigar relações semânticas entre descrições de jogos da Steam e seus respectivos gêneros.

[cite_start]O objetivo principal é agrupar jogos com base apenas em suas descrições textuais e verificar se esses agrupamentos correspondem às classificações de gênero reais (ex: Action, RPG, Strategy)[cite: 32, 33, 34].

## 📂 Sobre o Dataset

[cite_start]O conjunto de dados utilizado provém de datasets públicos da Steam (Kaggle) e contém informações detalhadas sobre os jogos[cite: 8, 9]. As principais colunas utilizadas na análise são:

* [cite_start]**description / short_description**: Texto descritivo do jogo (utilizado para agrupamento)[cite: 13, 21].
* [cite_start]**genres**: Gêneros associados ao jogo (utilizado para validação)[cite: 12].
* [cite_start]**Outros atributos**: Preço, avaliações positivas/negativas, tempo médio de jogo[cite: 16, 17, 19].

## 🚀 Metodologia (Pipeline)

O projeto segue um pipeline clássico de Ciência de Dados para textos, conforme as etapas abaixo:

1.  [cite_start]**Pré-processamento de Texto**: Limpeza, tokenização e normalização das descrições dos jogos[cite: 41].
2.  **Extração de Características (Feature Extraction)**:
    * [cite_start]Criação da matriz **TF-IDF** para representar a importância dos termos[cite: 42].
    * [cite_start]*(Opcional/Extra)* Uso de **Embeddings** com modelos de linguagem (SentenceTransformers) para captura semântica[cite: 50, 57].
3.  **Redução de Dimensionalidade**:
    * [cite_start]Aplicação de **PCA** (Principal Component Analysis) ou **Truncated SVD** para reduzir o ruído e a complexidade dos dados antes do agrupamento[cite: 43].
4.  **Agrupamento (Clustering)**:
    * [cite_start]Aplicação de algoritmos de aprendizado não supervisionado (ex: K-Means, DBSCAN ou Hierárquico) para segmentar os jogos[cite: 46].
5.  **Análise e Validação**:
    * Interpretação dos clusters formados.
    * [cite_start]Verificação da distribuição de gêneros dentro de cada grupo para validar a hipótese de similaridade textual[cite: 33, 47].

## 🛠 Tecnologias Utilizadas

* **Python 3**
* **Pandas & NumPy**: Manipulação e análise de dados.
* **Scikit-Learn**: Algoritmos de ML (Clustering), PCA e TF-IDF.
* **NLTK / Spacy**: Processamento de linguagem natural.
* **Matplotlib / Seaborn**: Visualização de dados.
* [cite_start]**SentenceTransformers (Hugging Face)**: Geração de embeddings (etapa avançada)[cite: 57].

## 📊 Resultados Esperados

O projeto busca responder às seguintes perguntas de negócio/pesquisa:
* [cite_start]Há uma diferença clara nas distribuições de gêneros entre os grupos formados apenas pelo texto? [cite: 89]
* [cite_start]As descrições dos jogos são preditores confiáveis de seus gêneros? [cite: 90]

---
*Este projeto foi desenvolvido como parte da disciplina de [Nome da Disciplina] da [Sua Faculdade].*
