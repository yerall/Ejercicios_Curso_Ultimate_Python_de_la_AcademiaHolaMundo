
# Descripción.
Este programa calcula el cambio que debe darse al cliente según el pago y el total de la cuenta.

## Pruebas.
1. Entrada: Total: 100, Pago: 100.
	- Salida: "El cliente ha pagado el monto exacto. No se requiere cambio".
2. Entrada: Total: 50, Pago: 40.
	- Salida: "El cliente ha pagado menos. Faltan 10.0 dólares".
3. Entrada: Total: 75, Pago: 100.
	- Salida: "El cliente ha pagado de más. El cambio es 25.0 dólares”.

# Resolución
```python
total_cuenta = float(input("Ingrese el total de la cuenta: "))

if total_cuenta <= 0:
    print("El total de la cuenta debe ser mayor que 0.")
else:
    pago_cliente = float(input("Ingrese el pago del cliente: "))
    diferencia = pago_cliente - total_cuenta
    if diferencia == 0:
        print("El cliente pagó el monto exacto.")
    elif diferencia < 0:
        print(f"Faltan {-diferencia} dólares para completar el pago.")
    else:
        print(f"El cambio es de {diferencia} dólares.")
```
