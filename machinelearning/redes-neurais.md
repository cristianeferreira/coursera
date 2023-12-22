# Redes neurais

### Arquitetura

* Cada camada possui um ou mais neurônio, cada neurônio é uma sigmóide que recebe todos os outputs da camada anterior.
* A função de ativação é justamente essa sigmóide (mas pode ser outra função). A ativação é a saída.
* Notação: a primeira camada é o input, as intermediárias são as hidden layers, e a última é output layer.

### Treinamento e Parâmetros

* Número de camadas e de units de cada camada
* Função de ativação: sigmoide, RELU (g(z)=0 se z<0 e g(z)=z cc), softmax (multiclassificação)
   * A composição de RELUS permite criar uma função de saída que é a composição de funções. São usadas nas hidden layers 
* Perda: BinaryCrossEntropy (a da regressão logística), MSE
   * Deve ser definida conforme o objetivo da rede: classificar ou regredir 
* Epochs: número de passos do gradient descent
* SOFTMAX: cada output ai é $e^{z_{i}} / ({e^{z_{1}} + ... + e^{z_{k}}})$
* ADAM (Adaptative Moment Estimation): ajusta o learning rate conforme variabilidade da direção do ajuste a cada passo. Se dois ajustes são na mesma direção, é porque ela está boa, e o learning rate pode aumentar.

### Tipos de camadas

* Dense: todos os neurônios de uma camada se ligam a todos da camada seguinte
* Convolucional: cada neurônio se liga apenas a parte da camada seguinte. Ex: em imagem, um neurônio por região, só se liga aos adjacentes.
* 
