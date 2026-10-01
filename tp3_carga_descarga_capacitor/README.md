# TP3 — Carga y descarga de un capacitor

Informe en `tp3_carga_descarga_capacitor.ipynb`. Los gráficos y las salidas ya están embebidos
en el notebook (se puede leer sin correr nada). Para regenerar todo: *Restart Kernel + Run All*
(necesita `numpy`, `matplotlib` y el archivo `datos/DS0000.CSV`).

## Objetivo

Antes de la instancia de medición, la cátedra pidió una muestra teórica del comportamiento de
carga y descarga de un capacitor $C$ en serie con una resistencia $R$: calcular la constante de
tiempo $\tau = RC$, graficar $V_C(t)$ e $I(t)$ esperadas, y usarlas como referencia para configurar
el generador de funciones y el osciloscopio. Después se incorporó la medición real hecha con el
osciloscopio y se comparó contra la curva teórica.

## Estructura

1. **Objetivo**
2. **Materiales y montaje** — equipos usados, cómo se conectó el circuito y fotos del montaje
3. **Introducción teórica** — esquema del circuito RC (con el sentido de referencia de $I$),
   ecuaciones de carga y descarga, la regla de $5\tau$
4. **Elección de los parámetros** — $R$, $C$ y $V_0$ usados, y la potencia que disipa $R$
5. **Construcción de las curvas teóricas** — $V_C(t)$ e $I(t)$ esperadas, a la frecuencia real
   usada en la medición (200 Hz)
6. **Análisis** (de la muestra teórica)
7. **Mediciones con el osciloscopio**
   - 7.1. Constante de tiempo medida
   - 7.2. Comparación con la curva teórica
   - 7.3. Señal completa: medición vs. muestra teórica a 200 Hz
   - 7.4. Frecuencia del generador: criterio de diseño vs. usada
   - 7.5. Análisis de las mediciones
8. **Conclusiones** (compara $\tau$ teórico vs. medido, explica la diferencia por la resistencia
   de salida del generador, y cierra la justificación de usar 200 Hz en vez del criterio de $5\tau$)

## Parámetros del circuito

| | Valor |
|---|---:|
| $R$ | $150\,\Omega$ |
| $C$ | $2\,\mu F$ |
| $V_0$ | $5\,V$ |
| Frecuencia del generador | $200\,Hz$ |
| $\tau$ teórico ($RC$) | $0{,}30\,ms$ |
| $\tau$ medido (osciloscopio) | $(0{,}404\pm0{,}008)\,ms$ |

## Equipos

| Equipo | Modelo |
|---|---|
| Generador de funciones | GW Instek AFG-2005 (impedancia de salida $50\,\Omega$) |
| Osciloscopio | GW Instek GDS-1102A-U |

Las fotos del montaje están en `imagenes/` y también embebidas en el notebook (sección 2).

## Resultado principal

El $\tau$ medido es un 35 % mayor que el teórico, de forma consistente en los 6 flancos
capturados. La causa es la resistencia de salida del generador de funciones: según el
fabricante, el AFG-2005 tiene $50\,\Omega$ de impedancia de salida, que quedan en serie con $R$.
Con $R_{tot}=200\,\Omega$ el $\tau$ teórico pasa a ser $0{,}40\,ms$, que coincide con lo medido.

La señal medida tiene ~2,6 V pico a pico en vez de los 5 V que entregaba el generador porque la
sonda estaba configurada en `0.5X` en el osciloscopio (2,58 V × 2 ≈ 5,2 V). No afecta a $\tau$.

## Pendiente

- Nada por ahora.
