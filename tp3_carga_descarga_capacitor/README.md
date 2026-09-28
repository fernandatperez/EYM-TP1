# TP3 — Carga y descarga de un capacitor

Informe en `tp3_carga_descarga_capacitor.ipynb`. Los gráficos y las salidas ya están embebidos
en el notebook (se puede leer sin correr nada). Para regenerar todo: *Restart Kernel + Run All*
(necesita `numpy`, `matplotlib`, `scipy`, y el archivo `datos/DS0000.CSV`).

## Objetivo

Antes de la instancia de medición, la cátedra pidió una muestra teórica del comportamiento de
carga y descarga de un capacitor $C$ en serie con una resistencia $R$: calcular la constante de
tiempo $\tau = RC$, graficar $V_C(t)$ e $I(t)$ esperadas, y usarlas como referencia para configurar
el generador de funciones y el osciloscopio. Después se incorporó la medición real hecha con el
osciloscopio y se comparó contra la curva teórica.

## Estructura

1. **Objetivo**
2. **Introducción teórica** — circuito RC, ecuaciones de carga y descarga, la regla de $5\tau$
3. **Elección de los parámetros** — $R$, $C$ y $V_0$ usados, y la potencia que disipa $R$
4. **Construcción de las curvas teóricas** — $V_C(t)$ e $I(t)$ esperadas, a la frecuencia real
   usada en la medición (200 Hz)
5. **Análisis** (de la muestra teórica)
6. **Mediciones con el osciloscopio**
   - 6.1. Constante de tiempo medida
   - 6.2. Comparación con la curva teórica
   - 6.3. Señal completa: medición vs. muestra teórica a 200 Hz
   - 6.4. Frecuencia del generador: criterio de diseño vs. usada
   - 6.5. Análisis de las mediciones
7. **Conclusiones** (compara $\tau$ teórico vs. medido, discute la causa probable de la
   diferencia, y cierra la justificación de usar 200 Hz en vez del criterio de $5\tau$)

## Parámetros del circuito

| | Valor |
|---|---:|
| $R$ | $150\,\Omega$ |
| $C$ | $2\,\mu F$ |
| $V_0$ | $5\,V$ |
| Frecuencia del generador | $200\,Hz$ |
| $\tau$ teórico ($RC$) | $0{,}30\,ms$ |
| $\tau$ medido (osciloscopio) | $0{,}40\,ms$ |

## Resultado principal

El $\tau$ medido es un 35 % mayor que el teórico, de forma consistente en los 6 flancos
capturados. Una causa probable (a confirmar con el equipo) es la resistencia de salida del
generador de funciones ($\approx 50\,\Omega$ en serie con $R$): con $R_{tot}=200\,\Omega$ el
$\tau$ teórico pasa a ser $0{,}40\,ms$, que coincide con lo medido.

## Pendiente

- Confirmar la causa de la diferencia de $\tau$ midiendo $R$ y $C$ con instrumentos, y
  verificando la impedancia de salida real del generador.
- Confirmar la amplitud configurada en el generador y el factor de atenuación de la sonda: la
  señal medida tiene ~2,6 V pico a pico, no los $5\,V$ de la muestra teórica, y no debería afectar
  a $\tau$ pero sí a cualquier comparación de niveles de tensión.
