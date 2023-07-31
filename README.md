# Problema 4: Detección de fraude con identificación de anomalías
## Introducción

La detección de fraude se refiere a la identificación de transacciones o comportamientos anormales por parte de los clientes. A menudo, este comportamiento anómalo puede indicar que algo no está bien con la transacción o el reclamo de seguro, lo que requiere una retención hasta que se pueda realizar una evaluación adicional.

## Importancia

En la era actual de los pagos digitales, donde se realizan trillones de transacciones con tarjeta por día, la detección de fraudes es un desafío importante. De acuerdo con el Índice de Violación de Datos, más de 5 millones de registros se están robando a diario, una estadística preocupante que muestra que el fraude es muy común tanto para los pagos de tipo "Card-Present" como "Card-not Present". Tener un modelo que pueda predecir o anticipar un posible fraude puede marcar una gran diferencia para una empresa, ya que puede ayudar a prevenir pérdidas económicas significativas y mantener la confianza de los clientes.

## Desarrollo del problema técnico

Desarrollar un modelo de detección de fraude basado en la identificación de anomalías utilizando un conjunto de datos proporcionado. El modelo debe ser capaz de clasificar transacciones en fraudulentas o normales.

## Información sobre el conjunto de datos.

Este conjunto de datos, proveniente de un instituto anónimo, contiene las siguientes características:

distance_from_home: la distancia desde el hogar donde ocurrió la transacción.

distance_from_last_transaction: la distancia desde donde ocurrió la última transacción.

ratio_to_median_purchase_price: relación del precio de la transacción de compra al precio de compra mediano.

repeat_retailer: si la transacción ocurrió desde el mismo minorista.

used_chip: si la transacción se realizó a través de un chip (tarjeta de crédito).

used_pin_number: si la transacción ocurrió usando un número PIN.

online_order: si la transacción es una orden en línea.

fraud: si la transacción es fraudulenta.

# Concluciones 

Después de un estudio de los indicadores más comunes que manifiestan el fraude; y la investigación de las estrategias más utilizadas para la detección de estos males se decide investigar las posibles técnicas de Machine Learning (ML) que pueda predecir y detectar algunos posibles casos de fraude. Para esto se analizó un experimento sobre diferentes algoritmos, implementado en Python, donde se aplica algoritmos de aprendizaje supervisado para detectar comportamientos fraudulentos basados en fraudes anteriores y utiliza métodos de aprendizaje no supervisados para descubrir nuevos tipos de actividades fraudulentas. La investigación concluyó que uno de los mejores algoritmos dada su eficiencia para balancear los datos es la técnica de sobremuestreo de minorías sintéticas (SMOTEENN), ya que crea muestras nuevas y sintéticas que son bastante similares a las observaciones existentes en la clase minoritaria. Después de un balanceo se decide evaluar diferentes modelos de ML de aprendizaje supervisado, donde se evidenció que el modelo de Random Forest tiene un mejor rendimiento. 

Para la demostración de anomalías, se utilizó el algoritmo Isolation Forest, ya que para este solo se necesita definir con antelación la contaminación, para determinar este valor se conto con el porciento de la clase minoritaria, al ser un valor tan bajo, se tomo como referencia que fuese un valor igualmente bajo. Al evaluar todos estos algoritmos pudimos llegar a la conclusión que el caso ideal fuese, utilizar los modelos de aprendizaje supervisado, pero este tiende a fallar cuando los datos históricos son pocos y vagamente etiquetados, debido al alto costo en tiempo y recursos de la auditoría. Sin embargo, los modelos de aprendizaje no supervisado, permite detectar anomalías en los datos, por lo que sería muy eficiente para la detección de estos delitos, no obstante, cabe mencionar que el uso de estos algoritmos es más impreciso, ya que es necesario definir el hiperparametro el nivel de contaminación. 
