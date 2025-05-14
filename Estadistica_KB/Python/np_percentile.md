# 📘 np.percentile

## 🧠 Definición
`np.percentile` calcula el **percentil** de los datos: el valor por debajo del cual cae un cierto porcentaje de los datos.

---

## 🔧 Sintaxis
```python
np.percentile(a, q, axis=None, interpolation='linear', keepdims=False)
```

Parámetros:
- `a`: arreglo de entrada.
- `q`: percentil o lista de percentiles a calcular (entre 0 y 100).
- `interpolation`: método para calcular si el percentil cae entre dos valores.

---

## 🧪 Ejemplo
```python
import numpy as np

a = np.array([10, 20, 30, 40, 50])
p25 = np.percentile(a, 25)
p75 = np.percentile(a, 75)

print("Percentil 25:", p25)
print("Percentil 75:", p75)
```

---

## 🖥️ Salida esperada
```text
Percentil 25: 20.0
Percentil 75: 40.0
```

---

## 💡 Notas / tips

- Útil para calcular el **rango intercuartílico (IQR)**: `IQR = P75 - P25`.
- Percentiles comunes: 25 (Q1), 50 (mediana), 75 (Q3).
- Asegúrate de que los datos estén **ordenados** internamente por la función.

---

## 🔁 Notas relacionadas
- [[mediana]]
- [[IQR]]
- [[distribución de frecuencias]]
- [[np.sort]]
- [[np.array]]
