
# ¿Cómo funciona?
Este programa calcula cuánto costaría un producto en diferentes monedas extranjeras a partir de una cantidad ingresada en moneda local.
1. Solicita al usuario que ingrese una cantidad en su moneda local.
2. Convierte la cantidad a las siguientes monedas:
	 - USD: cantidad * 0.050
	 - EUR: cantidad * 0.047
	 - GBP: cantidad * 0.039
	 - JPY: cantidad * 7.71
3. Muestra los resultados de cada conversión.

## Entradas
Cantidad en moneda local.

## Salidas
Cantidad equivalente en USD, EUR, GBP y JPY.

## Ejemplos
- Entrada: 100 -> USD: 5.00, EUR: 4.70, GBP: 3.90, JPY: 771.00
- Entrada: 250 -> USD: 12.50, EUR: 11.75, GBP: 9.75, JPY: 1927.50
- Entrada: 50 -> USD: 2.50, EUR: 2.35, GBP: 1.95, JPY: 385.50

# Resolución
```python
moneda_local = float(input("Introduce la cantidad de tu moneda local: "))

moneda_USD = moneda_local * 0.050
moneda_EUR = moneda_local * 0.047
moneda_GBP = moneda_local * 0.039
moneda_JPY = moneda_local * 7.71

print(f"\n-Entrada:{moneda_local}\n-USD:{moneda_USD}\n-EUR:{moneda_EUR}\n-GBP:{moneda_GBP}\n-JPY:{moneda_JPY}\n")
```
