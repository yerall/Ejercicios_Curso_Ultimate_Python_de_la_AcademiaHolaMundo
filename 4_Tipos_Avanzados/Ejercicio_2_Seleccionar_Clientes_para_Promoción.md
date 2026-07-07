
# Descripción
Este ejercicio se enfoca en identificar a los clientes que califican para una promoción. Los clientes califican si el monto de sus compras es mayor o igual a 150 dólares.

## Entrada
Un diccionario con:
- Claves (str): IDs de los clientes.
- Valores (float o int): Montos de las compras.

## Salida
Una lista con los IDs de los clientes que califican para la promoción

## Ejemplo de uso
```python
compras = {
	"Cliente1": 200,
	"Cliente2": 100,
	"Cliente3": 180,
}
clientes_promocion = aplicar_promocion(compras)
print(clientes_promocion) # ['Cliente1', 'Cliente3']
```

# Resolución
```python
def aplicar_promocion(compras):
	clientes = []

	for cliente in compras:
		if compras[cliente] >= 150:
			clientes.append(cliente)
	return clientes

compras = {
	"Cliente1": 200,
	"Cliente2": 100,
	"Cliente3": 180,
	"Cliente4": 140,
	"Cliente5": 150,
	"Cliente6": 300,
	"Cliente7": 50
}

print(aplicar_promocion(compras))
```


