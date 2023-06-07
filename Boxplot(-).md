# Boxplot

- Apenas um eixo pois é apenas uma variável.

- separado em mediana, q1 e q3 (primeiro e terceiro quartil)
	- q1 divide em 25%
	- q3 divide me 75%

- fecha em um retângulo que tem 50% dos dados
- Se calcularmos a distância entre os quartis, teremos o intervalo interquartil.
	Se a caixa for comprida, então os dados estão espalhados, se for curta, os dados estão concentrados.

- Definir um limite superior e inferior para o boxplot.
	Será um valor que corresponda ao limite inferior e superior presente no gráfico.
	Valores fora dos limites são chamados de 'Outliers', valores extremos.

	- Outliers pode ajudar a identificar
		- possíveis erros
		- grandes distorções
		- Fraudes


## Utilizando boxplot com o Pandas

```Python
import pandas as pd

df = pd.read_csv('data.csv')

df.boxplot(column=['player_height', 'age'])


```
