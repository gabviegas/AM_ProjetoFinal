<p align="center">
  
![Logo](imagens/park.png)

</p>

# EcoAlt: Modelagem de Altitude de Fungos Nativos

A proposta do projeto é elaborar um modelo preditivo com dados sobre espécies de fungos nativos do Brasil para determinar a ordem predominante de fungos em uma determinada região. Esse tipo de análise ]pode ser útil para fins comerciais, dado que fungos apresentam uma gama de aplicações medicinais, culinárias, entre outras. Além disso, pode auxiliar em estudos de biogeografia, fornecendo insights sobre como as condições do ambiente culmina na ocorrência e predominância dessas espécies.

## Começando

O projeto visa aplicar técnicas de aprendizado de máquina para prever a ordem de uma espécie de fungo nativa do Brasil com base em sua localização. Baseando-se em características como municipality, família, longitude mínima e latitude mínima observadas, o modelo busca identificar padrões ecológicos e geográficos que influenciam a distribuição das ordens desses fungos.
Essas instruções permitirão que você obtenha uma cópia do projeto em operação na sua máquina local para fins de desenvolvimento e teste.
Consulte **[Implantação](#-implanta%C3%A7%C3%A3o)** para saber como implantar o projeto. 

## 🔨 Etapas do projeto

- [ ] Acesso e tratamento de dados.
- [ ] Seleção de atributos.
- [ ] Elaborar um modelo de base para analisar as relações entre as variáveis analisadas.
- [ ] Desenvolver uma matriz de confusão. |verificar a aplicabilidade|
- [ ] Realizar splitting dos dados e testes.
- [ ] Implementar floresta aleatória.
- [ ] Teste com K-NN vizinhos.
- [ ] Teste com Naive Bayes/Support Vector Machine.
      
##  Implantação

Para a implantação desse projeto foi utilizada a interface do Jupyter Notebook para elaborar o código fonte, em conjunto com as ferramentas pandas, matplolib, numpy e sklearn para carregamento, tratamento e exibição dos dados utilizados no projeto. 

## 🛠️ Construído com

As seguintes ferramentas foram utilizadas para a elaboração do projeto:

### K-NN Vizinhos: 
O funcionamento de um modelo preditivo induzido por este algoritmo é simples: ao receber um certo exemplo x, o algoritmo checa a distância deste exemplo  com relação aos exemplos que ele ja conhece(vizinhos). O valor predito pelo modelo será a média dos alvos dos k vizinhos mais próximos do exemplo de entrada( k vizinhos com menor distância).[1].

### Floresta aleatória: 
Combina funções de predição aproximadamente não viesadas fazendo uma classificação, treinado com covariáveis dadas pelas predições dos modelos a serem combinados. É formada por diversas árvores de decisão onde o processo de construir cada das árvores de decisão desta floresta envolve amostragem dos exemplos e de atributos.[2].

### Optuna:
É um módulo para resolver problemas envolvendo otimização com parâmetros numéricos e categóricos que proprociona buscas mais estratégico do que a busca aleatória e mais eficiente de que a busca em grade. Pontanto, é uma estrutura de software de otimização automática de hiperparâmetros de um modelo de aprendizado de máquina que também se integra ao  acompanhamento e monitoramento de modelo e avaliação.

### Métricas de classificação:
Este módulo oferece várias funções  para medir o desempenho de modelos de classificação, incluindo funções de perda e pontuações. Algumas métricas podem exigir estimativas de probabilidade da classe positiva, valores de confiança ou valores de decisões binárias. A maioria das implementações permite que cada amostra forneça uma contribuição ponderada à pontuação geral, por meio do parâmetro.

### Recall:
É uma métrica usada para medir a proporção de positivos verdadeiros que são corretamente idendtificados. Sendo intuitivamenete a capacidade do classificador de encontrar todas as amostras positivas, é muito útil em situações em que a deteção de casos positivos é crucial e a ocorrência de falsos negativos é indejada.

### Naive Bayes:
Os classificadores Naive Bayes são um conjunto de algoritmos probabilísticos que realizam predições com base no Teorema de Bayes. São chamados "naive" (ingênuo) porque assumem uma relação de independência condicional entre as features que analisa.

$$
P(A | B) = \frac{P(A) P(B | A)}{P(B)}.
$$

O Teorema de Bayes descreve a probabilidade de ocorrência de um evento A ocorrer sabendo que um evento B ocorreu. É uma ferramenta extremamente poderosa, que proporciona a possibilidade de atualizar uma probabilidade inicial matematicamente, tendo aplicações extremamante difundidas em diversas áreas, como aprendizado de máquina, saúde, ou mesmo a vida cotidiana. Para a equação acima, temos os termos:

* $P(A|B):$ probabilidade de A sabendo que B ocorreu.
* $P(B|A):$ probabilidade de B sabendo que A ocorreu.
* $P(A):$ probabilidade inicial de A, o que se sabia de A antes de B ocorrer.
* $P(B):$ é a probabilidade total de B.

#### Aplicação ao contexto

Foi mencionado que Naive Bayes é um conjunto de algoritmos porbabilísticos.

### Baseline: Também conhecido como: dummy, linha de base ou modelo fictício. No contexto de ciência de dados e aprendizado de máquina, a linha de base pode ser vista como uma solução de referência que define um ponto de partida. Ele foi projetado para ser simples e de fácil implementação, como um modelo que sempre prevê a média (para problemas de regressão) ou a classe mais frequente (para problemas de classificação). 

## Referências
CASSAR, Daniel. "ATP-203 2.1- Aprendizado de máquina, k-NN e métricas.ipynb" [Material de sala de aula]. Aprendizado de Máquina, 07 de agosto de 2024, Ilum - Escola de Ciência.

IZBICKI, Rafael; DOS SANTOS, Tiago Mendonça. Aprendizado de máquina: uma abordagem estatística. 2020. Disponível em: http://www.rizbicki.ufscar.br/ame/.
