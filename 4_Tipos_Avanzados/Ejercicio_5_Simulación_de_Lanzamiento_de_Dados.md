
# Descripción
Vamos a mejorar un ejercicio de una sección anterior, este ejercicio simula el lanzamiento de un dado una cantidad específica de veces. El programa debe calcular la frecuencia de cada cara en porcentaje.

## Entrada
Un entero que indica cuántas veces se lanza el dado.

## Salida
Porcentaje de veces que apareció cada cara.

## Ejemplo de uso
```python
tirar_dados(10)
```

# Resolución
```python
import random

def tirar_dados(veces):
	if veces <= 0:
		print("Error: El número de lanzamientos debe ser mayor a 0.")
		return

	frecuencias = [0, 0, 0, 0, 0, 0]

	for i in range(veces):
		resultado = random.randint(1, 6)
		frecuencias[resultado - 1] += 1

	if veces == 1:
		print("Salió la cara:", resultado)
	else:
		print("\nResultados:")
		for i in range(6):
			porcentaje = (frecuencias[i] / veces) * 100
			print(f"Cara {i + 1}: {porcentaje:.2f}%")

veces = int(input("¿Cuántas veces desea lanzar el dado? "))
tirar_dados(veces)
```
