# SIMILARIDADE DE PRODUTOS

Esse projeto tem o intuito de analisar a similaridade de produtos.

## METODOLOGIA
Para encontrar a similaridade dos produtos irei utilizar Word2Vec + similaridade dos cossenos.

>**Como Word2Vec funciona ?**
Ele funciona utilizando uma rede neural de 3 camadas. Utilizando uma janela de palavras que estão antes e depois para prever qual a palavra que está no meio. Como resultado desse treinamento ele cria um dicionario em que o significado de cada palavra é um vetor que representa a palavra em um plano n-dimensional.

>**Como similaridade dos cossenos funciona ?**
A partir da localização das palavras em um plano n-dimensional criado pelo Word2Vec, podemos dizer que as palavras que estão proximas são parecidas enquanto as que estão mais distantes uma das outras tem um significado diferente. O valor do cosseno pode variar de -1 (cosseno de 0, logo as palavras estão no mesmo ponto no plano n-dimensional) até 1 (cosseno de 180, quando as palavras estão opostas).

>**E como aplicamos isso para uma descrição, que possui mais de uma palavra ?**
Para isso vamos fazer a média dos vetores de cada palava e aplicamos a similaridade dos cossenos nesses vetores resultantes.


## BASE DE DADOS
A base utilizada nas analises é uma base com os brinquedos da Amazon disponivel no Kaggle. VOce pode fazer o download dela a partir desse link: https://www.kaggle.com/PromptCloudHQ/toy-products-on-amazon

> [Toy Products on Amazon](https://www.kaggle.com/PromptCloudHQ/toy-products-on-amazon) by [PromptCloudHQ](https://www.kaggle.com/PromptCloudHQ) is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

## INSTALAÇÃO
Para poder utilizar esse projeto você precisa ter instalado:
1. Python
2. pip
3. Jupyter Notebook
4. As bibliotecas no arquivo de [requirements](./requirements.txt).

## REFERENCIAS
Os seguintes posts me ajudaram a entender melhor como o Word2Vec e a similaridade dos cossenos funciona

https://medium.freecodecamp.org/how-to-get-started-with-word2vec-and-then-how-to-make-it-work-d0a2fca9dad3

https://towardsdatascience.com/introduction-to-word-embedding-and-word2vec-652d0c2060fa

https://medium.com/explore-artificial-intelligence/word2vec-a-baby-step-in-deep-learning-but-a-giant-leap-towards-natural-language-processing-40fe4e8602ba

https://medium.com/luizalabs/similaridade-entre-t%C3%ADtulos-de-produtos-com-word2vec-5e26199862f0
