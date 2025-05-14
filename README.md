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

Também foi incluido a implementação de uma rede neural para o cálculo da função seno utilizando **scikit-learn**, feita pelo professor durante a aula de Física Computacional. Essa versão serviu como base para compreender os métodos e reproduzi-los em PyTorch.

---

Por fim, este projeto implementa um modelo de rede neural treinado para **aprender a operação de derivação de funções**, utilizando o `MLPRegressor` do `scikit-learn`. O modelo é treinado com **dados sintéticos gerados a partir de polinômios e suas derivadas analíticas**, permitindo que ele aprenda a estimar a derivada de uma função com base apenas na sua forma discreta (amostrada).

O conjunto de dados é construído a partir de **funções polinomiais aleatórias normalizadas**, com ruído adicionado, e suas respectivas derivadas. A rede recebe como entrada a amostra da função \( f(x) \) e aprende a prever \( f'(x) \), funcionando como um **"estimador de derivadas"**.

A arquitetura da rede consiste em um **MLP com 10 camadas ocultas**, cada uma contendo **10 neurônios** e função de ativação `tanh`. O treinamento é realizado com o otimizador **Adam**, e o modelo é ajustado até convergir, com detecção de estagnação no aprendizado (*early stopping*).

Após o treinamento, o modelo é testado com **funções que não foram vistas durante o treino**, como seno, cosseno e um polinômio simples. Os resultados são apresentados graficamente, **comparando a derivada verdadeira com a estimativa feita pela rede**.
