
# ¿Cómo funciona?
Este programa convierte una temperatura dada en grados Celsius a dos escalas diferentes: Fahrenheit y Kelvin.
1. Pide al usuario que ingrese una temperatura en grados Celsius.
2. Realiza las siguientes conversiones:
	- **Celsius a Fahrenheit**: (grados Celsius * 9/5) + 32
	- **Celsius a Kelvin**: grados Celsius + 273.15
3. Muestra las temperaturas convertidas en ambas escalas.

## Entradas
Temperatura en grados Celsius (puede ser un número entero o decimal).

## Salidas
1. Temperatura en grados Celsius.
2. Temperatura en grados Fahrenheit.
3. Temperatura en grados Kelvin.

## Ejemplos
- Entrada: 0 -> Fahrenheit: 32, Kelvin: 273.15
- Entrada: 100 -> Fahrenheit: 212, Kelvin: 373.15
- Entrada: -40 -> Fahrenheit: -40, Kelvin: 233.15
- Entrada: 37 -> Fahrenheit: 98.6, Kelvin: 310.15

# Resolución
```python
celsius = float(input("Por favor ingrese la temperatura en grados Celsius: "))
operacion_fahrenheit = ((celsius * 9) / 5) + 32
operacion_kelvin = celsius + 273.15

print(f"""\nLa temperatura ingresada es {celsius} grados C.
    \nEn Fahrenheit, esto es {operacion_fahrenheit} grados F.
    \nEn Kelvin, esto es {operacion_kelvin} K.
""")
```

