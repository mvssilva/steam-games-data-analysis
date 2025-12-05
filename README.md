# Steam Games Text Analytics: Unsupervised Learning

Este projeto aplica técnicas de **Processamento de Linguagem Natural (NLP)** e **Aprendizado Não Supervisionado (Clustering)** para investigar relações semânticas entre descrições de jogos da Steam e seus respectivos gêneros.

O objetivo principal é agrupar jogos com base apenas em suas descrições textuais e verificar se esses agrupamentos correspondem às classificações de gênero reais (ex: Action, RPG, Strategy)[cite: 32, 33, 34].

## Sobre o Dataset

O conjunto de dados utilizado provém de datasets públicos da Steam e contém informações detalhadas sobre os jogos. As principais colunas utilizadas na análise são:

* **description / short_description**: Texto descritivo do jogo (utilizado para agrupamento).
* **genres**: Gêneros associados ao jogo (utilizado para validação).

Informações que estão presentes no conjunto de dados e não seram utilizadas nessa pesquisa.
* **Outros atributos**: Preço, avaliações positivas/negativas, tempo médio de jogo.

## Metodologia 

O projeto segue um pipeline clássico de Ciência de Dados para textos, conforme as etapas abaixo:

1.  **Pré-processamento de Texto**: Limpeza, tokenização e normalização das descrições dos jogos.
2.  **Extração de Características (Feature Extraction)**:
    * Criação da matriz **TF-IDF** para representar a importância dos termos.
    * *(Opcional/Extra)* Uso de **Embeddings** com modelos de linguagem (SentenceTransformers) para captura semântica.
3.  **Redução de Dimensionalidade**:
    * Aplicação de **PCA** (Principal Component Analysis) para reduzir o ruído e a complexidade dos dados antes do agrupamento.
4.  **Agrupamento (Clustering)**:
    * Aplicação de algoritmos de agrupamento (Ainda serão escolhidos) para segmentar os jogos.
5.  **Análise e Validação**:
    * Interpretação dos clusters formados.
    * Verificação da distribuição de gêneros dentro de cada grupo para validar a hipótese de similaridade textual.

## Tecnologias Utilizadas

* **Python 3**
* **Pandas & NumPy**: Manipulação e análise de dados.
* **Scikit-Learn**: Algoritmos de ML (Clustering), PCA e TF-IDF.
* **NLTK / Spacy**: Processamento de linguagem natural.
* **Matplotlib / Seaborn**: Visualização de dados.
* **SentenceTransformers (Hugging Face)**: Geração de embeddings (etapa avançada).

## Resultados Esperados

O projeto busca responder às seguintes perguntas de negócio/pesquisa:
* Há uma diferença clara nas distribuições de gêneros entre os grupos formados apenas pelo texto? 
* As descrições dos jogos são preditores confiáveis de seus gêneros? 

Este projeto foi desenvolvido na disciplina de Ciência de Dados da Universidade Federal do Espírito Santo (UFES), ministrada pelo Prof. Giovanni Comarela.
