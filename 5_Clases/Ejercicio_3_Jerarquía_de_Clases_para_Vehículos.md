
# Descripción
Este ejercicio define una jerarquía de clases para representar diferentes tipos de vehículos. Se implementa una clase base Vehiculo con atributos comunes y subclases especializadas para coches, motos y bicicletas.

## Clases
1. Vehiculo (Clase Base): Representa un vehículo genérico con los atributos:
	- marca: Marca del vehículo.
	- modelo: Modelo del vehículo

## Métodos
- `descripcion()`: Devuelve una descripción en formato "`Marca: <marca>, Modelo: <modelo>`".
- Coche (Subclase de Vehiculo): Especializa la clase base para coches y redefine el método `descripcion()` para incluir el prefijo "`Coche - `".
- Moto (Subclase de Vehiculo): Especializa la clase base para motos y redefine el método `descripcion()` para incluir el prefijo "`Moto - `".
- Bicicleta (Subclase de Vehiculo): Especializa la clase base para bicicletas y redefine el método `descripcion()` para incluir el prefijo "`Bicicleta - `".

## Pruebas
1. Crear instancias de cada tipo de vehículo con las siguientes marcas y modelos:
	- Coche: "Nissan", "Versa"
	- Moto: "Yamaha", "MT-07"
	- Bicicleta: "Giant", "Escape 3"
	- Llamar al método `descripcion()` en cada instancia y verificar la salida

## Datos de prueba y salida esperada
```
Coche - Marca: Nissan, Modelo: Versa
Moto - Marca: Yamaha, Modelo: MT-07
Bicicleta - Marca: Giant, Modelo: Escape 3
```

# Resolución
```python
class Vehiculo:
	def __init__(self, marca, modelo):
		self.marca = marca
		self.modelo = modelo

	def descripcion(self):
		return f"Marca: {self.marca}, Modelo: {self.modelo}"

class Coche(Vehiculo):
	def descripcion(self):
		return f"Coche - {super().descripcion()}"

class Moto(Vehiculo):
	def descripcion(self):
		return f"Moto - {super().descripcion()}"

class Bicicleta(Vehiculo):
	def descripcion(self):
		return f"Bicicleta - {super().descripcion()}"

coche = Coche("Nissan", "Versa")
moto = Moto("Yamaha", "MT-07")
bicicleta = Bicicleta("Giant", "Escape 3")

print(coche.descripcion())
print(moto.descripcion())
print(bicicleta.descripcion())
```
