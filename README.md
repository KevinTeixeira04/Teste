# Fashion MNIST — Classificação de Peças de Roupa

## Objetivo
Desenvolver um modelo de aprendizado de máquina capaz de classificar imagens de roupas e acessórios em 10 categorias distintas, utilizando o dataset Fashion MNIST.

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
- **fundamentosIA.ipynb**:  Notebook principal com todas as etapas do projeto
- **README.md**: Arquivo com informações do projeto e instruções
   
## Como abrir no Google Colab
1. Acesse o repositório no GitHub.
2. Faça o download do arquivo fundamentosIA.ipynb.
3. Acesse o Google Colab e escolha Arquivo → Abrir Notebook → Upload → Procurar.
4. Selecione o arquivo baixado e abra.
5. Execute todas as células em ordem.
   
## Modelos utilizados
- **DummyClassifier** — baseline de referência, sempre prevê a classe mais frequente
- **SGDClassifier** — modelo linear treinado por gradiente descendente estocástico 
- **RandomForestClassifier** — conjunto de 100 árvores de decisão com profundidade máxima de 30

## Principais resultados

| Modelo | Acurácia | F1-score (weighted) |
|--------|----------|----------------------|
| Baseline (DummyClassifier) | 10.01% | 0.018 |
| SGDClassifier | 85.41% | 0.8537 |
| **RandomForestClassifier** | **97.88%** | **0.9787** |

O RandomForestClassifier foi escolhido como modelo final por apresentar o melhor desempenho em todas as métricas avaliadas. As principais dificuldades ocorreram entre classes que são visualmente similares: Shirt, Coat e Pullover (roupas de cima com silhueta parecida) e Sandal, Sneaker e Ankle Boot (calçados que possuem estrutura semelhante).

## Divisão das contribuições
- Pedro Henrique Macedo Antunes: seções 5.1 (Identificação e descrição do problema), 5.2 (Compreensão dos dados) e 5.3 (Análise Exploratória)
- Diogo Lima de Oliveira: seções 5.4 (Pré-Processamento) e 5.5 (Separação dos dados)
- Kevin Teixeira de Araújo Carvalho: seções 5.6 (Modelagem) e 5.7 (Avaliação e Discussão)

## Link do vídeo 
Colocar aqui.

