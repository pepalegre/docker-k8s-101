# CronJob ETL programado

## Objetivo

Automatizar la ejecución periódica del ETL.

## Archivo principal

`labs/04-k8s-analitica/trabajo/k8s-batch/03-cronjob-etl.yaml`

## Demo breve

```bash
kubectl apply -f labs/04-k8s-analitica/trabajo/k8s-batch/03-cronjob-etl.yaml
kubectl -n analytics-lab get cronjobs
kubectl -n analytics-lab get jobs --watch
```

## Continuar

- [03-configmap-y-secret.md](03-configmap-y-secret.md)
## Navegacion del libro

- [Anterior](01-job-etl-una-ejecucion.md)
- [Siguiente](03-configmap-y-secret.md)
