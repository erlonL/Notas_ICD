# APIs

request (via HTTP) -> response

APIs geralmente fornecem dados em JSON

```python
#como dicionários em python
{"nome" : "José da Silva"}
```

```python
import json

serialized = """{"nome" : "José da Silva",
		"idade" : 18}"""
# aspas triplas: \n e string

# carrega o dicionário do python
deserialized = json.loads(serialized)

# transforma dicionário para o formato json
json.dumps(deserialized)
```

## Usando APIs

acessando a API Pública do Github
```python
import requests, json

github_user = "erlonL"
endpoint = f"https://api.github.com/users/{github_user}/repos"

repos = json.loads(request.get(endpoint).text)
print(json.dumps(repos[0], indent = 4))

response = requests.get(endpoint)
d = json.loads(response.text)

print(json.dumps(d[0], indent = 4))
```

### API do twitter

twarc - biblioteca do python
developer.twitter.com

`pip install twarc2`

`twarc2 search zelda`

`twarc2 search zelda --limit 500` - Pesquisa com limite 500

`twarc2 stream-rule add palavra`

`twarc2 stream` - Pesquisa de forma filtrada
