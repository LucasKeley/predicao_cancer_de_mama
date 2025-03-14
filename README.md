# Predição de Câncer de Mama usando IA

Este projeto utiliza algoritmos de Machine Learning para prever a presença de câncer de mama em um conjunto de dados.  Exploramos diferentes modelos e técnicas de pré-processamento para alcançar a melhor acurácia possível.

## Descrição do Projeto

O objetivo principal deste projeto é construir e avaliar modelos de classificação para diagnosticar tecidos mamários como malignos ou benignos. Utilizamos o conjunto de dados "Breast Cancer Wisconsin (Diagnostic)" disponível no Kaggle. O projeto segue as seguintes etapas:

## Dados

O conjunto de dados utilizado foi extraído do Kaggle ([link para o dataset](https://www.kaggle.com/code/anandhuh/breast-cancer-prediction-accuracy-98-24/notebook)) e dividido em dois conjuntos:

* **Treinamento:** 426 amostras
* **Teste:** 143 amostras


1. **Preparação do Ambiente:**
   - Conexão com o Google Drive para acesso aos dados.
   - Importação das bibliotecas necessárias (pandas, plotly, scikit-learn, matplotlib).

2. **Carregamento e Análise Exploratória de Dados:**
   - Carregamento do dataset a partir do Google Drive.
   - Exibição inicial dos dados para uma visão geral.
   - Utilização de `dados.info()` e `dados.describe()` para entender a estrutura e estatísticas descritivas dos dados.
   - Visualizações com Plotly para explorar a distribuição das classes (maligno vs. benigno) e a relação entre as variáveis e a classe alvo.

3. **Pré-processamento de Dados:**
   - Remoção de colunas irrelevantes (`id`, `diagnosis`, `Unnamed: 32`).
   - Separação das características (X) e da variável alvo (Y - diagnóstico).
   - Codificação da variável alvo ('M' e 'B') usando LabelEncoder.
   - Divisão do conjunto de dados em treino e teste usando `train_test_split`.

4. **Modelagem:**
   - Treinamento e avaliação de três modelos de classificação:
     - **Dummy Classifier:** Serve como baseline para comparação.
     - **Árvore de Decisão:** Modelagem através de árvores de decisão.  Experimentação com diferentes profundidades máximas para otimizar a performance e interpretabilidade do modelo.
     - **KNN (K-Nearest Neighbors):**  Utilização de normalização (MinMaxScaler) para melhorar o desempenho do modelo KNN.

5. **Comparação de Resultados:**
   - Cálculo da acurácia de cada modelo.
   - Gráfico de barras para visualização comparativa das acurácias.


## Tecnologias Utilizadas

- **Python:** Linguagem de programação principal.
- **Pandas:** Manipulação e análise de dados.
- **Plotly:** Criação de gráficos interativos.
- **Scikit-learn:** Biblioteca de Machine Learning para pré-processamento, modelagem e avaliação.
- **Matplotlib:** Criação de gráficos estáticos.
- **Google Colab:** Ambiente de desenvolvimento na nuvem.


## Como Executar o Projeto

1. **Google Colab:** O código foi desenvolvido para ser executado no Google Colab.  Basta abrir o arquivo .ipynb no Colab.
2. **Conectar o Google Drive:** Siga as instruções do notebook para conectar o Google Drive e fornecer o caminho correto para o dataset.


## Dados

O dataset utilizado é o Breast Cancer Wisconsin (Diagnostic), disponível em: [https://www.kaggle.com/code/anandhuh/breast-cancer-prediction-accuracy-98-24/notebook](https://www.kaggle.com/code/anandhuh/breast-cancer-prediction-accuracy-98-24/notebook)

## Resultados

Os resultados obtidos para cada algoritmo são apresentados abaixo:


| Algoritmo          | Acurácia |
|-------------------|----------------------|
| Dummy Classifier  |  0.6293706293706294  |
| Árvore de Decisão | 0.8881118881118881   |
| KNN               | 0.951048951048951    |

Acurácia Dammy: 0.6293706293706294
Acurácia Árvore: 0.8881118881118881
Acurácia KNN: 0.951048951048951

