# Cero como indistinguibilidad: resolución espectral y referencia local

*Un resultado de control sobre la fórmula explícita de ψ(x)*

**Autor:** Nik  |  **Estado:** borrador 0.3  |  **Fecha:** octubre de 2026

## Resumen

Se propone entender el «cero» de una observación como indistinguibilidad entre dos objetos bajo una proyección o respecto de un referente. Se distinguen dos mecanismos: (i) cero por resolución, definido como pertenencia al núcleo de un operador de proyección P\_ℓ, y (ii) cero por referencia local, definido como diferencia nula respecto de un referente cuando medición y observación ocurren en el mismo contexto de medición. Se evalúa numéricamente el mecanismo (i) en la suma sobre los ceros no triviales de ζ que aparece en la fórmula explícita de ψ(x) − x. Se define un observable (ΔRMS por cero) y se muestra, con controles, que su signo depende de la ventana de observación, pero que esa dependencia no es específica de ζ: la reproducen frecuencias con espaciado de Poisson y, en lo esencial, frecuencias con espaciado tipo GUE. El número de ondas distinguibles en una ventana se cuantifica con la matriz de Gram. Se formaliza el cero dinámico como punto fijo inestable de un doble pozo (tasa de salida 4αλ) y se presenta además un ejemplo químico (cargas parciales de HCl) como ilustración de que una polaridad depende de cómo se la define. El resultado principal es negativo y acotado: la «polaridad» por cero no es una propiedad aritmética de ζ, sino un efecto de resolución espectral y de repulsión de niveles.

**Palabras clave:** indistinguibilidad, proyección, resolución espectral, fórmula explícita, ceros de la función zeta, matrices aleatorias, electronegatividad.

## Abstract

We propose to treat the «zero» of an observation as indistinguishability under a projection or relative to a reference. Two mechanisms are separated: zero by resolution (membership in the kernel of a projection P\_ℓ) and zero by local reference (a null difference with respect to a referent, arising when measurement and observation take place in the same measurement context). The first mechanism is tested numerically on the sum over nontrivial zeros of ζ in the explicit formula for ψ(x) − x. A per-zero observable (ΔRMS) is defined; its sign is shown to depend on the observation window, but not specifically on ζ: Poisson-spaced frequencies reproduce the effect, and GUE-spaced frequencies reproduce it essentially fully. The number of distinguishable waves in a window is quantified through the Gram matrix. The main result is negative and bounded: per-zero «polarity» is a spectral-resolution and level-repulsion effect, not an arithmetic property of ζ.

## 1. Introducción

En varios dominios la propiedad de un objeto (ser «activo», «nulo», «polar») depende de la escala o del referente con que se lo observa. Este trabajo formaliza una versión mínima de esa idea y la somete a una prueba numérica con controles.

**Alcance.** No se propone una teoría unificada ni se hacen afirmaciones sobre física fundamental. Las contribuciones son: (a) una definición operacional de «cero» como indistinguibilidad (sección 2); (b) un experimento numérico con controles sobre la suma de ceros de la fórmula explícita (secciones 3 y 4); (c) un ejemplo químico ilustrativo (sección 5); (d) un ejemplo mínimo de cero dinámico, con su tasa de salida (sección 2.4). El mecanismo de cero por referencia local (sección 2.3) se presenta solo como definición y no se contrasta. El resultado de (b) es en gran parte negativo y se reporta como tal.

## 2. Marco formal

### 2.1 Cero por resolución

Sea V un espacio de observables con producto interno y sea {P\_ℓ} una familia de proyecciones ortogonales (P\_ℓ² = P\_ℓ, P\_ℓ\* = P\_ℓ) indexada por una escala ℓ. Dos observables a y b son indistinguibles a escala ℓ si P\_ℓ(a − b) = 0. El «cero a escala ℓ» es el núcleo ker P\_ℓ. Si aumentar ℓ significa aumentar la resolución, es decir, si los rangos son anidados (ran P\_ℓ ⊆ ran P\_ℓ' para ℓ' ≥ ℓ), el núcleo decrece: ker P\_ℓ' ⊆ ker P\_ℓ para ℓ' ≥ ℓ. Lo que es cero a baja resolución puede dejar de serlo a alta resolución.

**Ceros naturales y ceros construidos.** Un cero por resolución puede darlo la naturaleza o construirse a propósito. La capa de ozono anula una banda del espectro solar, y las gafas de protección anulan la de un láser concreto: en ambos casos la banda cae en el núcleo de la proyección que realiza el filtro. El camuflaje del tigre, seleccionado evolutivamente, lo vuelve indistinguible de su fondo bajo la resolución de la presa. Lo natural suele ser específico y poco ajustable; lo construido puede diseñarse para una banda dada. Son ejemplos ilustrativos y no se contrastan.

**Convención de notación.** En el programa Amalgam el cero observable se escribe 0 = P\_ℓ(Ω), donde Ω es la clase de configuraciones de tensión neta nula. Es consistente con lo anterior: si P\_ℓ es lineal y anula esa clase (Ω ⊆ ker P\_ℓ), entonces P\_ℓ(Ω) = {0}. En este trabajo se usa la definición por núcleo; la forma P\_ℓ(Ω) solo reescribe que la clase Ω se proyecta al vector nulo.

### 2.2 Distinguibilidad en una ventana

Sea t = log x y sea I\_L = \[t₀, t₀ + L\] una ventana de longitud L. Para dos ondas f y g, se toma como medida de distinguibilidad d\_L(f, g) = ‖f − g‖ en L²(I\_L), con f y g normalizadas. Como ‖f − g‖² = 2 − 2 Re⟨f, g⟩ depende de la fase relativa, en lo que sigue se usa el solapamiento en módulo |⟨f, g⟩|, que es invariante ante una fase global. Para exponenciales complejas de frecuencias γ y γ', el solapamiento normalizado es exactamente

|⟨e^{iγt}, e^{iγ't}⟩| / L = |sinc((γ − γ')L/2)|, con sinc(u) = sin(u)/u.

Frecuencias con |γ − γ'| ≪ 2π/L son prácticamente indistinguibles en I\_L. Es un criterio del tipo Rayleigh y la forma clásica del límite de Fourier entre ancho de ventana y resolución en frecuencia. No se invoca ningún principio cuántico.

**Distinguibilidad como ángulo.** El solapamiento normalizado es el coseno de un ángulo entre vectores unitarios: θ\_L(γ, γ') = arccos |sinc((γ − γ')L/2)|. La distancia de Fisher–Rao entre distribuciones discretas tiene la misma estructura: d\_FR(p, q) = 2 arccos(Σ\_i √(p\_i q\_i)), el doble del ángulo entre los vectores unitarios (√p\_i) y (√q\_i). Para una distribución de Bernoulli de parámetro Σ, d\_FR(Σ₀, 0) = 2 arcsen(√Σ₀), de modo que la distancia de Σ = ½ al borde Σ = 0 es π/2. La divergencia de la métrica g(Σ) = 1/(Σ(1 − Σ)) en el borde es un efecto de la parametrización: con Σ = sen²θ la métrica es 4 dθ², plana y sin singularidad. Ambas nociones son distancias angulares en un espacio de Hilbert, aunque sobre espacios distintos; no se pretende identificarlas.

### 2.3 Cero por referencia local

Sean a y b dos magnitudes medidas contra un mismo referente r. Se dice que hay cero por referencia local si a − b = 0 exactamente cuando ambas se miden respecto de r, pero a − b ≠ 0 al cambiar de referente. «Local» significa que la medición y la observación ocurren en el mismo contexto de medición, es decir, contra el mismo referente r: el cero existe en ese contexto y no persiste fuera de él. Ejemplo: la microgravedad. El peso aparente de un astronauta respecto de su nave es nulo porque ambos caen con la misma aceleración, aunque la gravedad terrestre sigue actuando y, respecto del suelo, el movimiento es acelerado. Este cero requiere condiciones ajustadas (igualdad exacta), de modo que una perturbación arbitrariamente pequeña lo reemplaza por un valor pequeño no nulo, que bajo una resolución finita se lee otra vez como cero. En órbita, los términos de marea y otras perturbaciones impiden que el cero sea exacto, y en una nave se mantiene con correcciones de propulsión.

Ejemplos del mismo tipo son la cancelación activa de ruido y la óptica adaptativa: anulan un efecto en un punto o contexto dado mediante retroalimentación, y el cero desaparece si se interrumpe el control. Esa forma de cero mantenido corresponde a un punto fijo inestable como el de la sección 2.4. Un superconductor en levitación da la versión pasiva: el campo magnético es nulo en su interior (efecto Meissner, en los de tipo I) y, en los de tipo II, el anclaje de flujo fija la posición en un pozo estable; lo que se anula es la fuerza neta, no la gravedad. No se usa aquí el otro cero del superconductor, la resistencia nula, que proviene de un orden colectivo y pertenece al tercer uso de la sección 2.5. Estos ejemplos son ilustrativos y no se contrastan.

En este trabajo **solo se evalúa el mecanismo 2.1**; el mecanismo 2.3 se deja como definición, sin contrastación numérica.

### 2.4 Cero dinámico: un ejemplo mínimo

Se llama cero dinámico a un punto fijo inestable de un flujo: una diferencia nula que se mantiene solo mientras no haya perturbación. Ejemplo mínimo: un grado de libertad φ con el potencial de doble pozo V(φ) = λ(φ² − 1)², λ > 0, y flujo de gradiente φ̇ = −α V'(φ), α > 0.

```latex
\dot{\varphi} = -4\alpha\lambda\,\varphi(\varphi^2 - 1), \qquad V''(0) = -4\lambda < 0
```

Linealizando en φ = δ con |δ| ≪ 1, δ̇ = 4αλ δ, de modo que δ(t) = δ₀ e^(4αλt). El punto φ = 0 es inestable y la tasa 4αλ mide su fragilidad: una perturbación inicial δ₀ sale de un entorno de radio ε en un tiempo ≈ ln(ε/|δ₀|)/(4αλ). Las trayectorias convergen a los mínimos φ = ±1. Es la ruptura espontánea de simetría habitual de un doble pozo simétrico (bifurcación de horquilla). El ejemplo cuantifica la idea de que un cero dinámico requiere condiciones ajustadas, pero no establece que de él «emerjan» distinciones en general.

Contraste: un cero estático (nodo), como la cancelación de sonido en un punto, no tiene crecimiento temporal; su fragilidad es espacial, porque depende de la posición respecto del punto de cancelación.

### 2.5 Tres usos de la palabra «cero»

1. **Indistinguibilidad bajo proyección** (secciones 2.1 a 2.3): lo que cae en el núcleo de P\_ℓ, o la diferencia nula respecto de un referente.
2. **Punto fijo o crítico de un flujo:** grad V = 0, con estabilidad determinada por el signo de V'' (sección 2.4).
3. **Cero de una función:** los ceros no triviales de ζ de la sección 3.

No son lo mismo y este trabajo no los identifica. En particular, el borde Σ = 0 de una distribución de Bernoulli es una certeza, es decir, una distinción perfecta, y no una indistinción: la máxima indistinción corresponde a Σ = ½.

## 3. Caso de estudio: la suma sobre ceros en ψ(x) − x

### 3.1 Fórmula explícita

Para x > 1 no entero, la fórmula explícita de Riemann–von Mangoldt es

ψ(x) = x − Σ\_ρ x^ρ/ρ − log(2π) − ½ log(1 − x⁻²),

donde ρ recorre los ceros no triviales de ζ (Davenport, cap. 17; Montgomery y Vaughan, teorema 12.5, para la versión truncada). Bajo la hipótesis de Riemann, ρ = ½ + iγ, y cada par conjugado aporta

−2√x · \[½ cos(γ log x) + γ sen(γ log x)\] / (¼ + γ²).

### 3.2 Observable ΔRMS por cero

Sea C(x) = −log(2π) − ½ log(1 − x⁻²) y sea S\_n(x) la suma de C(x) y de los aportes de los primeros n pares de ceros, ordenados por γ creciente. Sobre una ventana I de x, se define

ΔRMS\_n = RMS\_I(S\_n) − RMS\_I(S\_{n−1}), con S\_0 = C.

Se trata del RMS de la expresión truncada, no del error respecto de ψ(x). El cuadrado medio del error ψ(x) − x en intervalos [X, 2X] es objeto de Brent, Platt y Trudgian (2022); aquí no se usan sus cotas, y solo se calcula el RMS de sumas truncadas sobre ventanas fijas. Dado que S\_n = S\_{n−1} + a\_n, con a\_n el aporte del n-ésimo cero,

media(S\_n²) − media(S\_{n−1}²) = media(a\_n²) + 2 · media(S\_{n−1} · a\_n).

El primer término es positivo; el segundo es un término cruzado de signo arbitrario. El signo de ΔRMS\_n coincide con el de esta diferencia. En consecuencia, «la contribución de un cero al RMS» no es una cantidad aditiva ni intrínseca: depende de los demás términos presentes y de la ventana.

### 3.3 Datos, ventanas y controles

- **Ceros:** los primeros 500 ceros no triviales (γ hasta 811,18), calculados con mpmath. Se supone la hipótesis de Riemann solo en la forma de la fórmula de la sección 3.1.
- **Ventanas en x:** \[50, 5·10²\], \[10², 10³\], \[10², 10⁴\], \[10³, 10⁵\].
- **Ponderación:** malla uniforme en log x (que pondera por dx/x) y malla uniforme en x (RMS lineal), ambas con 30 000 puntos.
- **Control de fases:** mismas frecuencias γ\_n con fases aleatorias uniformes (las mismas fases en las cuatro ventanas), 20 sorteos.
- **Control de Poisson:** 500 frecuencias con espaciado de Poisson y la misma densidad que los ceros, fase cero, 20 sorteos.
- **Control GUE:** 500 autovalores centrales de matrices GUE de 2000 × 2000, desplegados con la función de conteo del semicírculo y llevados a la densidad de los ceros por interpolación, fase cero, 15 sorteos (8 en el análisis de Gram).
- Los valores «±» son desviaciones estándar entre sorteos de control.

## 4. Resultados

### 4.1 Los signos de ΔRMS dependen de la ventana

La **consistencia** es la fracción de ceros cuyo signo de ΔRMS es idéntico en las cuatro ventanas.

| Malla | ζ | Fases aleatorias | γ de Poisson |
| --- | --- | --- | --- |
| Uniforme en log x | 42,4 % | 36,9 ± 2,1 % | 40,1 ± 3,1 % |
| Uniforme en x | 26,2 % | 23,0 ± 1,5 % | 26,3 ± 2,0 % |

Menos de la mitad de los ceros conserva su signo en las cuatro ventanas, y en este primer tramo el control de Poisson da una consistencia indistinguible de la de ζ (la sección 4.4 muestra que esto no se repite en otro tramo). La fracción de ΔRMS negativos depende de la ponderación: entre las ventanas, 18,4–19,2 % (log x) y 27,0–30,6 % (x) en ζ, frente a 22,4–25,3 % y 30,8–31,2 % en Poisson.

**Nota de cautela.** Con solo los primeros 100 ceros, ζ mostró una consistencia mayor que los controles (66,0 % frente a 50,5 ± 5,1 % con fases aleatorias y 47,2 ± 4,9 % con Poisson, malla log x). Esa diferencia desaparece con 500 ceros: es un efecto de muestra pequeña.

### 4.2 Los cambios de signo se relacionan con la cercanía de frecuencias

Para cada cero se toma d\_n = mín(γ\_n − γ\_{n−1}, γ\_{n+1} − γ\_n). El AUC es la probabilidad de que un cero que cambia de signo entre ventanas tenga menor d\_n que uno que no cambia (0,5 indica ausencia de relación).

|  | AUC (log x) | AUC (x) | % que cambia (log x) | % que cambia (x) |
| --- | --- | --- | --- | --- |
| ζ | 0,586 | 0,561 | 57,6 | 73,8 |
| Poisson | 0,493 ± 0,030 | 0,457 ± 0,039 | 59,2 ± 2,5 | 74,1 ± 2,2 |
| GUE | 0,588 ± 0,025 | 0,556 ± 0,018 | 63,5 ± 1,8 | 77,4 ± 2,0 |
| Fases aleatorias (mismas γ) | 0,594 ± 0,018 | 0,545 ± 0,028 | 62,2 ± 2,7 | 77,2 ± 2,5 |

En ζ existe una relación débil entre cercanía de frecuencias y cambio de signo; el control de Poisson no la muestra, pero el control GUE la reproduce prácticamente igual (AUC 0,588 y 0,556 frente a 0,586 y 0,561). El control de fases aleatorias, que conserva las frecuencias de ζ pero destruye sus fases, también da un AUC de 0,594 y 0,545, de modo que la relación proviene del espaciado de las frecuencias y no de las fases. La relación se explica, por tanto, por la repulsión de niveles y no por la aritmética de los primos. Queda una diferencia pequeña en la fracción que cambia (ζ por debajo de GUE: unos 3 σ en log x y 1,8 σ en x), que no se considera concluyente (sección 7) y que no se repite en el segundo tramo de ceros (sección 4.4).

### 4.3 Dimensión efectiva en una ventana

Se normaliza la onda de cada cero en I\_L (con t₀ = log 100) y se calcula la matriz de Gram G\_ij = ⟨f\_i, f\_j⟩. El **rango de participación** (Σλ)² / Σλ², con λ los autovalores de G, mide cuántas ondas son efectivamente distinguibles de las 500. Las ondas son reales, cos(γt) (multiplicadas por √x cuando se indica ponderación); con exponenciales complejas, como en la sección 2.2, los rangos resultan menores, de modo que el valor numérico depende de esta elección, aunque no el orden ζ ≈ GUE > Poisson.

| Ventana (2π/L) | Ponderación | ζ | GUE | Poisson |
| --- | --- | --- | --- | --- |
| L = ln 10 (2,73) | ninguna | 340 | 327 ± 2 | 261 ± 5 |
| L = ln 100 (1,36) | ninguna | 449 | 428 ± 3 | 333 ± 5 |
| L = ln 10 | √x | 271 | 270 ± 2 | 219 ± 4 |
| L = ln 100 | √x | 306 | 296 ± 2 | 240 ± 7 |

Aumentar la resolución (ventana más larga) aumenta el número de ondas distinguibles. ζ y GUE son similares y ambos superan por mucho a Poisson, porque la repulsión de niveles evita las frecuencias casi coincidentes. La ponderación por √x concentra el peso al final de la ventana y reduce la longitud efectiva, de modo que la escala relevante es una longitud efectiva y no L.

### 4.4 Segundo tramo de ceros (γ ≈ 10⁴)

Para estimar cuánto varían los estadísticos entre tramos, se repite el análisis con 500 ceros consecutivos, n = 10142 a 10641 (γ de 9998,85 a 10422,41), con las mismas ventanas y controles (40 sorteos de fases, de Poisson y de GUE). Este tramo no incluye los ceros anteriores, de modo que S\_0 = C y el observable ΔRMS es el de un bloque de ceros y no el de una suma parcial acumulada; el análisis de Gram solo depende de las frecuencias. Los valores de las secciones 4.4 a 4.6 se calculan con integrales analíticas y no con mallas (véase el apéndice A).

| | ζ | Fases aleatorias | Poisson | GUE |
| --- | --- | --- | --- | --- |
| Consistencia, log x (%) | 24,2 | 24,2 ± 1,8 | 30,0 ± 1,9 | 22,9 ± 1,8 |
| Consistencia, x (%) | 19,4 | 17,9 ± 1,6 | 20,9 ± 1,9 | 16,9 ± 1,4 |
| AUC, log x | 0,552 | 0,462 ± 0,027 | 0,407 ± 0,029 | 0,566 ± 0,029 |
| AUC, x | 0,530 | 0,466 ± 0,025 | 0,404 ± 0,031 | 0,534 ± 0,039 |
| % que cambia, log x | 75,8 | 75,8 ± 1,8 | 70,0 ± 1,9 | 77,1 ± 1,8 |
| % que cambia, x | 80,6 | 82,1 ± 1,6 | 79,1 ± 1,9 | 83,1 ± 1,4 |

Rango de participación (sección 4.3):

| Ventana | Ponderación | ζ | GUE | Poisson |
| --- | --- | --- | --- | --- |
| L = ln 10 | ninguna | 242 | 232 ± 3,2 | 194 ± 5,4 |
| L = ln 100 | ninguna | 358 | 356 ± 3,3 | 279 ± 7,0 |
| L = ln 10 | √x | 183 | 180 ± 2,3 | 156 ± 5,0 |
| L = ln 100 | √x | 209 | 206 ± 1,7 | 175 ± 5,2 |

En este tramo ζ reproduce a GUE en todos los estadísticos (dentro de unos 2 σ de control, salvo el rango con L = ln 10 sin ponderación, unos 3 σ por encima), y Poisson no lo hace: su consistencia en log x es mayor que la de ζ en unos 3 σ, y su rango de participación es mucho menor. La diferencia en la fracción que cambia respecto de GUE, que en el primer tramo era de unos 3 σ (sección 4.2), aquí es de menos de 1 σ, lo que respalda leerla como una fluctuación. Dos observaciones más. Primero, el control de Poisson no es indistinguible de ζ en este tramo, así que esa afirmación de la sección 4.1 no generaliza; el control relevante es GUE. Segundo, los valores de los controles dependen del tramo: el AUC de los controles de fases y de Poisson pasa de entre 0,47 y 0,58 en el primer tramo a entre 0,40 y 0,47 en este, y el AUC de ζ de 0,586 y 0,561 a 0,552 y 0,530.

### 4.5 Tercer tramo de ceros (γ ≈ 10⁵)

Mismo análisis con los ceros n = 138068 a 138567 (γ de 99998,90 a 100323,36), también como bloque con S\_0 = C.

| | ζ | Fases aleatorias | Poisson | GUE |
| --- | --- | --- | --- | --- |
| Consistencia, log x (%) | 20,0 | 21,6 ± 1,4 | 27,5 ± 1,8 | 19,0 ± 1,8 |
| Consistencia, x (%) | 14,8 | 16,3 ± 1,2 | 20,2 ± 1,8 | 14,9 ± 1,7 |
| AUC, log x | 0,530 | 0,448 ± 0,032 | 0,373 ± 0,031 | 0,541 ± 0,033 |
| AUC, x | 0,502 | 0,464 ± 0,033 | 0,398 ± 0,042 | 0,526 ± 0,038 |
| % que cambia, log x | 80,0 | 78,4 ± 1,4 | 72,5 ± 1,8 | 81,0 ± 1,8 |
| % que cambia, x | 85,2 | 83,7 ± 1,2 | 79,8 ± 1,8 | 85,1 ± 1,7 |

| Ventana | Ponderación | ζ | GUE | Poisson |
| --- | --- | --- | --- | --- |
| L = ln 10 | ninguna | 189 | 191 ± 1,7 | 164 ± 5,3 |
| L = ln 100 | ninguna | 305 | 308 ± 3,7 | 247 ± 6,3 |
| L = ln 10 | √x | 144 | 145 ± 1,2 | 129 ± 4,3 |
| L = ln 100 | √x | 167 | 167 ± 1,9 | 146 ± 4,8 |

ζ coincide con GUE en todos los estadísticos, dentro de 1 σ de control, y se separa de Poisson, cuya consistencia en log x es unos 4 σ mayor que la de ζ y cuyo rango de participación es menor. Con la malla uniforme de 30 000 puntos usada inicialmente, este tramo parecía mostrar una desviación de ζ respecto de GUE (consistencia en x de 9,4 % frente a unos 12,7 %, unos 3,7 σ); era un artefacto de muestreo, porque esa malla no resuelve las ondas cuando γ es grande (apéndice A), y desaparece con el cálculo analítico. Los «±» de los controles miden la variación entre sorteos y no la de ζ entre tramos, que con tres tramos aún no puede estimarse bien.

### 4.6 Sensibilidad

- **Constante C(x).** Cambiar el término constante de C de −log 2π a 0 o a −2 log 2π modifica el signo de ΔRMS en 1 a 5 % de los ceros (coincidencia de 95 a 99 %), de modo que no es relevante.
- **Orden de inclusión.** ΔRMS\_n depende de los ceros ya incluidos. En orden descendente de γ, solo coinciden entre 54 y 69 % de los signos con los del orden ascendente; con una permutación aleatoria coinciden entre 69 y 79 %. La consistencia pasa, según el tramo y la malla, de 14,8–41,8 % (orden ascendente) a 13,8–43,8 % (descendente) y 22,4–53,0 % (permutación aleatoria). Las comparaciones entre ζ y los controles usan siempre el orden ascendente y son homogéneas entre sí, pero el signo por cero no es una propiedad intrínseca del cero (confirma la advertencia de la sección 3.2).
- **Valor de partida t₀ en el análisis de Gram.** Con t₀ = log 50, log 100, log 10³ y log 10⁴, el rango de participación de ζ varía como máximo un 3 % (por ejemplo, 340 a 350 en el primer tramo con L = ln 10 sin ponderación), y no cambia el orden ζ ≈ GUE > Poisson.

## 5. Ejemplo ilustrativo: polaridad de H en HCl

La polaridad de un átomo en un enlace depende del par: en HCl, con las electronegatividades de Pauling χ(H) = 2,20 y χ(Cl) = 3,16, el H es el extremo δ⁺; en NaH, con χ(Na) = 0,93, el H es δ⁻. Para un mismo enlace, además, la «carga» depende de la definición adoptada, que actúa como una proyección distinta de la densidad electrónica:

- **Carga formal:** 0 en ambos átomos.
- **Carga derivada del dipolo:** q = μ/(e·r), con μ el momento dipolar medido y r la longitud de enlace; con μ = 1,1085 D (estado vibracional v = 0) y r = 1,2746 Å (valores de NIST) da q ≈ 0,18 e; con el dipolo de equilibrio, μₑ = 1,093 D, da 0,179 e, igual a dos cifras.
- **Carga de población** (p. ej. Mulliken, 1955): reparte la población electrónica entre los átomos con una regla fija, de modo que su valor depende de la base y del método de cálculo.

El ejemplo ilustra que «la polaridad» no es una cantidad única sino una función de la definición. Es solo cualitativo: no se reportan aquí cargas de población, porque su valor exige declarar método y base, y este trabajo no incluye un cálculo propio.

## 6. Discusión

1. La dependencia del signo de ΔRMS respecto de la ventana es real, pero se explica por resolución espectral: dos frecuencias más cercanas que ≈ 2π/L no se resuelven en una ventana de longitud L y sus términos cruzados no se anulan.
2. Ese efecto lo reproducen conjuntos de frecuencias sin aritmética (Poisson) y, en lo esencial, conjuntos con la repulsión de niveles de los ceros (GUE). No hay evidencia en estos datos de una propiedad específica de ζ.
3. La estadística de espaciado de los ceros coincide asintóticamente con la del GUE (Montgomery, 1973; Odlyzko, 1987). Las diferencias menores observadas respecto de GUE a la altura estudiada son compatibles con correcciones de tamaño finito documentadas en la literatura (Bogomolny et al., 2006), aunque este trabajo no las contrasta.
4. En los tres tramos analizados (secciones 4.3 a 4.5), el rango de participación de ζ coincide con el de GUE y se separa del de Poisson, y los estadísticos de signo de ζ coinciden con los de GUE dentro de unos 2 σ de control, con la excepción del rango con L = ln 10 sin ponderación en el segundo tramo (unos 3 σ). No se observa una desviación sistemática respecto de GUE.
5. Lo que sí queda establecido es una definición operacional (secciones 2.1 y 2.2), un observable bien definido (sección 3.2) y una medida cuantitativa de la indistinguibilidad en una ventana (sección 4.3).

## 7. Limitaciones

- Solo tres tramos de 500 ceros (los primeros, n = 10142 a 10641 y n = 138068 a 138567). Los estadísticos cambian de un tramo a otro (secciones 4.4 y 4.5), y con tres tramos no puede estimarse bien esa variación, de modo que las diferencias entre ζ y GUE no pueden juzgarse con las desviaciones entre sorteos de control.
- Número moderado de sorteos de control (8 a 20 en la tabla original del primer tramo, 40 en el resto).
- Los resultados dependen de la ponderación (log x frente a x) y de la elección de ventanas.
- El observable ΔRMS depende fuertemente del orden de inclusión de los ceros (sección 4.6); la constante C(x) y el valor de partida t₀ del análisis de Gram tienen efectos pequeños.
- El mecanismo de cero por referencia local (sección 2.3) no está contrastado.
- El ejemplo químico es cualitativo y sin cálculo propio; μ y r provienen de NIST.
- El ejemplo de la sección 2.4 tiene un solo grado de libertad; la extensión a un campo de la sección 8 solo se usa para calcular el Hessiano, y no se prueba ninguna otra propiedad de sistemas extendidos.

## 8. Observaciones conceptuales no evaluadas

Quedan dos hipótesis sin contrastar. La primera: un cero estático (nodo) y un cero dinámico (punto fijo inestable, sección 2.4) admiten cada uno una cantidad medible, y esas cantidades podrían distinguir a ζ de los controles de Poisson y GUE. La segunda: si el espectro de un operador asociado a un sistema (por ejemplo, el Hessiano de un potencial) perteneciera a la misma clase estadística que los ceros de ζ, debería mostrar estadística de espaciado GUE (Bohigas, Giannoni y Schmit; Berry y Keating). Las secciones 4.1 a 4.3 dan un criterio de contraste: consistencia de signos, AUC de vecinos cercanos y rango de participación frente a los controles GUE y Poisson. Un laplaciano en un intervalo, por ejemplo, tiene espectro regular y no GUE. Si el modelo de la sección 2.4 se extiende a un campo φ(x) en un intervalo de longitud L, con energía E[φ] = ∫(½|∇φ|² + V(φ)) dx y condiciones de Dirichlet, el Hessiano en φ = 0 es −Δ − 4λ, con autovalores (nπ/L)² − 4λ, así que ese modelo extendido no cumple el criterio. Mientras no exista una cantidad medible o un operador que lo cumpla, estas distinciones son terminología y no resultado.

## Apéndice A. Reproducibilidad

Los scripts `exact.py`, `exact_run.py` y `sens.py` (numpy, scipy, mpmath; semillas fijas) reproducen las secciones 4.3 a 4.6. Detalles que fijan los números:

- **Ceros.** `mpmath.zetazero`: primer tramo n = 1 a 500, segundo n = 10142 a 10641 y tercero n = 138068 a 138567. `exact_run.py` recibe un archivo `.npy` con las γ y el número de sorteos de control.
- **ΔRMS sin malla.** Cada aporte es a\_n(x) = c\_n √x cos(γ\_n t − δ\_n), con t = log x, c\_n = −2/√(¼ + γ\_n²) y δ\_n = atan2(γ\_n, ½). El signo de ΔRMS\_n es el de D\_n = media(a\_n²) + 2 media(C a\_n) + 2 Σ\_{m<n} media(a\_m a\_n), y todas las medias tienen forma cerrada (integrales de e^{pt} cos(γt + θ)), tanto con la ponderación en log x como en x.
- **Por qué no malla.** Las mallas uniformes de 30 000 puntos de la sección 3.3 dejan de resolver las ondas cuando γ·Δt se acerca a π (aliasing). No afecta al primer tramo (γ ≤ 811), donde el cálculo analítico coincide con la malla en la malla x y difiere en a lo sumo 0,6 puntos en log x (consistencia de 41,8 % frente a 42,4 %; la tabla de la sección 4.1 conserva los valores originales). En los tramos de γ ≈ 10⁴ y 10⁵ sí afecta: por ejemplo, la consistencia de ζ en x en el tercer tramo daba 9,4 % con la malla y es 14,8 % con el cálculo analítico.
- **Rango de participación.** Gram analítico de las ondas reales cos(γt) sobre I\_L con t₀ = log 100, con peso 1 o e^t (ponderación √x en amplitud), normalizado a diagonal unidad. Coincide con la versión por malla de 4000 puntos en los tres tramos.
- **Control GUE.** Matrices H = (A + A\*)/√2 de 2000 × 2000, con A de entradas complejas gaussianas; los autovalores se dividen por √n, de modo que el semicírculo tiene radio 2, y se despliegan con su función de conteo. Los 500 centrales se llevan a la densidad de los ceros por interpolación de N(T) = (T/2π) log(T/2πe) + 7/8.
- **Control de Poisson.** Espaciados exponenciales en la variable desplegada, con la misma interpolación.
- **Recálculo del primer tramo.** Con el motor analítico y 40 sorteos, los controles del primer tramo dan: fases 37,5 ± 2,3 % (log x) y 22,9 ± 1,5 % (x) de consistencia; Poisson 39,9 ± 2,6 % y 25,8 ± 1,6 %; GUE 37,5 ± 2,4 % y 23,4 ± 2,0 %. El rango de participación da ζ 340, 449, 271, 306 frente a GUE 337 ± 3,6, 440 ± 3,5, 273 ± 2,5, 302 ± 2,1.

## Referencias

Datos bibliográficos verificados contra la fuente (revista, editorial o repositorio) en octubre de 2026.

- Brent, R. P., Platt, D. J., Trudgian, T. S. (2022). The mean square of the error term in the prime number theorem. *Journal of Number Theory* 238, 740–762.
- Montgomery, H. L., Vaughan, R. C. (2007). *Multiplicative Number Theory I: Classical Theory*. Cambridge University Press (teorema 12.5).
- Davenport, H. *Multiplicative Number Theory*. Springer, Graduate Texts in Mathematics 74 (cap. 17, fórmula explícita para ψ(x)).
- Montgomery, H. L. (1973). The pair correlation of zeros of the zeta function. *Proc. Sympos. Pure Math.* 24, 181–193.
- Odlyzko, A. M. (1987). On the distribution of spacings between zeros of the zeta function. *Math. Comp.* 48, 273–308.
- Bogomolny, E., Bohigas, O., Leboeuf, P., Monastra, A. G. (2006). On the spacing distribution of the Riemann zeros: corrections to the asymptotic result. *J. Phys. A* 39, 10743–10754.
- NIST Computational Chemistry Comparison and Benchmark Database (CCCBDB), HCl (μₑ = 1,093 D; μ(v = 0) = 1,109 D; r = 1,2746 Å); NIST Chemistry WebBook, HCl (μ(v = 0) = 1,1085 D, Kaiser, E. W. (1970), *J. Chem. Phys.* 53, 1686; r\_e = 1,27455 Å; Rank, D. H., Rao, B. S., Wiggins, T. A. (1965), *J. Mol. Spectrosc.* 17, 122).
- Pauling, L. (1932). The nature of the chemical bond. IV. The energy of single bonds and the relative electronegativity of atoms. *J. Am. Chem. Soc.* 54, 3570–3582.
- Mulliken, R. S. (1955). Electronic population analysis on LCAO-MO molecular wave functions. I. *J. Chem. Phys.* 23, 1833–1840.
- Bohigas, O., Giannoni, M. J., Schmit, C. (1984). Characterization of chaotic quantum spectra and universality of level fluctuation laws. *Phys. Rev. Lett.* 52, 1–4.
- Berry, M. V., Keating, J. P. (1999). The Riemann zeros and eigenvalue asymptotics. *SIAM Review* 41, 236–266.
