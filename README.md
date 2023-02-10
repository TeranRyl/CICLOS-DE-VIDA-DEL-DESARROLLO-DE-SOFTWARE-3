# CVDS_Lab3_Testing
**AeroDescuentos**

Se está desarrollando para una aerolínea su módulo de liquidación de tiquetes aéreos. Para el mismo, se tiene una función que aplica descuentos a la tarifa base del vuelo dependiendo del tiempo de antelación de la reserva y la edad del pasajero. Los descuentos SON ACUMULABLES.

_Normativa 005, sobre los descuentos:_

- _ **15%** _ _de descuento sacando el billete con antelación superior a 20 días._

- _ **5%** _ _a los pasajeros con edad inferior a 18 años y_ _ **8%** _ _a los pasajeros con edad superior a 65 años._

La siguiente es la especificación de la función que se usará en el módulo del cálculo de los descuentos:

/\*\*

calcular la tarifa de cada billete según el trayecto, la antelación en la que se obtiene el billete y la edad del pasajero, de acuerdo con la normativa 005.

@param tarifaBase valor base del vuelo

@param diasAntelacion dias de antelación del vuelo @param edad - edad del pasajero

@throws ExcepcionParametrosInvalidos [XXXXXXXXXXXXXXXXXXXXXXXXXXX] \*\*/

public long calculoTarifa(long tarifaBase, int diasAntelacion, int edad)

1. De acuerdo con lo indicado, y teniendo en cuenta que NO hay precondiciones, en qué casos se debería arrojar una excepción de tipo ExcepcionParametrosInvalidos?. Agregue esto a la especificación.
2. En la siguiente tabla enumere un conjunto de clases de equivalencia que -según usted- creen una buena división del conjunto de datos de entrada de la función anterior:

![](RackMultipart20230210-1-ahn9vl_html_c715e40c65fdf705.png)

Número

Clase de equivalencia (en lenguaje natural o matemático).

Resultado

correcto /

incorrecto.

1. Para cada clase de equivalencia, defina un caso de prueba específico, definiendo: parámetros de entrada y resultados esperados.

1. A partir de las clases de equivalencia identificadas en el punto 2, identifique las condiciones límite o de frontera de las mismas.

1. Para cada una de las condiciones de frontera anteriores, defina casos de prueba específicos.
