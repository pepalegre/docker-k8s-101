# Criterios de entrega

## Requisitos obligatorios

- **Continuidad con el modulo 4**: en el README del `proyecto-final` debe quedar explicito que partes del laboratorio 4 (rutas o descripcion de lo heredado).
- **Arbol Kustomize funcional**: `k8s/base` + **dos overlays** distintos bajo `k8s/overlays/` (por ejemplo `local` y `demo`). Ambos deben construir sin error.
- **Sustitucion o fijacion de imagenes** coherente con Kustomize (`images:` o tags ya consistentes en YAML, pero debe haber **una** historia clara de version en el README).
- **`docs/operaciones.md`**: despliegue, validacion, job manual desde CronJob, rollback de la API, limpieza.
- **CronJob o Job** siguen siendo el proceso batch visible en cluster (heredado del lab 4, integrado en el arbol Kustomize).

## Requisitos recomendados (no bloquean, suman nota)

- Probes `liveness`/`readiness` en la API si el tiempo del curso lo permite.
- Limites de CPU/memoria en el overlay `demo` o documentados como deuda tecnica.

## Evidencias en `entregas/` (o carpeta acordada con el instructor)

- Salida de `kustomize build` para **cada** overlay (redirigida a un fichero o captura relevante).
- `kubectl get pods,svc -n <tu-namespace>` tras desplegar un overlay.
- Fragmento de logs de una ejecucion del ETL (job creado por el CronJob o manual).
- Captura o texto de la respuesta de `/health` (o endpoint de salud equivalente).
- Indicacion del **tag git** o version en README bajo la que revisar la entrega.

## LABORATORIO

- [01-heredar-y-empaquetar.md](laboratorio/01-heredar-y-empaquetar.md)

## Navegacion del libro

- [Anterior](02-versionado-kustomize-y-runbook.md)
- [Siguiente](laboratorio/01-heredar-y-empaquetar.md)
