
# ¿Cómo funciona?
Este programa asegura que los nombres ingresados por el usuario estén correctamente formateados.
1. Solicita al usuario los siguientes datos:
	- Primer nombre.
	- Segundo nombre (opcional).
	- Primer apellido.
	- Segundo apellido (opcional).
2. Elimina espacios innecesarios y capitaliza la primera letra de cada palabra.
3. Combina todos los nombres y apellidos en un nombre completo correctamente formateado.

## Entradas
- Primer nombre, segundo nombre (opcional), primer apellido, segundo apellido (opcional).

## Salidas
Nombre completo formateado.

## Ejemplos
- Entrada: " juan ", " carlos ", " perez ", " gomez " -> Salida: "Juan Carlos Perez Gomez"
- Entrada: " maria ", "", " lopez ", " martinez " -> Salida: "Maria Lopez Martinez"
- Entrada: " nicolas ", "", " schurmann ", "" -> Salida: "Nicolas Schurmann”

# Resolución
```python
nombre = input("Ingrese el primer nombre (Obligatorio): ").strip().capitalize()
segundo_nombre = input("Ingrese el segundo nombre (Opcional, presione enter para continuar): ").strip().capitalize()
primer_apellido = input("Ingrese el primer apellido (Obligatorio): ").strip().capitalize()
segundo_apellido = input("Ingrese el segundo apellido (Opcional, presione enter para continuar): ").strip().capitalize()

union = f"{nombre} {segundo_nombre} {primer_apellido} {segundo_apellido}".replace("  ", " ")
print(f"El nombre ingresado es {union.title()}")
```
