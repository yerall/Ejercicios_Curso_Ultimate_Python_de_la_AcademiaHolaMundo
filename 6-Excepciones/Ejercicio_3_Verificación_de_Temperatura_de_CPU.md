
# Descripción
Se presenta una función que verifica la temperatura de la CPU. Si la temperatura alcanza niveles críticos, se lanza una excepción personalizada. También hay mensajes de advertencia para temperaturas elevadas pero no críticas. Debes lanzar distintos mensajes de advertencia cuando la temperatura se encuentra sobre 75 y 90 grados celsius, pero debes lanzar un error si la temperatura es mayor a 100 grados celsius

## Datos de Prueba
```python
try:
	temperatura_actual = 95 # Cambia este valor para probar diferentes escenarios
	check_cpu_temperature(temperatura_actual)
except OverheatingError as e:
	print(e)
```

## Salida Esperada
```python
Advertencia: La temperatura de la CPU es muy alta.
```

# Resolución
```python
class ErrorTemperatura(Exception):
	pass

def revisar_temperatura(temperatura):
	if temperatura > 100:
		raise ErrorTemperatura("Error: La temperatura de la CPU es crítica.")
	elif temperatura >= 90:
		print("Advertencia: La temperatura de la CPU es muy alta.")
	elif temperatura >= 75:
		print("Advertencia: La temperatura de la CPU está elevada.")
	else:
		print("La temperatura de la CPU es normal.")

try:
	temperatura = int(input("Ingrese la temperatura de la CPU: "))
	revisar_temperatura(temperatura)
except ErrorTemperatura as error:
	print(error)
```
