
# Descripción
Este ejercicio tiene como objetivo ayudarte a comprender cómo calcular el total de una cuenta después de aplicar un descuento. Es ideal para practicar operaciones matemáticas simples y trabajar con funciones.

## Instrucciones:
1. Define una función que tome como parámetros el total de una cuenta y un porcentaje de descuento.
2. Calcula el monto correspondiente al descuento.
3. Resta el descuento del total original.
4. Devuelve el total final.

## Casos de ejemplo:
- Si tienes una cuenta de $1000 y un descuento del 20%, el resultado debe ser $800.
- ¿Qué pasa si aplicas un descuento del 0%? ¿Y del 100%?

# Resolución
```python
def calculo_descuento(total_cuenta, monto_descuento):
	descuento = total_cuenta * (monto_descuento / 100)
	monto_con_descuento = total_cuenta - descuento
	return monto_con_descuento

total_cuenta = int(input("Ingrese el monto de la cuenta: "))
monto_descuento = int(input("Ingrese el porcentaje del descuenta a la cuenta: "))

print(f"""
	\nEl monto de la cuenta es de {total_cuenta}
	\nEl monto del descuento es de {monto_descuento}%
	\nEl monto total con el descuento es {calculo_descuento(total_cuenta,monto_descuento)}
""")
```

