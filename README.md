# Recommender-System-with-Apache-Spark-MLlib

Este projeto envolve a construção de um sistema de recomendação usando Apache Spark MLlib. O objetivo é fornecer recomendações personalizadas aos usuários com base em conjuntos de dados de avaliações de filmes.

## Descrição

- O sistema de recomendação é desenvolvido utilizando o algoritmo ALS (Alternating Least Squares) disponível no MLlib do Apache Spark. O ALS é uma técnica comumente usada para filtragem colaborativa em sistemas de recomendação.

**O projeto consiste nos seguintes passos principais:**

1. Carregamento dos Dados: Os conjuntos de dados de avaliações de filmes são carregados no Spark. Esses conjuntos de dados geralmente incluem informações como ID do usuário, ID do filme, avaliação e timestamp.

2. Pré-processamento dos Dados (se necessário): Se os dados exigirem algum pré-processamento, como tratamento de valores ausentes ou transformação de formatos, essas etapas são realizadas para garantir a qualidade dos dados.

3. Divisão dos Dados em Conjuntos de Treinamento e Teste: Os dados são divididos aleatoriamente em conjuntos de treinamento e teste, permitindo a avaliação do desempenho do modelo.

4. Treinamento do Modelo de Recomendação: O algoritmo ALS é usado para treinar o modelo de recomendação com base nos dados de treinamento. Parâmetros como `maxIter` (número máximo de iterações) e `regParam` (parâmetro de regularização) são ajustados para otimizar o desempenho do modelo.

5. Avaliação do Modelo: O desempenho do modelo é avaliado usando métricas como Erro Quadrático Médio (RMSE). Isso fornece insights sobre como o modelo faz previsões em relação aos dados de teste.

6. Geração de Recomendações Personalizadas: Com base no modelo treinado, são geradas recomendações personalizadas para usuários e filmes específicos. As recomendações são baseadas nas preferências do usuário e nos padrões de avaliação encontrados nos dados.

## Dados do MovieLens

Os dados utilizados no projeto estão localizados na pasta "datasets". A estrutura da pasta é a seguinte:

```
datasets
├── u.data
└── u.item
```

- `u.data`: Arquivo contendo as avaliações de filmes pelos usuários, no formato UserID, MovieID, Rating e Timestamp.
- `u.item`: Arquivo contendo informações sobre os filmes, como título, gênero, ano de lançamento, entre outros.

Certifique-se de ter os arquivos de dados `u.data` e `u.item` na pasta "datasets" antes de executar o notebook.
## Dependências

Para executar o código, certifique-se de ter as seguintes dependências instaladas:

- Apache Spark
- Python (compatível com o Spark)

## Execução

1. Clone o repositório para o seu ambiente local:

```
git clone https://github.com/Andessonreis/Recommender-System-with-Apache-Spark-MLlib.git
```

2. Acesse o diretório do projeto:

```
cd Recommender-System-with-Apache-Spark-MLlib
```

3. Execute o arquivo `recommender_system.ipynb` no Jupyter Notebook ou no ambiente de sua escolha que suporte a execução de notebooks do Python.

4. Verifique a saída no notebook para obter as recomendações personalizadas para usuários e filmes específicos.

## Resultados

Aqui estão exemplos dos resultados obtidos:

### Recomendações Personalizadas para Usuários

```
+------+-------------------------------------------------------------------------------------------+
|userId|recommendations                                                                            |
+------+-------------------------------------------------------------------------------------------+
|1     |[{1449, 4.9930544}, {1405, 4.9770713}, {694, 4.9524665}, {169, 4.9166417}, {516, 4.891236}]|
+------+-------------------------------------------------------------------------------------------+
```

*Esses resultados representam as principais recomendações para o usuário com ID 1. Cada recomendação consiste em um par de valores, onde o primeiro valor é o ID do filme recomendado e o segundo valor é a pontuação da recomendação.*

### Recomendações Personalizadas para Filmes

```
+-------+-------------------------------------------------------------------------------------+
|movieId|recommendations                                                                      |
+-------+-------------------------------------------------------------------------------------+
|100    |[{173, 5.188312}, {4, 5.1520143}, {928, 5.1019526}, {808, 5.093348}, {118, 5.091296}]|
+-------+-------------------------------------------------------------------------------------+
```

*Esses resultados representam as principais recomendações para o filme com ID 100. Cada recomendação consiste em um par de valores, onde o primeiro valor é o ID do filme recomendado e o segundo valor é a pontuação da recomendação.*

## Fonte dos Dados

O conjunto de dados de avaliações de filmes utilizado neste projeto foi obtido no site do GroupLens Research (https://grouplens.org/datasets/movielens/). Especificamente, foi utilizado o conjunto de dados "MovieLens 100K Dataset", que contém dados de referência estáveis com 100.000 avaliações de 1.000 usuários em 1.700 filmes.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para obter mais informações.

## Contato
- Email: andessonreis@gmail.com
Sinta-se à vontade para entrar em contato caso tenha alguma dúvida ou precise de mais informações sobre o projeto.
