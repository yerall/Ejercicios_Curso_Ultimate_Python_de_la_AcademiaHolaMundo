
# Descripción
Este ejercicio te permitirá practicar cómo convertir valores entre diferentes unidades de tiempo. Es una excelente oportunidad para trabajar con estructuras condicionales y comprender las relaciones entre unidades de tiempo.

## Instrucciones:
1. Define tres funciones:
	- a_segundos: Convierte una cantidad y unidad dada a segundos.
	- de_segundos: Convierte una cantidad en segundos a otra unidad deseada.
	- convertir_tiempo: Usa las dos funciones anteriores para realizar una conversión completa entre dos unidades.
2. Considera las siguientes unidades:
3. segundo, minuto, hora, día, mes (30 días), año (365 días).

## Casos de ejemplo
- Convierte 2 horas a minutos: ¿Cuántos minutos son?
- Intenta convertir 5 minutos a años: ¿Qué mensaje de error obtienes?

# Resolución
```python
def a_segundos(cantidad, unidad):
	if unidad == 'segundo':
		return cantidad
	elif unidad == 'minuto':
		return cantidad * 60
	elif unidad == 'hora':
		return cantidad * 3600
	elif unidad == 'dia':
		return cantidad * 86400
	elif unidad == 'mes':
		return cantidad * 2592000 # Aproximadamente 30 días
	elif unidad == 'año':
		return cantidad * 31536000 # Aproximadamente 365 días
	else:
		return "ERROR"

def de_segundos(cantidad, unidad):
	if unidad == 'segundo':
		return cantidad
	elif unidad == 'minuto':
		return cantidad / 60
	elif unidad == 'hora':
		return cantidad / 3600
	elif unidad == 'dia':
		return cantidad / 86400
	elif unidad == 'mes':
		return cantidad / 2592000 # Aproximadamente 30 días
	elif unidad == 'año':
		return cantidad / 31536000 # Aproximadamente 365 días
	else:
		return "ERROR"

def convertir_tiempo(cantidad, unidad_origen, unidad_destino):
	segundos = a_segundos(cantidad, unidad_origen)
	if segundos is None:
		print("Unidad de origen no válida")
	else:
		resultado = de_segundos(segundos, unidad_destino)
		if resultado is None:
			print("Unidad de destino no válida")
		else:
			print(f"{cantidad} {unidad_origen}(s) son {resultado} {unidad_destino}(s)")

cantidad = float(input("Ingrese la cantidad: "))
unidad_origen = input("Unidad de origen (segundo, minuto, hora, dia): ")
unidad_destino = input("Unidad de destino (segundo, minuto, hora, dia): ")
convertir_tiempo(cantidad, unidad_origen, unidad_destino)
```
