
# Descripción
Este programa simula una caja registradora que acumula el precio de los productos ingresados por el usuario.

## Pruebas
1. Ingresar los precios de 10, 20 y 30 y luego fin.
	- Salida: "El total a pagar es: 60.00 dólares".
2. Ingresar "fin" sin precios.
	- Salida: "El total a pagar es: 0.00 dólares”.

# Resolución
```python
monto_total = 0.0

while True:
	precio = input("Ingrese el precio del producto o escriba 'fin' para terminar: ")
	if precio.lower() == "fin":
		break
	else:
		monto_total += int(precio)
		print(f"La cuenta va por {monto_total} dolares")

print(f"El monto total final es: {monto_total} dolares")
```
