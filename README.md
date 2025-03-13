# Transformada inversa de LaPlace
## Solución de ejercicios: 
### 💡**Ejemplo 1:**
Este ejemplo muestra lo que puede ocurrir cuando hay factores repetidos en el denominador. Buscamos $A, B, C$ de manera que:


$$\frac{8s^2 - 7s + 6}{s^2(s-2)} = \frac{A}{s} + \frac{B}{s^2} + \frac{C}{s-2}$$
\]

Esta igualdad se cumple solo cuando:

$$A s(s - 2) + B(s - 2) + C s^2 = 8s^2 - 7s + 6$$

- Se evalua las dos raíces del denominador:

- 1. Si $s = 0$, entonces:

$$A(0) + B(-2) + C(0) = 8 \cdot 0^2 - 7 \cdot 0 + 6$$

$$-2B = 6 \Rightarrow B = -3$$

- 2. Si $s = 2$, entonces:

$$A(2)(0) + B(0) + C(2^2) = 8 \cdot 2^2 - 7 \cdot 2 + 6$$

$$4C = 32 - 14 + 6 = 24 \Rightarrow C = 6$$

- Para obtener $A$ podemos dar a $s$ cualquier otro valor y usar los valores ya determinados para $$B$$ y $$C$$

- 3 si $$s = 1$$, entonces:

$$A(1)(-1) + B(-1) + C(1^2) = 8 \cdot 1^2 - 7 \cdot 1 + 6$$

$$- A - B + C = 8 - 7 + 6 = 7$$

$$- A - (-3) + 6 = 7$$

$$- A + 3 + 6 = 7 \Rightarrow -A = -2 \Rightarrow A = 2$$

- Por lo tanto:

$$F(s) = \frac{8s^2 - 7s + 6}{s^2(s-2)} = \frac{2}{s} - \frac{3}{s^2} + \frac{6}{s-2}$$


$$\mathcal{L}^{-1} \{ F(s) \} = 2 \mathcal{L}^{-1} \big( \frac{1}{s} \big)$$
$$- 3 \mathcal{L}^{-1} \big( \frac{1}{s^2} \big)$$
$$+ 6 \mathcal{L}^{-1} \big( \frac{1}{s-2} \big)$$

$$= 2 - 3t + 6e^{2t}$$

### 💡**Ejemplo 2:**
Determinar la transformada inversa de Laplace de:

$$F(s) = \frac{3s + 4}{(s^2 + 1)(s + 2)}$$

- El denominador tiene el factor cuadrático irreducible $s^2 + 1$, con raíces $s = \pm i$, y un factor lineal $(s + 2)$. La transformada inversa de $F(s)$ es:

$$f(t) = \mathcal{L}^{-1}\{F(s)\} = A \cos t + B sen t + C e^{-2t}$$

- Los coeficientes $A$ y $B$ se obtienen como:

$$A = \frac{1}{b} \Im \lim_{s \to i} (s^2 + 1)F(s)$$

- Sustituyendo $s = i$:


$$A = \Im \left( \frac{(3i + 4)(2 - i)}{(i + 2)(2 - i)} \right) = \frac{2}{5}$$

$$B = \frac{1}{b} \Re \lim_{s \to i} (s^2 + 1)F(s)$$

$$B = \Re \left( \frac{(3i + 4)(2 - i)}{(i + 2)(2 - i)} \right) = \frac{11}{5}$$

- El coeficiente $C$ se obtiene evaluando en $s = -2$:

$$C = \lim_{s \to -2} (s+2) F(s) = \frac{3s + 4}{s^2 + 1} \Big|_{s=-2} = \frac{-2}{5}$$

- La transformada inversa es:

$$f(t) = \frac{2}{5} \cos t + \frac{11}{5} sen t - \frac{2}{5} e^{-2t}$$

