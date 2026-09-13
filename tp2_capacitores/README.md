# TP2 — Capacitores

Informe en `tp2_capacitores.ipynb`. Los gráficos y 2 de las 3 fotos ya están embebidos en el
notebook (se puede leer sin correr nada). Para regenerar los gráficos: *Restart Kernel + Run
All* (necesita `numpy`, `matplotlib`).

## Objetivo

Armar capacitores de placas paralelas con distintas separaciones entre placas, medir su
capacidad y, a partir de eso, determinar la constante dieléctrica ($k$) y la susceptibilidad
dieléctrica ($X_e$) de los materiales usados como separador.

## Estructura

1. **Objetivo**
2. **Materiales y montaje** *(incompleto, ver Pendiente)*
3. **Introducción** — qué es un capacitor, de dónde sale $C=\dfrac{\varepsilon_0\,k\,A}{d}$
4. **Procedimiento experimental** — 3 configuraciones de capacitor de placas paralelas (20×20 cm),
   cambiando el material/separación entre placas
5. **Mediciones y resultados** — para cada configuración: tabla de 5 mediciones ($C$ vs. $d$),
   gráfico de $C$ contra $1/d$ con ajuste lineal, y (en 2 de las 3) el cálculo de $k$ y $X_e$ a
   partir de la pendiente de esa recta
6. **Conclusiones**

## Configuraciones medidas

| Configuración | Separador entre placas | $k$ | $X_e$ |
|---|---|---:|---:|
| 1 | Vidrio (distintos espesores) | $4\pm0{,}2$ | $3{,}0\pm0{,}2$ |
| 2 | Acrílico (distintos espesores) | $2\pm0{,}1$ | $1{,}0\pm0{,}1$ |
| 3 | Acrílico en las esquinas + aire | — | — *(sin calcular, ver Pendiente)* |

## Pendiente

- **Materiales y montaje** está marcado `_COMPLETAR_`, con una lista placeholder ("Placas de
  metal, Placas de vidrio, ETC").
- La **configuración 3** (acrílico + aire) tiene su tabla de datos y su gráfico con ajuste
  lineal, pero le falta el paso siguiente que sí tienen las otras dos: calcular $k$ y $X_e$ a
  partir de la pendiente. Las conclusiones finales tampoco la mencionan (solo dan $X_e$ de
  vidrio y acrílico).
- La imagen de la Introducción (estructura de un capacitor) está linkeada a una página externa
  (`circuitoelectrico.com`) — si esa página cae, la imagen se rompe. Las otras 2 fotos del
  montaje sí están embebidas dentro del notebook (no dependen de internet).
