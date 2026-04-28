# Step 01 - Crear configuración externa

Crear y aplicar:

- `00-configmap-etl.yaml`
- `01-secret-etl-db.yaml`

```bash
kubectl apply -f labs/04-k8s-analitica/trabajo/k8s-batch/00-configmap-etl.yaml
kubectl apply -f labs/04-k8s-analitica/trabajo/k8s-batch/01-secret-etl-db.yaml
```

## Siguiente

- [02-ejecutar-job.md](02-ejecutar-job.md)
## Navegacion del libro

- [Anterior](../03-configmap-y-secret.md)
- [Siguiente](02-ejecutar-job.md)
