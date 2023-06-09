# Agrupamento

Agrupamento (ou clusterização) é um conjunto de técnicas para encontrar grupos nos dados, em que dados são pareidos entre eles (distâncias próximas).

- Representação em pontos no espaço (gráfico)


## Aplicações

"Calcular média, mediana,..."
- Marketing: Agrupar pessoas com características parecidas / agrupar grupos de usuários em redes sociais.
- Detecção de fraudes: Detectar compras suspeitas que não se encaixam no perfil do usuário.

## K-means

Algoritmo para encontrar grupos em dados.
Separa o dataset em K grupos distintos (K é uma constante).

```python
import sklearn as sk

sk.cluster.KMeans()

```

Cada grupo será um centroide.
- Após inicializar o centroide, o segundo passo é verificar, para cada ponto, qual o centroide mais próximo.
- Terceiro passo: Reposicionar o cluster para cada centroide (calculando a média).
Pode ser necessário repetir os últimos dois passos até que os centroides estejam ajustados.

Obs: O resultado do K-means depende da inicialização aleatória dos centroides. Mas podemos setar uma seed (int, random_state) para que se tenha um resultado determinístico.

elbow method: serve para escolher o K quando se compara K's em um gráfico que assume uma forma de um cotovelo ou joelho.

### Implementação

```python
import pandas as pd
import seaborn as sns
from sklearn.cluster import KMeans

df = pd.read_csv('starbucks.csv')

sns.scatterplot(data=df, x='calories', y='carb')


df_group = df[['calories', 'carb']]
df_group


kmeans = KMeans(n_clusters=2) #inicializar definindo k

kmeans.fit(df_group) #agrupa os clusters

kmeans.labels_ #Mostra para cada elemento, seu respectivo agrupamento (0, 1, 2,...,n-1)


sns.scatterplot(data=df, x='calories', y='carb', hue = kmeans.labels_)


df[kmeans.labels_ == 0]

df[kmeans.labels_ == 1]


kmeans = KMeans(n_clusters=3) # Com 3 clusters
kmeans.fit(df_group)
kmeans.labels_

kmeans.cluster_centers_ #Mostra as coordenadas

# // Qual o melhor número para k

kmeans.inertia_

inertias = []
for i in range(1,11):
	kmeans = KMeans(n_clusters=i)
	kmeans.fit(df_group)
	inertias.append(kmeans.inertia_)


inertias

sns.lineplot(x= range(1,11), y = inertias)

```


```python
df_group = df[['calories', 'fat', 'carb', 'fiber', 'protein']]
df_group

kmeans = KMeans(n_clusters=3)
kmeans.fit(df_group)
kmeans.labels_

sns.scatterplot(data=df, x='calories', y='carb', hue = kmeans.labels_)


normalized_df = (df_group-df_group.mean())/df_group.std()
normalized_df


kmeans = KMeans(n_clusters=3)
kmeans.fit(df_normalized_df)

sns.scatterplot(data=normalized_df, x='calories', y='carb', hue = kmeans.labels_)


df[kmeans.labels_ == 0] # Verificando os grupos

df[kmeans.labels_ == 1]



```
