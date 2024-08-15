# Term Deposits Classification


Este projeto tem como objetivo prever se um cliente irá subscrever a um depósito a prazo com base em várias características fornecidas no conjunto de dados. O dataset foi processado, explorado e modelado usando diferentes técnicas de aprendizado de máquina para alcançar o melhor desempenho preditivo.

## Conjunto de Dados
- **Dados de Treinamento**: `Train.csv` (45.211 linhas, 17 colunas)
- **Dados de Teste**: `Test.csv` (4.521 linhas, 17 colunas)

### Visão Geral dos Dados
- Não foram encontrados valores ausentes nos conjuntos de dados de treino e teste.
- Não foram detectadas linhas duplicadas no conjunto de dados de treino.
- A variável alvo é `y`, indicando se um cliente subscreveu ou não a um depósito a prazo (sim ou não).

## Processamento de Dados
1. **Tratamento de Variáveis Categóricas**:
   - O `LabelEncoder` foi utilizado para converter variáveis categóricas em códigos numéricos.
   - Este passo foi aplicado tanto no conjunto de dados de treino quanto no de teste.

2. **Codificação de Características**:
   - Variáveis categóricas como `job`, `marital`, `education`, etc., foram transformadas utilizando o `LabelEncoder`.

3. **Análise de Correlação**:
   - Um heatmap foi utilizado para analisar as correlações entre as características. A maioria das correlações era fraca, indicando a necessidade de modelos não lineares.

## Análise Exploratória dos Dados (EDA)
- **Gráficos de Distribuição**: Histogramas foram criados para todas as características, a fim de entender suas distribuições.
- **Gráficos de Contagem**: Analisaram a contagem de várias categorias dentro das características, mostrando o desequilíbrio nas classes-alvo.
- **Box Plots**: Usados para detectar outliers e analisar a relação entre características numéricas e a variável alvo.

## Modelagem
Três modelos de aprendizado de máquina foram testados:

1. **Árvore de Decisão**:
   - `DecisionTreeClassifier` com profundidade máxima de 3.
   - Acurácia: **88,71%**
   - Matriz de Confusão:
     ```
     [[7756, 199],
      [ 822, 266]]
     ```

2. **Naive Bayes**:
   - `GaussianNB`.
   - Acurácia: **83,63%**
   - Matriz de Confusão:
     ```
     [[7056, 899],
      [ 581, 507]]
     ```

3. **Random Forest**:
   - `RandomForestClassifier` com 100 estimadores.
   - Acurácia: **90,22%** (Melhor Modelo)
   - Matriz de Confusão:
     ```
     [[7710, 245],
      [ 639, 449]]
     ```

## Conclusão
O modelo de Random Forest apresentou a maior acurácia entre os modelos testados. Mais ajustes e engenharia de características podem melhorar o desempenho do modelo.

