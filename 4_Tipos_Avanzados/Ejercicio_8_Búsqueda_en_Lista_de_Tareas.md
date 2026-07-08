
# Descripción
Busca tareas específicas en una lista utilizando dos métodos:
1. Por ID.
2. Por texto contenido en la descripción.

## Entrada
1. Una lista de diccionarios, donde cada diccionario tiene las claves:
2. 'id' (int): ID de la tarea.
3. 'descripcion' (str): Descripción de la tarea.
4. Un entero para buscar por ID.
5. Un texto para buscar coincidencias.

## Salida
1. La tarea que coincide con el ID.
2. Una lista de tareas que contienen el texto.

## Ejemplo de uso
```python
tareas = [
	{"id": 1, "descripcion": "Lavar los platos"},
	{"id": 2, "descripcion": "Sacar la basura"},
	{"id": 3, "descripcion": "Limpiar el baño"},
	{"id": 4, "descripcion": "Hacer la cama"},
	{"id": 5, "descripcion": "Cocinar la cena"},
	{"id": 6, "descripcion": "Pasear al perro"},
	{"id": 7, "descripcion": "Hacer la compra"},
	{"id": 8, "descripcion": "Planchar la ropa"},
	{"id": 9, "descripcion": "Regar las plantas"},
	{"id": 10, "descripcion": "Lavar el coche"}
]

buscar_tarea_por_id(tareas, 1)
buscar_tareas_por_texto(tareas, "platos")
```

## Salida esperada
```python
Tarea encontrada por ID 3: {'id': 3, 'descripcion': 'Limpiar el baño'}

Tareas encontradas con el texto 'co': [{'id': 5, 'descripcion': 'Cocinar la cena'}, {'id': 7, 'descripcion': 'Hacer la compra'}, {'id': 10, 'descripcion': 'Lavar el coche'}]

Tareas encontradas con el texto 'cO': [{'id': 5, 'descripcion': 'Cocinar la cena'}, {'id': 7, 'descripcion': 'Hacer la compra'}, {'id': 10, 'descripcion': 'Lavar el coche'}]

Tareas encontradas con el texto 'almuerzo': []
```


# Resultado
```python
def buscar_tarea_por_id(tareas, id):
	for tarea in tareas:
		if tarea["id"] == id:
			print("Tarea encontrada:")
			print(tarea)
			return

	print("No se encontró la tarea.")  

def buscar_tareas_por_texto(tareas, texto):
	print("Resultados:")

	encontrada = False

	for tarea in tareas:
		if texto.lower() in tarea["descripcion"].lower():
			print(tarea)
			encontrada = True

	if encontrada == False:
		print("No se encontraron tareas.")

tareas = [
	{"id": 1, "descripcion": "Lavar los platos"},
	{"id": 2, "descripcion": "Sacar la basura"},
	{"id": 3, "descripcion": "Limpiar el baño"},
	{"id": 4, "descripcion": "Hacer la cama"},
	{"id": 5, "descripcion": "Cocinar la cena"}
]

buscar_tarea_por_id(tareas, 3)
buscar_tareas_por_texto(tareas, "co")
```
