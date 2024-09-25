<h2>Sistema de Recomendação de Filmes</h2>
Este projeto implementa um sistema de recomendação utilizando um algoritmo de fatoração de matriz (ALS - Alternating Least Squares), baseado em um conjunto de dados de filmes e avaliações de usuários (ratings). O objetivo é recomendar filmes para os usuários com base em suas preferências anteriores, utilizando técnicas de filtragem colaborativa.

<h2>Conjuntos de Dados Utilizados</h2>
Filmes: Contém informações sobre os filmes, incluindo identificadores (IDs), títulos e gêneros.

Avaliações (Ratings): Inclui as avaliações dos usuários, contendo identificadores de usuário, identificadores de filmes e notas (ratings) atribuídas aos filmes.

<h2>Formato dos Dados:</h2>

<h4>Movies Dataset:</h4>

*movieId:* Identificador único do filme.

title: Título do filme.

genres: Gênero(s) do filme.

<h4>Ratings Dataset:</h4>

userId: Identificador único do usuário.

movieId: Identificador do filme avaliado.

rating: Avaliação do filme (de 0.5 a 5.0).

timestamp: Momento da avaliação.

<h2>Objetivo do Projeto:</h2>

O objetivo principal é construir um modelo que possa prever as avaliações que um usuário daria a filmes que ele ainda não avaliou. Para isso, é utilizado o algoritmo de ALS (Alternating 
Least Squares), amplamente adotado em sistemas de recomendação baseados em filtragem colaborativa.

<h2>Etapas do Projeto</h2>

<h4>Pré-processamento dos dados:</h4>

Conversão dos tipos de dados das colunas (e.g., userId, movieId, rating).

Remoção da coluna timestamp, que não é relevante para o modelo.

Tratamento de valores nulos.

<h2>Exploração dos dados:</h2>

Análise exploratória para entender a distribuição das notas e características dos filmes.

Cálculo de métricas como a esparsidade do conjunto de dados (percentual de valores que estão ausentes).

<h2>Divisão dos dados:</h2>

Separação dos dados em conjunto de treino e teste (e.g., 80% para treino e 20% para teste).

<h2>Treinamento do modelo de ALS:</h2>

<h4>Utilização da biblioteca PySpark para treinar o modelo de ALS com os seguintes parâmetros:</h4>

userCol: Coluna de identificador do usuário.

itemCol: Coluna de identificador do filme.

ratingCol: Coluna de avaliações dos usuários.

nonnegative: Definido como True, garantindo que os valores preditos sejam positivos.

coldStartStrategy: Estratégia definida como "drop" para remover predições sem correspondência nos dados de treino.

<h2>Validação Cruzada:</h2>

Aplicação de validação cruzada (K-fold) para ajustar os hiperparâmetros, incluindo:

rank: Número de fatores latentes.

regParam: Parâmetro de regularização.

Avaliação com métricas como Root Mean Squared Error (RMSE).

<h2>Avaliação do modelo:</h2>

Cálculo do RMSE no conjunto de teste para verificar a precisão do modelo.

Comparação de diferentes configurações de hiperparâmetros para identificar o melhor modelo.

<h2>Geração de Recomendações:</h2>

Utilização do modelo treinado para gerar recomendações de filmes para usuários com base em suas interações passadas.

<h2>Tecnologias Utilizadas:</h2>

PySpark: Usado para processamento distribuído e implementação do modelo de recomendação (ALS).

Jupyter Notebooks: Para organização do código e análise dos dados.

Python: Linguagem de programação principal do projeto.

Pandas: Para o pré-processamento de dados.

Um modelo de recomendação capaz de prever com alta precisão as notas que um usuário atribuiria a filmes que ele ainda não assistiu.

Avaliação da performance do modelo com métricas adequadas (como RMSE).

Geração de uma lista personalizada de recomendações de filmes para cada usuário.



<h2>Conclusão:</h2>
Este projeto demonstra a implementação de um sistema de recomendação utilizando um algoritmo eficiente e escalável, além de explorar conceitos fundamentais de aprendizado de máquina e análise de dados para solucionar um problema real.


<h4>Contribuições e feedback são bem-vindos!</h4>
