# Trabalho Prático 1 - Machine Learning: Classificação de Exoplanetas
#### Aluna: Sarah Mariana Guedes de Almeida
##### 3º período - *Ciência de Dados e Inteligência Artificial* - Pontifícia Universidade Católica de Minas Gerais
----
 Este repositório apresenta os códigos referentes notebook do Trabalho Prático 1 (TP1), da disciplina Aprendizado de Máquina I, cujo objetivo é comparar diferentes métodos de classificação aplicados a um problema real de classificação binária.

 O problema consiste em classificar candidatos a exoplanetas identificados pela sonda espacial Kepler da NASA, utilizando os dados do arquivo *"koi_data.csv"*. A sonda detecta sinais de possíveis exoplanetas, chamados de Kepler Objects of Interest (KOI), mas nem todos os sinais correspondem a exoplanetas reais. Muitos, na verdade, são falsos positivos causados por fenômenos astronômicos diversos. 

 Dessa forma, a tarefa é aprender a distinguir os KOIs confirmados como exoplanetas daqueles classificados como falsos positivos, com base em características extraídas de cada observação.

 Para isso, serão treinados e avaliados **seis métodos de classificação**: Naive Bayes, Decision Tree, k-Nearest Neighbors, Support Vector Machines, Random Forest e Gradient Tree Boosting.

 Cada método será analisado individualmente, com variação de hiperparâmetros quando aplicável, seguida de uma comparação geral entre os modelos ao final.

 A avaliação dos modelos será realizada por meio de validação cruzada k-fold com k = 5, utilizando métricas além da acurácia, de forma a capturar melhor o desempenho dos modelos diante da distribuição de classes presente nos dados. 

 Todo o pré-processamento será aplicado dentro do processo de validação, por meio de pipelines, a fim de evitar vazamento de dados e garantir uma avaliação metodologicamente correta.
