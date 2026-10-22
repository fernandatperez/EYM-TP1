# TP4 — Campo magnético

Informe en `tp4_campo_magnetico.ipynb`. El cuerpo teórico y el resultado principal ya están
completos; falta pulir redacción y, opcionalmente, embeber las fotos del armado.

## Objetivo

Determinar el campo magnético terrestre, usando un par de bobinas de Helmholtz para generar un
campo conocido y controlable, combinado con el campo terrestre en la misma región.

## Resultado

$$B_{tierra} = 18{,}21\,\mu T$$

Obtenido con $N=200$ vueltas, $d=0,12\,m$ ($l=d$, Helmholtz), ajustando la corriente hasta lograr
$45°$ de desviación en la brújula ($I=12,15\,mA$, circuito en serie: fuente → multímetro →
bobina 1 → bobina 2 → fuente). Coherente con los valores de referencia típicos para Argentina
(18 a 25 µT de componente horizontal, según fuentes generales — ver Conclusiones en el notebook).

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
4. **Procedimiento experimental** — circuito en serie (fuente → multímetro → bobina 1 → bobina 2),
   orientar las bobinas perpendicular al campo terrestre, subir la corriente hasta lograr 45° de
   desviación en la brújula
5. **Mediciones y resultados** — I=12,15 mA medidos en el punto de 45°, cálculo de B_tierra
6. **Conclusiones** — comparación contra valores de referencia y fuentes de error

## Pendiente

- Revisar/pulir la redacción de Mediciones y Conclusiones (se escribieron directo con los datos
  que fue pasando el grupo, conviene una relectura).
- Hay 8 fotos en `imagenes/` que documentan el armado y la medición
  (`bobinas_helmholtz.jpeg`, `fuente_frente.jpeg`, `fuente_atras.jpeg`, `medicion_radio.jpeg`,
  `medicion_separacion.jpeg`, `multimetro_lectura.jpeg`, `brujula_desviacion.jpeg`,
  `fuente_lectura_45grados.jpeg`) que todavía no están embebidas en el notebook — decidir si
  conviene sumar alguna a Materiales y montaje o a Mediciones, como se hizo en TP1-TP3.
- La foto `imagenes/pizarron_espira.jpeg` (pizarrón con la derivación) tampoco se usa en el
  notebook. La figura que sí se usa, embebida en la Introducción teórica, es `imagenes/campo.jpeg`
  (diagrama de la espira con $\theta$, $\vec{r}$ y $d\vec{B}$ descompuesto en $dB_x$ y $dB_y$).
- Falta el `tp4_campo_magnetico_ENTREGA.ipynb` (copia final), siguiendo la convención de TP1-TP3,
  una vez que el contenido esté cerrado.
