
# Instrucciones

En este ejercicio aprenderás a calcular el promedio de una serie de números. También trabajarás con parámetros variables en funciones.
1. Define una función que acepte un número variable de argumentos.
2. Si no se proporcionan números, devuelve 0.
3. Si se proporcionan números, calcula y devuelve el promedio.

## Casos de ejemplo:
- Calcula el promedio de los números 1, 2, 3, 4, 5.
- ¿Qué sucede si no proporcionas ningún número?

# Resolución
```python
def calcular_promedio(*numeros):
	if len(numeros) == 0:
		return 0
	return sum(numeros) / len(numeros)

cantidad = int(input("¿Cuántos números desea ingresar? "))
numeros = []

for i in range(cantidad):
	numero = float(input(f"Ingrese el número {i + 1}: "))
	numeros.append(numero)

promedio = calcular_promedio(*numeros)
print("El promedio es:", promedio)
```
