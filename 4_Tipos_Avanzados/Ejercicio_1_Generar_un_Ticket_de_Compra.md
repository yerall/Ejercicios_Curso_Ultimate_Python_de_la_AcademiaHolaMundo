
# Descripción
El objetivo de este ejercicio es crear un programa que genere e imprima un ticket de compra a partir de una lista de productos. Cada producto está representado por un diccionario con un nombre y un precio. El programa debe calcular la cantidad de cada producto, el subtotal de cada uno y el total de la compra.

## Entrada
Una lista de diccionarios con las claves:
- 'nombre' (str): El nombre del producto.
- 'precio' (float): El precio del producto.

## Ejemplo de salida

```
-----------------
Ticket de compra:
-----------------
Manzana x2 - $1.00
Pan x1 - $1.00
Leche x3 - $4.50
Galletas x3 - $6.00
-----------------
Total: $12.50
-----------------
```

## Ejemplo de uso

```python
productos = [
	{'nombre': 'Manzana', 'precio': 0.5},
	{'nombre': 'Manzana', 'precio': 0.5},
	{'nombre': 'Pan', 'precio': 1.0},
	{'nombre': 'Leche', 'precio': 1.5}
]
generar_ticket(productos)
```

# Resolución
```python
def generar_ticket(productos):
	nombres = []

	# Guardar los nombres sin repetir
	for producto in productos:
		if producto["nombre"] not in nombres:
			nombres.append(producto["nombre"])

	total = 0

	print("-----------------")
	print("Ticket de compra")
	print("-----------------")

	# Contar cada producto
	for nombre in nombres:
		cantidad = 0
		precio = 0

		for producto in productos:
			if producto["nombre"] == nombre:
				cantidad += 1
				precio = producto["precio"]

		subtotal = cantidad * precio
		total += subtotal

		print(f"{nombre} x{cantidad} - ${subtotal:.2f}")

	print("-----------------")
	print(f"Total: ${total:.2f}")
	print("-----------------")


productos = [
	{"nombre": "Manzana", "precio": 0.5},
	{"nombre": "Manzana", "precio": 0.5},
	{"nombre": "Pan", "precio": 1},
	{"nombre": "Leche", "precio": 1.5},
	{"nombre": "Leche", "precio": 1.5}
]

generar_ticket(productos)
```
