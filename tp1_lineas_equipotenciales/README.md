# TP1 — Potenciales y campos eléctricos

Informe en `tp1_lineas_equipotenciales.ipynb`. Los gráficos ya están embebidos: se puede leer sin
correr nada. Para regenerarlos: *Restart Kernel + Run All* (necesita `numpy`, `matplotlib`,
`scipy`).

## Estructura

1. **Objetivo**
2. **Introducción y marco teórico** — campo, potencial, `E = -∇V`, equipotenciales; modelo ideal
   de cada configuración con sus ecuaciones y las gráficas ideales (2.7).
3. **Desarrollo** — materiales, procedimiento, y para cada configuración: datos → equipotenciales
   medidas → ajuste → qué se ve (incluye cómo tienen que ser las líneas de campo, deducidas de
   las equipotenciales por perpendicularidad, sin reconstrucción numérica).
4. **Comparación ideal vs. medido** (gráficos lado a lado).
5. **Conclusiones** (incluye la discusión de cada configuración y la comparación entre ambas)
6. **Bibliografía y herramientas** (incluye declaración de uso de IA)

## Qué se agregó respecto del notebook base

- Teoría completa (2.1–2.6) con las ecuaciones de las equipotenciales ideales:
  rectangular `x = 2·V`, polar `θ = (π/2 / 10)·V`.
- Gráficas del modelo ideal (`modelo_ideal_rectangular`, `modelo_ideal_polar`).
- **Configuración 2 (láminas a 90°)** completa: análisis polar con vértice en `(25,15)`,
  cambio de coordenadas `x' = 25-x, y' = 15-y` para dejar el origen abajo-izquierda, y
  ajuste `V(θ)`.
- Comparación ideal vs. medido para las dos configuraciones + desvío medio por equipotencial
  (en cm y en grados).
- Fotos del montaje (`materiales.jpg`, `paralela.jpeg`, `polar.jpeg`).
- Texto reescrito en tono relajado.

**Sacado:** la reconstrucción numérica del campo (`griddata` + `streamplot`) que había en 3.3.4 y
3.4.4. Con puntos solo sobre 6 equipotenciales (no una grilla), interpolar el campo en todo el
plano era inferir más de lo que midamos. Ahora las líneas de campo se describen de forma
cualitativa: perpendiculares a las equipotenciales medidas.

## Resultados

| | Pendiente medida | Ideal | Desvío |
|---|---|---|---|
| Config 1 (`dV/dx`) | 0,40 V/cm | 0,50 V/cm | −20 % |
| Config 2 (`dV/dθ`) | 5,97 V/rad | 6,37 V/rad | −6 % |

La diferencia se atribuye a la caída de tensión en el contacto lámina–agua.

## Pendiente

- Nada por ahora — fotos ya puestas, sección de campo revisada.
