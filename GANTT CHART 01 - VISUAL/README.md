# Gantt 1.0 Spec — Power BI + Deneb + Vega

Visual avanzado de cronograma desarrollado en **Deneb + Vega para Power BI**, orientado a proyectos de construcción, infraestructura, EPC y Project Controls.

---

## Vista General

Este visual fue diseñado para transformar el Gantt tradicional en una herramienta real de análisis y toma de decisiones ejecutivas.

Incluye navegación dinámica, dependencias visuales, agrupadores colapsables, prioridades, hitos y seguimiento de avance orientado a PMO y Project Controls.

---

## Reconocimiento y Base de Desarrollo

Este visual ha sido desarrollado tomando como base e inspiración la propuesta original de Gantt creada por **Davide Bacci** para **Deneb + Vega en Power BI**.

A partir de dicha propuesta, se realizaron múltiples personalizaciones, mejoras funcionales y ajustes visuales orientados específicamente a:

- Gestión de proyectos de construcción
- Project Controls
- PMO
- Dashboards ejecutivos
- Seguimiento de avance físico y financiero
- Experiencia visual para comités de proyecto

### Mejoras incorporadas

- Agrupadores en escala de grises
- Prioridades con mayor contraste visual
- Hover optimizado
- Mejoras en navegación
- Compatibilidad con estructuras complejas
- Mejor lectura ejecutiva
- Optimización visual para construcción e infraestructura

Se reconoce y agradece el trabajo original de **Davide Bacci** como punto de partida técnico para esta evolución personalizada del visual.

---

## Features

### Navegación

- Zoom dinámico con rueda del mouse
- Escala automática:
  - Días
  - Meses
  - Años
  - Proyecto completo
- Botones rápidos de navegación
- Doble clic para reiniciar vista
- Paneo horizontal y vertical

---

### Gestión Visual

- Expandir/contraer fases
- Expandir/contraer todas las filas
- Columnas colapsables
- Agrupadores visuales optimizados
- Autoescalado del visual

---

### Dependencias

- Soporte para múltiples dependencias
- Resaltado automático de relaciones
- Visualización dinámica de secuencias

---

### Avance

- Barras de avance integradas
- Avance real vs planificado
- Variación de avance
- Priorización visual:
  - Baja
  - Media
  - Alta
  - Muy Alta

---

### Experiencia Ejecutiva

- Hover inteligente
- Tooltips dinámicos
- Diseño optimizado para PMO
- Visual ejecutivo para comité

---

## Tecnologías Utilizadas

- Power BI
- Deneb
- Vega v5
- JSON Specification

---

## Instalación

### 1. Instalar Deneb

Instalar el visual **Deneb** desde AppSource en Power BI.

---

### 2. Crear visual Deneb

Agregar el visual Deneb al reporte de Power BI.

---

### 3. Crear especificación Vega

Dentro de Deneb:

- New Specification
- Vega

---

### 4. Pegar el archivo JSON

Copiar el contenido de:

```bash
Gantt 1.0 Spec.json
```

y pegarlo dentro del editor Deneb.

---

## Estructura de Datos

La tabla debe contener la siguiente estructura:

| Columna | Tipo | Descripción |
|---|---|---|
| id | Texto/Número | Identificador único |
| fase | Texto | Nombre de fase |
| tarea | Texto | Nombre de tarea |
| hito | Boolean | Define si es hito |
| inicio | Fecha | Fecha inicio |
| fin | Fecha | Fecha fin |
| avance | Número | % avance real |
| planificado | Número | % avance planificado |
| predecesoras | Texto | IDs separados por coma |
| responsable | Texto | Responsable |
| prioridad | Texto | Baja / Media / Alta / Muy Alta |
| estado | Texto | Estado operativo |
| enlace | Texto | Hipervínculo opcional |
| proyecto | Texto | Nombre proyecto |

---

## Configuración

### Signals Configurables

| Signal | Descripción |
|---|---|
| showTooltips | Activar/desactivar tooltips |
| initDate | Fecha inicial del visual |
| showButtons | Mostrar botones |
| showDomainSpanLabel | Mostrar rango temporal |
| startGrain | Escala inicial |
| initPhaseState | Estado inicial de filas |
| initColumnState | Estado inicial columnas |
| textColour | Color principal texto |
| colours | Paleta de colores |
| statusColumn | Configuración prioridades |
| yRowHeight | Altura filas |
| yRowPadding | Padding filas |
| taskColumnWidth | Ancho columna tarea |
| startColumnWidth | Ancho fecha inicio |
| endColumnWidth | Ancho fecha fin |
| statusColumnWidth | Ancho prioridad |
| daysColumnWidth | Ancho duración |
| progressColumnWidth | Ancho avance |
| columnPadding | Espaciado columnas |

---

## Mejoras de Esta Versión

### Agrupadores Ejecutivos

Los agrupadores fueron ajustados a escala de grises para:

- Reducir competencia visual
- Mejorar lectura de tareas
- Resaltar hitos y actividades críticas

---

### Prioridades Mejoradas

Se incrementó el contraste visual de prioridades para facilitar lectura en:

- Dashboards ejecutivos
- Comités
- PMO
- Seguimiento de obra

---

### Hover Optimizado

- Mejor navegación visual
- Mejor lectura de relaciones
- Resaltado limpio de filas y tareas

---

## Casos de Uso

Ideal para:

- EPC
- Construcción
- Líneas de transmisión
- Subestaciones
- Infraestructura
- PMO
- Project Controls
- Valor Ganado
- Curva S
- Seguimiento ejecutivo

---

## Buenas Prácticas

- Mantener IDs únicos
- No usar jerarquías en fechas
- Mantener formatos consistentes
- Evitar exceso de dependencias

---

## Estructura Recomendada del Repositorio

```bash
Gantt-1.0-Spec/
│
├── README.md
├── Gantt 1.0 Spec.json
└── sample-data/
    └── ejemplo_gantt.xlsx
```

---

## Créditos

### Desarrollo y Personalización

**Ing. Walter Iván Guerrero**

Especialista en:

- Project Management
- Project Controls
- Power BI
- IA aplicada
- Automatización
- Dashboards ejecutivos

LinkedIn:

https://www.linkedin.com/in/ing-walterguerrero
