
# ¿Cómo funciona?
Este programa calcula el cambio que se debe devolver a un cliente después de una compra.
1. Solicita al usuario dos datos.
	- Cantidad de dinero entregada por el cliente.
	- Costo del producto.
2. Calcula el cambio restando el costo del producto al dinero entregado.
3. Muestra el cambio a devolver.

## Entradas
- Dinero entregado por el cliente.
- Costo del producto.

## Salidas
- Cambio a devolver.

## Ejemplos
- Entrada: 50, 30 -> Cambio: 20.0
- Entrada: 100, 75.5 -> Cambio: 24.5
- Entrada: 20, 20 -> Cambio: 0.0

# Resolución
```python
monto_compra = float(input("Ingrese el monto total de la compra: "))
cantidad_entregada = float(input("Ingrese la cantidad de dinero entregada: "))

if cantidad_entregada >= monto_compra:
	print(f"\nLa cantidad de entrega al cliente es de {cantidad_entregada-monto_compra}\n")
elif cantidad_entregada < monto_compra:
	print(f"\nAl cliente le falta por entregar {abs(cantidad_entregada - monto_compra)} para completar la compra de {monto_compra}\n")
else:
	print("ERROR")
```
