# Sentiment Analysis

### Criação do vocabulário

1. Crie um vetor de palavras com todas as palavras que aparecem nos tweets de exemplo
2. Classifique o conjunto de exemplos em positivo e nagativo
3. Para cada classe, conte quantas vezes a palavra apareceu no conjunto de tweets da classe, tendo assim o elemento c(i,j), que é a contagem da palavra i para a classe j.

### Preprocessing of tweets

1. Eliminate handles and URLs
2. Tokenize the string into words. 
3. Remove stop words like "and, is, a, on, etc."
4. Stemming- or convert every word to its stem. Like dancer, dancing, danced, becomes 'danc'. You can use porter stemmer to take care of this. 
5. Convert all your words to lower case.

### Extração de features do tweet

$x = [1, \sum{c_{pos,j}}, \sum{c_{neg,j}}]$ 
