# Catalogo De Visuales Power BI

Este catalogo organiza los visuales personalizados del repositorio **PowerBI-Walter** por categoria, audiencia y caso de uso. La idea es que cada nuevo visual tenga una ficha consistente para que cualquier usuario pueda entenderlo, probarlo y adaptarlo rapido en Power BI.

## Categorias

| Categoria | Proposito | Visuales actuales |
|---|---|---|
| Gestion de proyectos | Seguimiento de cronogramas, tareas, dependencias, fases e hitos. | Gantt Chart 01 - Visual, Gantt Chart 02 - Ejecutivo |
| Visuales ejecutivos | Lectura rapida para comites, PMO y direccion. | Gantt Chart 02 - Ejecutivo |
| Project Controls | Control de avance, prioridades, estados y desviaciones. | Gantt Chart 01 - Visual, Gantt Chart 02 - Ejecutivo |
| Planeacion y seguimiento | Monitoreo operativo de actividades por responsable, fechas y dependencias. | Gantt Chart 01 - Visual |

## Galeria

| Visual | Categoria | Audiencia | Caso de uso principal | Nivel | Carpeta |
|---|---|---|---|---|---|
| Gantt Chart 01 - Visual | Gestion de proyectos / Project Controls | Analistas Power BI, planners, project controls | Cronograma detallado con dependencias, fases, avance y navegacion dinamica. | Avanzado | [Abrir](GANTT%20CHART%2001%20-%20VISUAL/) |
| Gantt Chart 02 - Ejecutivo | Visuales ejecutivos / PMO | Gerentes de proyecto, direccion, comites ejecutivos | Cronograma ejecutivo para lectura rapida, prioridades, ruta critica y seguimiento de avance. | Avanzado | [Abrir](GANTT%20CHART%2002%20-%20EJECUTIVO/) |

## Ficha Estandar Por Visual

Cada visual publicado en este repositorio debe incluir esta informacion minima:

| Campo | Descripcion |
|---|---|
| Nombre | Nombre claro del visual y version. |
| Categoria | Gestion de proyectos, ejecutivo, riesgos, costos, avance, etc. |
| Audiencia | Usuario principal del visual. |
| Problema que resuelve | Situacion de negocio que atiende. |
| Archivos incluidos | `.pbix`, `.json`, `.xlsx`, thumbnail y README. |
| Columnas requeridas | Campos obligatorios del dataset. |
| Compatibilidad | Power BI, Deneb y Vega/Vega-Lite usados. |
| Instrucciones rapidas | Pasos para cargarlo en Power BI. |
| Casos de uso | Escenarios donde aporta valor. |
| Limitaciones | Supuestos, campos esperados o puntos a validar. |

## Estructura Recomendada Para Nuevos Visuales

```text
NOMBRE DEL VISUAL/
|
|-- README.md
|-- nombre_visual_1_0.pbix
|-- nombre_visual_1_0_spec.json
|-- nombre_visual_1_0_thumbnail.png
`-- sample_data.xlsx
```

## Criterios Para Agregar Un Nuevo Visual

- El visual debe resolver un caso de uso claro en Power BI.
- Debe incluir datos de ejemplo funcionales.
- El JSON debe pegarse y ejecutarse correctamente en Deneb.
- El README debe explicar requisitos, campos y pasos de uso.
- El thumbnail debe mostrar el visual real, no una imagen generica.
- Los nombres de columnas deben estar documentados.
- La version inicial debe estar identificada como `1.0` o equivalente.

## Roadmap De Galeria

| Prioridad | Visual sugerido | Valor esperado |
|---|---|---|
| Alta | Curva S fisica-financiera | Comparar avance planeado vs real en proyectos. |
| Alta | Matriz de riesgos ejecutiva | Comunicar criticidad, probabilidad e impacto. |
| Media | Indicadores PMO | KPIs de tiempo, costo, alcance y avance. |
| Media | Avance por contratista | Seguimiento por responsable o proveedor. |
| Baja | Timeline de hitos ejecutivos | Vista simplificada para presentaciones de comite. |
