# Viajes en auto

La cooperativa de remiseros de Doctor Olaechea nos pide que le armemos un programa para manejar cuánto cobrar los viajes.
La cooperativa pacta con cada cliente el precio por kilómetro que le va a cobrar. Estos son los valores que arregló con algunos clientes
- **Ludmila**: 18 pesos el kilómetro, valor fijo e inamovible.
- **Ana María**: 30 pesos el kilómetro si está económicamente estable, 25 pesos el kilómetro en caso contrario. Se sabe en cada momento si Ana María está o no económicamente estable.
- **Teresa**: arranca en 22 pesos el kilómetro, puede cambiar a cualquier otro valor.

A partir de estos valores, cada remisera tiene un margen de decisión sobre cuánto cobrar un viaje. En particular:
- **Roxana** le cobra a cada cliente el precio por kilómetro que pactó con la cooperativa sin variaciones.
- **Gabriela** le aumenta un 20%, porque su auto de alta gama.
- **Mariela** no aplica recargo, pero establece un mínimo de 50 pesos el viaje.
- **Juana** por su parte, cobra 100 pesos hasta 8 kilómetros, y 200 pesos si son más de 8 kilómetros. A Juana no le importa lo que pactó la agencia, le cobra lo mismo a todos.

Veamos cuánto cobra cada remisera un viaje de 10 kilómetros. En lo que sigue, se supone que Ana María está económicamente estable, y que no se cambió el valor pactado con Teresa.
- _Roxana_: a Ludmila 180 pesos (18 * 10), a Ana María 300, a Teresa 220.
- _Gabriela_: a Ludmila 216 pesos (180 * 1.2), a Ana María 360, a Teresa 264.
- _Mariela_: lo mismo que Roxana.
- _Juana_: 200 pesos a todos.

Si el viaje es de 2 kilómetros, los valores son estos:
- _Roxana_: a Ludmila 36 pesos (18 * 2), a Ana María 60, a Teresa 44.
- _Gabriela_: a Ludmila 43.20 pesos (36 * 1.2), a Ana María 72, a Teresa 52.80.
- _Mariela_: a Ludmila y a Teresa 50 pesos que es el mínimo, a Ana María 60.
- _Juana_: 100 pesos a todos.

<br>

Se pide armar un programa que permita calcular cuánto debe cobrarse por un viaje, conociendo remisera, cliente y cantidad de kilómetros.  
P.ej. si consultamos cuánto debe cobrarse un viaje de 10 kilómetros donde la remisera es Roxana y la cliente es Ludmila, el resultado debe ser 180.

<br>

## Lucía y la cadete

Considerar en el programa a dos nuevos personajes: la remisera Lucía y la ckiente Melina.

- **Lucía** es una remisera que hace reemplazos, o sea, cubre los turnos que las otras remiseras se tienen que tomar por alguna razón.
En cada momento, se sabe a quién está reemplazando Lucía.
Lucía cobra lo mismo que la remisera al que está reemplazando.
- **Melina** es una cadeta que trabaja para los otros clientes de la remisería. En cada momento trabaja para un cliente, se sabe cuál es. El precio por kilómetro pactado con Melina es 3 pesos menos que el precio del cliente para el que esté trabajando en cada momento.

P.ej. si Lucía está reemplazando a Mariela, y Melina está trabajando para Ludmila, entonces:
- por un viaje de 10 kilómetros Lucía le cobra a Melina 150 pesos (el precio por kilómetro es 15, tres menos que lo que se pactó con Ludmila).
- por un viaje de 1 kilómetro le va a cobrar 50 pesos, que es el mínimo que establece Mariela.

Si en cambio Lucía está reemplazando a Gabriela, y manteniendo que Melina trabaja para Ludmila, entonces los valores para 10 y 1 km son 216 y 21.6, porque corre el 20% de recargo que establece Gabriela.  
