# RESUMEN MODULOS

# Variables, booleanas, operadores numéricos y binarios
                            
## VARIABLES AMPLIADAS POR TEXTO

**Ampliar una variable con texto**

    - categoria1 = "verde"
    - color_detalle = categoria1 + ' ' + 'oscuro'
    - print(color_detalle)

> verde oscuro

**Otro método**

    - print(categoria1 + ' oscuro')

> verde oscuro

**Otro método**

    - print(categoria1, 'oscuro')

> verde oscuro

Se puede hacer creando una nueva variable y sumando str o con la , y el str.

**Repaso**:

- El contenido de una variable se muestra en el *output* con la función `print()`.

- Los tipos de datos de tipo `texto` o `*string*` se pueden definir con comillas simples o dobles, pero nunca sin comillas.

- Para encadenar texto se usa `+` o `,`.

## NÚMEROS ENTEROS, DECIMALES O STRINGS


- `Integer` ('int'): números sin decimales tanto positivos como negativos.

- `Float` ('float'): números con decimales tanto positivos como negativos.

- `Strings` ('str'): cadenas de caracteres, pueden delimitarse con comillas simples ' ' o dobles " " indistintamente.

**Para cambiar el tipo de dato o type casting**

    - variable = float/int/str()
    - type(variable)
    
### para cambiar tipo: variable nueva = int(variable antigua)

> te devuelve: class 'float/int/str'

**Comprobar el tipo de una variable**

    - isinstance(variable, float/int/str)

> Te devuelve True/False

*Para cambiar el tipo a bool simplemente habria que guardar postres como False, que tiene un valor 0 y es booleano.

## OPERACIONES ALGEBRAICAS

**Repaso**:

- Sumar con `+`.

- Restar con `-`.

- Multiplicar con `*`.

- Elevar a con `**`.

- Dividir con `/`.

- Dividir y redondear el resultado hacia abajo con `//`.

- El resto de una división con `%`.

**Método .round()**
 
 Le damos a la variale el número que tienen que redondear. Si añades un segundo argumento le dices cuantos decimales quieres:

    - print(round(variable, nº decimales))

## OPERACIONES BINARIAS

Introducción a las variables boolenanas. Devuelven True/False

- ==/is: Ver si los valores coinciden.
> Cuidado con is porque si es de tipo int coinciden en el resultado, pero si las variables son tipo float devulven resultados diferentes.

- !=/ is not: Ver si dos valores son diferentes.
> Cuidado con este tambien.

- Menor que (o igual) con `< (<=)`

- Mayor que (o igual) con `> (>=)`

- Para combinar dos operaciones binarias:

    - Ambas verdaderas con `and`

    - Ambas o solo una verdadera con `or`

    - Usa paréntesis  para estructurar la sentencia

## Métodos de los str y función input()

    -nombre_completo = nombre + ' ' + apellido
    -es igual a
    -print(nombre, apellido)

**Construir frase**

    - nombre = input()
    - bienvenida = hola + ' ' + nombre + ', ¡bienvenida a este bootcamp!'

### Otros métodos

- **.upper()**: Todas las letras mayúsculas

- **.lower()**: Todo minúsculas

- **.capitalize()**: Primera letra de la frase en mayúscula

- **.tittle()**: Primera letra de cada palabra en mayúscula

- **.swapcase()**: cambia minúsculas a mayúsculas y viceversa

- **.strip()**:  quita espacios del principio y final del str

- **.split()**: divide string en lista

- **.replace()**: reemplaza

- **.join()**: toma los elementos de una lista y los une en str (poner la lista dentro del paréntesis)

- `.find()`: encontrar el índice en que empiece el substring del argumento. Da '-1' si no existe el substring. *revisar*

> podemos especificar el separador dentro de los (). En Python '\n' es el salto de linea.

    - Ejemplos
    - bienvenida.upper()
    - don_quijote.split('\n')
    - saludo.replace('chicas', 'Adalaber')

> para que se queden los cambios guardar en variable nueva

# LISTAS 1

nombre = [contenido]

*Usar type() e insistance(,tipo) para comprobar los tipos de los elementos*

**Lista vacia**

    - notas_año = [vacía]
    - para añadirle contenido metemos las variables en el corchete
    - notas_año = [notas_bio, notas_mates]
    - pueden contener diferentes tipos de datos. Meter str con ('')

**Juntar listas**

>Se utiliza el operador + y el corchete con el elemento
 (la coma nos crea listas dentro de listas)

**Convertir variables str en listas**

    - Ejemplo:
         apellido = 'Lovelace'
         list(apellido) 

> Devuelve una lista con cada letra separado por ['']

`RECUERDA`: PARA SOBREESCRIBIR LA VARIABLE GUARDAR EN OTRA NUEVA

## PROPIEDADES DE UNA LISTA

- **len()**: cuantos elementos tenemos en una lista

- **min()/max()**: sacar el valor mínimo y máximo
> con listas de str los ordena alfabéticamente

- **in/not in**: nos devuelve un True/False de si hay un valor dentro de la lista

> Es un bool

    6.0 in notas_biologia_primer_año
    False

# MÉTODOS PARA LISTAS

- **.copy()**: hacer una copia de la lista

- **.clear()**: vaciar una lista (no reasignación a nueva variable)

- **.count()**: nº de elementos que hay en la lista de un valor determinado

    Ejemplo
    notas.count(6.8) - 4

- **.reverse()**: para ver de las más reciente a antigua.
> hacer un .copy() de la lista primero

-**.sort()**: ordena de menor a mayor
> hacer un .copy() primero

 *con .sort(reverse=True) ordenamos de mayor a menor*

 # LISTAS 2


Indexacion de listas

**Acceder a los elementos de la lista mediante los indices de los elementos.**

- Ejemplo: temps_semana = [número del indice que queremos sacar]

    - Los indices empiezan en 0.
    - Para acceder a ellos usamos []
    - Con la función len() miramos la longitud de la lista, el indice máximo al que podemos llegar.. Nuestro indice máximo siempre será *longitud de la lista -1* debido a que empiezan en 0.
    >- Ejemplo: temps_semana[len(temps_semana) - 1]


## Indices del final de la lista y metodo .index()

**Se puede usar el metodo len() y los índices negativos, que funcionan como una cuenta atrás.**

- Ejemplo: temps_semana[-1]. Es más sencillo que con len() pero se pueden usar los dos.
    - Para conocer la posición de un elemento de nuestra lista utilizamos .index()

    - Ejemplo: *temps_semana.index(elemento que queramos saber su posición)*


    > CUIDADO CON LOS ELEMENTOS DE LAS LISTAS QUE SON STR Y SIEMPRE SE TE OLVIDA PONER LAS COMILLAS UNO POR UNO.

**Obtener elementos de las listas**

- Obtenemos la longitud de la lista creada. len(temps_semana)
- La posicion del valor con index: temps_semana.index(valor)
- para obtener los elementos que queramos de nuestra lista ponemos el indice hasta el cual queramos sacar elementos: 

        > ejemplo: print(temps, temps[:5]). Esto nos daría temps [1, 2, 3, 4, 5]
        > si quisieramos las 5 ultimas: temps_ultimas = temps[-5:]

*lista con letras*
letras = ['a', 'b', 'c']

    para sacar dos elementos:
    - print('dos_primeras =',letras[0:2])
    - print('[1:3] =',letras[1:3])
    - print('[-2] =',letras[-2:])

**saltar elementos**
- start: indice de empezar
- stop: donde queremos terminar
- step: saltos que queremos dar en la busqueda

*fechas = [1, 2, 3, 4, 5]*
    - fechas[1::2] te saca los saltos de las fechas pares [2, 4]

    - fechas[::2] los impares
    - fechas[::3] de tres en tres
    - fechas[0:15:3] primera quincena y de tres tres
    - fechas[:2] la una y la dos
    - [x:] del elemento en adelante
    - [:2] hasta el elemento x

## Métodos de listas

**sorted() y funcion del**

- sorted() es para crear una lista sin sobreescribir la variable anterior (*a diferencia de sort()*)

    Ejemplo: 
    apellido = Gallego
    apellido_list = list(apellido)

    print(sorted(apellido))

>lo ordena de mayusculas a minusculas y por orden alfabetico

    Para darle la vuelta:

    - sorted(apellido, reverse=True)

- del: borra información

del apellido[2] eliminará la "l" de Gallego

## Más métodos para listas


**Ampliar listas con .append(), .extend() e .insert()**

- Con + se pueden unir por ejemplo dos listas. *Con .append() y .extend() también podemos añadir información:*

    Ejemplo: compras = ['Té]

    Elemento_str = 'sal'

    Elemento_lista = ['kiwi']

> Para añadir el string: compras.append(elemento_str) y nos lo añade

> para añadir la lista: compras.append(elemento_lista) y nos la añade


*IMPORTANTE: -Aquí el resultado es una lista como esta ['Té', 'sal', ['kiwi]]*

    - Para acceder a la lista kiwi y despues al elemento kiwi tendríamos que poner dos index, primero a la lista y luego al elemento: compras[2][0]

- Con extend se añaden uno por uno: compras2.extend(elemento_lista2) resultaría en ['té', 'sal', 'kiwi']

- Con .insert() metemos un elemento en un indice específico.

    - Ejemplo de las letras del apellido: apellido = Galego

    - apellido.insert(2, 'l') da como resultado 'Gallego'


    > Insertó la letra l en el indice 2


 **Pop() y remove()**

    - Quitar y devolver de un índice conocido con .pop()
    
    - elimina por indice lista_num.pop y me dice lo que me ha eliminado

    - Quitar sin devolver el primer instante de un contenido conocido con .remove() 
> elimina por elemento lista_num.remove(2)
    
    - del lista_num[2] 
> no es especifico de lista, puede borrar variables enteras del lista_num (desaparece entera)



# Diccionarios

- Para definirlos se usan las llaves {}
- Están compuestos por una (key - obligatoria) y un valor (value tipo str, list, números...)

**key(unica)-value = pueden ser ambas cualquier tipo de dato**

> - diccionario1 = { 'lunes': 1, 'martes':2, 'miércoles':3 }*
> - diccionario3 = { 'lunes': [1, "peras"], 'martes':[2, "manzanas"], 'miércoles':[3, "brocoli"] }

- Método dict()
> dias2 = dict( jueves = 'thursday', viernes='friday' )
*Básicamente crea diccionario sin utilizar las llaves y las '' de los str*

- Update(): para insertar nuevos elementos en los diccionarios
> diccionario3.update( { 'jueves' : [4, 'chorizo'] } )
De esta manera se inserta una nueva key-value con la info. No tiene que tener la misma estructura.

> - Lo mismo que update() es: 
> diccionario['país'] = 'Italia' 

*Para ver una información concreta en el diccionario*
- midiccionario['la key que quiero]
>- gato1['tipo'] - 'europeo común'

**- Además del método Update() podemos incorporar una nueva key con []**

>- gato1['vacunado'] = True

*Cuidado si las fechas empiezan con 0, hay que usar ('')*

## Propiedades de un dict

    - Funcion len() : nos devuelve el nº de elementos
    - print(len(nombre diccionario))

    - In/ not in: para comprobar si existe una clave
>cumpleaños in gato1

**Métodos específicos: keys() y values()**
- `.keys()`: obtenemos todas las keys
>- gato1.keys()

- `.values()`: obtenemos todos los values
>- gato1.values()

- `.items()`: tuplas con el par key-value

**Más métodos para diccionarios** 
- `copy()`: copia
> -gatitos = gato1.copy()

- `get()`: Busca un elemento a partir de su clave:
> -igual que gato1['tipo'] || gato1.get('tipo')

*Se le puede añadir parámetro extra y nos devuelve un output*
> - gato1.get('castrado', 'esa key no existe') : devuelve el output 'Esa key no existe'

- `setdefault()`: Igual que get, si la key no existe la crea y le asigna el value por defecto que indicamos.
> - gato1.setdefault('vacunas', 'no tiene') 
*Aparece al final de la lista esa key-value.*

    - estos dos nos ayudan a que la ejecucion de nuestro diccionario no se pare.

    
- `sorted()`: ordena

> sorted(gato1): ordena las keys

> sorted(gato1.items): ordena por las keys, devuelve lista

> sorted(gato1.items(), reverse = True): la ordena del revés

> sorted(gato1.values()) 

    - sale error si son diferentes (str, int)

- `pop()`: elimina una key especifica
> gato1.pop(vacunas)   

- `popitem()`: elimina el ultimo par de key-value
> gato1.popitem()

- `clear()`: vacía el diccionario, igual que en las listas
> gato1.clear()



# TUPLAS Y SETS

Las tuplas una vez creadas son inmutables.
Son indexables como los diccionarios y las listas, pero su orden no cambiara.
Igual que los diccionarios, 

## Definir tuplas

Con paréntesis `()`, pero con un pequeño detalle, *habrá que poner comas.*
Con el método `tuple()` de Python. 

**Método paréntesis ()**

    - tupla1 = (3,)
    - print(tupla1, 'es del tipo', type(tupla1)) : 
    - (3,) es del tipo <class 'tuple'>

    - tupla2 = 2,3,4 lo entenderá como tupla.

> si no ponemos (,) lo entenderá como un número

**Método tuple()**

    - lista = [2,3] (class, list)
    - tuple(lista)

> guardar la tupla en una nueva variable

Al convertir un dccionario en tupla por defecto lo hará sobre las keys.
Para hacerlo sobre los values/items:

    - tupla(diccionario.values())
    - tupla(diccionario.items())

Si tenemos una serie de variables definidas, podemos unirlas todas en una tupla mediante los paréntesis.

    - propiedades = (peso, cantidad, color, año, categoria)
    - (type(propiedades))

> una vez definidas las variables podemos eliminarlas mecon el método `del` : del peso, cantidad, color, año, categoria

## Operaciones con tuplas

Se pueden sumar con el oprador `+`, pero obligatoriamente tienen que estar definidas como tuplas. *Si no, da error*

**Repaso**

- Definir tuplas con `,` y parentesis `()`.

- Convertir otro contenedor a una tupla con `tuple()`.

- Juntar tuplas con `+`.

## Propiedades y métodos de las tuplas

- Misma **indexación** que las listas: [0] primer contenido, [-1] último.

- **len():** para obtener cuantos elementos hay 

    -len(variable)

- **in/not in:** 'Madrid' in propiedades

- **.count()/ .index()**:

    - variable.count(elemento)
    - variable.index(posicion)

La principal diferencia con otros contenedores es que su contenido no puede cambiar.
*No se puede reasignar sus elementos*

Ejemplo: en las listas podemos cambiar el valor de un elemento en una posición de esta manera:

> variable[posicion] = valor / lista[1] = 3

Al intentar hacer eso con una tupla devuelve error.

## MODIFICAR EL CONTENIDO DE UNA TUPLA

Convirtiéndola a una **lista**, hacer las modificaciones que queramos, y convertirla a una tupla de nuevo usando `tuple()`.

    - lista1 = list(tupla1) : devuelve lista []
    - Con el método .extend() añadimos la tupla que queramos añadir a la lista.
        - lista1.extend(tupla2)

    - volvemos a convertir en tupla esa lista 
        - tupla1 = tuple(lista1)


Haciendo la **suma** de dos tuplas (tienen que ser ambas tuplas)

    - tupla1 = tupla1 + tupla2

## Función Zip()

Esta función produce tuplas, nos va a crear parejas de los elementos.
Convertimos dos listas a tuplas

    zip1 = zip(lista1, lista2)
    devuelve algo como esto:

        <zip at 0x7f193ed2adc0>
    
    para hacerlo legible: list(zip1)

    > esta función solo tiene un uso, luego desaparece si no lo almacenamos en una nueva variable.

 - **.sort()**: nos ordena en función de número o letra dependiendo de lo que hayamos guardado primero en zip().

`Zip()` se corta al tamaño de la lista más corta.

# SETS

- Los sets son "sacos" desordenados con contenidos únicos, es decir *no se puede meter el mismo contenido más que una vez*

- No puedes saber dónde en el set se encuentra un contenido específico, *no pueden ser indexados*.

- Pueden ser unidos con otros sets, pero elimina los elementos duplicados y guarda los elementos de *modo aleatorio*.

> se pueden crear con set() o directamente usando las llaves {'','',''}

## Métodos para SETS

### Buscar elementos con in/not in

    - print('Huevos' is alergenos) : True/False

### Añadir elementos al SET

**Añadir un elemento con .add()**

    - alergenos.add('Apio')

**Añadir varios elementos con .update()**

    Creamos una lista con los elementos a añadir
        - actualizacion = ['Mostaza', 'Sesamo']

    Aplicamos el .update() y después printeamos:
        - alergenos.update(actualizacion)

*Podemos hacerlo con el Método llaves {} en lugar de lista []*

    - actualizacion2 = {'Altramuces'}

    Aplicamos el .update() y después printeamos:
        - alergenos.update(actualizacion2)

**Otros métodos válidos para SETS**

- `.copy()`: para hacer una copia del set.

- `len()`: cuántos elementos tiene el set.

- `.pop()`: nos elimina un elemento de manera `aleatoria`.

- `.clear()`: vaciamos el contenido del set.

**Eliminar elementos en concreto**


- `.remove()`: eliminamos el elemento que especifiquemos en el ()

- `.discard()`: lo mismo. La diferencia entre ambos es que `.remove()` devuelve *error* si ya hemos eliminado un elemento, y `.discard()` no.

## Operaciones con sets

Los sets nos permiten hacer comparaciones entre sí, ya que cada elemento es único.

- **union()**: une dos sets.

> set3= set1.union(set2)

*También podemos hacer esta unión mediante* `|`

> set3 = set1 | set2

- **.intersection()**:  nos devuelve los elementos comunes en sets

> set3 = set1.intersection(set2)

*También podemos hacer esta unión mediante* `&`

- **.difference()**: nos devuelve los elementos `presentes en un set pero no en el otro.`

> set3 = set1.difference(set2) : por ejemplo, 'a'

    -  AQUÍ EL ORDEN ES IMPORTANTE

*También podemos hacer esta unión mediante* `-`

-**.symmetric_difference()**: los elementos que no están presentes en ambos conjuntos.

> set3 = set1.symmetric_difference(set2) : por ejemplo 'a' y 'd'

## Otros métodos de comprobación

-**.isdisjoint()**: comparar que los sets no tienen ningún elemento en común. Devuelve True si todos los elementos son diferentes y False si alguno coincide

-**.issubset()**: Compara si un set es superset de otro, es decir, si todos los elementos de un set están contenidos en un subset.







