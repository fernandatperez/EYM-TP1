# TP4 — Campo magnético

Informe en `tp4_campo_magnetico.ipynb`. Fusiona el trabajo de nuestro grupo (método de la
brújula) con el de un compañero que avanzó por su cuenta en la rama `tp4-final` (análisis de
error y referencia WMM), y suma la comparación contra el experimento del sensor Vernier que hizo
el resto de la clase.

`tp4_campo_magnetico_ENTREGA.ipynb` es una copia para mandar por mail. A diferencia del TP2 y el
TP3, acá **no** es autocontenida: el diagrama de la espira (sección 3) se referencia desde
`imagenes/campo.jpeg` como archivo externo, igual que en el TP1 — hay que mandar la carpeta
`imagenes/` junto con el notebook para que esa imagen se vea.

## Objetivo

Determinar la componente horizontal del campo magnético terrestre con bobinas de Helmholtz, por
dos métodos independientes (brújula y sensor), comparando además contra el modelo geomagnético
WMM.

## Resultado

**Método de la brújula** (el confiable):

$$B_{tierra} = (18{,}2\pm0{,}7)\,\mu T$$

Con $N=200$, $d=0,12\,m$ ($l=d$, Helmholtz), $I_{45}=12,15\,mA$. Comparado contra el modelo
**WMM2025** para la UNSAM el día de la medición ($16,92\,\mu T$): un 7,6% más alto, del orden del
doble del error estimado — la lectura del ángulo es la fuente de error dominante.

**Método del sensor** (no concluyente): la curva teórica da un pico ~4 veces más alto que el
medido con el sensor Vernier, y las curvas solo coinciden lejos del centro — un patrón que no se
explica por el campo terrestre (que daría un corrimiento parejo, no un factor que desaparece en
los extremos). La hipótesis más consistente es un problema de calibración del sensor (la llave de
amplificación HIGH x200 / LOW x10), sin poder confirmarlo.

## Estructura

1. **Objetivo**
2. **Materiales y montaje** — los dos armados: bobinas de Helmholtz + brújula (N=200, d=l=12cm) y
   bobinas + sensor Vernier (N=100, d=12,375cm, l=10,5cm)
3. **Introducción teórica** — Biot-Savart, mano derecha, superposición, cable infinito, espira
   circular (campana), dos espiras (M), comparación de separaciones l/d, Helmholtz, N vueltas,
   método de la brújula (incluye por qué 45° minimiza el error de lectura, con diagrama vectorial)
4. **Procedimiento experimental** — 4.1 método de la brújula (pasos detallados, con las
   precauciones que agregó el compañero), 4.2 método del sensor
5. **Mediciones y resultados** — 5.1 comparación teoría vs. sensor (gráfico + discusión de la
   discrepancia), 5.2 resultado de la brújula con análisis de error y comparación contra WMM
6. **Conclusiones** — síntesis de los dos experimentos

## Pendiente

- Hay 8 fotos del armado de la brújula en `imagenes/` (`bobinas_helmholtz.jpeg`,
  `fuente_frente.jpeg`, `fuente_atras.jpeg`, `medicion_radio.jpeg`, `medicion_separacion.jpeg`,
  `multimetro_lectura.jpeg`, `brujula_desviacion.jpeg`, `fuente_lectura_45grados.jpeg`) y 6 del
  experimento del sensor en `imagenes/experimento/` — ninguna está embebida todavía en el
  notebook. Decidir si conviene sumar alguna a Materiales y montaje.
- Falta reconciliar esta rama (`tp4-final-para-entrega`) con `tp4-final` (la del compañero) y con
  `main` — hay trabajo de TP4 en las tres, con superposición parcial.
