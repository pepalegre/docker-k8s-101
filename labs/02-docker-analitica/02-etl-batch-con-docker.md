# ETL batch con Docker

## Objetivo

Crear proceso batch separado del servicio API.

## Crear archivos

- `labs/02-docker-analitica/trabajo/stack-analitica/etl/requirements.txt`
- `labs/02-docker-analitica/trabajo/stack-analitica/etl/etl.py`
- `labs/02-docker-analitica/trabajo/stack-analitica/etl/Dockerfile`

## Demo breve

```bash
cd labs/02-docker-analitica/trabajo/stack-analitica
docker build -t analytics-etl:0.1.0 ./etl
```

## Continuar

- [03-compose-api-db-etl.md](03-compose-api-db-etl.md)
## Navegacion del libro

- [Anterior](01-api-fastapi-con-docker.md)
- [Siguiente](03-compose-api-db-etl.md)
