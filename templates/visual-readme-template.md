# Nombre Del Visual

Resumen corto del visual: que representa, para quien esta pensado y que decision ayuda a tomar.

## Vista Del Visual

![Nombre del visual](nombre_visual_thumbnail.png)

## Ficha Tecnica

| Campo | Valor |
|---|---|
| Categoria | Gestion de proyectos / Ejecutivo / Project Controls / Riesgos / Costos |
| Audiencia | Analista Power BI / PMO / Gerencia / Comite |
| Tecnologia | Power BI + Deneb + Vega o Vega-Lite |
| Version | 1.0 |
| Archivo Power BI | `nombre_visual_1_0.pbix` |
| Spec JSON | `nombre_visual_1_0_spec.json` |
| Dataset ejemplo | `sample_data.xlsx` |

## Caso De Uso

Explica el problema que resuelve el visual y cuando conviene usarlo.

## Archivos Incluidos

| Archivo | Uso |
|---|---|
| `README.md` | Documentacion del visual. |
| `nombre_visual_1_0.pbix` | Reporte Power BI de ejemplo. |
| `nombre_visual_1_0_spec.json` | Especificacion para Deneb. |
| `nombre_visual_1_0_thumbnail.png` | Imagen de referencia. |
| `sample_data.xlsx` | Datos de ejemplo. |

## Columnas Requeridas

| Columna | Tipo | Obligatoria | Descripcion |
|---|---|---:|---|
| `id` | Texto/Numero | Si | Identificador unico. |
| `categoria` | Texto | Si | Grupo, fase o clasificacion. |
| `valor` | Numero | Si | Medida principal del visual. |
| `fecha` | Fecha | No | Fecha asociada al registro. |

## Uso Rapido

1. Abre Power BI Desktop.
2. Carga el dataset de ejemplo.
3. Agrega el visual Deneb.
4. Crea una nueva especificacion.
5. Copia y pega el JSON del visual.
6. Asigna los campos requeridos.
7. Ajusta formato, colores o parametros segun tu proyecto.

## Buenas Practicas

- Mantener nombres de columnas consistentes.
- Usar tipos de datos correctos en Power BI.
- Evitar valores nulos en campos obligatorios.
- Probar el visual con datos reales antes de publicarlo.

## Limitaciones

- Documenta aqui cualquier supuesto del visual.
- Indica campos que no deben renombrarse.
- Indica si requiere Vega o Vega-Lite.

## Creditos

Desarrollo y personalizacion: **Ing. Walter Ivan Guerrero**.
