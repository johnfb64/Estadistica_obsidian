# 📘 Mediana ponderada

## 🧠 Definición
La **mediana ponderada** es el valor dentro de un conjunto ordenado de datos que supera el 50% del peso acumulado. A diferencia de la mediana tradicional, cada dato tiene un peso (o frecuencia relativa) que influye en su importancia dentro del conjunto.

---

## 📊 Ejemplo: Notas y pesos

### Datos

| Valor $x_i$ | Peso $p_i$ |
|-------------|------------|
| 2           | 0.10       |
| 5           | 0.20       |
| 6           | 0.15       |
| 7           | 0.25       |
| 9           | 0.30       |

---

### Paso a paso

1. ✅ Ordenar los datos por valor (ya están ordenados en este caso).
2. ➕ Acumular los pesos progresivamente:

| Valor $x_i$ | Peso $p_i$ | Peso acumulado |
|-------------|------------|----------------|
| 2           | 0.10       | 0.10           |
| 5           | 0.20       | 0.30           |
| 6           | 0.15       | 0.45           |
| 7           | 0.25       | 0.70 ⬅️        |
| 9           | 0.30       | 1.00           |

---

## 📌 Interpretación

🔴 El valor **7** es la **mediana ponderada**, porque es el primer valor cuya **acumulación de peso supera el 50%** del total.

---

## ⚙️ Proceso paso a paso

1. Ordenar los datos por valor ascendente.
2. Acumular los pesos de cada fila.
3. Identificar el primer valor cuyo peso acumulado sea **mayor o igual a 0.50**.
4. Ese valor es la **mediana ponderada**.

---

## 🖥️ Código de apoyo (Python)

```python
valores = [2, 5, 6, 7, 9]
pesos = [0.10, 0.20, 0.15, 0.25, 0.30]

peso_acumulado = 0
for i, (v, p) in enumerate(zip(valores, pesos)):
    peso_acumulado += p
    if peso_acumulado >= 0.5:
        print(f"La mediana ponderada es: {v}")
        break
```

---

## 🔁 Relacionado
- [[mediana_ponderada]]
- [[mediana]]
- [[distribuciones_acumuladas]]
