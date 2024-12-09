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
