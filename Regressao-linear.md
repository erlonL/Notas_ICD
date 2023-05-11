# Regressão Linear

## Modelo
É um 'blueprint', que matematicamente serve para <b>prever uma relação</b> de uma variável (utiliza dados anteriores).

> "Usar o número de pessoas e o nível de fome delas para determinar as quantidades de ingredientes de uma receita".

# Regressão Linear

- Exemplo:
    - Em um scatterplot, se é observada uma tendência, pode-se representar a relação utilizando a regressão linear através de um modelo.

```python
import matplotlib.pyplot as plt
import seaborn as sns

sns.scatterplot(data, x, y)
plt.show()

# // Gráfico //

```

### Matematicamente

$f(x) = ax + b$

a = inclinação
b = deslocamento

### Qual reta utilizar?

- A reta que mais está próxima aos dados, a que tenha o menor <b>erro médio quadrático</b>
\* erro médio quadrático: calcula-se as <u>distâncias</u> entre o ponto desejado e a reta, quanto maior a distância, maior o erro.

### Plotando

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import linregress

sns.scatterplot(data, x, y)
plt.show()

result = linregress(df[''], df[''])

result.slope
result.intercept

def predict(x):
    return x*slope + result.intercept

# Prediz o valor da casa a partir da median_income 6
predict(6)

# Plotando a reta

plt.scatter(x,y)
plt.plot((x,y), (predict(x), predict(y)), c = 'red') # x e y inicial, x e y final
plt.show()

```
