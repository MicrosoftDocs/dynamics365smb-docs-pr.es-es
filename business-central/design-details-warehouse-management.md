---
title: Administrar actividades de almacén
description: 'Además de recibos y envíos, Business Central admite una serie de actividades internas de almacén.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/09/2023
ms.custom: bap-template
---

# Información general de la gestión de almacenes

Hay dos cosas que son importantes para todas las empresas que mueven mercancías físicamente dentro y fuera de su almacén:

* Tienen una visión general de los niveles de inventario y la ubicación de los artículos en el almacén.
* Pueden recibir, recoger y enviar artículos de forma rápida y precisa.

Para ayudar a las empresas a lograr esas cosas, las funciones de almacén en [!INCLUDE[prod_short](includes/prod_short.md)] agregan las siguientes capacidades a la gestión de inventario:

* Ubicaciones
* Envíos de almacén
* Picking de inventario
* Hoja trabajo mov.

Implemente estas características en diferentes combinaciones para adaptar sus procesos de almacén a su empresa. Permita una mayor complejidad a medida que su empresa crece y sus procesos cambian.

## Descripción general de las diferentes opciones de configuración

Puede configurar funciones de almacén de varias formas. Es importante elegir opciones que mejoren sus procesos sin causar gastos generales. La siguiente tabla ofrece una descripción general de las configuraciones típicas para tratar con bienes físicos.

|Nivel de complejidad|Descripción|Configuración|Cód. ubicación|Ejemplo de flujo de entrada|Ejemplo de flujo de salida|Ejemplo de flujo interno|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|No hay ninguna actividad de almacén dedicada.|Registrar desde pedidos y diarios||Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Pedido de compra|Pedido de venta| Orden de producción -> diario de consumo|  
|Básico|Publicación consolidada de recepción/envío para múltiples pedidos.|**Recepción requerida**<br>**Envío requerido**|Opcional. Controlado por el control de alternancia Código Bin es Obligatorio|Órdenes de compra -> Certificado de depósito|Pedido de venta -> Cabecera envío almacén|Igual que en el caso anterior.|
|Básico|Pedido por pedido.|Requerir almacenamiento o Requerir picking. </br><br/> **NOTA**: Aunque las configuraciones se denominan **Picking requerido** y **Ubicación requerida**, todavía puede registrar recibos y envíos directamente desde los documentos empresariales de origen en las ubicaciones donde se selecciona estas casillas de verificación.|Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Orden de compra -> Ubicación de inventario|Pedido de venta -> Picking de inventario|Pedido de producción -> Picking de inventario|
|Avanzado|Publicación consolidada de recepción/envío para múltiples pedidos.<br /><br />Actividades de selección/ubicación consolidadas para múltiples documentos de origen.|Requerir recepción + Requerir ubicación,</br> Requerir envío + Requerir picking|Opcional. Controlado por el control de alternancia Código Bin es Obligatorio|Órdenes de compra -> Recibo de almacén -> Ubicación de almacén|Órdenes de venta -> Envíos de almacén -> Seleccionar hoja de trabajo -> Selecciones de almacén| Orden de producción -> Seleccionar hoja de trabajo -> Selecciones de almacén -> diario de consumo|
|Avanzado|Igual que arriba + Actividades de selección/ubicación dirigidas|Selección y ubicación dirigidas (los conmutadores dependientes se habilitarán automáticamente)|Obligatoria|Igual que en el caso anterior.|Igual que en el caso anterior.| Orden de producción -> Seleccionar hoja de trabajo -> Diario de consumo de selecciones de almacén|

La complejidad aumenta con el tamaño de su organización y la cantidad de departamentos y personas involucradas. Un proceso puede ser simple, por ejemplo, cuando la misma persona crea y contabiliza un documento de ventas. Los procesos también pueden ser más complejos e involucrar varios pasos y personas. Los siguientes pasos son un ejemplo de un proceso más complejo:

1. Un procesador de pedidos crea un pedido de ventas.
1. Un gerente de almacén crea instrucciones de recolección.
1. Un empleado del almacén finaliza el flujo registrando el envío del almacén.

El nivel de complejidad también se ve afectado por los tipos de documentos que utiliza en las actividades de su almacén. Por ejemplo, puede usar documentos de recibo de almacén y ubicación de almacén para su flujo de entrada, pero use documentos de selección de inventario para su flujo de salida.

Otro factor que afecta la complejidad es cómo se representa su almacén físico en [!INCLUDE[prod_short](includes/prod_short.md)]. Obtenga más información en [Modelado del almacén físico](#modeling-the-physical-warehouse).

## Modelado del almacén físico

Tiene varias opciones para representar la configuración real de su almacén en [!INCLUDE[prod_short](includes/prod_short.md)]. Sus elecciones determinan cómo trabajará con las características del almacén.

La ubicación de los artículos puede ser estantes, ubicaciones o contenedores, y existen ventajas y desventajas para cada opción.

### Ubicaciones y contenedores

Para manejar bienes físicos, debe tener al menos una ubicación. Puede usar múltiples ubicaciones o usar contenedores para modelar su almacén y estructura organizacional.

Por lo general, las ubicaciones son la forma preferida de organizar las operaciones que se distribuyen en áreas geográficas. Sin embargo, en algunos casos, es posible que desee crear varias ubicaciones que estén ubicadas en el mismo lugar. El uso de ubicaciones tiene las siguientes ventajas:

* Otorgue acceso mediante las páginas **Empleado de almacén** y **Centros de responsabilidad**.
* Defina calendarios, rutas y tiempos de manejo de entrada y salida para el cálculo y la planificación de fechas. Obtenga más información en [Sobre la funcionalidad de la planificación](production-about-planning-functionality.md).
* Especifique las dimensiones predeterminadas y use diferentes configuraciones de publicación de inventario.
* Configurar los parámetros de planificación. Obtenga más información en [Parámetros de planificación](production-about-planning-functionality.md#planning-parameters).  
* Use diferentes funciones de almacén para cada ubicación.

### Estantes y contenedores

Si siempre almacena un artículo en el mismo lugar, puede usar el campo **N.º de estante** en las páginas **Tarjeta de artículo** o **Tarjeta de unidad de inventario**. Este campo puede utilizarse como sistema de almacenamiento manual básico en entornos sin ubicaciones. El valor del campo se copia desde la ficha de producto en línea de documento e informes, pero es solo informativo. El valor no se utiliza en las actividades de almacén o en los cálculos de disponibilidad.

Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos.

* Uno o más contenedores fijos para un artículo.
* Contenedores para operaciones específicas, como un contenedor de envío o un contenedor de salida de producción.
* Restricciones de capacidad y peso de la ubicación (solo para ubicación y recolección dirigidas).
* Valoración de ubicación (solo para selección y ubicación dirigidas).

## Flujo de trabajo de almacén típico

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|En un flujo básico pedido por pedido, use una ubicación de inventario para registrar la recepción de artículos en las ubicaciones, incluido cualquier exceso de recepción. O bien, si está consolidando varios pedidos en el recibo, use un recibo de almacén.|[Flujo de entrada](design-details-inbound-warehouse-flow.md)|
|Registre el envío de artículos desde ubicaciones de almacén. En una base de pedido por pedido, use una selección de inventario. O bien, si está consolidando varios pedidos en el envío, use un envío de almacén.|[Flujo de salida](design-details-outbound-warehouse-flow.md)|
|Manejar artículos dentro de la ubicación del almacén. Por ejemplo, cuando mueve componentes a producción o hace un recuento de inventario físico.|[Flujo interno](design-details-internal-warehouse-flows.md)|

Configure los procesos de almacén adecuados para su empresa. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).

## Terminología relacionada con la gestión de almacenes

### Niveles de complejidad

Usamos los términos "básico" y "avanzado" para diferenciar entre niveles de complejidad. Esta diferenciación sencilla abarca diferentes niveles de complejidad en configuraciones de ubicación, tal como admiten distintos documentos de almacén. El nivel más avanzado de almacenamiento se conoce como "Almacenamiento y recolección dirigidos". Para usar la ubicación dirigida y la selección para una ubicación, active el control de alternancia **ubicación dirigida y elija** en la página **Tarjeta de ubicación**.

### Flujos de almacén

* Flujo entrante: los productos se trasladan a la ubicación del almacén y se ponen a disposición, como compras y transferencias de entrada.
* Flujo de salida: seleccione y envíe artículos a clientes u otras ubicaciones.
* Flujo interno: maneje elementos dentro de una ubicación. Por ejemplo, los componentes se mueven a producción o se hace un recuento de inventario físico.

### Documentos básicos  

Los siguientes documentos se utilizan en flujos básicos de almacén.

* Ubicación existencias
* Picking inventario
* Movimiento inventario
* Diario productos
* Diario reclasificación producto

### Documentos avanzados  

Los siguientes documentos se utilizan en flujos avanzados de almacén.

* Recep. almacén
* Hoja trabajo ubic.
* Ubicar almacén
* Hoja trabajo picking
* Picking almacén
* Hoja trabajo mov.
* Movimiento almacén
* Picking interno de almacén
* Almacenamiento interno de almacén
* Hoja trab. creación ubicación
* Hoja trab. creac. cont. ubic.
* Diario de productos de almacén
* Diario de reclasificación de artículos de almacén

### Páginas y configuraciones

Esta sección describe los conceptos detrás de las páginas clave y la configuración para el almacenamiento.

#### Ubicaciones y contenido de ubicación

Una ubicación es un dispositivo de almacenamiento diseñado para contener partes diferenciadas. Es la unidad de contenedor de menos tamaño en [!INCLUDE[prod_short](includes/prod_short.md)]. Las cantidades de producto en las ubicaciones se denominan *contenidos de ubicación*. Una búsqueda desde campo de **Producto** o el campo **Cód. ubicación** en cualquier línea de documento relacionada con el almacén muestra la disponibilidad calculada del producto en la ubicación.  

Los contenidos de ubicación puede ser **Fijos**, **Dedicados**, o **Predeterminados** para definir cómo el contenido de la ubicación puede utilizarse. Las ubicaciones con ninguna de estas propiedades se conocen como ubicaciones *aleatorias*.  

Una ubicación fija guarda productos asignados al código de ubicación. La propiedad bin fija garantiza que incluso si se vacía el contenedor, el contenido del contenedor no desaparece. Puede volver a seleccionar el contenedor tan pronto como se reponga su contenido.  

Una ubicación dedicada guarda contenido de ubicación que solo puede seleccionarse para el recurso dedicado que utiliza la ubicación. Por ejemplo, un centro de máquinas. Otro contenido no relacionado con picking, como las cantidades de salida en un registro de envío, se pueden consumir de una ubicación dedicada. Solo el contenido de la ubicación que tiene en cuenta el algoritmo de **Crear picking** está protegido en una ubicación dedicada.  

[!INCLUDE [prod_short](includes/prod_short.md)] usa la propiedad de ubicación **predeterminada** para sugerir ubicaciones a las actividades de almacén. En las ubicaciones que usan ubicación y recolección dirigidas, no se usa la propiedad de ubicación predeterminada. En los almacenen donde se requieren ubicaciones, la propiedad especifica dónde colocar los productos en los flujos de entrada. En los flujos de salida, la propiedad especifica de dónde extraer productos.  

> [!NOTE]  
> Si los productos de salida se colocan en varias ubicaciones, los productos se extraen primero de las ubicaciones no predeterminadas para vaciar su contenido y, a continuación, los productos restantes se extraen de la ubicación predeterminada.  

Puede tener una ubicación predeterminada por producto y ubicación.  

#### Tipo ubicación

Las ubicaciones que utilizan ubicación y selección dirigidas pueden utilizar tipos de ubicación. Los tipos de contenedores controlan las actividades que permite para un contenedor. Los siguientes tipos de ubicación están disponibles:  

|Tipo ubicación|Descripción|  
|------------------|---------------------------------------|  
|RECEPC|Artículos que se reciben pero no se guardan.|  
|ENVIAR|Productos de los que se ha realizado el picking de las líneas de los envíos de almacén, pero que no se han registrado como enviados.|  
|UBICAR|Normalmente, productos que se almacenan en unidades de medida grandes a las que no desea que tenga acceso para realizar el picking. Estos contenedores no se utilizan para realizar pedidos, ni para pedidos de producción ni para envíos, por lo que su uso puede estar limitado. Este tipo de contenedor es útil cuando compra una gran cantidad de artículos. Las ubicaciones siempre deben tener una clasificación de ubicación baja, de modo que los artículos con ubicaciones PUTPICK de clasificación más alta se guarden primero. Reabastezca periódicamente este tipo de contenedores para que sus artículos estén disponibles en contenedores tipo PUTPICK o PICK.|  
|PICKING|Productos que solo se van a usar para picking. Solo puede hacer movimientos para el reabastecimiento de estas ubicaciones, no por ubicación.|  
|COLOCARPICKING|Artículos en ubicaciones que se sugieren para ubicaciones y picking. Probablemente, las ubicaciones de este tipo tengan distintos rankings de ubicación. Configure las ubicaciones de almacenamiento masivo con rankings de ubicación más bajos que las ubicaciones de picking normales o las ubicaciones del área de picking de seguimiento.|  
|QC|Esta ubicación se utiliza para ajustes de inventario si se especifica en la ficha de almacén en el campo **Cód. ubicación ajuste**. También puede configurar ubicaciones de este tipo para productos defectuosos y productos que es preciso inspeccionar. puede mover productos a este tipo de ubicación si desea que no se tenga a consulta a los mismos desde el flujo de productos normal. **Nota**: A diferencia de resto de tipos de ubicación, el de **QC** no tiene seleccionada de forma predeterminada ninguna de las casillas de verificación de manejo de artículos. El contenido que sitúe en una ubicación de control de calidad no se incluye de los flujos del artículo.|  

Con las excepciones de los tipos de contenedores PICK, PUTPICK y PUTAWAY, el tipo de contenedor define la actividad permitida para un contenedor. Por ejemplo, solo puede usar una ubicación de tipo RECEPCIÓN para recibir en ella productos o para seleccionar productos de ella.  

> [!NOTE]  
> Debe usar movimientos para mover artículos a contenedores RECIBIR y QC. use movimientos para mover artículos de contenedores SHIP y QC.  

#### Ranking ubicación

En la gestión avanzada del almacén, puede automatizar y optimizar cómo se recogen los productos en hojas de trabajo de colocación y selección clasificando las ubicaciones. Se propone la extracción y colocación de productos según los criterios de clasificación.

Los procesos de ubicación se optimizan según el ranking de ubicación mediante la sugerencia de ubicaciones de ranking superior con respecto a las de ranking inferior. Los procesos de picking sugieren primero productos con la clasificación más alta del contenido de la ubicación. La reposición de ubicación sugiere las ubicaciones de rango inferior antes que las ubicaciones de rango superior.  

La clasificación de los contenedores y el contenido de los contenedores son las propiedades básicas que guían a los empleados del almacén en el almacén.  

#### Configuración de ubicación

En el almacenamiento avanzado, puede especificar los siguientes valores de capacidad para controlar cómo y en qué contenedores almacena artículos:

* Cantidad
* Cubos totales
* Peso  

Puede asignar una unidad de medida base (UOM) a los artículos. Una unidad de medida base puede ser piezas, paletas, litros, gramos o cajas. También puede crear unidades de medida más grandes en función de su unidad de medida base. Por ejemplo, si las piezas son su unidad de medida básica, un palé puede equivaler a 16 piezas.  

Si un artículo tiene más de una UOM, establezca la cantidad máxima para cada UOM en la ficha del artículo. Si gestiona un artículo en unidades y palés, el campo **Cdad. máxima** de la página **Contenido ubicación** para ese producto deberá estar igualmente en unidades y palés. De lo contrario, la cantidad permitida para esa ubicación no se calculará correctamente.  

Antes de establecer restricciones de capacidad para contenidos de ubicación en una ubicación, asegúrese de que la unidad de medida y las dimensiones del producto se hayan definido en el producto.  

> [!NOTE]  
> Solo puede usar varias unidades de medida en ubicaciones que usan ubicación y recolección dirigidas. En el resto de las configuraciones, solo puede usar contenidos de ubicación en la unidad de medida base. En todas las transacciones con un unidad de medida mayor que la unidad de medida base del producto, la cantidad se convierte a la unidad de medida base.  

#### Zona

En la gestión avanzada del almacén, las ubicaciones se pueden agrupar en las zonas para controlar el direccionamiento del flujo de trabajo de las actividades de almacén para los almacenes.  

Una zona podría ser una zona de recepción o una zona de almacenamiento, y cada zona puede componerse de más ubicaciones.  

La mayoría de las propiedades asignadas a una zona se asignan a las ubicaciones que se crean para la zona.  

#### Clase almacén

En el almacenamiento avanzado, puede asignar códigos de clase de almacén a las siguientes entidades: 

* Artículos
* Ubicaciones
* Zonas

Las clases de almacén controlan dónde almacenar artículos. Puede dividir una zona en varias clases de almacén. Por ejemplo, podría almacenar productos en la zona de recepción como congelados, peligrosos o de otra clase.

Cuando trabaja con clases de almacén y una ubicación de recepción o envío predeterminada, debe elegir manualmente las ubicaciones apropiadas en la recepción y en las líneas de albarán de almacén.  

En los flujos entrantes, el código de clase está resaltado con líneas de entrada cuando el código de clase del producto no coincide con la ubicación predeterminada de recepción. Si no se han asignado las ubicaciones predeterminadas correctas, la cantidad no puede recibirse.  

#### Almacén

Una ubicación es una estructura física o lugar donde se recibe, almacena y envía el inventario. Una ubicación puede ser un almacén, un vehículo de servicio, una sala de exposición, una planta o un área de una planta. El inventario a menudo se organiza en contenedores y zonas.

#### Primero en caducar primero en salir

Si selecciona la casilla **Picking según FEFO** en la ficha desplegable **Directivas ubicación** de la página **Ficha de almacén**, los productos con seguimiento se seleccionan en el almacén según su fecha de vencimiento. Primero se realiza el picking de los productos con las fechas de vencimiento más tempranas.  

Las actividades de almacén en todos los documentos de picking y de movimientos se ordenan según FEFO, a menos que los productos tengan asignados números de serie o de lote. Si una parte de la cantidad, pero no toda, en la línea tiene ya asignados números de lote o de serie, la cantidad restante se ordena según el método FEFO.  

Cuando se realiza la selección por FEFO, el programa recopila los productos que caducan en primer lugar y el resultado es una lista temporal de seguimiento de productos basada en la fecha de vencimiento. Si dos productos tienen la misma fecha de caducidad, se selecciona primero aquel cuyo número de lote o de serie sea menor. Si los números de lote o de serie son iguales, se selecciona primero el producto que se registró en primer lugar. Los criterios estándar para seleccionar productos en ubicaciones de selección, como Ranking ubicación y División bulto, se aplican a la lista temporal de seguimiento de productos FEFO.  

#### Plantilla ubicar

Las plantillas de ubicación especifican un conjunto de reglas con prioridad que se aplican al crear ubicaciones. Por ejemplo, una plantilla de ubicación puede requerir que coloque artículos en una ubicación con contenido de ubicación que tenga la misma unidad de medida. Si no se puede encontrar un contenedor similar con suficiente capacidad, el artículo debe colocarse en un contenedor vacío. Se asigna una plantilla de ubicación a un producto y a una ubicación.  

## Consulte también .

[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]