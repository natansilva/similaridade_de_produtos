# SIMILARIDADE DE PRODUTOS

Esse projeto tem o intuito de analisar a similaridade de produtos. A base de dados escolhida para a analise foi uma lista com os brinquedos disponiveis na Amazon que estão hospedados no Kagle.
Esse é o link para você fazer download dela: https://www.kaggle.com/PromptCloudHQ/toy-products-on-amazon

## METODOLOGIA
Para encontrar a similaridade dos produtos irei utilizar Word2Vec + similaridade dos cossenos.

>**Como Word2Vec funciona ?**
Ele funciona utilizando uma rede neural de 3 camadas. Utilizando uma janela de palavras que estão antes e depois para prever qual a palavra que está no meio. Como resultado desse treinamento ele cria um dicionario em que o significado de cada palavra é um vetor que respresnta a palavra em um plano n-dimensional.

>**Como similaridade dos cossenos funciona ?**
A partir da localização das palavras em um plano n-dimensional criado pelo Word2Vec, podemos dizer que as palavras que estão proximas são parecidas enquanto as que estão mais distantes uma das outras tem um significado diferente. O valor do cosseno pode variar de -1 (cosseno de 0, logo as palavras estão no mesmo ponto no plano n-dimensional) até 1 (cosseno de 180, quando as palavras estão opostas).

>**E como aplicamos isso para uma descrição, que possui mais de uma palavra ?**
Para isso vamos fazer a média dos vetores de cada palava e aplicamos a similaridade dos cossenos nesses vetores resultantes.
