# TP2 — Capacitores

Informe en `tp2_capacitores.ipynb`. Los gráficos y las fotos ya están embebidos en el notebook
(se puede leer sin correr nada; el esquema de la Introducción es un SVG dibujado inline, no
depende de ninguna imagen externa). Para regenerar los gráficos: *Restart Kernel + Run All*
(necesita `numpy`, `matplotlib`).

`tp2_capacitores_ENTREGA.ipynb` es una copia para mandar por mail. A diferencia del TP1, acá no
hizo falta convertir nada: todas las fotos ya viven como adjuntos nativos de Jupyter dentro del
propio `.ipynb` (no como archivos sueltos en una carpeta aparte), así que el archivo de trabajo ya
es autocontenido — la copia es solo para mantener la misma convención de nombres que el TP1.

## Objetivo

Armar capacitores de placas paralelas con distintas separaciones entre placas, medir su
capacidad y, a partir de eso, determinar la constante dieléctrica ($k$) y la susceptibilidad
dieléctrica ($X_e$) de los materiales usados como separador.

## Estructura

1. **Objetivo**
2. **Materiales y montaje**
3. **Introducción** — qué es un capacitor, de dónde sale $C=\dfrac{\varepsilon_0\,k\,A}{d}$
4. **Procedimiento experimental** — 3 configuraciones de capacitor de placas paralelas (20×20 cm),
   cambiando el material/separación entre placas
5. **Mediciones y resultados** — para cada una de las 3 configuraciones: tabla de 5 mediciones
   ($C$ vs. $d$), gráfico de $C$ contra $1/d$ con ajuste lineal, y el cálculo de $k$ y $X_e$ a
   partir de la pendiente de esa recta
6. **Conclusiones** (compara las 3 configuraciones y discute fuentes de error)

## Qué se agregó respecto de la versión anterior

- **Materiales y montaje** completo (antes decía `_COMPLETAR_` con una lista placeholder).
- **Configuración 1** (acrílico en las esquinas + aire): cálculo de $k$ y $X_e$ a partir de la
  pendiente, que antes quedaba sin cerrar. Da $k=(1{,}06\pm0{,}01)$, bastante más cerca del aire
  que del acrílico puro — tiene sentido porque el acrílico solo ocupa una fracción chica del área
  entre placas. Es la única configuración de la que tenemos fotos (F, F+B, F+C, F+E), por eso va
  primera en el orden de presentación.
- El esquema de un capacitor en la Introducción pasó de una imagen linkeada a un sitio externo
  (que podía romperse) a un SVG dibujado inline, así no depende de internet.
- **Conclusiones** reescritas para comparar las 3 configuraciones (no solo vidrio y acrílico) y
  para discutir las fuentes de error del experimento.

## Configuraciones medidas

| Configuración | Separador entre placas | $k$ | $X_e$ |
|---|---|---:|---:|
| 1 | Acrílico en las esquinas + aire | $1{,}06\pm0{,}01$ | $0{,}06\pm0{,}01$ |
| 2 | Vidrio (distintos espesores) | $4\pm0{,}2$ | $3{,}0\pm0{,}2$ |
| 3 | Acrílico (distintos espesores) | $2\pm0{,}1$ | $1{,}0\pm0{,}1$ |

## Pendiente

- Nada por ahora.
