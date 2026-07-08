
# Descripción
Este ejercicio calcula el costo total de la promoción, es decir, la suma de los descuentos aplicados a los clientes elegibles.

## Entrada
Un diccionario con:
- Claves (str): IDs de los clientes.
- Valores (float o int): Montos de las compras.

## Salida
Un número que representa el costo total de los descuentos aplicados.

## Ejemplo de uso

```python
compras = {
	"Cliente1": 200,
	"Cliente2": 100,
	"Cliente3": 180,
}
costo_promocion = calcular_costo_promocion(compras)
print(costo_promocion) # 38.0
```

# Resolución
```python
def calcular_costo_promocion(compras):
	costo_total = 0

	for cliente in compras:
		if compras[cliente] >= 150:
			descuento = compras[cliente] * 0.10
			costo_total += descuento

	return costo_total

compras = {
	"Cliente1": 200,
	"Cliente2": 100,
	"Cliente3": 180,
	"Cliente4": 140,
	"Cliente5": 150,
	"Cliente6": 300,
	"Cliente7": 50
}

print(calcular_costo_promocion(compras))
```

