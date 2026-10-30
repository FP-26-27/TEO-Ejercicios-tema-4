# Ejercicios del tema 4: Funciones

Cree una carpeta ``src``, y dentro de la misma un archivo ``ejercicioX.py`` para cada ejercicio que vaya a resolver, sustituyendo la X por el número del ejercicio. Implemente en cada archivo la función solicitada por el ejercicio correspondiente, asegurándose de que las pruebas de la función se realicen como programa principal.

### Ejercicio 1: definición y llamada a una función
El precio de un billete del Metro de Sevilla depende del número de saltos del viaje, siendo 0,82€ para 0 saltos, 1,17€ para 1 salto y 1,37€ para 2 saltos. Escriba una función `calcula_precio` que reciba como parámetro el número de saltos y devuelva como resultado el precio del billete.

Pruebe la función con el siguiente código para mostrar en pantalla el precio de un billete para viajes con 0, 1 y 2 saltos:

```python
for saltos in range(3):
    precio_billete = 
    print(f"Precio del billete con {saltos} salto(s): {precio_billete} €")
```

### Ejercicio 2: parámetros con valores por defecto
Modifique la función del ejercicio anterior para que tome por defecto 0 saltos.

Pruebe la función realizando dos llamadas, una con 0 saltos y otra con 1 salto. Utilice el número mínimo de parámetros necesarios en cada llamada.

```python
precio_billete = 
print(f"Precio del billete con 0 saltos: {precio_billete} €")
precio_billete = 
print(f"Precio del billete con 1 salto: {precio_billete} €")
```

### Ejercicio 3: referencia a parámetros por nombre
Añada a la función del ejercicio anterior un segundo parámetro que indique el número de billetes que queremos comprar. Su valor por defecto será 1.

Para probar la función, realice varias llamadas con las siguientes condiciones:
1. Calcular el precio de 1 billete con 0 saltos
2. Calcular el precio de 2 billetes con 0 saltos
3. Calcular el precio de 1 billete con 2 saltos
4. Calcular el precio de 2 billetes con 1 salto

Utilice en cada llamada el número mínimo de parámetros necesarios.

```python
precio_billete = 
print(f"1. Precio del billete: {precio_billete} €")

precio_billete = 
print(f"2. Precio del billete: {precio_billete} €")

precio_billete = 
print(f"3. Precio del billete: {precio_billete} €")

precio_billete = 
print(f"4. Precio del billete: {precio_billete} €")
```

### Ejercicio 4: funciones como parámetros
La siguiente función tiene como segundo parámetro una función que indica una operación a realizar sobre la lista:

```python
def transforma(lista, operacion):
    return operacion(lista)
```

Complete estas llamadas a la función para que realicen la operación que se indica en cada caso:

```python
lista = [5, 7, 2, 3, 15, 9]

r1 = 
print(f"Tamaño de la lista: {r1}")

r2 = 
print(f"Valor máximo de la lista: {r2}")

r3 = 
print(f"Suma de los elementos de la lista: {r3}")
```

### Ejercicio 5: funciones sin nombre
Esta otra función también tiene como segundo parámetro una función, que representa en este caso un filtro que se aplica sobre la lista.

```python
def filtra(lista, filtro):
    lista_filtrada =  []
    for e in lista:
        if filtro(e):
            lista_filtrada.append(e)
    return lista_filtrada
```

Complete las llamadas para que el filtro produzca la lista que se indica en cada caso, utilizando funciones sin nombre.

```python
lista = [5, -7, 2, 0, 15, 9, -1, -3, 10, 0, -13, 21]

lista_positivos = 
print(f"Números positivos: {lista_positivos}")

lista_pares = 
print(f"Números pares: {lista_pares}")

lista_impares_negativos = 
print(f"Números impares negativos: {lista_impares_negativos}")
```

### Ejercicio 6: tipado de funciones

La siguiente `namedtuple` representa los datos de un entrenamiento deportivo:

```python
Entreno = NamedTuple('Entreno', [('tipo', str), ('fechahora', datetime), ('ubicacion', str), ('duracion', int), ('distancia', float), ('compartido', bool)])
```

Complete las cabeceras de las siguientes funciones utilizando tipado, sabiendo que:
* La función f1 recibe una lista de entrenamientos `entrenos`, una duración `duracion` y un parámetro `compartido` con valor `False` por defecto, y devuelve una lista de tuplas, cada una de las cuales está formada por una ubicación y una fecha y hora.
* La función f2 recibe una lista de entrenamientos `entrenos`, una distancia `distancia` y un tipo `tipo` que puede ser `None`, y devuelve un conjunto de ubicaciones.
* La función f3 recibe una lista de entrenamientos `entrenos`, una fecha `fecha` que puede ser `None` y tiene valor `None` por defecto, y no devuelve nada.

```python
from typing import NamedTuple
from datetime import datetime, date

Entreno = NamedTuple('Entreno', [('tipo', str), ('fechahora', datetime),
                                 ('ubicacion', str), ('duracion', int), 
                                 ('distancia', float), ('compartido', bool)])

def f1():
    pass

def f2():
    pass

def f3():
    pass
```