# Configurar client/server OPC UA & Exibir dados em uma aplicação front-end em React com Vite

Neste projeto é criada uma **aplicação front-end em React com Vite** para exibir os dados do **cliente OPC UA** que recebe esses dados do **server OPC UA**.

Para isso, adiciona-se uma **camada intermediária**: um pequeno servidor Web em Python (Flask ou FastAPI). Isso porque o React (que roda no navegador) não consegue se conectar diretamente a um servidor OPC UA. Ele precisa de uma API HTTP para solicitar os dados.

### 1. Um servidor Web em Python (que chamaremos de web_api.py) irá:

  - Conectar-se ao seu opcua_server.py como um cliente OPC UA.

  - Ler os dados do OPC UA.

  - Expor um endpoint HTTP (ex: /api/data) que o front-end React pode consumir.

### 2. A aplicação React (vite-opcua-dashboard) irá:

  - Fazer requisições HTTP para o web_api.py.

  - Exibir os dados recebidos em uma interface amigável.



## 1. Crie o Servidor Web (Python FastAPI)
Vamos usar FastAPI por ser moderno e fácil de usar.

Crie um novo arquivo chamado **web_api.py**:

```bash
# web_api.py
```


