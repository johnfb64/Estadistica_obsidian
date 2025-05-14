# 📘 np.where

## 🧠 Definición
`np.where` es una función de NumPy que permite **seleccionar elementos condicionalmente** en un arreglo.  
Tiene dos modos principales de uso:

1. Como **filtro**: devuelve los **índices** donde se cumple una condición booleana.
2. Como **selector ternario**: devuelve valores según condición, tipo `si condición → A, si no → B`.

---

## 🔧 Sintaxis
```python
np.where(condición)                  # modo índice
np.where(condición, valor_si_True, valor_si_False)  # modo ternario
```

Parámetros:
- `condición`: expresión booleana elemento a elemento.
- `valor_si_True`: valor devuelto cuando la condición es verdadera.
- `valor_si_False`: valor devuelto cuando es falsa.

---

## 🧪 Ejemplo
```python
import numpy as np

x = np.array([1, 2, 3, 4, 5])

# Modo 1: Índices donde x es mayor que 3
indices = np.where(x > 3)

# Modo 2: Selector ternario
resultado = np.where(x > 3, x, 0)
```

---

## 🖥️ Salida esperada
```text
# Modo 1
(array([3, 4]),)

# Modo 2
array([0, 0, 0, 4, 5])
```

---

## 💡 Notas / tips

- En [[desviacion_ponderada]] y [[mediana_ponderada]] usamos `np.where` para ubicar el primer índice donde el peso acumulado ≥ 0.5.
- En el modo índice, `np.where(cond)` devuelve una **tupla de arrays**, por eso el acceso típico es `np.where(...)[0][0]`.

---

## 🔁 Notas relacionadas
- [[subindice]]
- [[desviacion]]
- [[estadisticos_ordinales]]
- [[funciones_numpy]]
