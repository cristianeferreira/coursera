# Sentiment Analysis

### Preprocessing of tweets

1. Eliminate handles and URLs
2. Tokenize the string into words. 
3. Remove stop words like "and, is, a, on, etc."
4. Stemming- or convert every word to its stem. Like dancer, dancing, danced, becomes 'danc'. You can use porter stemmer to take care of this. 
5. Convert all your words to lower case.

### Criação do vocabulário e frequencias

1. Crie um vetor de palavras com todas as palavras que aparecem nos tweets de exemplo
2. Classifique o conjunto de exemplos em positivo e nagativo
3. Para cada classe, conte quantas vezes a palavra apareceu no conjunto de tweets da classe, tendo assim o elemento c(i,j), que é a contagem da palavra i para a classe j.

### Extração de features do tweet

$x = [1, \sum{c_{pos,i}}, \sum{c_{neg,i}}]$ com i para as palavras do tweet.

O 1 é para redução de vieses.
