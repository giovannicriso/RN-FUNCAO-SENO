Descrição do Repositório

Este projeto implementa uma rede neural simples em **PyTorch** com o objetivo de aprender a função seno no intervalo de `0` a `4π`.  
A rede é composta por:

- Uma camada de entrada com 1 neurônio;
- Uma camada oculta com 50 neurônios utilizando a função de ativação *Tanh*;
- Uma camada de saída com 1 neurônio.

O conjunto de dados de treinamento é gerado a partir de 1000 pontos igualmente espaçados, onde as entradas correspondem aos valores do eixo `x` e as saídas são os respectivos valores de `sin(x)`. Esses dados são convertidos em tensores do PyTorch para serem processados pela rede.

O modelo é treinado utilizando o otimizador **Adam**, com taxa de aprendizado de `0.01`, e a função de perda escolhida é o erro quadrático médio (**MSE**).  
O treinamento ocorre ao longo de 500 épocas, com a perda sendo exibida a cada 100 épocas para acompanhamento do progresso.

Após o treinamento, o modelo é avaliado utilizando um novo conjunto de dados de teste, e os resultados são comparados com os valores reais da função seno em um gráfico gerado com `matplotlib`.  
O resultado final mostra que a rede neural é capaz de aprender e prever com boa precisão o comportamento da função seno.

---

Além disso, este repositório também inclui a implementação de uma rede neural para o cálculo da função seno utilizando **scikit-learn**, feita pelo professor durante a aula de Física Computacional. Essa versão serviu como base para compreender os métodos e reproduzi-los em PyTorch.
