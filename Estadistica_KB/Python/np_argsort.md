# 📘 np.argsort

## 🧠 Definición
`np.argsort` devuelve los **índices que ordenarían un arreglo**. Es decir, te indica en qué orden deben moverse los elementos para que el arreglo quede ordenado de menor a mayor.

---

## 🔧 Sintaxis
```python
np.argsort(a, axis=-1, kind=None, order=None)
```

Parámetros:
- `a`: arreglo de entrada.
- `axis`: eje a lo largo del cual ordenar.
- `kind`: tipo de algoritmo de ordenamiento (por defecto, 'quicksort').

---

## 🧪 Ejemplo
```python
import numpy as np

a = np.array([42, 7, 13])
indices = np.argsort(a)

print("Índices ordenados:", indices)
print("Valores ordenados:", a[indices])
```

---

## 🖥️ Salida esperada
```text
Índices ordenados: [1 2 0]
Valores ordenados: [ 7 13 42]
```

---

## 💡 Notas / tips

- Es muy útil cuando quieres ordenar **otro arreglo asociado** (por ejemplo, etiquetas, pesos, etc.).
- También se puede usar para calcular **rangos** o posiciones relativas de valores.
- No modifica el arreglo original, solo devuelve los índices.

---

## 🔁 Notas relacionadas
- [[media_aritmetica]]
- [[mediana]]
- [[mediana_ponderada]]
- [[distribución_de_frecuencias]]
- [[IQR]]
- [[np_array]]
