---
title: Acerca de órdenes de producción | Documentos de Microsoft
description: Las órdenes de producción se usan para gestionar la conversión de los materiales adquiridos en productos manufacturados. Las órdenes de producción (solicitudes de proyecto o de trabajo) dirigen el trabajo por las distintas instalaciones (centros de trabajo o de máquina) de la planta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b02aa262089d5c341fb3b535f2af82c7085e99ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252969"
---
# <a name="about-production-orders"></a>Sobre los pedidos de producción
Las órdenes de producción se usan para gestionar la conversión de los materiales adquiridos en productos manufacturados. Las órdenes de producción dirigen el trabajo por los distintos centros de trabajo o de máquina de la planta.  

Antes de empezar con producción, la mayoría de las empresas realizan una planificación de suministros, normalmente una vez por semana, para calcular cuántos pedidos de producción y de compra ejecutar para cubrir la demanda de ventas esa semana. Los pedidos de compra suministran los componentes que se requieren según la L.M de producción para fabricar los productos finales.

Las órdenes de producción son los componentes esenciales de la funcionalidad de fabricación del sistema. Contienen la información siguiente:  

-   Productos planificados para fabricación  
-   Materiales necesarios para las órdenes de producción planificadas  
-   Productos que se acaban de fabricar  
-   Materiales que ya se han seleccionado  
-   Productos que se han fabricado en el pasado  
-   Materiales que se utilizaron en operaciones de fabricación anteriores  

Las órdenes de producción son los puntos de partida de:  

-   La planificación de la fabricación futura  
-   El control de la fabricación actual  
-   El seguimiento de la fabricación terminada  

## <a name="production-order-creation"></a>Creación de órdenes de producción  
Las órdenes de producción se pueden crear una por una, manualmente, desde la página **Orden producción**, o se pueden generar desde las páginas **Planificación pedido venta** o **Planificación de pedidos**. Para crear varias órdenes se utiliza la página **Hoja planificación**.  

Las órdenes de producción se crean utilizando información sobre:  

- Productos  
- LM producción
- Rutas  
- Centros de máquina  
- Centros de trabajo  

## <a name="limitations-on-production-order-creation"></a>Limitaciones en la creación de órdenes de producción  
Las órdenes de producción se reservan automáticamente y se realiza el seguimiento hasta su origen cuando:  

-   Se crean desde la **Hoja planificación**  
-   Se crean con la función de pedido de la página **Planificación pedido venta**  
-   Se crean desde la página **Planificación de pedidos**  
-   Se usa la función **Replanificar** en las órdenes de producción  

Para obtener más información, vea [Seguimiento de relaciones entre demanda y suministro](production-how-track-demand-supply.md).

Las órdenes de producción creadas por otros métodos no se reservan automáticamente, ni se realiza su seguimiento.   

## <a name="production-order-status"></a>Estado de las órdenes de producción  
El estado de una orden de producción controla su comportamiento en el sistema. La forma y el contenido de una orden de producción se rigen por el estado de la misma. Las órdenes de producción se muestran en páginas diferentes según sus estados. El estado de una orden de producción no se puede cambiar manualmente, es necesario usar la función **Cambiar estado**.  

### <a name="simulated-production-order"></a>Orden de producción simulada  
La orden de producción simulada es exclusiva porque tiene las características siguientes:  

- Como su nombre implica, es una simulación y su finalidad principal es su uso para crear ofertas y costes; por ejemplo, se puede usar si un departamento de investigación y desarrollo desea obtener una estimación del coste de un producto propuesto. Una orden de producción simulada sirve como ejemplo de una orden de producción.  
- No afecta a la planificación de pedidos. La Planificación (MPS y MRP) no tiene en cuenta ni se ve afectada por las órdenes de producción simuladas. Además, una orden de producción simulada no se puede usar como libro, porque deja de existir cuando se cambia su estado.  

### <a name="planned-production-order"></a>Orden de producción planificada  
La orden de producción planificada es exclusiva porque tiene las características siguientes:  

- Las órdenes de producción planificadas se pueden crear automáticamente desde un pedido de venta.  
- Las órdenes de producción planificadas son iguales que las órdenes de producción lanzadas y proporcionan datos para la planificación de los requisitos de capacidad, ya que muestran los requisitos de capacidad totales por centro de trabajo o de máquina.  
- Las órdenes de producción planificadas representan la mejor estimación de la carga de trabajo futura de un centro de trabajo o de máquina, en función de la información disponible. Normalmente, se generan desde la planificación, pero también se pueden crear manualmente. Si se tiene en cuenta que se eliminan en las planificaciones posteriores, la creación manual no resulta práctica.  
- Si se generan en planificación, se crea una "planificación de liberación órdenes" sugerida, que contiene la cantidad, la fecha de lanzamiento y la fecha de vencimiento. La lógica del sistema de planificación se basa en el sistema de reposición, las directivas de reaprovisionamiento y los modificadores de pedido con que se encuentra en el proceso de planificación de la demanda neta.  
- Para conocer sus efectos, observe la carga de cada centro de trabajo o de máquina de la ruta de una orden de producción planificada.  

### <a name="firm-planned-production-order"></a>Orden de producción planificada en firme  
La orden de producción planificada en firme es exclusiva porque tiene las características siguientes:  

- Una orden de producción planificada en firme se puede crear a partir de un pedido de venta.  
- Una orden de producción planificada en firme actúa como marcador de posición, dentro del programa de planificación, de un proyecto futuro liberado en la planta.  
- Una orden de producción planificada en firme se puede generar desde la planificación, o se puede crear manualmente o a partir de pedidos de venta. No se elimina en las planificaciones posteriores.  
- Si se generan en planificación, se crea una "planificación de liberación órdenes" sugerida, que contiene la cantidad, la fecha de lanzamiento y la fecha de vencimiento. La lógica del sistema de planificación se basa en el sistema de reposición, las directivas de reaprovisionamiento y los modificadores de pedido con que se encuentra en el proceso de planificación de la demanda neta.  
- Para conocer sus efectos, observe la carga de cada centro de trabajo o de máquina de la ruta de una orden de producción planificada en firme.  

### <a name="released-production-order"></a>Orden de producción lanzada  
La orden de producción lanzada es exclusiva porque tiene las características siguientes:  

- Las órdenes de producción lanzadas se pueden crear automáticamente desde un pedido de venta.  
- El lanzamiento de una orden de producción no implica que se hayan preparado los materiales o que el proyecto haya avanzado físicamente a la primera operación.  
- En un entorno de fabricación contra pedido, no es raro crear una orden de producción lanzada en cuanto se introduce el pedido de venta.  
- El consumo de material y la salida del producto reales se pueden registrar manualmente con una orden de producción lanzada. Además, la baja automática del consumo y la salida del producto sólo tienen lugar con las órdenes de pedido lanzadas.  

### <a name="finished-production-order"></a>Orden de producción terminada  
La orden de producción terminada es exclusiva porque tiene las características siguientes:  

- Normalmente, una orden de producción terminada es la que ya se ha fabricado.  
- La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando. Si se termina una orden de producción, los costes se pueden ajustar y conciliar.  
- Las órdenes de producción terminadas se usan para crear informes estadísticos y para posibilitar el seguimiento de los pedidos (de venta, de producción y de compra, por ejemplo). La posibilidad de realizar el seguimiento hasta una orden de producción terminada permite revisar el historial detallado.  
- Las órdenes de producción terminadas no se pueden modificar nunca.  

## <a name="production-order-execution"></a>Ejecución de las órdenes de producción  
Una vez que se ha creado y programado una orden de producción, se tiene que lanzar a la planta para su ejecución. Durante la ejecución de la orden se registra lo siguiente:  

- Los materiales preparados o consumidos  
- El tiempo de trabajo invertido en la orden  
- La cantidad de producto principal producida  

Esta información se puede registrar manualmente o con la información automática, según los productos configurados en el campo de Método de baja.  

### <a name="material-consumption"></a>Consumo de material  
El programa ofrece diversas opciones para que las empresas de fabricación puedan registrar el consumo de material. Por ejemplo, se puede registrar de forma manual, lo que puede ser aconsejable si los componentes se sustituyen con frecuencia o la cantidad de productos rechazados es mayor que la prevista.  

El consumo de material se puede procesar mediante el diario de consumo. Además, el programa lo puede registrar automáticamente, lo que se denomina creación automática de informes. Los métodos de creación de informes son::  

-   Manual  
-   Adelante  
-   Atrás  

El método de creación manual de informes de consumo usa el diario de consumo para especificar la preparación de material.  

El método de creación de informes anticipados presupone que la cantidad esperada de todos los materiales de todo el pedido se consume al lanzar una orden de producción, salvo que se usen códigos de conexión de ruta. Si se usan códigos de conexión de ruta, el material consumido después del inicio del paso operativo se registra en el diario de salida. Para llevar a cabo la baja hacia adelante de toda la orden de producción, es necesario lo siguiente:  

- Todos los productos de la lista de materiales de producción de nivel superior deben tener seleccionado el método de baja hacia adelante en la ficha de producto correspondiente.  
- Se deben eliminar todos los códigos de conexión de ruta de la lista de materiales de producción.  

El método de creación de informes retroactivos registra la cantidad real de todo el material preparado o consumido cuando el estado de una orden de producción se cambia a *Terminada*, salvo que se usen códigos de conexión de ruta. Si se usan códigos de conexión de ruta, el material se consume una vez que se ha registrado una cantidad del producto principal para el paso operativo en el Diario de salida.  

Al actualizar la orden de producción, el método de baja se copia de la ficha del producto. Puesto que el método de baja de cada componente de la orden de producción controla cómo y cuándo se registra el consumo, es importante tener en cuenta que el método de baja de un producto concreto se puede cambiar directamente en la orden de producción.  

#### <a name="automatic-consumption-posting-flushing"></a>Registro automático del consumo (consumo automático)  
La ventaja del consumo automático es que reduce en gran medida el volumen de datos que se debe introducir. Con la posibilidad de realizar el consumo automático de una operación, se puede automatizar el proceso completo del registro del consumo y la salida. El inconveniente es que podría no registrar con exactitud, o ni siquiera advertir la existencia de rechazo. Los métodos de registro automático son:  

- Baja hacia adelante de toda la orden  
- Baja hacia adelante por operación  
- Baja hacia atrás por operación  
- Baja hacia atrás de toda la orden  

#### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Registro automático - Baja hacia adelante de toda la orden  
Si realiza la baja hacia adelante de la orden de producción al comienzo del proyecto, el comportamiento del sistema es muy parecido al del consumo manual. La diferencia principal es que el consumo tiene lugar automáticamente.  

- Todo el contenido de la lista de materiales de producción se consume y deduce de las existencias en el momento en que se actualiza la orden de producción lanzada.  
- La cantidad de consumo es la cantidad por montaje indicada en la lista de materiales de producción, multiplicada por el número de productos principales que se esté produciendo.  
- No es necesario registrar ninguna información en el diario de consumo si se va a llevar a cabo la baja de todos los productos.  
- Al consumir los productos desde las existencias, no importa en qué momento se realizan los movimientos del diario de salida, ya que este diario no tiene efecto alguno en esto modo de registro del consumo.  
- No se pueden definir códigos de conexión de ruta.  

La baja hacia adelante de toda la orden está indicada en entornos de producción con:  

-   Un número reducido de defectos  
-   Un número reducido de operaciones  
-   Un alto consumo de componentes en las operaciones iniciales  

#### <a name="automatic-reporting---forward-flushing-by-operation"></a>Registro automático - Baja hacia adelante por operación  
El consumo por operación le permite realizar deducciones en las existencias durante una operación concreta de la ruta del producto principal. El material se enlaza a la ruta mediante códigos de conexión de ruta, que se corresponden con los códigos de conexión de ruta aplicados a los componentes en la lista de materiales de producción.  

El consumo tiene lugar cuando se inicia la operación con el mismo código de conexión de ruta. Se entiende que se ha iniciado cuando se registra alguna actividad en el diario de salida relativa a la operación. La actividad podría ser simplemente la introducción de un tiempo de preparación.  

La cantidad de consumo es la cantidad por montaje indicada en la lista de materiales de producción, multiplicada por el número de productos principales que se esté produciendo (cantidad prevista).  

Esta técnica está indicada en casos en que haya un gran número de operaciones y algunos componentes no se necesitan hasta más adelante en la secuencia de montaje. De hecho, en una configuración Just-in-Time (JIT), los productos podrían no estar listos cuando se empieza la orden de producción lanzada.  

El material se puede consumir durante las operaciones mediante el uso de códigos de conexión de ruta. Algunos componentes no se pueden usar hasta las operaciones finales de montaje y no se deben retirar de las existencias hasta ese momento.  

#### <a name="automatic-reporting---back-flushing-by-operation"></a>Registro automático - Baja hacia atrás por operación  
La baja hacia atrás por operación registra el consumo una vez que se ha registrado la operación en el diario de salida.  

La ventaja de este método es que se conoce el número de piezas principales acabadas de la operación.  

El material de la lista de materiales de producción se enlaza a los registros de la ruta mediante códigos de conexión de ruta. La baja hacia atrás se produce cuando se registra con una cantidad acabada una operación con un código de conexión de ruta concreto.  

La cantidad de baja es la cantidad por montaje indicada en la lista de materiales de producción multiplicada por el número de productos principales registrados como cantidad de salida en la operación. Puede no ser la cantidad prevista.  

#### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Registro automático - Baja hacia atrás de toda la orden  
En este método no se tienen en cuenta los códigos de conexión de ruta.  

No se selecciona ningún componente hasta que el estado de la orden de producción lanzada se cambia a *Terminada*. La cantidad de consumo es la cantidad por montaje indicada en la lista de materiales de producción, multiplicada por el número de productos principales que se han terminado y agregado a las existencias.  

Efectuar la baja retroactiva de toda la orden de producción requiere la misma configuración que la baja hacia adelante: el método de creación de informes se debe establecer en hacia atrás en la tarjeta de producto para todos los productos de la lista de materiales principal. Además, todos los códigos de conexión de ruta se deben eliminar de la lista de materiales de producción.  

### <a name="production-output"></a>Salida de producción  
El programa proporciona la posibilidad de realizar el seguimiento del tiempo invertido en el trabajo de una orden de producción, además de registrar la cantidad producida. Esta información puede resultar útil para determinar con más precisión los costes de producción. Los fabricantes que utilicen un sistema de costes estándar, pueden registrar la información real para desarrollar estándares más avanzados.  

La salida se puede procesar mediante el diario de salida, pero, además, el programa la puede registrar automáticamente. El programa copia el método de purga de las fichas del centro de máquina o centro de trabajo en la ruta de la orden de producción al realizar una actualización. Lo mismo que sucede con el consumo de materiales, para la salida hay tres métodos de registro:  

- Manual  
- Adelante  
- Atrás  

El método manual se usa el diario de salida para especificar el tiempo invertido y la cantidad producida.  

El método adelantado registra la salida esperada (y el tiempo), que se registra automáticamente al lanzar la orden de producción. Los códigos de conexión de ruta no se tienen en cuenta en la baja hacia adelante de la salida.  

El método retroactivo registra la salida esperada (y el tiempo), que se registra automáticamente al terminar la orden de producción. Los códigos de conexión de ruta no se tienen en cuenta en la baja hacia atrás de la salida.  

### <a name="posting-consumption-and-output"></a>Registro del consumo y la salida  
Puede utilizar cualquier combinación de consumo automático e información registrada manualmente, tanto para el consumo como para la salida. Por ejemplo, si lo desea puede realizar la baja automática hacia adelante de los componentes, pero utilizar el diario de consumo para registrar el rechazo. De igual forma, podría registrar automáticamente la salida y usar el diario de salida para registrar el rechazo del producto principal o el tiempo adicional invertido en la orden.  

Por último, si introduce el consumo y la salida manualmente, debe determinar la secuencia en que va a registrar la información. Puede registrar el consumo en primer lugar y usar un método abreviado para introducir la información, que se basa en la cantidad de salida prevista. Pero, si lo prefiere, puede introducir primero la salida, mediante la función **Desplegar ruta**. A continuación, registraría el consumo en función de la cantidad de salida real.  

### <a name="production-journal"></a>Diario de producción  
El diario de producción combina las funciones del diario de consumo y de los diarios de salida en uno solo, al que se puede tener acceso directamente desde una orden de producción lanzada.  

La finalidad del diario de producción es la de proporcionar una única interfaz en la que registrar el consumo y la salida de una orden de producción.  

El diario de producción tiene una presentación sencilla y ofrece la posibilidad de:  

- Registrar la salida y el consumo relacionados con una orden de producción  
- Relacionar componentes con operaciones  
- Relacionar datos reales de operaciones con las estimaciones estándar de la ruta de la orden de producción y las líneas de los componentes  
- Registrar e imprimir un resumen de los datos registrados de operaciones de la orden de producción  

En el diario de producción se pueden realizar muchas de las mismas funciones que en los diarios de consumo y salida. Las dimensiones, el seguimiento de productos y los contenidos de ubicación se manejan de la misma forma que en dichos diarios.  

Con todo, el diario de producción difiere de los diarios de consumo y salida en que:  

- Se tiene acceso a él directamente desde una línea de orden de producción lanzada y predefinida con los datos relevantes.  
- Permite definir los tipos de componentes que se van a manipular en función de un filtro por método de baja del diario.  
- Las cantidades y los tiempos ya registrados para la orden se muestran al final de diario como movimientos reales.  
- Los campos donde el registro de datos es irrelevante aparecen en blanco y no se pueden editar.  
- El usuario puede configurar el modo en que las cantidades de salida se predefinen en el diario; por ejemplo, que la última operación debe tener establecida la cantidad de salida en cero.  
- Si sale del diario sin registrar los cambios, aparece un mensaje de solicitud en el que se le permite permanecer en el diario.  
- Muestra juntos las operaciones y los componentes en una estructura lógica que proporciona una vista general del proceso de producción.  

En el diario de producción, las cantidades de consumo se registran como movimientos de producto negativos, las cantidades de salida se registran como movimientos de producto positivos y los tiempos invertidos se registran como movimientos de capacidad.  

## <a name="see-also"></a>Consulte también
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
