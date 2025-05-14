# 📘 np.array


## 🧠 Definición
Esta funcion crea un arreglo n-dimensional a partir de listas u otras secuencias. Es la base para muchas de las operaciones matrices. 

---

## 🔧 Sintaxis
```python
np.array(object, dtype=None, copy=True, ndmin=0)
```

Funcion:
np.array

Parámetros:
- object: lista o lista de listas que se convertirá en arreglo.
- dtype: tipo de dato (opcional)
- ndmin: Numero minimo de dimenciones

---

## 🧪 Ejemplo
```python
import numpy as np

# Crear un arreglo de 1 dimensión
a = np.array([1, 2, 3])
print("Arreglo 1D:", a)

# Crear un arreglo de 2 dimensiones (matriz)
b = np.array([[1, 2], [3, 4]])
print("Arreglo 2D:\n", b)
```

---

## 🖥️ Salida esperada
```text
Arreglo 1D: [1 2 3]
Arreglo 2D:
 [[1 2]
  [3 4]]
```

---

## 💡 Notas / tips

- Si se mezclan tipos, Numpy convierte todo al tipo mas general

---

## 🔁 Notas relacionadas
- [[np_array]]
- [[np_zeros]]
- [[np_reshape]]
- [[Media_aritmética]]
- [[varianza]]
- [[desviación_estándar]]
- [[mediana]]
- [[mediana ponderada]]
- [[distribución_de_frecuencias]]
- [[IQR]]
