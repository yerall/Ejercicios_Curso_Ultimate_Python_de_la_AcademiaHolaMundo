
# Descripción
Este ejercicio introduce la clase CajaRegistradora, que permite gestionar productos y pagos, y la clase Cuentas, que registra múltiples cuentas, calcula el total de ventas y determina el ticket promedio

# Clase CajaRegistradora

## Atributos
- `productos`: Lista de productos agregados, cada uno representado como un diccionario con nombre y precio.

## Métodos
1. `__init__()`: Inicializa una lista vacía de productos.
2. `agregar_producto(nombre, precio)`: Agrega un producto especificando su nombre y precio.
3. `obtener_total()`: Calcula y devuelve el total de los precios de los productos en la lista.
4. `dar_cambio(pago)`: Calcula y devuelve el cambio basado en el pago proporcionado. Si el pago es insuficiente, devuelve un mensaje de error. Limpia la lista de productos tras calcular el cambio.
5. `listar_productos()`: Devuelve la lista actual de productos agregados.

# Clase Cuentas

## Atributos:
- `cuentas`: Lista de cuentas registradas, cada una con sus productos y total. 

## Métodos
1. `__init__()`: Inicializa una lista vacía de cuentas.
2. `agregar_cuenta(caja_registradora)`: Agrega una cuenta a la lista basada en los productos y el total de una instancia de CajaRegistradora.
3. `obtener_total_cuentas()`: Calcula y devuelve el total de todas las cuentas registradas.
4. `obtener_ticket_promedio()`: Calcula y devuelve el ticket promedio de todas las cuentas. Si no hay cuentas, devuelve 0.
5. `listar_cuentas()`: Devuelve la lista de cuentas registradas.

## Pruebas
1. Agregar productos y registrar cuentas
2. Agregar productos y registrar cuentas en Cuentas.
3. Verificar el total de ventas y el ticket promedio del día.
4. Listar las cuentas registradas.

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

class Cuentas:
	def __init__(self):
		self.cuentas = []

	def agregar_cuenta(self, caja):
		cuenta = {
			"productos": caja.productos,
			"total": caja.obtener_total()
		}
		self.cuentas.append(cuenta)

	def total_ventas(self):
		total = 0
		for cuenta in self.cuentas:
			total += cuenta["total"]
		return total

	def ticket_promedio(self):
		if len(self.cuentas) == 0:
			return 0
		return self.total_ventas() / len(self.cuentas)

	def mostrar_cuentas(self):
		return self.cuentas


caja = CajaRegistradora()
registro = Cuentas()

caja.agregar_producto("Manzana", 0.5)
caja.agregar_producto("Pan", 1.0)

registro.agregar_cuenta(caja)

caja.productos = []

caja.agregar_producto("Leche", 1.5)

registro.agregar_cuenta(caja)

print(registro.mostrar_cuentas())
print("Total vendido:", registro.total_ventas())
print("Ticket promedio:", registro.ticket_promedio())
```
