---
title: Acerca de las órdenes de producción
description: Obtenga información órdenes de producción y cómo se usan para gestionar la conversión de los materiales adquiridos en productos manufacturados.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Acerca de las órdenes de producción

Las órdenes de producción se usan para gestionar la conversión de los materiales adquiridos en productos manufacturados. Las órdenes de producción dirigen el trabajo por los distintos centros de trabajo o de máquina de la planta.  

Antes de empezar con producción, la mayoría de las empresas realizan una planificación de suministros, normalmente una vez por semana, para calcular cuántos pedidos de producción y de compra ejecutar para cubrir la demanda de ventas esa semana. Los pedidos de compra suministran los componentes que se requieren según la L.M de producción para fabricar los productos finales.

Las órdenes de producción son los componentes esenciales de la funcionalidad de fabricación y contienen la información siguiente:  

- Productos planificados para fabricación  
- Materiales necesarios para las órdenes de producción planificadas  
- Productos que se han fabricado  
- Materiales que ya se han seleccionado  
- Productos que se han fabricado en el pasado  
- Materiales que se utilizaron en operaciones de fabricación anteriores  

Las órdenes de producción son los puntos de partida de:  

- La planificación de la fabricación futura  
- El control de la fabricación actual  
- El seguimiento de la fabricación terminada  

## Creación de órdenes de producción  

Puede crear órdenes de producción una por una, manualmente, desde la página **Orden producción**, o se pueden generar desde las páginas **Planificación pedido venta** o **Planificación de pedidos**. También puede crear varias órdenes se utiliza la página **Hoja planificación**.  

Puede crear órdenes de producción utilizando información sobre:  

- Artículos  
- L.M. de producción
- Rutas  
- Centros de máquina  
- Centros de trabajo  

## Limitaciones en la creación de órdenes de producción  

Las órdenes de producción se reservan automáticamente y se realiza el seguimiento hasta su origen cuando:  

- Se crean desde la [Hoja planificación](production-how-to-run-mps-and-mrp.md)  
- Creado desde la página [Planificación de pedidos de venta](production-how-to-create-production-orders-from-sales-orders.md)  
- Se crean desde la página [Planificación de pedidos](production-how-to-plan-for-new-demand.md)  
- Se usa la función [Replanificar](production-how-to-replan-refresh-production-orders.md) en las órdenes de producción  

Para obtener más información, vea [Seguimiento de relaciones entre demanda y suministro](production-how-track-demand-supply.md).

Las órdenes de producción creadas por otros métodos no se reservan automáticamente, ni se realiza su seguimiento.

## Estado de las órdenes de producción  

El estado de una orden de producción controla su comportamiento en la aplicación. La forma y el contenido de una orden de producción se rigen por el estado de la misma. Las órdenes de producción se muestran en páginas diferentes según sus estados. No puede cambiar el estado de una orden de producción manualmente. Debe usar la función **Cambiar estado** en la orden de producción individual o en la página **Cambiar estado orden prod.**.  

### Orden producción simulada  

Una orden de producción simulada es exclusiva porque tiene las características siguientes:  

- Como su nombre lo indica, es una simulación que puede utilizar para cotizaciones y cálculos de costos. Por ejemplo, cuando el departamento de Investigación y Desarrollo quiere obtener una estimación de costes de un artículo propuesto. Una orden de producción simulada sirve como ejemplo de una orden de producción.  
- No afectan a la planificación de pedidos. La Planificación (MPS y MRP) no tiene en cuenta ni se ve afectada por las órdenes de producción simuladas. Además, una orden de producción simulada no se puede usar como libro, porque deja de existir cuando se cambia su estado.  

### Orden producción planificada  

Una orden de producción planificada es exclusiva porque tiene las características siguientes:  

- Las órdenes de producción planificadas se pueden crear automáticamente desde un pedido de venta.  
- Las órdenes de producción planificadas son iguales que las órdenes de producción lanzadas y proporcionan datos para la planificación de los requisitos de capacidad, ya que muestran los requisitos de capacidad totales por centro de trabajo o de máquina.  
- Las órdenes de producción planificadas representan la mejor estimación de la carga de trabajo futura de un centro de trabajo o de máquina, en función de la información disponible. Normalmente, se generan desde la planificación, pero también se pueden crear manualmente. Si se tiene en cuenta que se eliminan en las planificaciones posteriores, la creación manual no resulta práctica.  
- Si se generan en planificación, se crea una "planificación de liberación órdenes" sugerida, que contiene la cantidad, la fecha de lanzamiento y la fecha de vencimiento. La lógica del sistema de planificación se basa en el sistema de reposición, las directivas de reaprovisionamiento y los modificadores de pedido con que se encuentra en el proceso de planificación de la demanda neta.  
- Para conocer sus efectos, observe la carga de cada centro de trabajo o de máquina de la ruta de una orden de producción planificada.  

### Orden producción planificada en firme  

Una orden de producción planificada en firme es exclusiva porque tiene las características siguientes:  

- Una orden de producción planificada en firme se puede crear a partir de un pedido de venta.  
- Una orden de producción planificada en firme actúa como marcador de posición, dentro del programa de planificación, de un proyecto futuro liberado en la planta.  
- Una orden de producción planificada en firme se puede generar desde la planificación, o se puede crear manualmente o a partir de pedidos de venta. No se elimina en las planificaciones posteriores.  
- Si se generan en planificación, se crea una "planificación de liberación órdenes" sugerida, que contiene la cantidad, la fecha de lanzamiento y la fecha de vencimiento. La lógica del sistema de planificación se basa en el sistema de reposición, las directivas de reaprovisionamiento y los modificadores de pedido con que se encuentra en el proceso de planificación de la demanda neta.  
- Para conocer sus efectos, observe la carga de cada centro de trabajo o de máquina de la ruta de una orden de producción planificada en firme.  

### Orden de producción lanzada  

La orden de producción lanzada es exclusiva, porque tiene las características siguientes:  

- Las órdenes de producción lanzadas se pueden crear automáticamente desde un pedido de venta.  
- El lanzamiento de una orden de producción no implica que se hayan preparado los materiales o que el proyecto haya avanzado físicamente a la primera operación.  
- En un entorno de fabricación contra pedido (MTO), no es raro crear una orden de producción lanzada en cuanto se introduce el pedido de venta.  
- El consumo de material y la salida del producto reales se pueden registrar manualmente con una orden de producción lanzada. Además, la baja automática del consumo y la salida del producto sólo tienen lugar con las órdenes de pedido lanzadas.  

### Orden producción terminada  

Una orden de producción terminada es exclusiva, porque tiene las características siguientes:  

- Normalmente, una orden de producción terminada es la que ya se ha fabricado.  
- La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando. Tras terminar una orden de producción, los costes se pueden ajustar y conciliar.  
- Las órdenes de producción terminadas se usan para crear informes estadísticos y para posibilitar el seguimiento de los pedidos (de venta, de producción y de compra, por ejemplo). La posibilidad de realizar el seguimiento hasta una orden de producción terminada permite revisar el historial detallado.  
- Las órdenes de producción terminadas no se pueden modificar nunca.  

## Ejecución de las órdenes de producción  

Tras crear y programar una orden de producción, se tiene que lanzar a la planta para su ejecución. Durante la ejecución de la orden se registra lo siguiente:  

- Los materiales preparados o consumidos  
- El tiempo de trabajo invertido en la orden  
- La cantidad de producto principal producida  

Puede registrar esta información manualmente o por medio de informes automáticos. El método depende de la configuración en el campo Método de lavado del artículo y centro de trabajo.  

### Consumo de material  

[!INCLUDE [prod_short](includes/prod_short.md)] ofrece varias opciones sobre cómo registrar el consumo de material. Por ejemplo, se puede registrar de forma manual, lo que puede ser aconsejable si los componentes se sustituyen con frecuencia o la cantidad de productos rechazados es mayor que la prevista.  

El consumo de material se puede procesar mediante el [diario de consumo](production-how-to-post-consumption.md). Además, la aplicación lo puede registrar automáticamente por [!INCLUDE [prod_short](includes/prod_short.md)], lo que se denomina creación automática de informes (lavado). Están disponibles los métodos de generación de informes manual, directo y retroactivo.

El método de creación manual de informes de consumo usa el diario de consumo para especificar la preparación de material.  

El método de creación de informes anticipados presupone que la cantidad esperada de todos los materiales de todo el pedido se consume al lanzar una orden de producción, salvo que se usen códigos de conexión de ruta. Si se usan códigos de conexión de ruta, el material consumido después del inicio del paso operativo se registra en el diario de salida. Para llevar a cabo la baja hacia adelante de toda la orden de producción, es necesario lo siguiente:  

- Todos los productos de la lista de materiales de producción de nivel superior deben tener seleccionado el método de baja hacia adelante en la ficha de producto correspondiente.  
- Se deben eliminar todos los códigos de conexión de ruta de la lista de materiales de producción.  

El método de creación de informes retroactivos registra la cantidad real de todo el material preparado o consumido cuando el estado de una orden de producción se cambia a *Terminada*, salvo que se usen códigos de conexión de ruta. Si se usan códigos de conexión de ruta, el material se consume una vez que se ha registrado una cantidad del producto principal para el paso operativo en el Diario de salida.  

Al actualizar la orden de producción, el método de baja se copia de la ficha del producto. Puesto que el método de baja de cada componente de la orden de producción controla cómo y cuándo se registra el consumo, es importante tener en cuenta que el método de baja de un producto concreto se puede cambiar directamente en la orden de producción. Para obtener más información, consulte [Bajar componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).

### Salida de producción  

[!INCLUDE [prod_short](includes/prod_short.md)] proporciona la capacidad de realizar el seguimiento del tiempo invertido en el trabajo de una orden de producción, además de registrar la cantidad producida. Esta información puede resultar útil para determinar con más precisión los costes de producción. Los fabricantes que utilicen un sistema de costes estándar, pueden registrar la información real para desarrollar estándares más avanzados.  

La salida se puede procesar mediante el [diario de salida](production-how-to-post-output-quantity.md), pero, además, se puede registrar automáticamente. [!INCLUDE [prod_short](includes/prod_short.md)] copia el método de purga de las fichas del centro de máquina o centro de trabajo en la ruta de la orden de producción al realizar una actualización. Lo mismo que sucede con el consumo de materiales, para la salida existen los métodos de registro manual, adelantado o retroactivo.

El método manual se usa el diario de salida para especificar el tiempo invertido y la cantidad producida.  

El método adelantado registra la salida esperada (y el tiempo), que se registra automáticamente al lanzar la orden de producción. Los códigos de conexión de ruta no se tienen en cuenta en la baja hacia adelante de la salida.  

El método retroactivo registra la salida esperada (y el tiempo), que se registra automáticamente al terminar la orden de producción. Los códigos de conexión de ruta no se tienen en cuenta en la baja hacia atrás de la salida.  

### Registro del consumo y la salida  

Puede utilizar cualquier combinación de consumo automático e información registrada manualmente, tanto para el consumo como para la salida. Por ejemplo, si lo desea puede realizar la baja automática hacia adelante de los componentes, pero utilizar el diario de consumo para registrar el rechazo. De igual forma, podría registrar automáticamente la salida y usar el diario de salida para registrar el rechazo del producto principal o el tiempo adicional invertido en la orden.  

Por último, si introduce el consumo y la salida manualmente, debe determinar la secuencia en que va a registrar la información. Puede registrar el consumo en primer lugar y usar un método abreviado para introducir la información, que se basa en la cantidad de salida prevista. Pero, si lo prefiere, puede introducir primero la salida, mediante la función **Desplegar ruta**. A continuación, registraría el consumo en función de la cantidad de salida real.  

### Diario de producción  

El [diario de producción](production-how-to-register-consumption-and-output.md) combina las funciones del diario de consumo y de los diarios de salida en uno solo, al que se puede tener acceso directamente desde una orden de producción lanzada.  

La finalidad del diario de producción es la de proporcionar una única interfaz en la que registrar el consumo y la salida de una orden de producción.  

El diario de producción tiene una presentación sencilla y ofrece la posibilidad de:  

- Registrar la salida y el consumo relacionados con una orden de producción  
- Relacionar componentes con operaciones  
- Relacionar datos reales de operaciones con las estimaciones estándar de la ruta de la orden de producción y las líneas de los componentes  
- Registrar e imprimir un resumen de los datos registrados de operaciones de la orden de producción  

En el diario de producción se pueden realizar muchas de las mismas funciones que en los diarios de consumo y salida. Las dimensiones, el seguimiento de artículos y el contenido del contenedor se manejan de la misma manera.  

Con todo, el diario de producción difiere de los diarios de consumo y salida en que:  

- Se tiene acceso a él directamente desde una línea de orden de producción lanzada y predefinida con los datos relevantes.  
- Permite definir los tipos de componentes que se van a manipular en función de un filtro por método de baja del diario.  
- Las cantidades y los tiempos ya registrados para la orden se muestran al final de diario como movimientos reales.  
- Los campos donde el registro de datos es irrelevante aparecen en blanco y no se pueden editar.  
- El usuario puede configurar el modo en que las cantidades de salida se predefinen en el diario; por ejemplo, que la última operación debe tener establecida la cantidad de salida en cero.  
- Si sale del diario sin registrar los cambios, aparece un mensaje de solicitud en el que se le permite permanecer en el diario.  
- Muestra juntos las operaciones y los componentes en una estructura lógica que proporciona una vista general del proceso de producción.  

En el diario de producción, las cantidades de consumo se registran como movimientos de producto negativos, las cantidades de salida se registran como movimientos de producto positivos y los tiempos invertidos se registran como movimientos de capacidad.  

## Consulte también

[Fabricación](production-manage-manufacturing.md)
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
