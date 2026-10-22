# TP4 — Campo magnético

Informe en `tp4_campo_magnetico.ipynb`. Todavía en desarrollo.

## Objetivo

Determinar el campo magnético terrestre, usando un par de bobinas de Helmholtz para generar un
campo conocido y controlable, combinado con el campo terrestre en la misma región.

## Estructura

1. **Objetivo**
2. **Materiales y montaje** — par de bobinas de Helmholtz (N=200 espiras cada una, d≈0,12m,
   l=d confirmado con el armado real), fuente de tensión continua BAW HY3005D, y una brújula
   como instrumento de medición
3. **Introducción teórica** — ley de Biot-Savart, regla de la mano derecha, principio de
   superposición, campo de un cable infinito, campo sobre el eje de una espira circular
   (con gráfico de la curva de campana resultante), qué pasa al sumar dos espiras coaxiales
   separadas una distancia l (gráfico de la "M" que forma la superposición de los dos campos),
   una comparación de 6 separaciones l/d en un mismo gráfico para mostrar cuándo aparece esa
   M y cuándo no, la explicación de las bobinas de Helmholtz (por qué l=d da una región de
   campo uniforme, con gráfico de zoom comparando l=0,8d, 1d y 1,2d), la generalización a
   bobinas de N vueltas aplicada a los valores reales del armado (da B_centro = 1498,6 µT por
   cada Ampere), y el método de la brújula / galvanómetro de tangentes (por qué buscan una
   desviación de 45°: ahí B_bobina=B_tierra, sin necesidad de calcular ningún arcotangente)
4. **Procedimiento experimental** — orientar las bobinas perpendicular al campo terrestre, subir
   la corriente hasta lograr 45° de desviación en la brújula, registrar esa corriente
5. **Mediciones y resultados**
6. **Conclusiones**

## Pendiente

- **Falta el valor de la corriente $I$** medida en el laboratorio (la que logra los 45° de
  desviación) — con eso se calcula $B_{tierra}$ en la sección de Mediciones y resultados.
- **Mediciones y resultados y Conclusiones** siguen marcados `_COMPLETAR_`.
- Hay 4 fotos del equipo en `imagenes/` (`bobinas_helmholtz.jpeg`, `fuente_frente.jpeg`,
  `fuente_atras.jpeg`, `medicion_radio.jpeg`, `medicion_separacion.jpeg`) que todavía no están
  embebidas en el notebook — son material de referencia por ahora.
- La foto `imagenes/pizarron_espira.jpeg` (pizarrón con la derivación) tampoco se usa en el
  notebook. La figura que sí se usa, embebida en la Introducción teórica, es `imagenes/campo.jpeg`
  (diagrama de la espira con $\theta$, $\vec{r}$ y $d\vec{B}$ descompuesto en $dB_x$ y $dB_y$).
