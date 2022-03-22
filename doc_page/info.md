# Introduction

Python es un lenguaje de programación potente y fácil de aprender. Posee eficientes estructuras de datos de alto nivel y un enfoque sencillo pero efectivo de la programación orientada a objetos. La sintaxis elegante, los tipos de datos dinámicos y el hecho de ser un lenguaje interpretado hacen de Python un lenguaje ideal para la creación de scripts y el desarrollo rápido de aplicaciones en todo tipo de áreas y plataformas.

El intérprete de Python y la biblioteca estándar están disponibles en forma de código fuente o código ejecutable para los principales sistemas operativos en el sitio web oficial de Python, https://www.python.org/, y puede distribuirse libremente. Ese sitio web también contiene información sobre muchos módulos, programas y herramientas para Python, así como documentación adicional.

El intérprete de Python puede ampliarse fácilmente con nuevas funciones y tipos de datos implementados en C o C++ (u otros lenguajes accesibles desde C). Python es también adecuado como lenguaje de extensión de aplicaciones.

# Hello World
El ejemplo siguiente muestra la plantilla de programa básico de Python 3 

    def main():
        print("¡Hola, mundo!")


    if __name__ == "__main__":
        main()

Las instrucciones que forman el programa, se escribirían dentro de la función main(), es decir, sangradas cuatro espacios.

    def main():
    print("¡Hola, mundo!")
    print("¡Adiós, mundo!")


    if __name__ == "__main__":
        main()

# Tipos de datos
## Enteros y decimales
Python distingue entre números enteros y decimales. Al escribir un número decimal, el separador entre la parte entera y la parte decimal es un punto.

        >>> 3
        3
        >>> 4.5
        4.5

Si se escribe un número con parte decimal 0, Python considera el número como número decimal.

        >>> 3.0
        3.0

Se puede escribir un número decimal sin parte entera, pero lo habitual es escribir siempre la parte entera:

        >>> .3
        0.3

## Operaciones basicas

Las cuatro operaciones aritméticas básicas son la suma (+), la resta (-), la multiplicación (*) y la división (/).

Al hacer operaciones en las que intervienen números enteros y decimales, el resultado es siempre decimal. En el caso de que el resultado no tenga parte decimal, Python escribe 0 como parte decimal para indicar que el resultado es un número decimal:

    >>> 4.5 * 3
    13.5
    >>> 4.5 * 2
    9.0

Al sumar, restar o multiplicar números enteros, el resultado es entero.

    >>> 1 + 2
    3
    >>> 3 - 4
    -1
    >>> 5 * 6
    30

Al dividir números enteros, el resultado es siempre decimal, aunque sea un número entero. Cuando Python escribe un número decimal, lo escribe siempre con parte decimal, aunque sea nula.

    >>> 9 / 2
    4.5
    >>> 9 / 3
    3.0

Dividir por cero genera un error:

    >>> 5 / 0
    Traceback (most recent call last):
    File "<pyshell#22>", line 1, in <module>
        5 / 0
    ZeroDivisionError: division by zero
    >>>

# Variables
En algunos lenguajes de programación, las variables se pueden entender como "cajas" en las que se guardan los datos, pero en Python las variables son "etiquetas" que permiten hacer referencia a los datos (que se guardan en unas "cajas" llamadas objetos).

Python es un lenguaje de programación orientado a objetos y su modelo de datos también está basado en objetos.

Para cada dato que aparece en un programa, Python crea un objeto que lo contiene. Cada objeto tiene:

* un identificador único (un número entero, distinto para cada objeto). El identificador permite a Python referirse al objeto sin ambigüedades.
* un tipo de datos (entero, decimal, cadena de caracteres, etc.). El tipo de datos permite saber a Python qué operaciones pueden hacerse con el dato.
* un valor (el propio dato).

Así, las variables en Python no guardan los datos, sino que son simples nombres para poder hacer referencia a esos objetos. Si escribimos la instrucción ...

    a = 2

... Python:

* crea el objeto "2". Ese objeto tendrá un identificador único que se asigna en el momento de la creación y se conserva a lo largo del programa. En este caso, el objeto creado será de tipo número entero y guardará el valor 2.
* asocia el nombre a al objeto número entero 2 creado.

Así, al describir la instrucción anterior no habría que decir 'la variable a almacena el número entero 2', sino que habría que decir 'podemos llamar a al objeto número entero 2'. La variable a es como una etiqueta que nos permite hacer referencia al objeto "2", más cómoda de recordar y utilizar que el identificador del objeto.

Por otro lado, en Python se distingue entre objetos mutables y objetos inmutables:

* Los objetos inmutables son objetos que no se pueden modificar. Por ejemplo, los números, las cadenas y las tuplas son objetos inmutables
* Los objetos mutables son objetos que se pueden modificar. Por ejemplo, las listas y los diccionarios son objetos mutables.

En el caso de los objetos inmutables (como los números) no hay mucha diferencia entre considerar la variable como una caja o como una etiqueta, pero en el caso de los objetos mutables (como las listas) pensar en las variables como cajas puede llevar a error.

Por economía del lenguaje, en estos apuntes se utilizan expresiones como "guardar un valor en una variable" en vez de "guardar el valor en un objeto y asociar una variable al objeto", pero el alumno debe tener presente lo que ocurre en realidad en Python.
  
En el ejemplo siguiente se almacena el número decimal 2.5 en una variable de nombre x (como se comenta en el apartado anterior, realmente habría que decir que se crea la etiqueta x para hacer referencia al objeto número decimal 2.5). Fíjese en que los números decimales se escriben con punto (.) y no con coma (,).

    >>> x = 2.5

La variable se escribe siempre a la izquierda de la igualdad. Si se escribe al revés, Python genera un mensaje de error:

    >>> 2.5 = x
    SyntaxError: can't assign to literal

Si una variable no se ha definido previamente, escribir su nombre genera un mensaje de error:

    >>> x = -10
    >>> y
    Traceback (most recent call last):
    File "<pyshell#1>", line 1, in <module>
        y
    NameError: name 'y' is not defined
    >>> nombre = Pepito Conejo
    SyntaxError: invalid syntax


La instrucción del borra completamente una variable.



# Entrada y Salida

En un entorno interactivo (por ejemplo, en IDLE), para que python nos muestre el valor de una variable basta con escribir su nombre.

    >>> a = 2
    >>> a
    2

También se puede conocer el valor de varias variables a la vez escribiéndolas entre comas (el entorno interactivo las mostrará entre paréntesis), como muestra el siguiente ejemplo:

    >>> a = b = 2
    >>> c = "pepe"
    >>> a
    2
    >>> c, b
    ('pepe', 2)

## print    

En los programas, para que python nos muestre texto o variables hay que utilizar la función print().

La función print() permite mostrar texto en pantalla. El texto a mostrar se escribe como argumento de la función:

    print("Hola")

----------

    Hola

Las cadenas se pueden delimitar tanto por comillas dobles (") como por comillas simples (').

    print('Hola')

----------

    Hola

La función print() admite varios argumentos seguidos. En el programa, los argumentos deben separarse por comas. Los argumentos se muestran en el mismo orden y en la misma línea, separados por espacios:

    print("Hola", "Adiós")
--------
    Hola Adiós

Cuando se trata de dos cadenas seguidas, se puede no escribir comas entre ellas, pero las cadenas se escribirán seguidas, sin espacio en blanco entre ellas:

    print("Hola" "Adiós")
------
    HolaAdios

Al final de cada print(), Python añade automáticamente un salto de línea:

    print("Hola")
    print("Adiós")
-----
    Hola
    Adiós
## input

La función input() permite obtener texto escrito por teclado. Al llegar a la función, el programa se detiene esperando que se escriba algo y se pulse la tecla Intro, como muestra el siguiente ejemplo:

    print("¿Cómo se llama?")
    nombre = input()
    print(f"Me alegro de conocerle, {nombre}")

-----
    ¿Cómo se llama?
        Pepe
    Me alegro de conocerle, Pepe

Otra solución, más compacta, es aprovechar que a la función input() se le puede enviar un argumento que se escribe en la pantalla (sin añadir un salto de línea):

    nombre = input("¿Cómo se llama? ")
    print(f"Me alegro de conocerle, {nombre}")
---------
    ¿Cómo se llama? Pepe
    Me alegro de conocerle, Pepe


# if else

Sentencias condicionales: if ...

La estructura de control if ... permite que un programa ejecute unas instrucciones cuando se cumplan una condición. En inglés "if" significa "si" (condición).

Veamos un ejemplo. El programa siguiente pide un número positivos al usuario y almacena la respuesta en la variable "numero". Después comprueba si el número es negativo. Si lo es, el programa avisa que no era eso lo que se había pedido. Finalmente, el programa imprime siempre el valor introducido por el usuario. A continuación se pueden ver dos ejecuciones paso a paso de ese programa. En la primera el usuario escribe un valor negativo y en la segunda el usuario escribe un valor positivo:

    numero = int(input("Escriba un número positivo: "))
    if numero < 0:
        print("¡Le he dicho que escriba un número positivo!")
    print(f"Ha escrito el número {numero}")

--------
    Escriba un número positivo: -5
    ¡Le he dicho que escriba un número positivo!
    Ha escrito el número -5


# For

En general, un bucle es una estructura de control que repite un bloque de instrucciones. Un bucle for es un bucle que repite el bloque de instrucciones un número prederminado de veces. El bloque de instrucciones que se repite se suele llamar cuerpo del bucle y cada repetición se suele llamar iteración.

La sintaxis de un bucle for es la siguiente:

    for variable in elemento iterable (lista, cadena, range, etc.):
    cuerpo del bucle

El cuerpo del bucle se ejecuta tantas veces como elementos tenga el elemento recorrible (elementos de una lista o de un range(), caracteres de una cadena, etc.). Por ejemplo:

    print("Comienzo")
    for i in [0, 1, 2]:
        print("Hola ", end="")
    print()
    print("Final")
------------
    Comienzo
    Hola Hola Hola
    Final

Si la lista está vacía, el bucle no se ejecuta ninguna vez. Por ejemplo:

    print("Comienzo")
    for i in []:
        print("Hola ", end="")
    print()
    print("Final")

----------
    Comienzo

    Final

En el primer ejemplo, los valores que toma la variable no son importantes, lo que importa es que la lista tiene tres elementos y por tanto el bucle se ejecuta tres veces. El siguiente programa produciría el mismo resultado que el anterior:

    print("Comienzo")
    for i in [1, 1, 1]:
        print("Hola ", end="")
    print()
    print("Final")
--------
    Comienzo
    Hola Hola Hola
    Final

# While

Un bucle while permite repetir la ejecución de un grupo de instrucciones mientras se cumpla una condición (es decir, mientras la condición tenga el valor True).

La sintaxis del bucle while es la siguiente:

    while condicion:
        cuerpo del bucle

La ejecución de esta estructura de control while es la siguiente:

* Python evalúa la condición:
    * si el resultado es True se ejecuta el cuerpo del bucle. Una vez ejecutado el cuerpo del bucle, se repite el proceso (se evalúa de nuevo la condición y, si es cierta, se ejecuta de nuevo el cuerpo del bucle) una y otra vez mientras la condición sea cierta.
    * si el resultado es False, el cuerpo del bucle no se ejecuta y continúa la ejecución del resto del programa.

La variable o las variables que aparezcan en la condición se suelen llamar variables de control. Las variables de control deben definirse antes del bucle while y modificarse en el bucle while.

Por ejemplo, el siguiente programa escribe los números del 1 al 3:

    i = 1
    while i <= 3:
        print(i)
        i += 1
    print("Programa terminado")
--------
    1
    2
    3
    Programa terminado

Puede ver la ejecución paso a paso de este programa utilizando los iconos de avance y retroceso situados abajo a la derecha.

El ejemplo anterior se podría haber programado con un bucle for. La ventaja de un bucle while es que la variable de control se puede modificar con mayor flexibilidad, como en el ejemplo siguiente:

    i = 1
    while i <= 50:
        print(i)
        i = 3 * i + 1
    print("Programa terminado")
-------
    1
    4
    13
    40
    Programa terminado

Puede ver la ejecución paso a paso de este programa utilizando los iconos de avance y retroceso situados abajo a la derecha.    


Otra ventaja del bucle while es que el número de iteraciones no está definida antes de empezar el bucle, por ejemplo porque los datos los proporciona el usuario. Por ejemplo, el siguiente ejemplo pide un número positivo al usuario una y otra vez hasta que el usuario lo haga correctamente:

    numero = int(input("Escriba un número positivo: "))
    while numero < 0:
        print("¡Ha escrito un número negativo! Inténtelo de nuevo")
        numero = int(input("Escriba un número positivo: "))
    print("Gracias por su colaboración")
-----------
    Escriba un número positivo: -4
    ¡Ha escrito un número negativo! Inténtelo de nuevo
    Escriba un número positivo: -8
    ¡Ha escrito un número negativo! Inténtelo de nuevo
    Escriba un número positivo: 9
    Gracias por su colaboración
# Funciones

Las funciones se pueden crear en cualquier punto de un programa, escribiendo su definición.

La primera línea de la definición de una función contiene:

* la palabra reservada def
* el nombre de la función (la guía de estilo de Python recomienda escribir todos los caracteres en minúsculas separando las palabras por guiones bajos)
* paréntesis (que pueden incluir los argumentos de la función, como se explica más adelante)

Las instrucciones que forman la función se escriben con sangría con respecto a la primera línea.

Por comodidad, se puede indicar el final de la función con la palabra reservada return (más adelante se explica el uso de esta palabra reservada), aunque no es obligatorio.

Para poder utilizar una función en un programa se tiene que haber definido antes. Por ello, normalmente las definiciones de las funciones se suelen escribir al principio de los programas

El ejemplo siguiente muestra un programa que contiene una función y el resultado de la ejecución de ese programa.

    def licencia():
        print("Copyright 2020 Bartolomé Sintes Marco")
        print("Licencia CC-BY-SA 4.0")
        return

    print("Este programa no hace nada interesante.")
    licencia()
    print("Programa terminado.")

----------
    Este programa no hace nada interesante.
    Copyright 2020 Bartolomé Sintes Marco
    Licencia CC-BY-SA 4.0
    Programa terminado.

# Referencias

* All the documentacion in this page is taken from [mclibre](https://www.mclibre.org/consultar/python/index.html).
