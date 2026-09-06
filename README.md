# TP1 — Potenciales y campos eléctricos

Informe en `tp1_lineas_equipotenciales.ipynb`. Los gráficos ya están embebidos: se puede leer sin
correr nada. Para regenerarlos: *Restart Kernel + Run All* (necesita `numpy`, `matplotlib`,
`scipy`).

## Estructura

1. **Objetivo**
2. **Introducción y marco teórico** — campo, potencial, `E = -∇V`, equipotenciales; modelo ideal
   de cada configuración con sus ecuaciones y las gráficas ideales (2.7).
3. **Desarrollo** — materiales, procedimiento, y para cada configuración: datos → equipotenciales
   medidas → ajuste → líneas de campo → qué se ve.
4. **Comparación ideal vs. medido** (gráficos lado a lado) + discusión.
5. **Conclusiones**
6. **Bibliografía**

## Qué se agregó respecto del notebook base

- Teoría completa (2.1–2.6) con las ecuaciones de las equipotenciales ideales:
  rectangular `x = 2·V`, polar `θ = (π/2 / 10)·V`.
- Gráficas del modelo ideal (`modelo_ideal_rectangular`, `modelo_ideal_polar`).
- **Configuración 2 (láminas a 90°)** completa: análisis polar con vértice en `(25,15)`,
  cambio de coordenadas `x' = 25-x, y' = 15-y` para dejar el origen abajo-izquierda,
  ajuste `V(θ)` y reconstrucción de líneas de campo.
- Comparación ideal vs. medido para las dos configuraciones + desvío medio por equipotencial
  (en cm y en grados).
- Reconstrucción del campo (`E = -∇V` numérico) con `streamplot`.
- Texto reescrito en tono relajado.

## Resultados

| | Pendiente medida | Ideal | Desvío |
|---|---|---|---|
| Config 1 (`dV/dx`) | 0,40 V/cm | 0,50 V/cm | −20 % |
| Config 2 (`dV/dθ`) | 5,97 V/rad | 6,37 V/rad | −6 % |

La diferencia se atribuye a la caída de tensión en el contacto lámina–agua.

## Pendiente

- Pegar las **fotos del montaje** en la sección 3.1 (hay un placeholder).
