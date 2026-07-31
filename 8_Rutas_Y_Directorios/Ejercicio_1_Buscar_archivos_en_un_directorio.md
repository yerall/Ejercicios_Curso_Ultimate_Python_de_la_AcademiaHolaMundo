
# Descripción
Aquí se trabaja con **rutas y directorios** utilizando el módulo `os`. El programa recibirá la ruta de una carpeta y mostrará los archivos que contiene.

# Instrucciones
1. Importa el módulo `os`.
2. Solicita al usuario la ruta de un directorio.
3. Comprueba si el directorio existe.
4. Muestra los archivos que se encuentran dentro.
5. Si la ruta no existe, muestra un mensaje de error.

## Casos de ejemplo
Si el usuario introduce:

```
C:\Documentos
```

El programa podría mostrar:
```
Archivos encontrados:

tareas.txt
notas.txt
python.py
```

Si la carpeta no existe
```
El directorio no existe.
```

## Resolución
```python
import os

ruta = input("Ingrese la ruta del directorio: ")

if os.path.exists(ruta):
    archivos = os.listdir(ruta)

    print("\nContenido del directorio:")

    for archivo in archivos:
        print(archivo)
else:
    print("El directorio no existe.")
```
