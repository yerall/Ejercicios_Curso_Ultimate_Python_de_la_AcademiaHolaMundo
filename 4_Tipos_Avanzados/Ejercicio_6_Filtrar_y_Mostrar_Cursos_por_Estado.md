
# Descripción
Este ejercicio organiza una lista de cursos en tres grupos según su estado:
1. En progreso.
2. Completados.
3. No iniciados.

El programa debe mostrar cada grupo con un título correspondiente.

## Entrada
Una lista de diccionarios, donde cada diccionario tiene las claves:
- 'nombre' (str): Nombre del curso.
- 'estado' (str): Estado del curso.

## Salida
Tres listas separadas según el estado de los cursos.

## Ejemplo de uso:
```python
cursos = [
	{"nombre": "HTML", "estado": "en progreso"},
	{"nombre": "CSS", "estado": "completado"},
	{"nombre": "Python", "estado": "en progreso"},
	{"nombre": "Docker", "estado": "no iniciado"},
	{"nombre": "Java", "estado": "completado"}
]

mostrar_cursos_por_estado(cursos)
```

# Resolución
```python
def mostrar_cursos_por_estado(cursos):
	print("Cursos en progreso:")

	for curso in cursos:
		if curso["estado"] == "en progreso":
			print("-", curso["nombre"])

	print("\nCursos completados:")

	for curso in cursos:
		if curso["estado"] == "completado":
			print("-", curso["nombre"])

	print("\nCursos no iniciados:")

	for curso in cursos:
		if curso["estado"] == "no iniciado":
			print("-", curso["nombre"])

cursos = [
	{"nombre": "HTML", "estado": "en progreso"},
	{"nombre": "CSS", "estado": "completado"},
	{"nombre": "Python", "estado": "en progreso"},
	{"nombre": "Docker", "estado": "no iniciado"},
	{"nombre": "Java", "estado": "completado"}
]

mostrar_cursos_por_estado(cursos)
```
