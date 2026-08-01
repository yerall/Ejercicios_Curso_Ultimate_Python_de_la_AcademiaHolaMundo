
# Descripción
Ahora utilizaremos **rutas, directorios, listas y diccionarios**. El programa debe revisar una carpeta y contar cuántos archivos existen según su extensión.

## Instrucciones
1. Solicita al usuario una ruta.
2. Comprueba que el directorio exista.
3. Recorre los archivos de la carpeta.
4. Obtén la extensión de cada archivo.
5. Cuenta cuántos archivos existen de cada tipo.
6. Muestra los resultados.

## Ejemplo de uso
```
documentos/
    tarea.py
    programa.py
    notas.txt
    examen.txt
    foto.jpg
```

El resultado debería indicar:
```
Archivos Python: 2
Archivos TXT: 2
Archivos JPG: 1
```

## Resolución
```python
import os

ruta = input("Ingrese la ruta del directorio: ")

if os.path.exists(ruta):
    extensiones = {}
    archivos = os.listdir(ruta)

    for archivo in archivos:
        nombre, extension = os.path.splitext(archivo)
        if extension != "":
            extension = extension.lower()
            if extension in extensiones:
                extensiones[extension] += 1
            else:
                extensiones[extension] = 1
    print("\nCantidad de archivos:")

    for extension in extensiones:
        print(extension, ":", extensiones[extension])
else:
    print("El directorio no existe.")
```
