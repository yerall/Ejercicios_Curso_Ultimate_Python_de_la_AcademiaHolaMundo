
# Descripción
En este ejercicio trabajaremos con **inyección de dependencias**. La idea será crear una clase que necesite guardar información, pero que **no se encargue directamente de decidir dónde guardarla**. En lugar de eso, recibirá una función que realizará el guardado.

## Instrucciones
1. Crea una función llamada `guardar_archivo()`.
2. La función debe recibir una ruta y un texto.
3. Crea una clase llamada `Nota`.
4. La clase debe recibir una función para guardar la información.
5. Crea una nota y guárdala en un archivo.

## Caso de ejemplo
El usuario introduce:
```
Ruta: nota.txt
Texto: Estudiar módulos y directorios
```

El programa crea el archivo `nota.txt` con:
```
Estudiar módulos y directorios
```

## Resolución
```python
def guardar_archivo(ruta, texto):
    archivo = open(ruta, "w")
    archivo.write(texto)
    archivo.close()
    print("Archivo guardado correctamente.")

class Nota:
    def __init__(self, guardar):
        self.guardar = guardar
    def crear_nota(self, ruta, texto):
        self.guardar(ruta, texto)

ruta = input("Nombre del archivo: ")
texto = input("Escriba la nota: ")

nota = Nota(guardar_archivo)
nota.crear_nota(ruta, texto)
```
