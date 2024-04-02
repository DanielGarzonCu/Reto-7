# Reto-7

# 1 
Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

```mermaid

```

```ruby
numero : int = 1
while numero <= 100:
    print(f"{numero}: {numero ** 2}")
    numero += 1

```

# 2 
Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
```ruby
# Números impares del 1 al 999 
print("Números impares del 1 al 999:")
impar = 1
while impar <= 999:
    print(impar)
    impar += 2

# Números pares del 2 al 1000 
print("\nNúmeros pares del 2 al 1000:")
par = 2
while par <= 1000:
    print(par)
    par += 2

```
# 3 
Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado
```ruby
# Solicitar al usuario que ingrese un número natural n mayor que 2
n = int(input("Ingrese un número natural n ≥ 2: "))

# Verificar si n es mayor que 2
if n < 2:
    print("El número ingresado no es válido. Debe ser mayor o igual a 2.")
else:
    print(f"Números pares en forma descendente hasta 2 que son menores o iguales a {n}:")
    par = n if n % 2 == 0 else n - 1  # Comenzar desde n si es par, o desde n-1 si es impar
    while par >= 2:
        print(par)
        par -= 2

```

# 4 
En 2022 el país A tendrá una población de 25 millones de habitantes y el país B de 18.9 millones. Las tasas de crecimiento anual de la población serán de 2% y 3% respectivamente. Desarrollar un algoritmo para informar en que año la población del país B superará a la de A.

```ruby
def año_poblacion_superada(poblacion_A, tasa_crecimiento_A, poblacion_B, tasa_crecimiento_B):
    año = 2022
    while poblacion_B <= poblacion_A:
        año += 1
        poblacion_A *= (1 + tasa_crecimiento_A)
        poblacion_B *= (1 + tasa_crecimiento_B)
    return año

# Ejemplo de uso
año_superado = año_poblacion_superada(25, 0.02, 18.9, 0.03)
print("La población de B superará a la de A en el año:", año_superado)

```

# 5 
Imprimir el factorial de un número natural n dado.

```ruby
n = int(input("Ingrese un número natural para calcular su factorial: "))
def factorial(n):
    if n < 0:
        print("No se puede calcular el factorial de un número negativo.")
    elif n == 0:
        print("El factorial de 0 es 1.")
    else:
        resultado = 1
        i = 1
        while i <= n:
            resultado *= i
            i += 1
        print(f"El factorial de {n} es: {resultado}")
factorial(n)
```

# 6 
Implementar un algoritmo que permita adivinar un número dado de 1 a 100, preguntando en cada caso si el número es mayor, menor o igual.

```ruby
def adivinar_numero():
    print("Piensa en un número del 1 al 100.")
    print("Lo adivinare.")
    print("Por favor, responde con 'mayor', 'menor' o 'igual'.")

    limite_inferior = 1
    limite_superior = 100
    intentos = 0

    while True:
        intento = (limite_inferior + limite_superior) // 2
        respuesta = input(f"¿Es {intento} tu número? ")

        if respuesta == "igual":
            print(f"¡Adiviné tu número en {intentos} intentos!")
            break
        elif respuesta == "mayor":
            limite_inferior = intento + 1
        elif respuesta == "menor":
            limite_superior = intento - 1
        else:
            print("Por favor, responde con 'mayor', 'menor' o 'igual'.")

        intentos += 1
adivinar_numero()
```
# 7 
Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.
```ruby
def print_divisors(n):
    print("Los divisores del número son:")
    i = 1 
    while i <= n: 
        if n % i == 0:
            print(i)
        i += 1 

numero = int(input("Ingrese un número entre 2 y 50: "))

if 2 <= numero <= 50:
    print_divisors(numero)
else:
    print("El número ingresado no está en el rango permitido (2-50).")
```
# 8 
Implementar el algoritmo que muestre los números primos del 1 al 100. Nota: use funciones
```ruby
def es_primo(numero):
    if numero < 2:
        return False
    i = 2
    while i <= int(numero ** 0.5):
        if numero % i == 0:
            return False
        i += 1
    return True

print("Los números primos del 1 al 100 son:")
numero = 1
while numero <= 100:
    if es_primo(numero):
        print(numero) 
    numero += 1
```
