
# Descripción
Aquí se implementa una clase `CuentaBancaria` que maneja depósitos, retiros y saldos, con excepciones personalizadas para manejar errores como retiros de cantidades negativas o superiores al saldo disponible.

## Datos de Prueba
```python
try:
	cuenta = CuentaBancaria("123456789", "Juan Perez", 1000)
	cuenta.mostrar_saldo()
	cuenta.depositar(500)
	cuenta.retirar(2000)
except ErrorRetiro as e:
	print(e)

try:
	cuenta.retirar(-100)
except ErrorRetiro as e:
	print(e)
```

## Salida Esperada
```python
Saldo actual: 1000
Depósito exitoso. Nuevo saldo: 1500
('Fondos insuficientes para realizar el retiro.', 401)
('La cantidad a retirar debe ser positiva.', 400)
```

# Resolución
```python
class ErrorRetiro(Exception):
	pass

class CuentaBancaria:
	def __init__(self, numero, propietario, saldo):
		self.numero = numero
		self.propietario = propietario
		self.saldo = saldo

	def mostrar_saldo(self):
		print("Saldo actual:", self.saldo)

	def depositar(self, cantidad):
		if cantidad > 0:
			self.saldo += cantidad
			print("Depósito realizado.")
		else:
			print("La cantidad debe ser mayor que 0.")

	def retirar(self, cantidad):
		if cantidad <= 0:
			raise ErrorRetiro("La cantidad debe ser mayor que 0.")
		if cantidad > self.saldo:
			raise ErrorRetiro("Fondos insuficientes.")
		self.saldo -= cantidad
		print("Retiro realizado.")

cuenta = CuentaBancaria("123456", "Juan", 1000)
cuenta.mostrar_saldo()
cuenta.depositar(500)

try:
	cuenta.retirar(2000)
except ErrorRetiro as error:
	print(error)

try:
	cuenta.retirar(-100)
except ErrorRetiro as error:
	print(error)
```
