### O que fazer se o modelo estiver com erro grande demais?

* Mais exemplos
* Mais atributos
* Menos atributos
* Criar novos atributos (p.ex. $x^2$)
* Aumentar ou diminuir fator de regularização $\lambda$

### Avaliando o seu modelo

* Dividir os exemplos em treino, cross-validation e teste. O cross-validation escolhe o modelo. O teste gera a métrica do modelo escolhido.
* Pode dividir o conjunto (treino+CV) em blocos, e treinar/CV para todas as combinações de amostras treino+CV. Escolhe a de menor erro médio no CV.
* Parâmetro de regularização: variar i em $\lambda = 0,01 * 2^i$
