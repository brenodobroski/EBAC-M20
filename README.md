# Projeto de Classificação de Score de Crédito com Naive Bayes

## Visão Geral do Projeto

Este projeto tem como objetivo desenvolver um modelo de machine learning para prever o score de crédito de clientes. Utilizando um conjunto de dados sobre características demográficas e financeiras, foi aplicado o algoritmo **Gaussian Naive Bayes** para classificar o score em três categorias: Baixo (Low), Médio (Average) e Alto (High).

O projeto demonstra um fluxo completo de trabalho em ciência de dados, desde o carregamento e verificação dos dados, treinamento do modelo, até a avaliação de sua performance com métricas como acurácia, recall e a análise da matriz de confusão.

## Metodologia

O algoritmo Naive Bayes foi escolhido por ser um classificador probabilístico simples e eficiente. Ele se baseia no Teorema de Bayes com a suposição (ingênua, ou *naive*) de independência condicional entre as features. Para este projeto, foi utilizada a implementação `GaussianNB` da biblioteca `scikit-learn`, adequada para features contínuas.

As principais etapas do projeto foram:
1.  **Carregamento e Análise dos Dados**: Os dados foram divididos em conjuntos de treino (`X_train`, `y_train`) e teste (`X_test`, `y_test`). Foi verificado o balanceamento das classes na base de treino.
2.  **Treinamento do Modelo**: O modelo `GaussianNB` foi treinado com os dados de treino balanceados (`X_train_balanced.csv` e `y_train_balanced.csv`).
3.  **Avaliação de Performance**: O modelo foi avaliado em ambos os conjuntos (treino e teste) para verificar seu desempenho e capacidade de generalização.

## Ferramentas e Bibliotecas

* **Python 3**
* **Pandas**: para manipulação e análise de dados.
* **Scikit-learn**: para aplicação do modelo Naive Bayes e cálculo das métricas de avaliação (`accuracy_score`, `recall_score`, `confusion_matrix`).
* **Plotly**: para a visualização da matriz de confusão.
* **Jupyter Notebook**: como ambiente de desenvolvimento.

## Resultados

O modelo apresentou um desempenho excelente, com alta acurácia e recall tanto nos dados de treino quanto nos de teste, indicando uma boa capacidade de generalização.

### Performance nos Dados de Treino
* **Acurácia**: 90.08%
* **Recall (Macro Avg)**: 90.08%
* **Matriz de Confusão (Treino)**: O modelo demonstrou alta performance na previsão das categorias "Médio" e "Alto", com uma pequena quantidade de erros na classificação da categoria "Baixo".

### Performance nos Dados de Teste
* **Acurácia**: 97.56%
* **Recall (Macro Avg)**: 94.44%
* **Matriz de Confusão (Teste)**: O desempenho nos dados de teste foi ainda superior, com apenas um erro de classificação, validando a eficácia do modelo.

## Conclusão

O projeto demonstrou com sucesso a aplicação do algoritmo Naive Bayes para um problema de classificação de score de crédito multiclasse. Os resultados indicam que, mesmo com sua simplicidade, o modelo foi capaz de aprender os padrões nos dados e realizar previsões com alta precisão. Este trabalho serve como uma base sólida para a exploração de modelos mais complexos e aprofundamento em técnicas de otimização e avaliação de classificadores.
