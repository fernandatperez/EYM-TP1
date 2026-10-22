# TP4 — Campo magnético

Informe en `tp4_campo_magnetico.ipynb`.

## Estructura

1. **Objetivo**
2. **Materiales y montaje** — dos bobinas de $N=200$ vueltas, radio 12 cm, separadas 12 cm
   (Helmholtz), fuente de corriente continua, amperímetro y brújula común de laboratorio
3. **Introducción teórica** — ley de Biot-Savart, regla de la mano derecha, principio de
   superposición, campo de un cable infinito, campo sobre el eje de una espira circular
   (con gráfico de la curva de campana resultante), qué pasa al sumar dos espiras coaxiales
   separadas una distancia l (gráfico de la "M" que forma la superposición de los dos campos),
   una comparación de 6 separaciones l/d en un mismo gráfico para mostrar cuándo aparece esa
   M y cuándo no, y la explicación de las bobinas de Helmholtz (por qué $l=d$ da una región de
   campo uniforme, con gráfico de zoom comparando $l=0,8d$, $1d$ y $1,2d$)
4. **Procedimiento experimental** — determinación del campo magnético terrestre con una
   brújula en el centro de bobinas de Helmholtz, por el método de los 45° (la corriente con la
   que la aguja marca 45° da $B_H = B_T$, entonces $B_T = k\,I_{45}$), con diagrama de la suma
   vectorial, pasos de la medición y muestra teórica de la corriente esperada
5. **Mediciones y resultados** — corriente $I_{45}$ medida y cálculo de $B_T$ con su error
   (corriente, lectura del ángulo y radio de las bobinas), y comparación con el modelo WMM
6. **Conclusiones**

## Resultados

- Medición: $I_{45} = 12,15\,mA$, que da $B_T = (18,2 \pm 0,7)\,\mu T$.
- Referencia del modelo WMM2025 en la UNSAM el 22/10/2026: componente horizontal $16,92\,\mu T$
  (calculada con el paquete `pygeomag`, que implementa los coeficientes oficiales del WMM).
  Diferencia: $+7,6\%$.

## Notas

- La foto `imagenes/pizarron_espira.jpeg` (pizarrón con la derivación) es solo una referencia de
  trabajo, no se usa en el notebook. La figura que sí se usa, embebida en la Introducción
  teórica, es `imagenes/campo.jpeg` (diagrama de la espira con $\theta$, $\vec{r}$ y $d\vec{B}$
  descompuesto en $dB_x$ y $dB_y$).
