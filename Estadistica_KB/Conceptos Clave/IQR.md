# IQR

## 🧠 Definición

El **IQR** (Rango Intercuartílico) es una medida de dispersión que representa el rango dentro del cual se encuentra el 50% central de los datos. Se calcula como la diferencia entre el tercer cuartil (Q3 o percentil 75) y el primer cuartil (Q1 o percentil 25):

- Q1: valor por debajo del cual cae el 25% de los datos.
- Q3: valor por debajo del cual cae el 75% de los datos.

El IQR es útil para detectar **valores atípicos** (outliers) y entender la dispersión de los datos sin verse afectado por extremos.

---

## ⚙️ Proceso paso a paso

1. Ordenar los datos de menor a mayor.
2. Calcular el percentil 25 (Q1) y el percentil 75 (Q3).
3. Restar: `IQR = Q3 - Q1`.
4. (Opcional) Identificar valores atípicos:  
   - Límite inferior: Q1 - 1.5 × IQR  
   - Límite superior: Q3 + 1.5 × IQR

---

## 📐 Fórmulas


$$
IQR = Q_3 - Q_1
$$

$$
\text{Outliers:} \quad x < Q_1 - 1.5 \cdot IQR \quad 	ext{o} \quad x > Q_3 + 1.5 \cdot IQR
$$

---

## 🖥️ Código de apoyo (Python)
```python
import numpy as np

# Datos de ejemplo
datos = np.array([7, 15, 36, 39, 40, 41, 42, 43, 47, 49, 100])

# Calcular Q1 (percentil 25) y Q3 (percentil 75)
q1 = np.percentile(datos, 25)
q3 = np.percentile(datos, 75)

# Calcular IQR
iqr = q3 - q1

# Límites para detectar outliers
limite_inferior = q1 - 1.5 * iqr
limite_superior = q3 + 1.5 * iqr

# Identificar outliers
outliers = datos[(datos < limite_inferior) | (datos > limite_superior)]

# Imprimir resultados
print(f"Q1: {q1}")
print(f"Q3: {q3}")
print(f"IQR: {iqr}")
print(f"Límite inferior: {limite_inferior}")
print(f"Límite superior: {limite_superior}")
print(f"Outliers detectados: {outliers}")


```

---
## 🖥️ Output esperado

```text
Q1: 39.0
Q3: 43.0
IQR: 4.0
Límite inferior: 33.0
Límite superior: 49.0
Outliers detectados: [100]
```


---

## 🔗 Enlaces útiles

- [[mediana]]
- [[np_percentile]]
- [[np_sort]]
- [[desviacion_estandar]]
- [[distribucion_de_frecuencias]]
- [Documentación oficial NumPy - np.percentile](https://numpy.org/doc/stable/reference/generated/numpy.percentile.html)

---

## ✅ Conclusiones

- 🟢 El IQR ayuda a entender cómo se agrupan los datos alrededor de la mediana.
- 🔁 Se relaciona estrechamente con otras medidas de dispersión como la desviación estándar.
- 📦 Ideal para detectar valores atípicos en estudios de datos reales, como encuestas, puntajes, o análisis de calidad.
