English description below

Polynomial Regression

Criei este projeto para implementar uma regressão polinomial de formal manual usando Python e bibliotecas como NumPy, Matplotlib e Scikit-learn. 
Estava curioso para observar o desempenho do modelo manual.

Passos Tomados

Geração dos Dados: 

Primeiramente, gerei dados sintéticos usando uma fórmula polinomial de grau 5 para criar os valores de  Y em função de 
X, com adição de ruído aleatório. 
O conjunto de dados foi composto por 10.000 pontos, e os valores de X foram gerados aleatoriamente na faixa de 2 a 5.

Visualização Inicial: 

Visualizei os dados gerados em gráfico de dispersão para observar a distribuição dos pontos e a relação entre 
X e Y.

Transformação Polinomial e Normalização: 

Para aplicar a regressão polinomial, transformei os dados de entrada 
X em suas respectivas características polinomiais de grau 5 utilizando PolynomialFeatures do Scikit-learn. 
Também normalizei os dados usando StandardScaler para padronizar a escala das variáveis.

Treinamento do Modelo de Regressão Linear: 

A regressão linear foi aplicada ao conjunto de dados transformado e normalizado. 
O modelo foi treinado e avaliei os coeficientes do modelo, o intercepto, e o desempenho do ajuste utilizando o coeficiente de determinação 
𝑅².

Curvas de Aprendizado: 

Para analisar o comportamento do modelo em diferentes tamanhos de conjunto de treinamento, 
gerei curvas de aprendizado usando learning_curve() que mostraram os erros de treinamento e validação em função do tamanho do conjunto de dados. 
Utilizei o erro quadrático médio (RMSE) como métrica de avaliação.

Pipeline de Regressão Polinomial: 

Para otimizar o processo de transformação e treinamento, utilizei um pipeline que combina as transformações polinomiais, 
a normalização e a regressão linear em uma única etapa. As curvas de aprendizado foram novamente geradas para avaliar o desempenho do pipeline.

Implementação Manual da Transformação Polinomial: 

Para fins educativos, implementei uma versão manual das transformações polinomiais e da normalização dos dados, 
sem utilizar as funções prontas do Scikit-learn. Utilizando álgebra linear, 
calculei a solução dos coeficientes do modelo utilizando o método dos mínimos quadrados.

Avaliação do Modelo: 

Por fim, apliquei o modelo treinado a um novo conjunto de dados gerado de forma semelhante ao primeiro, 
para calcular o erro quadrático médio (MSE) entre as previsões e os valores reais, avaliando o desempenho do modelo em dados não vistos.

Tecnologias Utilizadas

Python

NumPy

Matplotlib

Scikit-learn



Regularization Ridge

Criei este projeto para explorar a regularização em modelos de regressão, especificamente utilizando Ridge Regression. 
Utilizei a abordagem polinomial para gerar dados, foram aplicadas técnicas de regularização, como o Ridge Regression e o método de stochastic gradient de forma manual.

Passos Tomados

Geração dos Dados: 

Similar ao projeto anterior, foram gerados dados sintéticos utilizando uma função polinomial de grau 5, com adição de ruído aleatório. 

O conjunto de dados foi composto por 10.000 pontos.

Visualização Inicial: Os dados gerados foram visualizados em um gráfico de dispersão para observar a distribuição dos pontos e a relação entre as variáveis 
X e Y.

Transformação Polinomial e Normalização: 

A transformação polinomial de grau 6 foi aplicada aos dados, expandindo as características de X para incluir potências maiores. 
Em seguida, os dados foram normalizados utilizando a média e o desvio padrão das características, para garantir que todas as variáveis estivessem na mesma escala.

Regularização Ridge Manual: 

Para entender melhor o impacto da regularização, implementei a regularização Ridge manualmente, adicionando o termo de regularização 
λ à fórmula dos mínimos quadrados, que ajuda a prevenir overfitting.

Gradiente Descendente com Regularização: 

A seguir, implementei o gradiente descendente com regularização L2 (Ridge) utilizando uma taxa de aprendizado (eta) fixa e o número de iterações ajustado. 
O modelo foi treinado por 10.000 épocas para minimizar o erro quadrático médio.

Gradiente Descendente Estocástico (Mini-Batch): 

Para melhorar a eficiência, apliquei o Stochastic gradient descent (SGD) com mini-batches. 
Implementei este método para atualizar os parâmetros em pequenos lotes de dados, o que pode acelerar o processo de treinamento.

Uso de Ridge Regression: 

O modelo de Ridge Regression foi implementado utilizando o Ridge do Scikit-learn. O parâmetro de regularização 
𝛼 foi ajustado para encontrar o melhor valor, utilizando o método de validação cruzada RidgeCV.

Avaliação do Modelo: 

O modelo foi avaliado com dados de teste, calculando o erro quadrático médio (MSE) entre as previsões do modelo e os valores reais. 
O desempenho do modelo foi comparado entre os métodos manuais e os métodos do Scikit-learn.

RidgeCV: 

Finalmente, apliquei o RidgeCV, que realiza a busca pelo melhor valor de 
α utilizando validação cruzada. O modelo foi treinado, e o melhor valor de 
α foi encontrado.

Tecnologias Utilizadas

Python

NumPy

Matplotlib

Scikit-learn




Lasso & ElasticNet Regularization


Criei este projeto para explorar a regularização Lasso e ElasticNet em modelos de regressão polinomial. 

Utilizei uma abordagem similar à dos projetos anteriores, 
abordei a regularização tanto no formato L1 (Lasso) quanto na combinação L1-L2 (ElasticNet).

Passos Tomados

Geração dos Dados: 

Assim como nos exemplos anteriores, gerei um conjunto de dados sintéticos com 10.000 pontos, onde a variável 
Y é definida por um polinômio de grau 5 com ruído adicionado.

Visualização Inicial: 

Os dados gerados foram visualizados em um gráfico de dispersão para examinar a relação entre 
X e Y.

Transformação Polinomial e Normalização: 

Os dados foram transformados para um espaço polinomial de grau 6 e, em seguida, normalizados utilizando a média e o desvio padrão.

Regularização Lasso e ElasticNet Manual: 

Implementei a regularização Lasso (L1) e ElasticNet (L1-L2) manualmente no gradiente descendente, utilizei o termo de regularização apropriado para cada caso. 

Early Stopping: 

Para fins educativos, implementei a técnica de early stopping de forma manual, 
onde o treinamento é interrompido se não houver melhorias significativas no MSE após um certo número de épocas.

Uso de Lasso e ElasticNet do Scikit-learn: 

Para comparação, utilizei as implementações de Lasso e ElasticNet do sklearn e avaliei seu desempenho em termos de erro quadrático médio.


Tecnologias Utilizadas

Python

NumPy

Matplotlib

Scikit-learn





Polynomial Regression

I created this project to implement polynomial regression manually using Python and libraries such as NumPy, Matplotlib, and Scikit-learn. 
I was curious to observe the model's performance through a manual implementation.

Steps Taken

Data Generation: 

First, I generated synthetic data using a degree 5 polynomial formula to create the values of Y as a function of X, with the addition of random noise. The dataset consisted of 10,000 points, and the values of X were randomly generated in the range of 2 to 5.

Initial Visualization: 

I visualized the generated data in a scatter plot to observe the distribution of points and the relationship between X and Y.

Polynomial Transformation and Normalization: 

To apply polynomial regression, I transformed the input data X into its respective degree 5 polynomial features using PolynomialFeatures from Scikit-learn. I also normalized the data using StandardScaler to standardize the variable scales.

Training the Linear Regression Model: 

Linear regression was applied to the transformed and normalized dataset. The model was trained, and I evaluated the model's coefficients, intercept, and the performance of the fit using the coefficient of determination 𝑅².

Learning Curves: 

To analyze the model's behavior with different training set sizes, I generated learning curves using learning_curve() to show training and validation errors as a function of dataset size. I used the root mean squared error (RMSE) as the evaluation metric.

Polynomial Regression Pipeline: 

To optimize the transformation and training process, I used a pipeline combining polynomial transformations, normalization, and linear regression into a single step. Learning curves were generated again to evaluate the pipeline's performance.

Manual Polynomial Transformation Implementation: 

For educational purposes, I implemented a manual version of the polynomial transformations and data normalization without using Scikit-learn's built-in functions. Using linear algebra, I computed the solution for the model's coefficients using the least squares method.

Model Evaluation:

Finally, I applied the trained model to a new dataset generated similarly to the first, to calculate the mean squared error (MSE) between the predictions and actual values, evaluating the model's performance on unseen data.

Technologies Used:

Python

NumPy

Matplotlib

Scikit-learn

Ridge Regularization

I created this project to explore regularization in regression models, specifically using Ridge Regression. I used a polynomial approach to generate data and applied regularization techniques, such as Ridge Regression and manual stochastic gradient methods.

Steps Taken

Data Generation: 

Similar to the previous project, synthetic data was generated using a degree 5 polynomial function with random noise added. The dataset consisted of 10,000 points.

Initial Visualization: 

The generated data was visualized in a scatter plot to observe the distribution of points and the relationship between X and Y.

Polynomial Transformation and Normalization: 

A degree 6 polynomial transformation was applied to the data, expanding the features of X to include higher powers. Then, the data was normalized using the mean and standard deviation of the features to ensure all variables were on the same scale.

Manual Ridge Regularization: 

To better understand the impact of regularization, I manually implemented Ridge regularization by adding the regularization term 
λ to the least squares formula, which helps prevent overfitting.

Gradient Descent with Regularization: 

Next, I implemented gradient descent with L2 regularization (Ridge) using a fixed learning rate (η) and an adjusted number of iterations. The model was trained for 10,000 epochs to minimize the mean squared error.

Stochastic Gradient Descent (Mini-Batch): 

To improve efficiency, I applied Stochastic Gradient Descent (SGD) with mini-batches. This method updates the parameters in small batches of data, which can speed up the training process.

Ridge Regression Use: 

The Ridge Regression model was implemented using the Ridge class from Scikit-learn. The regularization parameter α was adjusted to find the best value using the RidgeCV cross-validation method.

Model Evaluation: 

The model was evaluated with test data by calculating the mean squared error (MSE) between the model's predictions and the actual values. The model's performance was compared between the manual methods and Scikit-learn's methods.

RidgeCV:

Finally, I applied RidgeCV, which performs a search for the best α value using cross-validation. The model was trained, and the optimal 
α value was found.

Technologies Used:

Python

NumPy

Matplotlib

Scikit-learn

Lasso & ElasticNet Regularization

I created this project to explore Lasso and ElasticNet regularization in polynomial regression models. I used a similar approach to the previous projects, addressing regularization in both L1 (Lasso) and the combination of L1-L2 (ElasticNet).

Steps Taken

Data Generation: 

As in the previous examples, I generated a synthetic dataset with 10,000 points, where the variable Y is defined by a degree 5 polynomial with added noise.

Initial Visualization: 

The generated data was visualized in a scatter plot to examine the relationship between X and Y.

Polynomial Transformation and Normalization: 

The data was transformed into a degree 6 polynomial space and then normalized using the mean and standard deviation.

Manual Lasso and ElasticNet Regularization: 

I manually implemented Lasso (L1) and ElasticNet (L1-L2) regularization in gradient descent, using the appropriate regularization term for each case.

Early Stopping: 

For educational purposes, I implemented early stopping manually, where training is interrupted if no significant improvement in MSE is observed after a set number of epochs.

Using Lasso and ElasticNet from Scikit-learn: 

For comparison, I used the Scikit-learn implementations of Lasso and ElasticNet and evaluated their performance in terms of mean squared error.

Technologies Used:

Python

NumPy

Matplotlib

Scikit-learn
