# TP1 – Classificação de Exoplanetas com Machine Learning
 
Trabalho Prático 1 da disciplina **Aprendizado de Máquina I** (3º período do curso de Ciência de Dados na PUC Minas). O objetivo foi comparar seis métodos de classificação aplicados a um problema real: distinguir candidatos a exoplanetas confirmados de falsos positivos, utilizando dados da sonda espacial Kepler da NASA.
 
---
 
## Objetivo
 
Treinar, avaliar e comparar os algoritmos Naive Bayes, Decision Tree, K-Nearest Neighbors, Support Vector Machine, Random Forest e Gradient Tree Boosting sobre o dataset `koi_data.csv`, composto por 5.202 observações e 43 colunas. A avaliação foi realizada com validação cruzada estratificada k-fold (k=5), utilizando acurácia, precisão, recall e F1-score como métricas, necessário dado o leve desbalanceamento de classes (60% falsos positivos / 40% confirmados).
 
---
 
## Metodologia
 
- Pré-processamento com `StandardScaler` dentro de pipelines, evitando vazamento de dados.
- Variação de hiperparâmetros em cada modelo (profundidade da árvore, número de vizinhos, kernel do SVM, número de estimadores) para identificar o melhor equilíbrio entre bias e variância.
- Classe positiva definida como `CONFIRMED` em todas as métricas.
---
 
## Resultados
 
| Modelo | Acurácia | Precisão | Recall | F1-score |
|---|---|---|---|---|
| Naive Bayes *(baseline)* | 0.917 | 0.846 | 0.972 | 0.905 |
| Decision Tree (`max_depth=6`) | 0.949 | 0.919 | 0.959 | 0.939 |
| SVM (`kernel=linear`) | 0.951 | 0.922 | 0.961 | 0.941 |
| K-NN (`k=5`) | 0.896 | 0.812 | 0.967 | 0.883 |
| Random Forest (`n=100`) | **0.970** | **0.966** | 0.961 | **0.963** |
| Gradient Boosting (`n=100`) | 0.970 | 0.957 | **0.970** | 0.963 |
 
---
 
## Conclusão
 
O **Random Forest** foi escolhido como modelo final. Apesar do desempenho praticamente idêntico ao Gradient Boosting (F1-score de 0.963 em ambos), o Random Forest apresentou treinamento significativamente mais rápido (~3s vs ~8s), graças ao treinamento paralelo das árvores, e maior estabilidade em relação à variação de hiperparâmetros. Em um cenário prático que valoriza eficiência computacional e robustez, essas características o tornam a escolha mais adequada.
 
---
 
## Tecnologias
 
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat&logo=python&logoColor=white)
 
---
 
## Fonte dos dados
 
[koi_data_csv](df/koi_data.csv)
