# reto-7
Imprimir del 1 al 100 con su respectivo cuadrado:

    for i in range(1, 101):
        print(i, "al cuadrado es", i * i)

Imprimir impares del 1 al 999 y pares del 2 al 1000

    print("Impares del 1 al 999:")
    for i in range(1, 1000, 2):
        print(i)
    print("\nPares del 2 al 1000:")
    for i in range(2, 1001, 2):
        print(i)

Imprimir pares en forma descendente hasta 2, menores o iguales a n (n ≥ 2)

    n = int(input("Ingrese un número mayor o igual a 2: "))
    if n % 2 != 0:
       n = n - 1
    for i in range(n, 1, -2):
       print(i)

Imprimir números del 1 a n con su respectivo factorial

    n = int(input("Ingrese un número natural: "))
    for i in range(1, n + 1):
       f = 1
       for j in range(1, i + 1):
           f = f * j
       print("El factorial de", i, "es", f)

Calcular 2 elevado a la n usando ciclo for
    
    n = int(input("Ingrese el exponente n: "))
    resultado = 1
    for i in range(n):
        resultado = resultado * 2
    print("2 elevado a", n, "es", resultado)

Calcular xⁿ (x real, n natural) sin usar **

    for tabla in range(1, 10):
        print("Tabla del", tabla)
        for i in range(1, 11):
            print(tabla, "x", i, "da", tabla * i)
        print()

Aproximar la exponencial e^x con n términos de la serie de Taylor:

    import math
    
    x = float(input("Ingrese el valor de x: "))
    n = int(input("Ingrese el número de términos: "))
    suma = 0
    
    for i in range(n + 1):
       f = 1
       for j in range(1, i + 1):
           f = f * j
       suma = suma + (x ** i) / f
    
    print("Aproximación de exp(", x, ") con", n, "términos es:", suma)
    print("Valor real usando math.exp:", math.exp(x))
    print("Diferencia:", abs(math.exp(x) - suma))
