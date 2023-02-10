# CVDS_Lab3_Testing

Nombre de los integrantes del taller:
- Daniel Esteban Perez Bohorquez
- Juan Francisco Teran Roman

Proyecto: Testing

Entrega del laboratorio: https://github.com/TeranRyl/CVDS_Lab3_Testing.git

_______________________________________________________________________________________________________________________________________________________________________

**AeroDescuentos** 

Se está desarrollando para una aerolínea su módulo de liquidación de tiquetes aéreos. Para el mismo, se tiene una función que aplica descuentos a la tarifa base del vuelo dependiendo del tiempo de antelación de la reserva y la edad del pasajero. Los descuentos SON ACUMULABLES. 

*Normativa 005, sobre los descuentos:*

- ***15%** de descuento sacando el billete con antelación superior a 20 días.*  
- ***5%**  a los pasajeros con edad inferior a 18 años y  **8%**  a los pasajeros con edad superior a 65 años.*  

La siguiente es la especificación de la función que se usará en el módulo del cálculo de los descuentos:

/\*\* 

*calcular la tarifa de cada billete según el trayecto, la antelación*  

*en la que  se obtiene el billete y la edad del pasajero, de acuerdo* 

*con la normativa 005.*

*@param tarifaBase valor base del vuelo*

*@param diasAntelacion dias de antelación del vuelo*

*@param edad - edad del pasajero* 

*@throws ExcepcionParametrosInvalidos [XXXXXXXXXXXXXXXXXXXXXXXXXXX]* 

\*\*/ 

*public long calculoTarifa(long tarifaBase, int diasAntelacion, int edad)* 

1. De acuerdo con lo indicado, y teniendo en cuenta que NO hay precondiciones, en qué casos se debería arrojar una excepción de tipo ExcepcionParametrosInvalidos?. Agregue esto a la especificación.
    
    La excepcion se deberia arrojar en aquellos casos en los que la edad sea negativa o igual a cero, la tarifa base sea negativa, o los dias de antelacion sean negativos.

/\*\* 

*calcular la tarifa de cada billete según el trayecto, la antelación*  

*en la que  se obtiene el billete y la edad del pasajero, de acuerdo* 

*con la normativa 005.*

*@param tarifaBase valor base del vuelo*

*@param diasAntelacion dias de antelación del vuelo*

*@param edad - edad del pasajero* 

*@throws ExcepcionParametrosInvalidos edad menor o igual a cero, dias de antelacion negativos, o tarifa base negativa* 

\*\*/ 

*public long calculoTarifa(long tarifaBase, int diasAntelacion, int edad)* 


2. En la siguiente tabla enumere un conjunto de clases de equivalencia que -según usted- creen una buena división del conjunto de datos de entrada de la función anterior: 



|Número |Clase de equivalencia (en lenguaje natural o matemático).|Resultado correcto / incorrecto.|
| - | - | - |
|1|Edad del pasajero igual a 0|Incorrecto|
|2|Edad del pasajero negativa|Incorrecto|
|3|Dias de antelacion del vuelo negativos|Incorrecto|
|4|Dias de antelacion del vuelo igual a 0|Correcto|
|5|Valor base del vuelo negativo|Incorrecto|
|6|Valor base del vuelo igual a 0|Correcto|
|7|Edad del pasajero mayor a 0|Correcto|
|8|Dias de antelacion del vuelo mayor a 0|Correcto|
|9|Valor base del vuelo mayor a 0|Correcto|


3. Para cada clase de equivalencia, defina un caso de prueba específico, definiendo: parámetros de entrada y resultados esperados.

|Número de Clase de equivalencia|Parametros de entrada|Resultados esperados|
| - | - | - |
|1|(100, 23, 0)|ExcepcionParametrosInvalidos|
|2|(100, 23, -10)|ExcepcionParametrosInvalidos|
|3|(100, -2, 18)|ExcepcionParametrosInvalidos|
|4|(100, 0, 17)|95|
|5|(-100, 3, 18)|ExcepcionParametrosInvalidos|
|6|(0, 15, 17)|0|
|7|(100, 15, 17)|95|
|8|(100, 15, 21)|100|
|9|(100, 22, 19)|85|

4. A partir de las clases de equivalencia identificadas en el punto 2, identifique las condiciones límite o de frontera de las mismas.

|Número de Clase de equivalencia|Condicion limite de la entrada|
| - | - |
|1|edad = 0|
|2|-∞ < edad < 0|
|3|-∞ < diasAntelacion < 0|
|4|diasAntelacion = 0|
|5|-∞ < tarifaBase < 0|
|6|taarifaBase = 0|
|7|0 < edad < ∞|
|8|0 < diasAntelacion < ∞|
|9|0 < tarifaBase < ∞|

5. Para cada una de las condiciones de frontera anteriores, defina casos de prueba específicos.

|Número de Clase de equivalencia|Caso de prueba|
| - | - |
|1|edad = 0|
|2|edad = -15|
|3|diasAntelacion = -10|
|4|diasAntelacion = 0|
|5|tarifaBase = -12|
|6|tarifaBase = 0|
|7|edad = 66|
|8|diasAntelacion = 77|
|9|tarifaBase = 18|
