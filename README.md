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

* K-NN Vizinhos: O funcionamento de um modelo preditivo induzido por este algoritmo é simples: ao receber um certo exemplo x, o algoritmo checa a distância deste exemplo  com relação aos exemplos que ele ja conhece(vizinhos). O valor predito pelo modelo será a média dos alvos dos k vizinhos mais próximos do exemplo de entrada( k vizinhos com menor distância).[1].
* Floresta aleatória: Combina funções de predição aproximadamente não viesadas fazendo uma classificação, treinado com covariáveis dadas pelas predições dos modelos a serem combinados. É formada por diversas árvores de decisão onde o processo de construir cada das árvores de decisão desta floresta envolve amostragem dos exemplos e de atributos.[2].
* Métricas de classificação:
* Optuna: é um módulo para resolver problemas envolvendo otimização com parâmetros numéricos e categóricos que proprociona buscas mais estratégico do que a busca aleatória e mais eficiente de que a busca em grade. Pontanto, é uma estrutura de software de otimização automática de hiperparâmetros de um modelo de aprendizado de máquina que também se integra ao  acompanhamento e monitoramento de modelo e avaliação. 

## Referências
[1]. CASSAR, Daniel. "ATP-203 2.1- Aprendizado de máquina, k-NN e métricas.ipynb" [Material de sala de aula]. Aprendizado de Máquina, 07 de agosto de 2024, Ilum - Escola de Ciência.

[2].IZBICKI, Rafael; DOS SANTOS, Tiago Mendonça. Aprendizado de máquina: uma abordagem estatística. 2020. Disponível em: http://www.rizbicki.ufscar.br/ame/.
