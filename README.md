# Desafio Indicium - Ciência de Dados
 
Esse é um repositório em que se encontra todo o desafio proposto pela Indicium para Ciência de Dados. É um desafio em que "Você foi alocado(a) em um time da Indicium que está trabalhando atualmente junto a um cliente no processo de criação de uma plataforma de aluguéis temporários na cidade de Nova York.". Com isso, temos um dataset com vários registros de anúncios de apartamentos e casas.

Assim, foi realizado uma Análise Exploratória dos Dados e também foi desenvolvido modelos para previsão do preço de aluguel baseado nas features do problema.

## Como instalar
O Python utilizado para desenvolvimento desse desafio foi a versão 3.11.6. Após baixar todo o repositório, abra o terminal e digite:
```
pip install -r requirements.txt
```
Com esse comando você instalará todas as dependências do projeto e estará pronto para abrir e utilizar todos os arquivos desse repositório, inclusive os notebooks.

A análise exploratória dos dados pode ser encontrada em [indicium_EDA.ipynb](https://github.com/davirpp/Desafio-Indicium/blob/main/indicium_EDA.ipynb) ou em formato pdf em [indicium_EDA.pdf](https://github.com/davirpp/Desafio-Indicium/blob/main/pdf_notebooks/indicium_EDA.pdf).

Após o desenvolvimento do modelo que pode ser visto em [indicium_prediction.ipynb](https://github.com/davirpp/Desafio-Indicium/blob/main/indicium_prediction.ipynb), percebi que os outliers que podem ser vistos na análise exploratória, estavam influenciando a performance do modelo, com isso, fiz o mesmo procedimento para criação de um modelo preditivo mas eliminando os outliers, porém os outliers neste contexto aparentam ser imóveis de luxo, então removê-los pode excluir uma parte importante dos dados, mas quis testar a performance do modelo diminuindo sua variância e os resultados foram satisfatórios. O notebook desenvolvido com o tratamento dos outliers está disponível em [indicium_prediction_no_outlier.ipynb](https://github.com/davirpp/Desafio-Indicium/blob/main/indicium_prediction_no_outlier.ipynb).

Os modelos de normalização dos dados e modelos de predição podem ser vistos na pasta [models-scalers](https://github.com/davirpp/Desafio-Indicium/tree/main/models-scalers). Para utilizá-los, baixe os modelos e vamos utilizar a biblioteca do Python chamada _joblib_. Para instalar basta colocar no terminal:
```
pip install joblib
```
Com a biblioteca instalada, a utilização é super simples:
```
model = joblib.load('path.pkl')
```
Assim, você já pode fazer suas predições (lembre-se de tratar os dados de input conforme demonstrado nos notebooks).

Explicações sobre os dados e respostas para algumas hipóteses, podem ser vistas diretamente nos notebooks.

Espero que goste!
