
# Descripción.
Este programa convierte una cantidad de dinero de una divisa a otras.
Divisas soportadas: USD (dólares estadounidenses), EUR (euros), y MXN (pesos mexicanos).
El usuario ingresa la cantidad y la divisa de origen, y el programa calcula las cantidades equivalentes en las otras divisas.

## Tasas de Conversión.
- 1 USD = 0.95 EUR
- 1 USD = 20.28 MXN
- 1 EUR = 21.36 MXN

## Pruebas.
1. Entrada: 100 USD. Salida: 95 EUR, 2028 MXN.
2. Entrada: 100 EUR. Salida: 105.26 USD, 2136 MXN.
3. Entrada: 100 MXN. Salida: 4.93 USD, 4.68 EUR.
4. Entrada: Divisa no válida. Salida: "Divisa no válida. Por favor, elige entre USD, EUR o MXN.”.

# Resolución
```python
tasa_USD_a_EUR = 0.95
tasa_USD_a_MXN = 20.28
tasa_EUR_a_MXN = 21.36

cantidad = float(input("Introduce la cantidad a convertir: "))
divisa_origen = input("Introduce la divisa de origen (USD, EUR o MXN): ").upper()

if divisa_origen in ["USD", "EUR", "MXN"]:
	divisa_destino = 0
	if divisa_origen == "USD":
		cantidad_euros = cantidad * tasa_USD_a_EUR
		cantidad_pesos = cantidad * tasa_USD_a_MXN
		print(f"Por tu(s): {cantidad} dolar(es) obtendras: {cantidad_euros} euros o {cantidad_pesos} pesos mexicanos.")
	elif divisa_origen == "EUR":
		cantidad_dolares = cantidad / tasa_USD_a_EUR
		cantidad_pesos = cantidad * tasa_EUR_a_MXN
		print(f"Por tu(s): {cantidad} euro(s) obtendrás: {cantidad_dolares} dólares o {cantidad_pesos} pesos mexicanos.")
	else:
		cantidad_dolares = cantidad / tasa_USD_a_MXN
		cantidad_euros = cantidad / tasa_EUR_a_MXN
		print(f"Por tu(s): {cantidad} peso(s) obtendrás: {cantidad_dolares} dólares o {cantidad_euros} euros.")
elif divisa_origen not in ["USD", "EUR", "MXN"]:
	print("Divisa de origen no válida.")
	exit()
else:
	print("ERROR")
```
