
# Descripción
En este ejercicio, se implementa una clase CajaRegistradora que permite gestionar productos y pagos. La clase incluye métodos para agregar productos, calcular el total y dar cambio. Si el cliente no proporciona suficiente dinero, se lanza una excepción.

## Datos de Prueba
```python
caja = CajaRegistradora()
caja.agregar_producto('Manzana', 0.5)
caja.agregar_producto('Pan', 1)
print("Total:", caja.obtener_total())
print("Cambio:", caja.dar_cambio(2))
print("Cambio:", caja.dar_cambio(1))
```

## Salida Esperada
```python
Total: 1.5
Cambio: 0.5
ValueError: El pago es insuficiente.
```

# Resolución
```python
class CajaRegistradora:
	def __init__(self):
		self.productos = []

	def agregar_producto(self, nombre, precio):
		self.productos.append({"nombre": nombre, "precio": precio})

	def obtener_total(self):
		total = 0

		for producto in self.productos:
			total += producto["precio"]
		return total

	def dar_cambio(self, pago):
		total = self.obtener_total()
		if pago < total:
			raise ValueError("El pago es insuficiente.")
		return pago - total

caja = CajaRegistradora()

caja.agregar_producto("Manzana", 0.5)
caja.agregar_producto("Pan", 1)

print("Total:", caja.obtener_total())

try:
	print("Cambio:", caja.dar_cambio(2))
	print("Cambio:", caja.dar_cambio(1))
except ValueError as error:
	print(error)
```
