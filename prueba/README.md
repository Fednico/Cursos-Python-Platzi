Curso De pensamiento computacional con Python

Documentación de una función:

El docstring o la documentación está dividido en tres partes importantes que son las siguientes:

- Primero se da una descripción clara y concisa de la función y su funcionamiento
- En medio se agrega la descripción de los diferentes parámetros, su tipo, su nombre y que es lo que se espera de esos parámetros
- Por ultimo se agrega que es lo que devuelve nuestra función

Hay una extenion de visual studio code que nos facilita esto:

<https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring>

Luego de instalarla podemos configurar en la extensión que tome como formato lo documentado en PEP257


**Recursividad:**

- Algorítmica: una forma de crear soluciones utilizando el principio de divide y vencerás. Esto significa que podemos resolver un problema grande encontrando una solución base y reutilizarla.
- Programática: una técnica programática mediante la cual una función se llama a si misma.

![Imagen que contiene Esquemático

Descripción generada automáticamente](Aspose.Words.da9cb750-9c0f-4690-98d2-f3481438e447.001.png)

Python posee un limite de recursividad, para saberlo y modificarlo:

\>>> import sys

\>>> print(sys.getrecursionlimit())

1000

Para modificar ese límite

sys.setrecursionlimit(**n**) # **n** es el nuevo **l**ímite a establecer

**Funciones como objetos**

Una de las características más poderosas de Python es que todo es un objeto, incluyendo las funciones. Las funciones en Python son “ciudadanos de primera clase”.

Esto, en sentido amplio, significa que en Python las funciones:

- Tienen un tipo
- Se pueden pasar como argumentos de otras funciones
- Se pueden utilizar en expresiones
- Se pueden incluir en varias estructuras de datos (como listas, tuplas,
  diccionarios, etc.)

**Argumentos de otras funciones**

Hasta ahora hemos visto que las funciones pueden recibir parámetros para realizar los cómputos que definen. Algunos de los tipos que hemos pasado son tipos simples como cadenas, números, listas, etc. Sin embargo, también pueden recibir funciones para crear abstracciones más poderosas. Veamos un ejemplo:

**def** **multiplicar\_por\_dos**(n):

`    `**return** n \* 2

**def** **sumar\_dos**(n):

`    `**return** n + 2

**def** **aplicar\_operacion**(f, numeros):

`    `resultados = []

`    `**for** numero **in** numeros:

`        `resultado = f(numero)

`        `resultados.append(resultado)

\>>> nums = [1, 2, 3]

\>>> aplicar\_operacion(multiplicar\_por\_dos, nums)

[2, 4, 6]

\>>> aplicar\_operacion(sumar\_dos, nums)

[3, 4, 5]

**Funciones en expresiones**

Una forma de definir una función en una expresión es utilizando el keyword lambda. lambda tiene la siguiente sintaxis: lambda <vars>: <expresion>.

Otro ejemplo interesante es que las funciones se pueden utilizar en una expresión directamente. Esto es posible ya que como lo hemos platicado con anterioridad, en Python las variables son simplemente nombres que apuntan a un objeto (en este caso a una función). Por ejemplo:

sumar = **lambda** x, y: x + y

\>>> sumar(2, 3)

5

**Funciones en estructuras de datos**

Las funciones también se pueden incluir en diversas estructuras que las permiten almacenar. Por ejemplo, una lista puede guardar diversas funciones a aplicar o un diccionario las puede almacenar como valores.

**def** **aplicar\_operaciones**(num):

`    `operaciones = [abs, float]

`    `resultado = []

`    `**for** operacion **in** operaciones:

`        `resultado.append(operacion(num))

`    `**return** resultado

\>>> aplicar\_operaciones(-2)

[2, -2.0]

Como pudimos ver, las funciones son objetos muy versátiles que nos permiten tratarlas de diversas maneras y que nos permiten añadir capas adicionales de abstracción a nuestro programa.

Compártenos cómo te imaginas que estas capacidades de Python te pueden ayudar a escribir mejores programas.


TUPLAS:

Tuplas:

- Secuencias inmutables de objetos, osea son listas de valores que no podemos modificar.
- Pueden ser de tipo
  - Entero int (1,)
  - Flotante float (2.0,)
  - String (‘String’)
  - Booleano (true)
- Las tuplas al igual que los strings podemos acceder por indice

*my\_tuple(1,2,3)
my\_tuple[0] = 1
my\_tuple[1] = 2
my\_tuple[2] = 3*

- Podemos desempaquetar tuplas, para ello hay que definir ciertas variales para reasignarlas.
  x, y, z = my\_tuple
  x = 1 y=2 z=3

**Rangos.**

- Representan una secuencia de enteros, y se definen como range(inicio, fin, paso), y al igual que las cadenas y las tuplas, los rangos son inmutables.
- Son muy eficientes en uso de memoria y normalmente son utilizados en *for loops*.
- Nuevamente, el final no es inclusivo 👀.
- Para ver la dirección en memoria de un objeto, usamos la función id(objeto).
- Si lo que queremos es comparar igualdad de objetos en lugar de igualdad de valores, podemos hacer objeto is objeto\_2.
- Solución al reto: range(1, 100, 2)

my\_range = range(1, 10, 1)

print(type(my\_range)) #Tipo 

**for** i **in** range(2, 10, 2): #Imprime pares

`	`print(i)

