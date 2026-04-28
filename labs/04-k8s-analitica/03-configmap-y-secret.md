# ConfigMap y Secret

## Objetivo

Separar configuración funcional y credenciales.

## Archivos

- `00-configmap-etl.yaml`
- `01-secret-etl-db.yaml`

## Demo breve

```bash
kubectl apply -f labs/04-k8s-analitica/trabajo/k8s-batch/00-configmap-etl.yaml
kubectl apply -f labs/04-k8s-analitica/trabajo/k8s-batch/01-secret-etl-db.yaml
kubectl -n analytics-lab get configmap,secret
```

# LABORATORIO

- [01-crear-configuracion.md](laboratorio/01-crear-configuracion.md)
## Navegacion del libro

- [Anterior](02-cronjob-etl-programado.md)
- [Siguiente](laboratorio/01-crear-configuracion.md)
