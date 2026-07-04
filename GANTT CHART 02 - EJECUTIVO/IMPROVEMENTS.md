# Mejoras Priorizadas - Gantt Chart 02 Ejecutivo

Este documento resume la auditoria del visual como producto reutilizable para Power BI + Deneb + Vega.

## Diagnostico Rapido

El visual tiene una propuesta clara para comites, PMO y direccion: prioriza lectura ejecutiva, ruta critica, estados, avance y desviaciones. Su mayor oportunidad esta en cerrar brechas de reutilizacion: dataset de ejemplo funcional, compatibilidad documentada y consistencia entre README y JSON.

## Audiencias Validadas

| Perfil | Valor principal | Ajuste recomendado |
|---|---|---|
| Usuario ejecutivo | Vista limpia de avance, ruta critica y prioridades. | Mantener pocas columnas visibles y reforzar indicadores criticos. |
| Analista Power BI | Reutilizacion del JSON en nuevos modelos. | Proveer dataset funcional y documentar schema real. |
| Gerente de proyecto | Seguimiento rapido de tareas en riesgo. | Destacar retrasos, criticidad y responsables en tooltips. |

## Mejoras Prioridad Alta

1. Rehacer `Gantt_Demo_Table.xlsx`, porque actualmente aparece sin filas ni columnas detectables.
2. Validar el schema del JSON: el archivo declara `https://vega.github.io/schema/vega/v1.json`, mientras el README menciona Vega v5.
3. Documentar campos requeridos para ruta critica: `ruta_critica`, `estado`, `avance_planificado` y `prioridad`.
4. Agregar validaciones de dataset para evitar que el visual quede en blanco.
5. Alinear README, JSON y archivo Excel para que usen los mismos nombres de columnas.

## Mejoras Prioridad Media

1. Agregar indicadores ejecutivos sugeridos: tareas criticas abiertas, avance promedio, desviacion promedio y proximos hitos.
2. Mejorar tooltip con responsable, estado, avance real, avance planificado y desviacion.
3. Crear una paleta ejecutiva por estado: completado, en ejecucion, retrasado, critico y vigilancia.
4. Agregar una seccion de troubleshooting para cuando Deneb no renderiza datos.
5. Estandarizar nombres de archivo para futuras versiones, por ejemplo `gantt_ejecutivo_1_0_spec.json`.

## Mejoras Prioridad Baja

1. Crear una version compacta para slides o comites de alta direccion.
2. Agregar una ficha de benchmark frente al Gantt operativo.
3. Preparar release notes por version.

## Recomendaciones Para El JSON

- Validar si el spec debe migrarse formalmente a Vega v5.
- Revisar campos calculados relacionados con criticidad y desviacion.
- Documentar los signals ejecutivos y ocultar detalles avanzados en una seccion secundaria.
- Mantener un modo inicial orientado a `All` para comites, con opcion de zoom temporal.
- Asegurar que nulos en `ruta_critica`, `estado` o `avance_planificado` no rompan el render.

## Recomendaciones Para El Dataset

- Crear datos de ejemplo reales con al menos 12 a 20 tareas.
- Usar fechas reales y no texto.
- Incluir casos de prueba para tareas completadas, retrasadas, criticas y en vigilancia.
- Incluir hitos, dependencias y responsables.
- Mantener `avance` y `avance_planificado` en escala 0 a 100.

## Checklist De Siguiente Iteracion

- [ ] Reconstruir `Gantt_Demo_Table.xlsx`.
- [ ] Validar schema Vega real en Deneb.
- [ ] Alinear README con JSON despues de validar schema.
- [ ] Actualizar screenshot si cambia el resultado visual.
- [ ] Preparar release `gantt-ejecutivo-1.1`.
