![ensaio-machine-learning](https://github.com/EdinanMarinho/ensaio-machine-learning/assets/61295729/e746848a-419d-4980-b4c0-b39a19b4e96d)

# Ensaio de Machine Learning

Estudo de Machine Learning investigando algoritmos de Classificação, Regularização e Clusterização, com o propósito de compreender como diferentes hiperparâmetros e a distribuição dos conjuntos de treinamento, validação e teste afetam o desempenho dos modelos de machine learning, podendo resultar em overfitting ou underfitting.

Para esse estudo foram utilizados conjunto de dados préviamente preparados e separados, prontos para aplicação nos algoritmos.

## Descrição
A empresa Data Money acredita que a expertise no treinamento e ajuste fino dos algoritmos, feito pelos Cientistas de Dados da empresa, é a principal motivo dos ótimos resultados que as consultorias vem  entregando aos seus clientes.

## Objetivo
O propósito deste projeto é conduzir ensaios com algoritmos de Classificação, Regressão e Clusterização, para estudar a mudança do comportamento da performance, a medida que os valores dos principais  parâmetros de controle de overfitting e underfitting mudam.

# Planejamento da solução
## Produto final
O produto final será 7 tabelas mostrando a performance dos algoritmos, avaliados usando múltiplas métricas, para 3 conjuntos de dados diferentes: Treinamento, validação e teste.

## Algoritmos ensaiados
### Classificação:
Algoritmos: KNN, Decision Tree, Random Forest e Logistic Regression 
Métricas de performance: Accuracy, Precision, Recall e F1-Score

### Regressão:
Algoritmos: Linear Regression, Decision Tree Regressor, Random Forest Regressor, Polinomial Regression, Linear Regression Lasso, Linear Regression Ridge, Linear Regression Elastic Net, Polinomial Regression Lasso, Polinomial Regression Ridge e Polinomial Regression Elastic Net 
Métricas de performance: R2, MSE, RMSE, MAE e MAPE

### Agrupamento:
Algoritmos: K-Means e Affinity Propagation

Métricas de performance: Silhouette Score
## Ferramentas utilizadas
Python 3.8 e Scikit-learn

# Desenvolvimento
## Estratégia da solução
 
Com o propósito de ensaiar os algoritmos de Machine Learning, utilizarei a linguagem Python para escrever os códigos e treinar cada um dos algoritmos. Vou variar seus principais parâmetros de ajuste de overfitting e observar a métrica final.
O conjunto de valores que fizerem os algoritmos alcançarem a melhor performance, serão aqueles escolhidos para o treinamento final do algoritmo.

## O passo a passo
Passo 1: Divisão dos dados em treino, teste e validação.
Passo 2: Treinamento dos algoritmos com os dados de treinamento, utilizando os parâmetros “default”.
Passo 3: Medir a performance dos algoritmos treinados com o parâmetro default, utilizando o conjunto de dados de treinamento.
Passo 4: Medir a performance dos algoritmos treinados com o parâmetro “default”, utilizando o conjunto de dados de validação.
Passo 5: Alternar os valores dos principais parâmetros que controlam o overfitting do algoritmo até encontrar o conjunto de parâmetros apresente a melhor performance dos algoritmos.
Passo 6: Unir os dados de treinamento e validação.
Passo 7: Retreinar o algoritmo com a união dos dados de treinamento e validação, utilizando os melhores valores para os parâmetros de controle do algoritmo.
Passo 8: Medir a performance dos algoritmos treinados com os melhores parâmetro, utilizando o conjunto de dados de teste.
Passo 9: Avaliar os ensaios e anotar os 3 principais Insights que se destacaram. 

# Os top 3 Insights
### Insight Top 1
Os algoritmos baseados em árvores apresentam uma performance superior em todas as métricas ao serem aplicados aos dados de teste durante o ensaio de Classificação.

## Insight Top 2
A performance dos algoritmos de classificação nos dados de validação foi bastante semelhante à performance nos dados de teste.

## Insight Top 3
Todos os algoritmo de regressão não apresentaram boas métricas de  performance, o que mostra uma necessidade de uma seleção de atributos e uma preparação melhor das variáveis independentes do conjunto de  dados.

# Resultados
## Ensaio de classificação:
### Sobre os dados de treinamento
| Algoritmo | Accuracy | Precision | Recall | F1-Score |
| ----------|----------| ----------| ------ | -------- |
| KNN       |0.944 | 0.958 | 0.910 | 0.933 |
| Decision Tree | 1.0 | 1.0 | 1.0 | 1.0 | 
| Random Forest | 1.0 | 1.0 | 1.0 | 1.0 | 
| Logistic Regression | 0.875 | 0.871 | 0,836 | 0,836 |

 ### Sobre os dados de validação
 | Algoritmo | Accuracy | Precision | Recall | F1-Score |
 | ----------|----------| ----------| ------ | -------- |
 | KNN       |0.920 | 0.934 | 0.878 | 0.905 |
 | Decision Tree | 0.930 | 0.914 | 0.924 | 0.919 | 
 | Random Forest | 0.965 | 0.973 | 0.944 | 0.959 | 
 | Logistic Regression | 0.874 | 0.869 | 0,835 | 0,852 |

 ### Sobre os dados de teste
 | Algoritmo | Accuracy | Precision | Recall | F1-Score |
 | ----------|----------| ----------| ------ | -------- |
 | KNN       |0.922 | 0.939 | 0.879 | 0.891 |
 | Decision Tree | 0.935 | 0.926 | 0.925 | 0.926 | 
 | Random Forest | 0.965 | 0.974 | 0.946 | 0.960 | 
 | Logistic Regression | 0.871 | 0.869 | 0,833 | 0,851 |

## Ensaio de regressão:
### Sobre os dados de treinamento

 | Algoritmo | R2       | MSE       | RMSE   | MAE      | MAPE |
 | ----------|----------| ----------| ------ | -------- | ---- |
 | Decision Tree Regressor   | 0.992 | 3.940 | 1.985 | 0.214 | 0.083 |
 | Random Forest Regressor | 0.9902 | 46.676 | 6.832 | 4.879 | 2.625 |
 | Linear Regression | 0.046 | 455.996 | 21.354 | 16.998 | 8.653 |
 | Linear Regression Lasso | 0.007 | 474.470 | 21,782 | 17.305 | 8.737 |
 | Linear Regression Ridge | 0.046 | 456.000 | 21.354 | 16.998 | 8.653 |
 | Linear Regression Elastic Net | 0.008 | 474.270 | 21.778 | 17.300 | 8.732 |
 | Polinomial Regression | 0.094 | 432.986 | 20.808 | 16.458 | 8.351 |
 | Polinomial Regression Lasso | 0.009 | 473.639 | 21.736 | 17.285 | 8.700 |
 | Polinomial Regression Ridge | 0.093 | 433.475 | 20.820 | 16.472 | 8.373 |
 | Polinomial Regression Elastic Net | 0.013 | 471.878 | 21.722 | 17.244 | 8.869 |
 
 ### Sobre os dados de validação
 | Algoritmo | R2       | MSE       | RMSE   | MAE      | MAPE |
 | ----------|----------| ----------| ------ | -------- | ---- |
 | Decision Tree Regressor   | 0.296 | 618.800 | 24.876 | 17.115 | 6.889 |
 | Random Forest Regressor | 0.330 | 320.010 | 17.039 | 13.039 | 7.058 |
 | Linear Regression | 0.040 | 458.447 | 21.411 | 17.040 | 8.683 |
 | Linear Regression Lasso | 0.008 | 473.750 | 21.766 | 17.265 | 8.696 |
 | Linear Regression Ridge | 0.040 | 458.450 | 21.411 | 17.039 | 8.682 |
 | Linear Regression Elastic Net | 0.066 | 445.768 | 21.113 | 16.750 | 8.548 |
 | Polinomial Regression | 0.066 | 445.768 | 21.113 | 16.750 | 8.548 |
 | Polinomial Regression Lasso | 0.010 | 472.913 | 21.747 | 17.238 | 8.682 |
 | Polinomial Regression Ridge | 0.068 | 445.184 | 21.099 | 16.739 | 8.569 |
 | Polinomial Regression Elastic Net | 0.013 | 471.408 | 21.712 | 17.200 | 8.675 |
 
 ### Sobre os dados de teste
 | Algoritmo | R2       | MSE       | RMSE   | MAE      | MAPE |
 | ----------|----------| ----------| ------ | -------- | ---- |
 | Decision Tree Regressor   | 0.090 | 442.848 | 21.044 | 16.830 | 7.883 |
 | Random Forest Regressor | 0.408 | 288.210 | 16.977 | 12.165 | 6.250 |
 | Linear Regression | 0.051 | 461.988 | 21.494 | 17.144 | 8.531 |
 | Linear Regression Lasso | 0.051 | 461.990 | 21.494 | 17.144 | 8.531 |
 | Linear Regression Ridge | 0.051 | 462.000 | 21.494 | 17.143 | 8.537 |
 | Linear Regression Elastic Net | 0.051 | 461.493 | 21.493 | 17.144 | 8.531 |
 | Polinomial Regression | 0.091 | 442.641 | 21.039 | 16.736 | 8.277 |
 | Polinomial Regression Lasso | 0.056 | 459.530 | 21.436 | 17.017 | 8.576 |
 | Polinomial Regression Ridge | 0.090 | 443.041 | 21.048 | 16.744 | 8.312 |
 | Polinomial Regression Elastic Net | 0.077 | 449.600 | 21.204 | 16.844 | 8.441 |
 
 ## Ensaio de clusterização:
| Algoritmo  | Número de Clusters | Average Silhouette Score | 
| ---------- | ----------         | ----------               | 
| K-Means    | 3 | 0,215  | 
| Affinity Propagation | 3   | 0,233             | 
 
 # Conclusão
Nesse ensaio de Machine Learning, consegui adquirir experiência e  entender melhor sobre os limites dos algoritmos entre os estados de  underffiting e overfitting. Algoritmos baseados em árvores são sensível quanto a profundidade do  crescimento e do número de árvores na floresta, fazendo com que a  escolha correta dos valores desses parâmetros impeçam os algoritmos de  entrar no estado de overfitting.

Os algoritmos de regressão, por outro lado, são sensíveis ao grau do  polinômio. Esse parâmetro controla o limite entre o estado de underfitting  e overfitting desses algoritmos.
Esse ensaio de Machine Learning foi muito importante para aprofundar o  entendimento sobre o funcionamento de diversos algoritmos de  classificação, regressão e clusterização e quais os principais parâmetros  de controle entre os estados de underfitting e overfitting.

# Próximos passos
Como próximos passos desse ensaio, pretendo ensaiar novos algoritmos  de Machine Learning e usar diferentes conjuntos de dados para aumentar  o conhecimento sobre os algoritmos e quais cenários são mais favoráveis  para o aumento da performance dos mesmos.

Também aplicar as habilidades que adquiri nesse ensaio em outros projetos, buscando resolver algum problema de negócio.
