
# Instrucciones

Este ejercicio simula el lanzamiento de un dado y calcula la frecuencia con la que aparece cada cara. Es perfecto para trabajar con estructuras de control y bucles.

El siguiente código utiliza un módulo del lenguaje python para generar un número aleatorio entre 1 y 6, este lo veremos en mayor profundidad más adelante:

```python
import random # esto va en la primera línea del archivo

resultado = random.randint(1, 6)
print(resultado)
```

Puedes utilizar esta misma línea de código en una función de esta manera:

```python
def dameNumero(desde, hasta):
    return random.randint(desde, hasta)
print(dameNumero(1, 6))
```

Utilizando el código de más arriba:
1. Define una función que simule lanzar un dado múltiples veces.
2. Cuenta cuántas veces aparece cada cara del dado.
3. Calcula el porcentaje de ocurrencia de cada cara.
4. Maneja errores si el número de lanzamientos no es válido (por ejemplo, 0 o números negativos).

## Casos de ejemplo:
- Lanza un dado 10 veces. ¿Qué porcentajes obtienes?
- Intenta lanzar un dado 0 veces. ¿Qué mensaje de error aparece?
- ¿Qué sucede si lanzas un dado 10000 veces? ¿Son los porcentajes cercanos al 16.67%?
- ¿Qué ocurre cuando lanzas el dado 1 vez?

# Resolución
```python
import random

def tirar_dados(veces):
	if veces <= 0:
		print("Error: El número de lanzamientos debe ser mayor a 0.")
	else:
		cara1 = cara2 = cara3 = cara4 = cara5 = cara6 = 0

		for i in range(veces):
			resultado = random.randint(1, 6)
			if resultado == 1:
				cara1 += 1
			elif resultado == 2:
				cara2 += 1
			elif resultado == 3:
				cara3 += 1
			elif resultado == 4:
				cara4 += 1
			elif resultado == 5:
				cara5 += 1
			else:
				cara6 += 1

		print(f"Cara 1: {(cara1 / veces) * 100}%")
		print(f"Cara 2: {(cara2 / veces) * 100}%")
		print(f"Cara 3: {(cara3 / veces) * 100}%")
		print(f"Cara 4: {(cara4 / veces) * 100}%")
		print(f"Cara 5: {(cara5 / veces) * 100}%")
		print(f"Cara 6: {(cara6 / veces) * 100}%")

veces = int(input("¿Cuántas veces desea lanzar el dado? "))
tirar_dados(veces)
```
