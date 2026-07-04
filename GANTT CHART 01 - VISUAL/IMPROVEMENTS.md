# Mejoras Priorizadas - Gantt Chart 01 Visual

Este documento resume la auditoria del visual como producto reutilizable para Power BI + Deneb + Vega.

## Diagnostico Rapido

El visual tiene una base fuerte para Project Controls: dependencias, fases colapsables, avance, prioridades, hitos y navegacion temporal. Es el visual mas orientado al usuario operativo o analista que necesita detalle de cronograma.

## Audiencias Validadas

| Perfil | Valor principal | Ajuste recomendado |
|---|---|---|
| Usuario ejecutivo | Lectura de avance, hitos y prioridades. | Reducir columnas visibles por defecto y reforzar resumen superior. |
| Analista Power BI | Spec reutilizable y configurable. | Documentar campos exactos, aliases y signals clave. |
| Gerente de proyecto | Seguimiento de tareas y dependencias. | Mejorar tooltips con responsable, variacion y predecesoras. |

## Mejoras Prioridad Alta

1. Corregir el dataset `Datos_Gantt.xlsx` para que `inicio` y `fin` sean fechas reales, no texto.
2. Corregir caracteres con encoding roto en el Excel, por ejemplo textos como `Planificaci�n` o `mi�rcoles`.
3. Documentar en el README los campos alternativos que el JSON reconoce: `planificado`, `avance_planificado` y `porc_planificado`.
4. Agregar una seccion de validacion del dataset antes de pegar el JSON en Deneb.
5. Incluir una captura en el README del visual para que el usuario vea el resultado esperado sin abrir Power BI.

## Mejoras Prioridad Media

1. Crear una version ejecutiva con menos columnas visibles por defecto.
2. Separar parametros configurables por categoria: navegacion, columnas, colores, filas y tooltips.
3. Agregar notas de personalizacion para colores corporativos.
4. Estandarizar nombres de archivo para futuras versiones, por ejemplo `gantt_visual_1_0_spec.json`.
5. Agregar ejemplos de valores validos para `prioridad`, `estado` y `hito`.

## Mejoras Prioridad Baja

1. Crear una mini guia de troubleshooting para errores comunes en Deneb.
2. Agregar release notes por version.
3. Crear una version demo con menor cantidad de campos para usuarios nuevos.

## Recomendaciones Para El JSON

- Mantener schema Vega v5, ya que el archivo actual declara `https://vega.github.io/schema/vega/v5.json`.
- Revisar tooltips para mostrar fechas con formato consistente.
- Centralizar paletas de estado y prioridad para facilitar personalizacion.
- Documentar signals mas usados en una tabla corta para evitar abrumar al usuario.
- Validar que los campos calculados manejen valores nulos en `predecesoras`, `enlace` y `estado`.

## Recomendaciones Para El Dataset

- Convertir fechas a tipo fecha real en Excel.
- Usar codificacion limpia con acentos correctos.
- Agregar columnas `estado`, `proyecto` y `avance_planificado` si se quieren explotar todas las capacidades del spec.
- Mantener `avance` en escala 0 a 100.
- Usar IDs unicos y predecesoras existentes.

## Checklist De Siguiente Iteracion

- [ ] Limpiar `Datos_Gantt.xlsx`.
- [ ] Validar el visual en Deneb despues de limpiar datos.
- [ ] Actualizar screenshot si cambia el resultado visual.
- [ ] Documentar signals clave en README.
- [ ] Preparar release `gantt-visual-1.1`.
