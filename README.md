# Fashion MNIST — Classificação de Peças de Vestuário

## Objetivo
Desenvolver um modelo de aprendizado de máquina capaz de classificar imagens de roupas e acessórios em 10 categorias distintas, utilizando o dataset Fashion MNIST como benchmark.

## Integrantes
- Pedro Henrique Macedo Antunes
- Kevin Teixeira de Araújo Carvalho
- Diogo Lima de Oliveira

## Fonte dos dados
- **Dataset:** Fashion MNIST
- **Origem:** [Kaggle — Zalando Research](https://www.kaggle.com/datasets/zalando-research/fashionmnist)
- **Descrição:** 70.000 imagens em escala de cinza (28x28 pixels) divididas em 10 classes de roupas e acessórios, com 6.000 amostras por classe no treino e 1.000 no teste.

## Tipo da tarefa
Classificação multiclasse — o atributo-alvo (`label`) representa uma das 10 categorias:


|
 Rótulo 
|
 Classe 
|
|
--------
|
--------
|
|
 0 
|
 T-shirt/top 
|
|
 1 
|
 Trouser 
|
|
 2 
|
 Pullover 
|
|
 3 
|
 Dress 
|
|
 4 
|
 Coat 
|
|
 5 
|
 Sandal 
|
|
 6 
|
 Shirt 
|
|
 7 
|
 Sneaker 
|
|
 8 
|
 Bag 
|
|
 9 
|
 Ankle boot 
|

## Organização dos arquivos
repositório
┣  fundamentosIA.ipynb # Notebook principal com todo o projeto
┗  README.md # Este arquivo

Os dados são carregados diretamente do Kaggle via `kagglehub` dentro do notebook, sem necessidade de download manual.

## Como abrir no Google Colab
1. Acesse [colab.research.google.com](https://colab.research.google.com)
2. Clique em **Arquivo → Abrir notebook → GitHub**
3. Cole a URL deste repositório e selecione o arquivo `fundamentosIA.ipynb`
4. Execute as células em ordem — a primeira célula instala e carrega o dataset automaticamente

## Modelos utilizados
- **DummyClassifier** — baseline de referência, sempre prevê a classe mais frequente
- **SGDClassifier** — modelo linear treinado por gradiente descendente estocástico (loss=hinge, equivalente a SVM linear)
- **RandomForestClassifier** — conjunto de 100 árvores de decisão com profundidade máxima de 30

## Principais resultados

| Modelo | Acurácia | F1-score (weighted) |
|--------|----------|----------------------|
| Baseline (DummyClassifier) | 10.01% | 0.018 |
| SGDClassifier | 85.41% | 0.8537 |
| **RandomForestClassifier** | **97.88%** | **0.9787** |

O **RandomForestClassifier** foi escolhido como modelo final por apresentar o melhor desempenho em todas as métricas avaliadas. As principais dificuldades ocorreram entre classes visualmente similares: Shirt, Coat e Pullover (roupas de cima com silhueta parecida) e Sandal, Sneaker e Ankle Boot (calçados com estrutura semelhante).
