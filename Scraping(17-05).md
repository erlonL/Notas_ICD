# Scraping

coletar dados através do processamento do HTML de uma página.

## HTML

Tags - < > < />


### Bibliotecas para scraping

requests

Beautiful Soup - acessar os elementos do HTML

`pip install beautifulsoup4 requests`

```python

from bs4 import BeautifulSoup
import requests

url = ("https://raw.githubusercontent.com/joelgrus/data/master/getting-data.html")

html = requests.get(url).text
soup = BeautifulSoup(html, "html.parsers") # parser - processa
```

html 

h1 - titulo
h2 - subtitulo

div - retangulo "invisivel" serve para separar o código.


```python
html

soup

type(soup)

# encontrar dados de acordo com as tags
soup.find("p")

tag_p = soup.p
tag_p

tag_p.text

soup.body

soup.p['id']

tag_p['id']



# todas as ocorrências de uma tag

soup.find_all('p')

soup('p')


# paragrafos de uma determinada classe

soup("p", {"class" : "important"})

soup("p", "important")

```

hierarquia

```html
<body>
	<div>
	-- elemtentos
```


```python
divs = soup("div")
divs


div_with_spans = divs[3]

div_with_spans('span')




```

