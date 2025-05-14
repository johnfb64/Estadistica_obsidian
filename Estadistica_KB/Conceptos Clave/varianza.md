
# 📘 Varianza

## 🧠 Definición
Medida de variabilidad que indica caunto se dispersan los datos respecto a la media. 
## 🧮 Fórmulas
$$
s^2 = \frac{1}{n - 1} \sum_{i=1}^{n}(x_i - \bar{x})^2
$$




```python
import numpy as np

x = [2, 4, 6, 8, 10]

var_poblacional = np.var(x)           # por defecto: ddof=0
var_muestral = np.var(x, ddof=1)      # ddof=1 → divide entre (n - 1)

print("Varianza poblacional:", var_poblacional)
print("Varianza muestral:", var_muestral)

```


$$
X = [2, 4, 6, 8, 10], \quad \bar{x} = 6
$$

$$
\sum_{i=1}^{5} (x_i - \bar{x})^2 =
(2 - 6)^2 + (4 - 6)^2 + (6 - 6)^2 + (8 - 6)^2 + (10 - 6)^2
$$

$$
= 16 + 4 + 0 + 4 + 16 = 40
$$

**Varianza muestral:**

$$
s^2 = \frac{40}{5 - 1} = 10
$$



---

## 🔗 Enlaces útiles

- [[varianza]]
- [[varianza_muestral]]
- [[varianza_poblacional]]


---

## ✅ Conclusiones

- 🟢 ¿Qué aprendiste?
- 🔁 ¿Cómo se relaciona con otros conceptos?
- 📦 ¿Cuándo usarías este concepto en estadística aplicada?