# Álgebra de Planos Relacionales (APR) v2: los planos como proyecciones

Oct 8, 2026 · @Nik

**Estado:** formalización de una hipótesis, borrador v2. **Marcas:** \[D\] se deduce con álgebra lineal estándar; \[H\] hipótesis; \[N\] interpretación libre.

## 0. Qué es esto y qué no

APR v2 propone un lenguaje común para decir que un mismo sistema se ve distinto según el plano de observación, y para medir cuánto se pierde al pasar de un plano a otro. Reemplaza al APR v1, que tenía operadores sin definir y dos reglas que se contradecían (ver sección 1).

Todo lo marcado \[D\] es álgebra lineal conocida (proyecciones ortogonales, ángulos principales, matrices de Gram). Lo que aporta APR v2 no es un resultado matemático nuevo sino un vocabulario unificado y su aplicación. No afirma nada sobre la función zeta, la hipótesis de Riemann, la conciencia ni la física fundamental.

## 1. Qué cambia respecto de v1

- **Plano:** en v1 era un «marco interpretativo» sin definición. En v2 es un subespacio con su proyección ortogonal.
- **Idempotencia de Π:** en v1 era una regla. En v2 sale sola de P² = P.
- **Transitividad de T:** v1 la pedía como regla (Tⱼₖ∘Tᵢⱼ = Tᵢₖ) junto con Tᵢᵢ = I. Tomando k = i, eso obligaba a que toda traducción fuera invertible, es decir, sin pérdida, y chocaba con el Teorema 3. En v2 la composición solo vale en casos precisos (Proposición 4).
- **Teorema 3 (τ ≥ c > 0):** no existe una constante universal. La tensión mínima y máxima dependen del par de planos (Proposición 3).
- **τ y la métrica:** v1 afirmaba la desigualdad triangular sin prueba. τ depende de X y del orden (i → j) y no define una métrica sobre planos; la distancia entre planos d sí es métrica.
- **Resonancia:** en v1 dependía de «autosimilitud fractal», sin definir. En v2 es igualdad de matrices de Gram (sección 6).
- **Fase:** v1 no la tenía. v2 trabaja sobre números complejos, así que la cancelación entra (sección 5).
- **Lo que se deja fuera, sin verificar:** autosimilitud de escala, λ-cálculo con planos, Árbol de la Vida como ejemplo. Quedan como extensiones \[H\].

## 2. Definiciones

**D1 (espacio).** H es un espacio de Hilbert complejo con producto interno ⟨·,·⟩. Para empezar, de dimensión finita. Un sistema es un vector X ∈ H, o una familia de vectores.

**D2 (plano).** Un plano p es un subespacio cerrado Vₚ ⊆ H. Su proyección ortogonal Pₚ cumple Pₚ² = Pₚ = Pₚ\*. El plano representa lo que ese marco de observación puede distinguir.

**D3 (vista).** X⁽ᵖ⁾ = Pₚ X.

**D4 (cero del plano).** Zₚ = ker Pₚ = Vₚ^⊥. Dos sistemas X e Y son indistinguibles en p si y solo si X − Y ∈ Zₚ. Es el mecanismo de «cero por resolución» de la v0.3 del paper del cero.

**D5 (anidados).** Vᵢ ⊆ Vⱼ significa que el plano j ve todo lo que ve el i, y quizá más. Se dice que j es más fino que i.

## 3. Operadores

- **Proyección:** Πₚ(X) = Pₚ X. Es idempotente \[D\]. En general no conmuta: PᵢPⱼ ≠ PⱼPᵢ, salvo cuando los planos conmutan \[D\].
- **Traducción:** Tᵢⱼ = Pⱼ restringida a Vᵢ, de Vᵢ en Vⱼ. Tiene norma ≤ 1.
- **Tensión:** τᵢⱼ(X) = 1 − ‖PⱼPᵢX‖² / ‖PᵢX‖², definida si PᵢX ≠ 0. Es la fracción de la energía de la vista i que no sobrevive al plano j. Equivale a sen²θ, con θ el ángulo entre la vista PᵢX y el subespacio Vⱼ \[D\]. Es la misma parametrización sen²θ que usa la v0.3 para Σ de Bernoulli.
- **Distancia entre planos:** d(i,j) = ‖Pᵢ − Pⱼ‖ (norma de operador). Es una métrica sobre planos, con valores en \[0,1\]. Vale 1 si algún vector unitario de un plano es ortogonal al otro \[D\].

τ depende de X y del orden i → j, y no es simétrica: con dim Vᵢ = 4 y dim Vⱼ = 5, el supremo de τᵢⱼ puede ser menor que 1 (0,904 en el ejemplo del apéndice), mientras que el de τⱼᵢ vale 1, porque hay un vector de Vⱼ ortogonal a Vᵢ. Para medir la distancia entre planos se usa d.

## 4. Proposiciones

**P1 (extremos de la tensión) \[D\].** τᵢⱼ(X) = 0 si y solo si PᵢX ∈ Vⱼ. τᵢⱼ(X) = 1 si y solo si PᵢX ⊥ Vⱼ. Es inmediato de la definición.

**P2 (traducción sin pérdida) \[D\].** Son equivalentes: (a) Vᵢ ⊆ Vⱼ; (b) Tᵢⱼ es una isometría; (c) τᵢⱼ(X) = 0 para todo X con PᵢX ≠ 0. Demostración: de (a) a (b), Pⱼv = v para todo v ∈ Vᵢ. De (b) a (a), como ‖v‖² = ‖Pⱼv‖² + ‖(I−Pⱼ)v‖², igualar ‖Pⱼv‖ = ‖v‖ fuerza (I−Pⱼ)v = 0, es decir, v ∈ Vⱼ. (b) y (c) son lo mismo escrito con v = PᵢX.

**P3 (límite de traducción; corrige el Teorema 3 de v1) \[D\].** El supremo de τᵢⱼ(X) sobre X es sen²θ\_max, donde cos θ son los valores singulares de Qⱼ\*Qᵢ (Qᵢ y Qⱼ son bases ortonormales de cada plano) y θ\_max es el mayor ángulo principal. Si dim Vᵢ > dim Vⱼ aparece un coseno 0 y el supremo es 1. Consecuencia: hay tensión positiva para algún sistema si y solo si Vᵢ ⊄ Vⱼ. «No hay traducción perfecta» es cierto entre planos no anidados, y falso entre anidados. No existe una constante c > 0 universal.

**P4 (composición; corrige las reglas 1 y 2 de v1) \[D\].** Tⱼₖ∘Tᵢⱼ = Tᵢₖ sobre Vᵢ cuando Vᵢ ⊆ Vⱼ o cuando Vₖ ⊆ Vⱼ. En general no se cumple. Demostración: si Vᵢ ⊆ Vⱼ, entonces Pⱼv = v y PₖPⱼv = Pₖv. Si Vₖ ⊆ Vⱼ, entonces PⱼPₖ = Pₖ; tomando adjunta, PₖPⱼ = Pₖ. Los planos forman una categoría solo a lo largo de cadenas anidadas. En el caso general las traducciones pierden información y se componen con pérdida.

**P5 (resonancia es equivalencia) \[D\].** Ver sección 6.

## 5. Fase y cancelación

Sobre los complejos, la norma de una vista depende de la fase relativa de sus componentes:

‖P(u + e^{iφ}w)‖² = ‖Pu‖² + ‖Pw‖² + 2 Re( e^{iφ} ⟨Pu, Pw⟩ )

El último término es la interferencia. Con la misma intensidad y fases opuestas puede anular la vista; con la misma fase la refuerza.

**Cancelación activa \[D\].** Dado un ruido n, el control c = −P n cumple P(n + c) = 0. Lo que sobrevive, (I−P)n, está en el núcleo del plano, es decir, es invisible para ese plano de todas formas. Es el silencio por cancelación de los auriculares.

Así se ve que la v0.3 describe dos caminos al mismo cero Zₚ:

- **Silencio por resolución:** n ∈ ker P desde el principio (la nevera que se deja de oír).
- **Silencio por cancelación:** n se lleva al núcleo con un control que lee la vista P n (el «cero por referencia local»). Si el control se apaga, el cero desaparece.

**Fase en Δ \[H\].** La intensidad I del lenguaje Δ corresponde a |amplitud|² = sen²θ, y olvida la fase. Por eso Δ no puede escribir bien la cancelación. El isomorfismo estructural enfocado consiste en añadir un campo de fase φ a cada símbolo; sin él, Δ es la proyección (sombra) del sistema con amplitudes.

## 6. Resonancia como igualdad de Gram

Sean x = (xₐ) en Vᵢ e y = (yₐ) en Vⱼ dos familias con el mismo conjunto de índices A. Su Gram es Gˣₐᵦ = ⟨xₐ, xᵦ⟩.

**D6 (resonancia).** x ⋈ y si y solo si Gˣ = Gʸ. Es decir, las dos familias tienen las mismas relaciones internas (normas y ángulos), aunque vivan en planos distintos.

**P5 \[D\].** ⋈ es una relación de equivalencia. Además, si Gˣ = Gʸ existe una isometría lineal U: gen(x) → gen(y) con U xₐ = yₐ. Demostración: definir U(Σ cₐ xₐ) = Σ cₐ yₐ. Está bien definida y conserva la norma porque ‖Σ cₐ xₐ‖² = c\* Gˣ c = c\* Gʸ c = ‖Σ cₐ yₐ‖².

**Grado de resonancia.** ρ(x,y) = ‖Gˣ − Gʸ‖\_F / ‖Gˣ‖\_F. Vale 0 si hay resonancia exacta. En datos reales se usa con un umbral declarado antes de mirar los resultados.

**Autosimilitud \[H\].** Podría definirse como resonancia entre una familia y una versión escalada de sí misma. No está formalizada aquí.

## 7. Integración

Dada una familia de planos {pₖ}:

- **Visto en común:** ∩ₖ Vₖ.
- **Visto por alguno:** Σₖ Vₖ (suma de subespacios).
- **Cero común** (lo que ningún plano distingue): ∩ₖ Zₖ = (Σₖ Vₖ)^⊥ \[D\].
- **Grafo de compatibilidad:** arista entre i y j si d(i,j) < ε. Las componentes conexas son las «vistas integradas» de v1, ahora con una métrica de verdad.

## 8. Ejemplo: las ventanas de observación de la v0.3

Tomamos H = L²(ℝ₊). Una ventana I define P\_I f = 1\_I f, que es una proyección ortogonal \[D\]. Su subespacio es el de las funciones soportadas en I, y su núcleo el de las que se anulan en I. Las proyecciones de ventanas conmutan: P\_I P\_J = P\_{I∩J}.

Tensión entre ventanas: τ\_IJ(f) = 1 − ∫\_{I∩J} |f|² / ∫\_I |f|². Con ventanas disjuntas, τ = 1: cada una es el cero de la otra.

Comprobación numérica de la definición: para f = cos(2π·7,3·t), I = \[0; 0,5) y J = \[0,3; 0,9), sale τ ≈ 0,60, que coincide con el cálculo a mano (el 60 % de la energía de I cae fuera de J). Es una verificación de la definición, no un resultado del paper.

La matriz de Gram de las ondas en la ventana I, G⁽ᴵ⁾ₐᵦ = ∫\_I fₐ fᵦ, es la de la sección 4.3 de la v0.3. Con APR v2 se puede decir que el rango de participación mide la dimensión efectiva del plano I sobre el span de las ondas, y que comparar ventanas es calcular ρ entre sus Gram normalizadas.

## 9. Puente con el Lenguaje Δ (todo \[H\])

- **I (intensidad):** sen²θ de la parametrización de Bernoulli. Olvida la fase.
- **T (tensión):** τᵢⱼ entre dos planos.
- **R (relación):** entradas fuera de la diagonal del Gram, ⟨xₐ, xᵦ⟩.
- **V (vaciamiento):** llevar un vector al núcleo de P.
- **M (memoria):** Gram entre el estado en t y en t+1, es decir, cuánto del estado pasado persiste.

## 10. Límites

- No hay resultado nuevo en matemáticas: es álgebra lineal estándar con vocabulario propio.
- τ no es métrica; d sí.
- La resonancia exacta es rígida. En datos se usa ρ con umbral prefijado.
- En dimensión infinita hay que cuidar que los subespacios sean cerrados. Las ventanas por indicador sí lo son.
- Esta v2 no habla de la función zeta, de primos ni de nada fuera del álgebra de planos. Los resultados del paper del cero se quedan en ese paper.

## 11. Pruebas propuestas (declarar antes, medir después)

1. **Ventanas de la v0.3.** Calcular la matriz de tensiones τ y los grados ρ entre las cuatro ventanas, para ζ, Poisson, GUE y fases aleatorias. Antes de mirar, escribir qué se espera. Si ζ no se separa de los controles, el resultado coincide con el de la v0.3: efecto de resolución.
2. **Planos de Δ.** Probar si dos instancias que reciben la misma firma con y sin campo de fase producen lecturas más cercanas cuando la fase está presente. Con un control de fases barajadas.

## 12. Implementación mínima (Python)

```python
import numpy as np

def proyector(B):
    # B: matriz d×k de rango completo cuyas columnas generan el plano
    Q, _ = np.linalg.qr(B)
    return Q @ Q.conj().T

def tension(Pi, Pj, X):
    v = Pi @ X
    return 1 - np.linalg.norm(Pj @ v)**2 / np.linalg.norm(v)**2   # = sen²θ

def distancia(Pi, Pj):
    return np.linalg.norm(Pi - Pj, 2)      # métrica de gap, en [0,1]

def cancelar(P, n):
    return -P @ n                           # P(n + c) = 0

def resonancia(X, Y):
    # columnas de X e Y = familias con el mismo índice; 0 = resonancia exacta
    GX, GY = X.conj().T @ X, Y.conj().T @ Y
    return np.linalg.norm(GX - GY) / np.linalg.norm(GX)
```

## Apéndice: verificación numérica

Con planos aleatorios en ℂ¹² (semilla fija 7) se comprobó: P² = P = P\*; τ = sen²θ; el supremo de τ sobre un plano coincide con el límite teórico de la Proposición 3 (0,904 teórico, 0,898 como máximo sobre 20 000 vectores muestreados, sin pasar el límite); la traducción es isométrica entre planos anidados; la composición falla en el caso general (error 0,20) y se cumple cuando Vₖ ⊆ Vⱼ; d cumple la desigualdad triangular; la cancelación c = −Pn anula la vista sin anular n + c; y dos familias con el mismo Gram se relacionan por una isometría. Estos resultados se reprodujeron al repetir el script. Esto confirma propiedades estándar. Las demostraciones válidas son las de las secciones 4, 5 y 6.
