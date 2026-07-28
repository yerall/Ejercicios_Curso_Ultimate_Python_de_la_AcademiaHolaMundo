
# Descripción
En este ejercicio aprenderás a utilizar un módulo creado por ti para realizar operaciones matemáticas. Supón que existe un archivo llamado operaciones.py con las funciones `sumar()`, `restar()`, `multiplicar()` y `dividir()`.

## Instrucciones
1. Importa el módulo `operaciones`.
2. Solicita al usuario dos números.
3. Muestra un menú con las cuatro operaciones.
4. Ejecuta la operación elegida utilizando las funciones del módulo.
5. Muestra el resultado.

## Casos de ejemplo
- Si el usuario ingresa 10 y 5 y selecciona sumar, el resultado debe ser 15.
- Si selecciona dividir, el resultado debe ser 2.

# Resolución

## Archivo `operaciones.py`

```python
def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def multiplicar(a, b):
    return a * b

def dividir(a, b):
    return a / b
```

## Archivo `main.py`

```python
import operaciones

numero1 = float(input("Primer número: "))
numero2 = float(input("Segundo número: "))

print("1. Sumar")
print("2. Restar")
print("3. Multiplicar")
print("4. Dividir")

opcion = int(input("Seleccione una opción: "))

if opcion == 1:
    print(operaciones.sumar(numero1, numero2))
elif opcion == 2:
    print(operaciones.restar(numero1, numero2))
elif opcion == 3:
    print(operaciones.multiplicar(numero1, numero2))
elif opcion == 4:
    print(operaciones.dividir(numero1, numero2))
else:
    print("Opción incorrecta.")
```
