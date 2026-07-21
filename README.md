# Fashion MNIST — Classificação de Peças de Roupa

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
Classificação multiclasse, o atributo-alvo (`label`) representa uma das 10 categorias: T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag e Ankle Boot.

## Organização dos arquivos
Repositório:
1. fundamentosIA.ipynb # Notebook principal com todo o projeto
2. README.md # Este arquivo
   
Os dados são carregados diretamente do Kaggle via `kagglehub` dentro do notebook, sem necessidade de download manual.

## Como abrir no Google Colab
1. Acesse o repositório no GitHub.
2. Abra o arquivo fundamentosIA.ipynb.
3. Clique em "Open in Colab" (caso disponível) ou acesse o Google Colab e escolha Arquivo → Abrir notebook → GitHub.
4. Execute todas as células em ordem.
   
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

O RandomForestClassifier foi escolhido como modelo final por apresentar o melhor desempenho em todas as métricas avaliadas. As principais dificuldades ocorreram entre classes visualmente similares: Shirt, Coat e Pullover (roupas de cima com silhueta parecida) e Sandal, Sneaker e Ankle Boot (calçados com estrutura semelhante).
