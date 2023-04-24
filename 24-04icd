## Seaborn

```pip install seaborn```
```import seaborn as sns```


```python
mydata = {'movies': ['movie1', 'movie2'], 'num_oscars': [1, 2]}

mydata['movies']

mydata['num_oscars']


# Criando o primeiro gráfico com filmes e seus números de oscars

sns.barplot(data = mydata, x='movies', y='num_oscars')

sns.barplot(x = mydata['movies'], y = mydata['num_oscars'])

# Adicionando Labels


ax = sns.barplot(x = mydata['movies'], y = mydata['num_oscars'])

ax.set(xlabel='Movies', ylabel='Oscars')
ax.set_title('Oscars')
x = ax 

```

## Gráfico de linha

```python

# Utilizado com dados lineares

data2 = dataframe

sns.lineplot(data = data2, x = 'year', y = 'passengers')

# As colunas já vêm com nome pois utilizamos um dataframe

# marker

# Adiciona um marcador nos pontos do gráfico
sns.lineplot(data = data2, x = 'year', y = 'passengers', marker = 'o')

# hue

sns.lineplot(data = data2, x = 'year', y = 'passengers', marker = 'o', hue = 'month)

# mover legenda
sns.movelegend(ax, "upper left", bbox_to_anchor=(0,5,1), ncol=2)

```

# Gráfico de dispersão

```python
sns.scatterplot(data = tips, x = 'total_bill', y = 'tip', hue = 'time', size='size')



# adicionando markers diferentes


markers = {'No': 'o', 'Yes': 'X'}

sns.lineplot(data = data2, x = 'year', y = 'passengers', 
hue = 'time', size = 'size', style='smoker')

```

# Gráfico de Histograma

```python

sns.displot(data = tips, x = 'tip')

# Só tem uma variável pois y é a frequência de certo valor

# binwidth modifica o tamanho das barras

sns.displot(data = tips, x = 'tip', binwidth=2)

# bins especifica a quantidade de bins

sns.displot(data = tips, x = 'tips', bins = 5)

```

# Gráfico de Pizza

```python

tips_per_day = tips.groupby('day').sum()


tips_per_day.plot.pie(y = 'tip')
```

# Matriz de correlação (heatmap)

```python
tips.corr()

sns.heatmap(data = tips.corr(), annot = True)
```

