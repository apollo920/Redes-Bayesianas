# Redes Bayesianas - Análise de Sobrevivência no Titanic

Este repositório contém um projeto de análise de dados utilizando Redes Bayesianas para prever a sobrevivência de passageiros no Titanic. O projeto foi desenvolvido em Python, utilizando bibliotecas como `pandas`, `scikit-learn`, e `pgmpy` para a construção e treinamento do modelo.

## Descrição do Projeto

O objetivo deste projeto é prever a sobrevivência de passageiros do Titanic com base em diversas variáveis, como classe da passagem, gênero, idade, tarifa paga, local de embarque, entre outras. O projeto segue as seguintes etapas:

1. **Carregamento e Exploração dos Dados**: O dataset utilizado é o famoso conjunto de dados do Titanic, disponível no Kaggle. O dataset contém informações sobre os passageiros, como nome, idade, sexo, classe da passagem, tarifa paga, local de embarque, e se sobreviveram ou não ao desastre.

2. **Tratamento de Valores Faltantes**: Foram identificadas e tratadas as variáveis com valores faltantes, como `Age` e `Embarked`. Para `Age`, os valores faltantes foram preenchidos com a mediana baseada na classe e no sexo do passageiro. Para `Embarked`, os valores faltantes foram substituídos pela moda.

3. **Discretização de Variáveis**: As variáveis contínuas, como `Age` e `Fare`, foram discretizadas em categorias para facilitar a modelagem. Além disso, variáveis como `Ticket` e `Cabin` foram transformadas em categorias que refletem informações relevantes, como o prefixo do ticket e o deck da cabine.

4. **Codificação de Variáveis Categóricas**: As variáveis categóricas foram codificadas em valores numéricos utilizando `LabelEncoder`, permitindo que o modelo possa processá-las.

5. **Construção e Treinamento da Rede Bayesiana**: Foi construída uma rede bayesiana utilizando a biblioteca `pgmpy`. A rede foi treinada com os dados discretizados e codificados, e foi utilizada para prever a sobrevivência dos passageiros.

6. **Avaliação do Modelo**: O modelo foi avaliado com base em métricas de desempenho, como acurácia, precisão, recall e F1-score.

## Tecnologias Utilizadas

- **Python**: Linguagem de programação utilizada para a análise de dados e construção do modelo.
- **Pandas**: Biblioteca para manipulação e análise de dados.
- **Scikit-learn**: Biblioteca para pré-processamento de dados e codificação de variáveis categóricas.
- **Pgmpy**: Biblioteca para construção e treinamento de redes bayesianas.

## Dataset Utilizado

O dataset utilizado é o `train.csv`, que contém informações sobre os passageiros do Titanic. O dataset foi obtido do Kaggle e contém as seguintes colunas:

- **PassengerId**: Identificador único do passageiro.
- **Survived**: Indica se o passageiro sobreviveu (1) ou não (0).
- **Pclass**: Classe da passagem (1 = Primeira Classe, 2 = Segunda Classe, 3 = Terceira Classe).
- **Name**: Nome do passageiro.
- **Sex**: Gênero do passageiro (male/female).
- **Age**: Idade do passageiro.
- **SibSp**: Número de irmãos/cônjuges a bordo.
- **Parch**: Número de pais/filhos a bordo.
- **Ticket**: Número do ticket.
- **Fare**: Tarifa paga pelo passageiro.
- **Cabin**: Número da cabine.
- **Embarked**: Porto de embarque (C = Cherbourg, Q = Queenstown, S = Southampton).

## Estrutura do Projeto

- **RedesBayesianas.ipynb**: Notebook Jupyter contendo todo o código do projeto, desde a carga dos dados até a construção e avaliação do modelo.
- **train.csv**: Dataset utilizado no projeto.

## Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/redes-bayesianas-titanic.git