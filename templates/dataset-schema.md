# Plantilla De Dataset Para Visuales

Esta guia define el estandar minimo recomendado para datasets de ejemplo usados en visuales Power BI + Deneb.

## Reglas Generales

- Usar fechas reales tipadas como fecha, no texto.
- Mantener encabezados en minusculas y sin espacios.
- Usar IDs unicos y estables.
- Evitar caracteres corruptos o problemas de encoding.
- Documentar valores permitidos para campos categoricos.
- Incluir al menos 10 filas de ejemplo cuando sea posible.

## Campos Base Para Visuales De Proyecto

| Columna | Tipo recomendado | Obligatoria | Ejemplo | Notas |
|---|---|---:|---|---|
| `id` | Texto/Numero | Si | 1 | Identificador unico. |
| `proyecto` | Texto | Si | Proyecto Demo | Nombre del proyecto. |
| `fase` | Texto | Si | Ingenieria | Agrupador principal. |
| `tarea` | Texto | Si | Revision de planos | Nombre de la actividad. |
| `responsable` | Texto | Si | PMO | Persona o area responsable. |
| `inicio` | Fecha | Si | 2026-05-04 | Fecha de inicio. |
| `fin` | Fecha | Si | 2026-05-10 | Fecha de termino. |
| `avance` | Numero | Si | 75 | Porcentaje 0 a 100. |
| `avance_planificado` | Numero | No | 80 | Porcentaje 0 a 100. |
| `predecesoras` | Texto | No | 1,2 | IDs separados por coma. |
| `prioridad` | Texto | No | Alta | Baja, Media, Alta, Muy Alta. |
| `estado` | Texto | No | En ejecucion | Estado operativo. |
| `hito` | Boolean | No | FALSE | TRUE/FALSE. |
| `ruta_critica` | Boolean | No | TRUE | TRUE/FALSE. |
| `enlace` | Texto | No | https://... | Hipervinculo opcional. |

## Validaciones Recomendadas

- `inicio` no debe ser mayor que `fin`.
- `avance` debe estar entre 0 y 100.
- `avance_planificado` debe estar entre 0 y 100.
- `prioridad` debe usar valores estandarizados.
- `predecesoras` debe referenciar IDs existentes.
- Las filas hito pueden tener `inicio` igual a `fin`.
