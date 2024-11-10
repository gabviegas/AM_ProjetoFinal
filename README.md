<p align="center">

# FunG: Modelagem de distribuição de famílias de Fungos

A proposta do projeto é elaborar um modelo preditivo com dados sobre espécies de fungos nativos do Brasil para determinar a família predominante de fungos em uma determinada região. Esse tipo de análise ]pode ser útil para fins comerciais, dado que fungos apresentam uma gama de aplicações medicinais, culinárias, entre outras. Além disso, pode auxiliar em estudos de biogeografia, fornecendo insights sobre como as condições do ambiente culmina na ocorrência e predominância dessas espécies. 

## Começando

O projeto visa aplicar técnicas de aprendizado de máquina para prever a ordem de uma espécie de fungo nativa do Brasil com base em sua localização. Baseando-se em características como municipality, família, longitude mínima e latitude mínima observadas, o modelo busca identificar padrões ecológicos e geográficos que influenciam a distribuição das ordens desses fungos. 


## 🔨 Etapas do projeto

- [ ] Acesso e tratamento de dados.
- [ ] Realizar splitting dos dados e testes.
- [ ] Otimização com Optuna.
- [ ] Modelo Baseline Classificador.
- [ ] Matriz de confusão.
- [ ] Implementar K-NN vizinhos.
- [ ] Implementar floresta aleatória.
- [ ] Teste com Naive Bayes.
- [ ] Comentar resultados.
      
##  Implantação

Para a implantação desse projeto foi utilizada a interface do Jupyter Notebook para elaborar o código fonte, em conjunto com as ferramentas pandas, matplolib, numpy, seaborn, sklearn para carregamento, tratamento e exibição dos dados utilizados no projeto. 

## 🛠️ Construído com

As seguintes ferramentas foram utilizadas para a elaboração do projeto:

### Optuna:
É um módulo para resolver problemas envolvendo otimização com parâmetros numéricos e categóricos que proprociona buscas mais estratégico do que a busca aleatória e mais eficiente de que a busca em grade. Pontanto, é uma estrutura de software de otimização automática de hiperparâmetros de um modelo de aprendizado de máquina que também se integra ao  acompanhamento e monitoramento de modelo e avaliação.

### Baseline:
Também conhecido como Dummy, linha de base ou modelo fictício. No contexto de ciência de dados e aprendizado de máquina, o baseline pode ser visto como uma solução de referência que define um ponto de partida. Ele foi projetado para ser simples e de fácil implementação, como um modelo que sempre prevê a média (para problemas de regressão) ou a classe mais frequente (para problemas de classificação). 

### K-NN Vizinhos: 
O funcionamento de um modelo preditivo induzido por este algoritmo é simples: ao receber um certo exemplo x, o algoritmo checa a distância deste exemplo  com relação aos exemplos que ele ja conhece(vizinhos). O valor predito pelo modelo será a média dos alvos dos k vizinhos mais próximos do exemplo de entrada( k vizinhos com menor distância).[1].

### Floresta aleatória: 
Combina funções de predição aproximadamente não viesadas fazendo uma classificação, treinado com covariáveis dadas pelas predições dos modelos a serem combinados. É formada por diversas árvores de decisão onde o processo de construir cada das árvores de decisão desta floresta envolve amostragem dos exemplos e de atributos.[2].

### Métricas de classificação:
Este módulo oferece várias funções  para medir o desempenho de modelos de classificação, incluindo funções de perda e pontuações. Algumas métricas podem exigir estimativas de probabilidade da classe positiva, valores de confiança ou valores de decisões binárias. A maioria das implementações permite que cada amostra forneça uma contribuição ponderada à pontuação geral, por meio do parâmetro.

* Recall:
É uma métrica usada para medir a proporção de positivos verdadeiros que são corretamente idendtificados. Sendo intuitivamenete a capacidade do classificador de encontrar todas as amostras positivas, é muito útil em situações em que a deteção de casos positivos é crucial e a ocorrência de falsos negativos é indejada.

### Naive Bayes (NB):
Os classificadores Naive Bayes são um conjunto de algoritmos probabilísticos que realizam predições com base no Teorema de Bayes. São chamados "naive" (ingênuo) porque assumem uma relação de independência condicional entre as features que analisa.

$$
P(C | X) = \frac{P(C) P(X | C)}{P(X)}
$$

O Teorema de Bayes descreve a probabilidade de ocorrência de um evento C ocorrer sabendo que um evento X ocorreu. É uma ferramenta extremamente poderosa, que proporciona a possibilidade de atualizar uma probabilidade inicial matematicamente, tendo aplicações extremamante difundidas em diversas áreas, como aprendizado de máquina, saúde, ou mesmo a vida cotidiana. Para a equação acima, temos os termos:

* $P(C|X):$ probabilidade de C sabendo que X ocorreu.
* $P(X|C):$ probabilidade de X sabendo que C ocorreu.
* $P(C):$ probabilidade inicial de C, o que se sabia de C antes de X ocorrer.
* $P(X):$ é a probabilidade total de X.

#### Aplicação ao contexto

Tomando ainda como referência a equação acima, considerando que $X = {X_1, X_2, X_3, ..., X_N}$, sendo X o conjunto das features que contribuem para os dados de treino e teste e que C representa uma classe que estamos tentando prever, o Teorema de Bayes é aplicado no NB de forma que a cada feature analisada em relação a uma classe tenha probabilidade de ocorrer independente de outra, o que resulta em:

$$
P(X|C) = P(X1|C) * P(X2|C)...P(X_N|C)
$$

Assim, a probabilidade que representa a relação da manisfetação das features dada um determinada classe pode ser representada pelo produto das probabilidades individuais de cada feature. o Teorema de Bayes aplicado ao contexto desse tipo de previsão fica:

$$
P(C | X) = \frac{P(X1|C) * P(X2|C)...P(X_N|C)}{P(X)}
$$

Assim, a probabilidade de uma classe C ocorrer se as features $X_1, X_2, ..., X_N$ se manifestarem pode ser calculada pelo teorema. É importante lembrar que essa probabilidade é a atualização de uma probailidade inicial P(C). Como temos 4 classes, esse processo é realizado para as 4. A classe que possuir a probabilidade mais alta será a indicada como correspondente ao conjunto de features utilizadas no cálculo.

Foi mencionado que Naive Bayes é um conjunto de algoritmos probabilísticos. Como opções de algoritmos para implementação dessa lógica, teríamos o `MultinomialNB`, altamente recomendado para a classificação de textos, `BernoulliNB`, recomendado para dados que apresentem distribuições Bernoulli multivariadas, `CategoricalNB` para dados distribuídos categoricamente e `GaussianNaiveBayes`, que assume que as variáveis analisadas estão seguindo uma distribuição Gaussiana. 
Os algoritmos que serão implementados nesse projeto serão os de Gaussian Naive Bayes e Complementar Naive Bayes (uma adaptação para conjunto de dados desbalanceados). 



## Referências
CASSAR, Daniel. "ATP-203 2.1- Aprendizado de máquina, k-NN e métricas.ipynb" [Material de sala de aula]. Aprendizado de Máquina, 07 de agosto de 2024, Ilum - Escola de Ciência.

IZBICKI, Rafael; DOS SANTOS, Tiago Mendonça. Aprendizado de máquina: uma abordagem estatística. 2020. Disponível em: http://www.rizbicki.ufscar.br/ame/.
