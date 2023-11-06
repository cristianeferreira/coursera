# Conteúdo:

* Aprendizado supervisionado: classificação e regressão
* Aprendizado não supervisionado: clustering, detecção de anomalia e PCA
* Sistemas de recomendação
* Reinforcement learning

# Regressão linear

### Vocabulário:

* features ou atributos,
* target: numérico ou categorias
* conjunto de treinamento, exemplos de treinamento (x(i), y(i))
* notação: m é o numero de exemplos de treino, n é o número de features
* $f(x) = \hat{y}$, onde $f(x)$ é a função de predição (estimativa, inferência)
* Regressão linear: $f(x) = wx + b$ onde $w, x$ são os parâmetros do modelo otimizados por um algoritmo
* Função de custo Minimum Squared Error (MSE): $J(w, b) = (1/2m) \Sigma _{i=1} ^{m} (\hat{y}^i – y^i)^2$

### Minimização da função custo:

Fazer o update de $w, b$ conforme as expressões:

$w = w - \alpha \frac{\partial}{\partial w} J(w,b)$

$b = b - \alpha \frac{\partial}{\partial w} J(w,b)$

onde $\alpha$ é o *learning rate*. Se $\alpha$ é muito pequeno, a convergência é lenta, e se é muito grande, diverge. Escolhas usuais são potências de 10. Para escolher, o ideal é plotar um gráfico de $\alpha$ por número de iterações para convergência. 

Plotar a learning curve (#iter x custo) para entender como está convergindo. Fixar um número de iterações pelo gráfico, ou testar variação desprezível do erro.

# Regressão logística

* Objetivo: classificação binária (0/1)
* Usa a técnica de regressão linear para ajustar uma sigmóide $g(z)$ nos dados, e define um valor limiar para $g(z)$ para ser a fronteira de decisão.
   * Sigmoide: $g(z) = \frac{1}{1+e^z}$
   * $z(x) = wx + b$, onde $x$ pode ter múltiplas features.
* É possível desenhar fronteiras não lineares: basta fazer uma z(x) não linear.
* A função custo não é MSE porque não é convexa 
* Função custo: $L(w,b) = (1/m) \Sigma_{i=1}^{m}\{\log(y^{(i)} f_{w,b}(x^{(i)}) + (1-y^{(i)}) (1-f_{w,b}(x^{(i)})))\}$

# Conceitos gerais

* Implementações:
   * Batch: cada passo usa todos os training examples
   * Pode usar um subconjunto dos exemplos a cada passo.
* Feature scaling: divide max, max-normalização (subtrai media, divide por max-min), z-score normalização
* Overfitting (high variance) vs Underfitting (high bias)
* Regularização: o overfitting está ligado normalmente a valores muito grandes nos parâmetros. Por isso se usa um parâmetro extra de regularização na função custo, que é um fator multiplicado pela soma dos parâmetros (L1) ou quadrados dos parâmetros (L2)


