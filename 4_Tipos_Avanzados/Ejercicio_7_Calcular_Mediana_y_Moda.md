
# Descripción
Este ejercicio calcula dos estadísticas importantes de una lista de números:
1. La mediana: Es el valor que separa la mitad superior de la mitad inferior de una lista ordenada de números. Si la lista tiene un número par de elementos, la mediana es el promedio de los dos valores centrales.
2. La moda: El valor que aparece con mayor frecuencia.

## Entrada
Una lista de números.

## Salida
La mediana y la moda de la lista.

## Ejemplo de uso
```python
datos = [1, 2, 2, 3, 4]
mediana, moda = calcular_mediana_y_moda(datos)
print(mediana, moda) # 2, 2

datos = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
mediana, moda = calcular_mediana_y_moda(datos)
print(mediana, moda) # 7, 10
```

## Salida esperada
```
Mediana: 2, Moda: 2
Mediana: 7, Moda: 10
```

# Resolución
```python
def calcular_mediana_y_moda(datos):
	datos.sort()

	cantidad = len(datos)

	# Calcular mediana
	if cantidad % 2 == 0:
		medio1 = datos[cantidad // 2 - 1]
		medio2 = datos[cantidad // 2]
		mediana = (medio1 + medio2) / 2
	else:
		mediana = datos[cantidad // 2]

	# Calcular moda
	moda = datos[0]
	mayor = 0

	for numero in datos:
		repeticiones = datos.count(numero)
		if repeticiones > mayor:
			mayor = repeticiones
			moda = numero
	return mediana, moda

datos = [1, 2, 2, 3, 4]

mediana, moda = calcular_mediana_y_moda(datos)

print("Mediana:", mediana)
print("Moda:", moda)
```
