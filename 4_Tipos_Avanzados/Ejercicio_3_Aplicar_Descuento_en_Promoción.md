
# Descripción
En este ejercicio, además de identificar a los clientes que califican para la promoción, se les aplica un descuento del 10%. El programa retorna:
1. Una lista con los IDs de los clientes que califican.
2. Un diccionario con los IDs de los clientes y sus montos ajustados después del descuento.

## Entrada
Un diccionario donde:
- Claves (str): IDs de los clientes.
- Valores (float o int): Montos de las compras.

## Salida
Dos elementos:
1. Lista de IDs de los clientes elegibles.
2. Diccionario con los montos ajustados

## Ejemplo de uso

```python
compras = {
	"Cliente1": 200,
	"Cliente2": 100,
	"Cliente3": 180,
}
resultado = aplicar_promocion(compras)
print(resultado) # [['Cliente1', 'Cliente3'], {'Cliente1': 180.0, 'Cliente3': 162.0}]
```

# Resolución
```python
def aplicar_promocion(compras):
	clientes = []
	descuentos = {}

	for cliente in compras:
		if compras[cliente] >= 150:
			clientes.append(cliente)

			nuevo_monto = compras[cliente] * 0.90
			descuentos[cliente] = round(nuevo_monto, 2)

	return clientes, descuentos

compras = {
	"Cliente1": 200,
	"Cliente2": 100,
	"Cliente3": 180,
	"Cliente4": 140,
	"Cliente5": 150,
	"Cliente6": 300,
	"Cliente7": 50
}

resultado = aplicar_promocion(compras)
print(resultado)
```
