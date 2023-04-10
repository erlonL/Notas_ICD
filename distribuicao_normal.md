# Distribuição Normal

quando dados se comportam de forma que há uma distribuição concentrada em uma parte 'média', fora desta parte central, a frequência diminui. 
	é modelada como uma curva em formato de sino.

definição:
	a curva normal pode ser ajustada usando dois parâmetros:
		- A média e o desvio padrão
		- Média
		- Desvio padrão achata a curva


## Z-score

Número de desvios padrões acima ou abaixo da média

É utilizado para normalizar os dados.

Após a aplicação do z-score
	-a média dos valores passa a ser zero.
	-desvio padrão passa a ser um.


## Calculando dados com distribuição normal

```Python
form scipy.stats import norm
 
norm.cdf(v1, m, d)

```

