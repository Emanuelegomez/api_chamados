# API de Chamados

## Descrição

Primeira versão de uma API de chamados desenvolvida com FastAPI. Nesta etapa, os dados são armazenados em memória.

## Tecnologias utilizadas

* Python
* FastAPI
* Uvicorn
* Pydantic

## Como executar

1. Ative o ambiente virtual:

```bash
.venv\Scripts\activate
```

2. Instale as dependências:

```bash
pip install -r requirements.txt
```

3. Execute a aplicação:

```bash
uvicorn main:app --reload
```

4. Acesse a documentação interativa:

```text
http://127.0.0.1:8000/docs
```

## Endpoints

* `GET /` — verifica se a API está funcionando.
* `GET /chamados` — lista os chamados.
* `POST /chamados` — cria um novo chamado.
* `GET /chamados/{id}` — consulta um chamado pelo ID.
* `GET /chamados/status/{status_chamado}` — filtra chamados pelo status.

## Validação

O modelo Pydantic `ChamadoEntrada` valida os campos obrigatórios:

* título
* descrição
* prioridade

A API retorna erro de validação quando um campo obrigatório não é informado.

## Armazenamento

Os chamados são armazenados em uma lista na memória. Os dados são perdidos quando a aplicação é encerrada.
