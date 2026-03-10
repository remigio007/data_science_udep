# Data Science UDEP

## Apuntes del Curso

1. **Sesión 3: Introducción a Python**

**-_Formatos de String:_**

**|| Enfocada a números ||**

| Método                | Sintaxis.        | Resultado.   | Lo que hace (3000000).                                   |
|-----------------------|------------------|--------------|----------------------------------------------------------|
| F-String (Moderno)    | f"{n:,}"         | 3,000,000    | Agrega comas de miles (automático).                      |
| F-String + Decimales  | f"{n:,.2f}"      | 3,000,000.00 | Comas de miles y 2 decimales fijos.                      |
| Operador % (Antiguo)  | "%d" % n         | 3000000      | Formato entero simple (sin comas).                       |
| Operador % (Flotante) | "%2.3f" % n      | 3000000.000  | Convierte a decimal con 3 dígitos tras el punto.         |
| Método .format()      | "{:,}".format(n) | 3,000,000    | Igual al f-string, pero funciona en Python viejo (2.7+). |
| Locale (Regional)     | f"{n:n}"         | 3.000.000    | Usa el separador según tu país (ej. punto en España).    |

**|| Enfocado a cadenas de texto ||**
| Acción            | Sintaxis (F-String) | Resultado (con texto="Hola") | Descripción                                                |
|-------------------|---------------------|------------------------------|------------------------------------------------------------|
| Alinear Izquierda | f"\|{texto:<10}\|"  | \|Hola \|                    | Reserva 10 espacios y pega el texto a la izquierda.        |
| Alinear Derecha   | f"\|{texto:>10}\|"  | \| Hola\|                    | Reserva 10 espacios y pega el texto a la derecha.          |
| Centrar           | f"\|{texto:^10}\|"  | \| Hola \|                   | Centra el texto en el ancho total.                         |
| Rellenar          | f"{texto:*^10}"     | ***Hola****                  | Rellena el espacio vacío con un carácter (en este caso *). |
| Truncar (Cortar)  | f"{texto:.2}"       | Ho                           | Solo muestra los primeros "X" caracteres.                  |
| Combinar          | f"{texto:*>10.3}"   | *******Hol                   | Reserva 10, rellena con * y corta a 3 letras.              |

**-_Operadores:_**

**|| Aritméticos ||**

| Operador | Descripción      | Ejemplo (a=10, b=3) | Resultado |
|----------|------------------|---------------------|-----------|
| +        | Suma             | a + b               | 13        |
| -        | Resta            | a - b               | 7         |
| *        | Multiplicación   | a * b               | 30        |
| /        | División (float) | a / b               | 3.333...  |
| //       | División Entera  | a // b              | 3         |
| %        | Módulo (residuo) | a % b               | 1         |
| **       | Potencia         | a ** b              | 1000      |

**|| Comparación ||**

| Operador | Descripción       | Ejemplo        |
|----------|-------------------|----------------|
| ==       | Igual a           | 5 == 5 → True  |
| !=       | Diferente de      | 5 != 3 → True  |
| >        | Mayor que         | 5 > 10 → False |
| <        | Menor que         | 5 < 10 → True  |
| >=       | Mayor o igual que | 5 >= 5 → True  |
| <=       | Menor o igual que | 5 <= 2 → False |

**|| Lógicos ||**

| Operador | Descripción                             | Ejemplo                    |
|----------|-----------------------------------------|----------------------------|
| and      | Devuelve True si ambos son ciertos      | (5 > 3) and (2 < 4) → True |
| or       | Devuelve True si al menos uno es cierto | (5 > 8) or (2 < 4) → True  |
| not      | Invierte el resultado (no es)           | not(5 > 3) → False         |


**|| Asignación ||**

| Operador             | Ejemplo                                       | Equivalente |
|----------------------|-----------------------------------------------|-------------|
| =                    | x = 5                                         | x = 5       |
| +=                   | x += 3                                        | x = x + 3   |
| -=                   | x -= 1                                        | x = x - 1   |
| *=, /=, //=, %=, **= | Igual que arriba con su respectiva operación. |             |

**|| Pertenencia e Identidad ||**

| Operador | Descripción                              | Ejemplo                  |
|----------|------------------------------------------|--------------------------|
| in       | True si el valor está en la secuencia    | 'a' in 'hola' → True     |
| not in   | True si el valor NO está en la secuencia | 'z' not in 'hola' → True |
| is       | True si son el mismo objeto (identidad)  | a is b                   |
| is not   | True si no son el mismo objeto           | a is not b               |


2. **Ejercicios de Python**
    - Ejercicios con creación de variables
    - Crear la variable lado de un cuadrado de longitud 5 y calcular su área.
    - Crear un número complejo con la parte imaginaria -3 y la real 2
    - Crear las variables precio unitario = 1500 y número de productos = 2000, hallando la venta total. Elegir los tipos de variables correctos.
    - Hallar el promedio de las estaturas de tres personas que miden 1.65, 1.93 y 1.86 centímetros.
    - Crear una cadena que diga su nombre, apellidos, profesión y ocupación actual. Utilizar cualquier forma o método.
    - Crear un código para expresar, en una cadena, la suma de dos números.
    - Ejemplo: 7 + 5 = 12. La respuesta del código debe ser: "El resultado de suma 7 + 5 es 12".
    - Escribir código Python para calcular el IMC (índice de masa corporal), que pida al usuario su peso (en kg) y estatura (en metros). Pista: El IMC es igual a la altura dividida entre el cuadrado de la estatura. Mostrar el resultados con dos decimales redondeados.
    - Escribir un programa que pregunte al usuario por la cantidad de trabajadores, por el número de horas trabajadas y el coste por hora. Después, debe mostrar por pantalla el monto totalapagar a los trabajadores. Escriba un mensaje de salida acorde con el problema.
    - Escribir un programa en Python que pida al usuario dos números enteros (primero un número mayor (n) y luego el menor (m)) y muestre por pantalla el siguiente mensaje: la división de (n) entre (m) da un cociente (c) y un resto (r) donde (n) y (m) son los números que ha ingresado el usuario y (c) y (r) son el cociente y el resto de la división entera respectivamente
    - Escribir un programa que pregunte el nombre del usuario en la consola y después de que el usuario lo introduzca, muestre por pantalla un mensaje similar a: "(el nombre ingresado) tiene (n) letras, donde (el nombre ingresado) es el nombre de usuario en mayúsculas y (n) es el número de letras que tienen el nombre. Pista: Utilice la función len() para calcular el número de letras que tiene una cadena.
    - Los teléfonos de un país tienen el siguiente formato prefijo-número-extension donde el prefijo es el código del país (para Perú es +51), y la extensión tiene dos dígitos (por ejemplo +51-9990941893-32). Escribir un programa que pregunte por un número de teléfono con este formato y muestre por pantalla el número de teléfono sin el prefijo y la extensión.
    - Elaborar un programa en Python en que el usuario pida los catetos de un triángulo rectángulo y que calcule la hipotenusa y su área. Use sólo las operaciones estándar de Python. No use librerias que todavía no se han explicado. Pista: Para elevar un número a una potencia, puede utilizar el operador (**).
    - Pedir por consola el nombre y el apellido de una persona y mostrar su usuario, que se conforma por las 3 primeras letras del nombre y del apellido. Ejemplo: Juan Perez tendría como usuario "Juaper"
    - Asigne una variable entera y otra variable flotante. Haga la suma, resta, multiplicación y división. Pregunte los tipos de variables que dan los resultados. ¿Nota algo?
    - Use el método str.format() con más de un formato para expresar: la empresa en la cual trabaja, el área en la que se desempeña, la cantidad de años de experiencia que tiene a la fecha, su profesion y su cargo actual. No se olvide de utilizar más de un formato hecho en clase.