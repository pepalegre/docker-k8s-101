# Definicion del proyecto final

## Que es (y que no es)

**Es** el cierre formal del curso: convertir lo que ya probaste en el laboratorio 4 en una **carpeta de proyecto** que otra persona pueda clonar, leer y reproducir con pasos claros.

**No es** volver a implementar desde cero la API, el ETL, el CronJob ni el pipeline a GHCR. Eso ya es el alcance del modulo 4. Si el laboratorio 4 no esta cerrado, completa primero su checklist antes de entrar aqui.

## Prerrequisito

Tener en el repo (rutas orientativas del lab 4):

- Codigo de `api` y `etl` bajo `labs/04-k8s-analitica/trabajo/apps/`.
- Manifiestos validados bajo `labs/04-k8s-analitica/trabajo/k8s-demo-manifests/`.
- Imagenes publicadas o al menos etiquetadas de forma coherente con lo que declaran los YAML (GHCR o carga en `kind` segun hayas hecho el lab).

## Objetivo del modulo 5

1. **Heredar** esos artefactos en un arbol `proyecto-final/` (sin romper el lab 4: copia, no muevas el original si prefieres conservar evidencias del modulo 4).
2. **Sustituir el conjunto de `kubectl apply -f ...` sueltos** por un arbol **Kustomize** (`base` + al menos **dos overlays** con comportamiento distinto: por ejemplo `local` para `kind` y `demo` para un perfil mas ligero o con otro numero de replicas).
3. **Documentar operacion**: como desplegar, como comprobar salud, como ejecutar un job manual desde el CronJob y como hacer **rollback** de la API.
4. **Versionar la entrega**: una etiqueta git o un numero de version en README que corresponda a las imagenes referenciadas en Kustomize.

## Estructura esperada (orientativa)

```text
proyecto-final/
  README.md                 # contexto, arquitectura en texto, enlace al lab 4
  docs/
    operaciones.md          # runbook: desplegar, validar, rollback, limpiar
  api/                      # heredado del lab 4 (copia)
  etl/                      # heredado del lab 4 (copia)
  k8s/
    base/                   # recursos comunes + kustomization.yaml
    overlays/
      local/                # kind / desarrollo (tu overlay principal)
      demo/                 # segundo entorno (parches distintos)
```

Docker Compose **no es obligatorio** en el proyecto final. Si lo incluyes, debe ser un extra claramente marcado (desarrollo local), no el nucleo de la entrega.

## Demo breve (profesor)

Mostrar un mismo `kustomize build` sobre dos overlays y la diferencia en replicas, imagenes o recursos; mostrar `docs/operaciones.md` con un rollback real sobre el Deployment de la API.

## Continuar

- [02-versionado-kustomize-y-runbook.md](02-versionado-kustomize-y-runbook.md)

## Navegacion del libro

- [Anterior](README.md)
- [Siguiente](02-versionado-kustomize-y-runbook.md)
