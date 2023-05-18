# Scraping

coletar dados através do processamento HTML de uma página.

## HTML

Tags - < > </ >

### Bibliotecas para scraping

requests

Beautiful Soup - acessar os elementos do HTML.

`pip install beautifulsoup4 requests`

```python

from bs4 import BeautifulSoup
import requests

url = ("https://raw.githubusercontent.com/joelgrus/data/master/getting-data.html")
```
