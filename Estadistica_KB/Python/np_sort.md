# 📘 np.sort

## 🧠 Definición
`np.sort` devuelve una **versión ordenada del arreglo** dado, sin modificar el arreglo original. Por defecto, ordena de menor a mayor.

---

## 🔧 Sintaxis
```python
np.sort(a, axis=-1, kind=None, order=None)
```

Parámetros:
- `a`: arreglo de entrada.
- `axis`: eje a lo largo del cual ordenar.
- `kind`: tipo de algoritmo de ordenamiento ('quicksort', 'mergesort', etc.).

---

## 🧪 Ejemplo
```python
import numpy as np

a = np.array([13, 7, 42])
ordenado = np.sort(a)

print("Original:", a)
print("Ordenado:", ordenado)
```

---

## 🖥️ Salida esperada
```text
Original: [13  7 42]
Ordenado: [ 7 13 42]
```

---

## 💡 Notas / tips

- A diferencia de `np.argsort`, devuelve directamente los valores ordenados.
- Es útil para preparar datos antes de calcular **mediana**, **percentiles**, o detectar valores atípicos.
- No modifica el arreglo original a menos que se use `sort()` como método del objeto array (`a.sort()`).

---

## 🔁 Notas relacionadas
- [[mediana]]
- [[IQR]]
- [[np_argsort]]
- [[np_array]]
