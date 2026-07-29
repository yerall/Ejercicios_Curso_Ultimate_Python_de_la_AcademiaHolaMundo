
# Descripción
En este ejercicio aprenderás a utilizar paquetes para organizar el código de un programa.

## Instrucciones

1. Crea un paquete llamado biblioteca.
2. En libros.py, crea una función para mostrar una lista de libros.
3. En prestamos.py, crea una función para mostrar los libros prestados.
4. Desde el programa principal importa ambas funciones y muéstralas.

## Casos de ejemplo
El programa debe mostrar:

```
Libros disponibles:
Python
Java
C++

Libros prestados:
Python
```

# Resolución

## Archivo `libros.py`
```python
def mostrar_libros():
    print("Libros disponibles:")
    print("Python")
    print("Java")
    print("C++")
```

## Archivo `prestamos.py`
```python
def mostrar_prestados():
    print("Libros prestados:")
    print("Python")
```

## Archivo `main.py`
```python
from biblioteca.libros import mostrar_libros
from biblioteca.prestamos import mostrar_prestados

mostrar_libros()
print()
mostrar_prestados()
```
