# Auditoria JSON - Gantt Chart 01 Visual

## Diagnostico Del JSON

El spec actual es una base robusta en Vega v5 para Deneb. Contiene 64 signals, 17 datasets internos, 14 capas de marcas, 7 escalas y 3 ejes. La arquitectura ya cubre navegacion, fases, tareas, dependencias, hitos, avance y prioridades.

## Fortalezas

- Schema declarado como Vega v5.
- Separacion clara entre datos de entrada, fases, tareas, hitos y dependencias.
- Signals configurables para columnas, zoom, filas y tooltips.
- Paleta de prioridades centralizada en `statusColumn`.
- Soporte para varios nombres de avance planificado: `planificado`, `avance_planificado` y `porc_planificado`.

## Riesgos Detectados

- El dataset de ejemplo debe limpiarse: fechas como texto y caracteres con encoding roto.
- Hay muchos signals; conviene documentar solo los mas utiles para usuarios finales.
- Campos opcionales como `estado`, `enlace`, `proyecto` y `predecesoras` deben manejarse con datos consistentes.
- Si el usuario cambia nombres de columnas, los transforms pueden dejar el visual en blanco.

## Version Optimizada Generada

Archivo creado: [Gantt 1.1 Optimized Spec.json](Gantt%201.1%20Optimized%20Spec.json)

Cambios aplicados en la version optimizada:

- Conserva la logica visual original.
- Mantiene schema Vega v5.
- Mejora la descripcion del spec.
- Agrega `usermeta` con nombre, version, autor, campos esperados y notas de compatibilidad.
- Deja documentado que el alcance de la optimizacion es metadatos, mantenimiento y reutilizacion.

## Campos Relevantes

| Campo | Uso |
|---|---|
| `id` | Identificador unico. |
| `fase` | Agrupador o fase. |
| `tarea` | Nombre de actividad. |
| `inicio` | Fecha de inicio. |
| `fin` | Fecha de termino. |
| `avance` | Avance real. |
| `planificado`, `avance_planificado`, `porc_planificado` | Avance planificado segun modelo. |
| `predecesoras` | Dependencias. |
| `prioridad` | Colores de prioridad. |
| `estado` | Estado operativo opcional. |
| `responsable` | Responsable de actividad. |

## Signals Recomendados Para Documentar

| Signal | Uso |
|---|---|
| `showTooltips` | Activa o desactiva tooltips. |
| `startGrain` | Vista temporal inicial. |
| `initDate` | Fecha inicial del dominio temporal. |
| `initPhaseState` | Estado inicial de fases. |
| `initColumnState` | Estado inicial de columnas. |
| `yRowHeight` | Altura de filas. |
| `taskColumnWidth` | Ancho de columna de tarea. |
| `statusColumn` | Paleta y etiquetas de prioridad. |

## Recomendaciones Para Siguiente Iteracion

1. Limpiar `Datos_Gantt.xlsx` antes de promover la version optimizada.
2. Probar `Gantt 1.1 Optimized Spec.json` en Deneb.
3. Si funciona igual que 1.0, reemplazar el JSON principal en una release formal.
4. Documentar una tabla corta de personalizacion para usuarios no tecnicos.
5. Agregar una seccion de troubleshooting para visual en blanco.
