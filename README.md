# PowerBI-Walter

Visuales personalizados para **Power BI** desarrollados con **Deneb**, **Vega** y **Vega-Lite**, orientados a dashboards ejecutivos, Project Controls, PMO, construccion, infraestructura y seguimiento de cronogramas.

Este repositorio funciona como una galeria practica de visuales reutilizables: cada visual incluye archivo `.pbix`, especificacion JSON, datos de ejemplo, imagen de referencia y documentacion de uso. Para una vista mas estructurada, consulta el [Catalogo de Visuales](VISUAL_CATALOG.md).

## Visuales Disponibles

| Visual | Enfoque | Archivos | Vista previa |
|---|---|---|---|
| [Gantt Chart 01 - Visual](GANTT%20CHART%2001%20-%20VISUAL/) | Cronograma avanzado con dependencias, fases, avance y navegacion dinamica. | `.pbix`, `.json`, `.xlsx`, `README.md` | ![Gantt Visual 1.0](GANTT%20CHART%2001%20-%20VISUAL/Gantt%20Visual%201.0%20Thumbnail.png) |
| [Gantt Chart 02 - Ejecutivo](GANTT%20CHART%2002%20-%20EJECUTIVO/) | Cronograma ejecutivo para comites, PMO y toma de decisiones. | `.pbix`, `.json`, `.xlsx`, `README.md` | ![Gantt Ejecutivo 1.0](GANTT%20CHART%2002%20-%20EJECUTIVO/Gantt%20Ejecutivo%201.0%20Thumbnail.png) |

## Objetivo

El objetivo de **PowerBI-Walter** es acelerar la creacion de visuales profesionales en Power BI para proyectos reales, especialmente cuando los visuales nativos no son suficientes para representar cronogramas, avance, prioridades, hitos, responsables y dependencias.

Estos visuales estan pensados para:

- Seguimiento ejecutivo de proyectos.
- Dashboards de construccion e infraestructura.
- Project Controls y PMO.
- Cronogramas de alto nivel para comites.
- Analisis de avance real vs planificado.
- Presentacion de tareas criticas, estados y prioridades.

## Requisitos

Para usar los visuales necesitas:

- Power BI Desktop.
- Visual **Deneb** instalado desde AppSource.
- Conocimientos basicos de carga de datos en Power BI.
- Archivo JSON del visual que quieras reutilizar.
- Dataset con las columnas esperadas por cada visual.

## Uso Rapido

1. Abre Power BI Desktop.
2. Instala o agrega el visual **Deneb**.
3. Carga el archivo Excel de ejemplo del visual.
4. Agrega un visual Deneb al reporte.
5. Crea una nueva especificacion en modo **Vega** o **Vega-Lite**, segun indique el README del visual.
6. Copia el contenido del archivo `.json`.
7. Pega la especificacion en Deneb.
8. Asigna los campos del dataset al visual.
9. Ajusta colores, textos, columnas o parametros segun tu caso de uso.

## Estructura Del Repositorio

```text
PowerBI-Walter/
|
|-- GANTT CHART 01 - VISUAL/
|   |-- Datos_Gantt.xlsx
|   |-- Gantt 1.0 Spec.json
|   |-- Gantt Visual 1.0 Thumbnail.png
|   |-- Gantt Visual 1.0.pbix
|   `-- README.md
|
|-- GANTT CHART 02 - EJECUTIVO/
|   |-- Gantt Ejecutivo 1.0 Spec.json
|   |-- Gantt Ejecutivo 1.0 Thumbnail.png
|   |-- Gantt Ejecutivo 1.0.pbix
|   |-- Gantt_Demo_Table.xlsx
|   `-- README.md
|
|-- templates/
|   |-- dataset-schema.md
|   |-- publish-checklist.md
|   `-- visual-readme-template.md
|
|-- VISUAL_CATALOG.md
|-- LICENSE
`-- README.md
```

## Comparativa De Visuales

| Caracteristica | Gantt Chart 01 - Visual | Gantt Chart 02 - Ejecutivo |
|---|---:|---:|
| Cronograma por tareas | Si | Si |
| Fases o agrupadores | Si | Si |
| Dependencias visuales | Si | Si |
| Hitos | Si | Si |
| Avance real | Si | Si |
| Avance planificado | Si | Si |
| Prioridades | Si | Si |
| Ruta critica | No documentada | Si |
| Enfoque operativo | Alto | Medio |
| Enfoque ejecutivo | Medio | Alto |

## Columnas Base Recomendadas

Cada visual puede tener campos especificos, pero la estructura base recomendada es:

| Columna | Descripcion |
|---|---|
| `id` | Identificador unico de la tarea. |
| `fase` | Fase, paquete de trabajo o agrupador. |
| `tarea` | Nombre de la actividad. |
| `hito` | Indicador para marcar hitos. |
| `inicio` | Fecha de inicio. |
| `fin` | Fecha de termino. |
| `avance` | Porcentaje de avance real. |
| `avance_planificado` o `planificado` | Porcentaje de avance planificado. |
| `predecesoras` | IDs de tareas predecesoras separados por coma. |
| `responsable` | Persona, area o contratista responsable. |
| `prioridad` | Baja, Media, Alta o Muy Alta. |
| `estado` | Estado operativo de la tarea. |
| `enlace` | Hipervinculo opcional. |
| `proyecto` | Nombre del proyecto. |

## Recursos Para Nuevos Visuales

| Recurso | Uso |
|---|---|
| [Catalogo de visuales](VISUAL_CATALOG.md) | Organiza los visuales por categoria, audiencia, nivel y caso de uso. |
| [Plantilla README](templates/visual-readme-template.md) | Estandar para documentar cada nuevo visual. |
| [Plantilla de dataset](templates/dataset-schema.md) | Campos, tipos y validaciones recomendadas para datos de ejemplo. |
| [Checklist de publicacion](templates/publish-checklist.md) | Control de calidad antes de publicar o promocionar un visual. |

## Nota Sobre Archivos Excel Fuente

Los archivos `.xlsx` incluidos en cada carpeta son fuentes asociadas a los reportes `.pbix`. Aunque una inspeccion externa pueda mostrar tipos, hojas o vistas diferentes, la referencia valida es el comportamiento dentro de Power BI y Power Query.

No renombres columnas, no cambies tipos de datos y no reemplaces estos Excel sin validar primero el impacto en el `.pbix`. Si se necesita un dataset didactico adicional para publicar ejemplos independientes, conviene crearlo como copia nueva y no sustituir la fuente actual.
## Buenas Practicas

- Mantener IDs unicos y estables.
- Mantener los archivos Excel fuente alineados con el modelo Power BI; no modificar tipos o columnas si el `.pbix` ya depende de ellos.
- Evitar nombres de columnas duplicados o inconsistentes.
- Mantener valores de prioridad estandarizados.
- Validar el JSON dentro de Deneb despues de cada ajuste.
- Documentar cualquier cambio relevante en el README del visual.
- Usar datos de ejemplo limpios para facilitar la reutilizacion.

## Roadmap

- Mejorar datasets de ejemplo con fechas tipadas y acentos corregidos.
- Validar compatibilidad exacta de cada spec con Deneb y Vega.
- Agregar una plantilla estandar para nuevos visuales.
- Crear mas visuales para Project Controls, avance fisico-financiero, curva S y riesgos.
- Publicar versiones/release notes por cada visual.

## Creditos

Desarrollo y personalizacion:

**Ing. Walter Ivan Guerrero**

Especialista en Project Management, Project Controls, Power BI, automatizacion, IA aplicada y dashboards ejecutivos.

LinkedIn: [www.linkedin.com/in/ing-walterguerrero](https://www.linkedin.com/in/ing-walterguerrero)

Algunos visuales toman como base e inspiracion propuestas de la comunidad Deneb/Vega para Power BI, con agradecimiento especial a **Davide Bacci** por su trabajo original en visuales Gantt avanzados.

## Licencia

Consulta el archivo [LICENSE](LICENSE) para conocer los terminos de uso del repositorio.





