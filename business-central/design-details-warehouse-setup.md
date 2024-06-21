---
title: 'Detalles de diseño: Configuración de almacén'
description: 'La funcionalidad del almacén contiene diferentes niveles de complejidad, que se define en gran medida por la configuración de ubicación en las fichas de almacén.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-warehouse-setup"></a>Detalles de diseño: Configuración de almacén

La funcionalidad de almacén en [!INCLUDE[prod_short](includes/prod_short.md)] contiene distintos niveles de complejidad, tal como se define mediante los permisos de licencia en los módulos ofrecidos. El nivel de complejidad de una solución de almacén se define en gran medida con la configuración de ubicación en las fichas de ubicación, que, a su vez, se controla mediante licencia, por lo que el acceso a los campos de configuración de ubicación está definido por la licencia. Además, los objetos de la aplicación en la licencia rigen qué documento de la IU que se deberá usar para las actividades de almacén permitidas.  
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

En la tabla siguiente se muestran los módulos que se requieren para definir los distintos niveles de complejidad de almacenamiento, que documentos de IU admite cada nivel y qué códigos de ubicación reflejan estos niveles en la base de datos de demostración de [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

|Nivel de complejidad|Descripción|Documento de IU|Ubicación de ejemplo|Requisito mínimo del módulo|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|No hay ninguna actividad de almacén dedicada.<br /><br /> Registro de recepción/envío de pedidos.|Pedido|AZUL|Inventario básico|  
|2|No hay ninguna actividad de almacén dedicada.<br /><br /> Registro de recepción/envío de pedidos.<br /><br /> Se requiere el código de ubicación.|Pedido, con código de ubicación|PLATA|Inventario básico/Ubicación|  
|3 <br /><br /> **NOTA**: A pesar de que las configuraciones se denominan **Picking requerido** y **Ubicación requerida**, todavía puede registrar recibos y envíos directamente desde los documentos empresariales de origen en las ubicaciones donde se selecciona estas casillas de verificación.|Actividad de almacén básica, pedido por pedido.<br /><br /> Registro de recepción/envío de documentos de ubicación/picking de inventario. <br /><br /> Se requiere el código de ubicación.|Ubicación inventario/Movimiento de inventario/Picking inventario, con código de ubicación|(PLATA + Requerir ubicación o Requerir ubicación)|Inventario básico/Ubicación/Almacén/Selección|  
|4|Actividad del almacén avanzada, para varios pedidos.<br /><br /> Registro de recepción o envío consolidado según registros de ubicación o selección de almacén.|Recepción de almacén/Ubicación de almacén/Picking de almacén/Envío de almacén/Hoja de trabajo de picking|VERDE|Inventario básico/Recepción en almacén/Almacén/Selección/Envío de almacén|  
|5|Actividad del almacén avanzada, para varios pedidos.<br /><br /> Registro de recepción o envío consolidado según registros de ubicación o selección de almacén.<br /><br /> Se requiere el código de ubicación.|Recepción de almacén/Ubicación de almacén/Picking de almacén/Envío de almacén/Hoja de trabajo de picking/Hoja de trabajo de ubicación, con código de ubicación|(VERDE + ubicación obligatorio)|Inventario básico/Ubicación/Recepción en almacén/Almacén/Selección/Envío de almacén|  
|6 <br /><br /> **Nota**: Este nivel se conoce como "SGA", ya que requiere el módulo más avanzado: Sistemas de gestión de almacenes.|Actividad del almacén avanzada, para varios pedidos<br /><br /> Registro de recepción o envío consolidado según registros de ubicación o selección de almacén<br /><br /> Se requiere el código de ubicación.<br /><br /> El código de zona o clase es opcional.<br /><br /> Empleados de almacén dirigidos por flujo de trabajo<br /><br /> Planificación de reposición de ubicación<br /><br /> Ranking ubicación<br /><br /> Configuración de ubicación por capacidad<br /><br /> Inserción  <!-- Hand-held device integration -->|Recepción de almacén/Ubicación de almacén/Picking de almacén/Envío de almacén/Movimiento de almacén/Hoja de trabajo de picking/Hoja de trabajo de ubicación/Picking almacén interno /Ubicación de almacén interno con código de ubicación/clase/zona<br /><br /> Varias hojas de trabajo para la administración de ubicaciones<br /><br /> Pantallas de ADCS|BLANCO|Inventario básico/Ubicación/Almacén/Recepción en almacén/Selección/Envío de almacén/Sistemas de gestión de almacenes/Almacenes y selecciones internos/Configuración de almacén/<!-- Automated Data Capture System/ -->Configuración de ubicación|  

Para ver ejemplos de cómo se usan los documentos de la IU por nivel de complejidad de almacén, consulte [Detalles de diseño: Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md).  

## <a name="bin-and-bin-content"></a>Ubicación y contenido de ubicación

Una ubicación es un dispositivo de almacenamiento diseñado para contener partes diferenciadas. Es la unidad de contenedor de menos tamaño en [!INCLUDE[prod_short](includes/prod_short.md)]. Las cantidades de producto en las ubicaciones se denominan contenido de ubicación. Una búsqueda desde campo de **Producto** o el campo **Cód. ubicación** en cualquier línea de documento relacionada con el almacén muestra la disponibilidad calculada del producto en la ubicación.  

Un contenido de ubicación puede tener una propiedad de Fija, Dedicada, o Predeterminada para definir cómo el contenido de la ubicación puede utilizarse. Las ubicaciones con ninguna de estas propiedades se conocen como ubicaciones aleatorias.  

Una ubicación fija guarda productos asignados al código de ubicación en cuestión. La propiedad de ubicación fija garantiza que, incluso si el contenido de ubicación se vacía momentáneamente, no desaparezca el contenido de ubicación y, por lo tanto, la ubicación se vuelva a seleccionar tan pronto como se haya repuesto.  

Una ubicación dedicada guarda contenido de ubicación que solo puede seleccionarse para el recurso dedicado, como un centro de máquina, que utiliza la ubicación en cuestión. Otro contenido no relacionado con picking, como las cantidades de salida en un registro de envío, se pueden consumir de una ubicación dedicada. Solo el contenido de la ubicación que tiene en cuenta el algoritmo de **Crear picking** está protegido en una ubicación dedicada.  

El sistema usa la propiedad de ubicación predeterminada para sugerir ubicaciones a las actividades de almacén. En los almacenes SGA no se usa la propiedad de ubicación predeterminada. En los almacenen donde se requieren ubicaciones, la propiedad se usa en los flujos de entrada para especificar dónde colocar los productos. En los flujos de salida, la propiedad se utiliza para especificar de dónde extraer productos.  

> [!NOTE]  
>  Si los productos de salida se colocan en varias ubicaciones, los productos se extraen primero de las ubicaciones no predeterminadas para vaciar su contenido y, a continuación, los productos restantes se extraen de la ubicación predeterminada.  

Solo puede haber una ubicación predeterminada por producto y ubicación.  

## <a name="bin-type"></a>Tipo ubicación

En instalaciones WMS puede restringir las actividades de almacén permitidas para una ubicación asignándoles un tipo de ubicación. Existen los siguientes tipos de ubicación:  

|Tipo ubicación|Descripción|  
|------------------|---------------------------------------|  
|RECEPC|Productos registrados como recibidos, pero no ubicados.|  
|ENV|Los productos de los que se ha realizado el picking de las líneas de los envíos de almacén, pero que no se han registrado como enviados.|  
|UBICAR|Normalmente, los productos se almacenan en unidades de medida grandes a las que no desea que tenga acceso para realizar el picking. Debido a que no se realiza el picking de estas ubicaciones, ya sea de órdenes de producción o envíos, el uso de una ubicación de tipo Ubicar puede estar limitado, pero este tipo de ubicación podría ser útil si ha comprado una gran cantidad de productos. Las ubicaciones de este tipo siempre deben tener un ranking de ubicación bajo, para que cuando se coloquen los productos recibidos, se ubiquen primero otras ubicaciones COLOCARPICKING de ranking más alto asignados al producto. Si utiliza este tipo de ubicación, debe realizar con regularidad la reposición de ubicación para que los productos almacenados en estas ubicaciones también estén disponibles en ubicaciones de tipo COLOCARPICKING o PICKING.|  
|PICKING|Productos que solo se van a usar para picking. El reabastecimiento de estas ubicaciones solo se puede realizar por el movimiento, no por ubicación.|  
|COLOCARPICKING|Artículos en ubicaciones que se sugieren para funciones de ubicación y de picking. Probablemente, las ubicaciones de este tipo tengan distintos rankings de ubicación. Puede configurar las ubicaciones de almacenamiento masivo como de este tipo con rankings de ubicación bajos comparados con las ubicaciones de picking normales o las ubicaciones del área de picking de seguimiento.|  
|QC|Esta ubicación se utiliza para ajustes de inventario si se especifica en la ficha de almacén en el campo **Cód. ubicación ajuste**. También puede configurar ubicaciones de este tipo para productos defectuosos y productos que es preciso inspeccionar. puede mover productos a este tipo de ubicación si desea que no se tenga a consulta a los mismos desde el flujo de productos normal. **Nota**: A diferencia de resto de tipos de ubicación, el de **QC** no tiene seleccionada de forma predeterminada ninguna de las casillas de verificación de manejo de artículos. Esto indica que el contenido que sitúe en una ubicación de control de calidad no se incluye de los flujos del artículo.|  

En todos los tipos de ubicación, excepto los tipos PICKING, COLOCARPICKING y UBICAR, no se permite ninguna otra actividad aparte de la definida por su tipo de ubicación. Por ejemplo, una ubicación de tipo **Recepción** solo se puede utilizar para recibir en ella productos o para seleccionar productos de ella.  

> [!NOTE]  
> Solo se puede realizar el movimiento a las ubicaciones de tipo RECEPC y QC. Del mismo modo, solo se pueden realizar movimientos desde ubicaciones del tipo ENV y QC.  

## <a name="bin-ranking"></a>Ranking ubicación

En la gestión avanzada del almacén se puede automatizar y optimizar cómo se recogen los productos en hojas de trabajo de colocación y selección clasificando las ubicaciones de modo que se proponga la extracción y colocación de productos según criterios de clasificación para utilizar el espacio de almacén óptimamente.  

Los procesos de ubicación se optimizan según el ranking de ubicación mediante la sugerencia de ubicaciones de ranking superior con respecto a las de ranking inferior. Del mismo modo, los procesos de picking se optimizan mediante la sugerencia en primer lugar de los productos de la ubicación con ranking alto. Además, se sugieren reposiciones de ubicación desde las ubicaciones de rango inferior a ubicaciones de rango superior.  

La clasificación de ubicación junto con la información del contenido de la ubicación son las propiedades básicas que permiten a los usuarios incluir productos en el almacén.  

## <a name="bin-setup"></a>Configuración de ubicación
En almacenes avanzados, las ubicaciones se pueden configurar con valores de capacidad, como cantidad, cubicaje total y peso, para controlar qué productos se almacenan en la ubicación y cómo.  

En cada ficha de producto, puede asignar una unidad de medida (UM) para el producto, como piezas, palés, litros, gramos o cajas. También puede tener una unidad de medida base para un producto y especificar unidades de medida mayores que se basen en ella. Por ejemplo, puede definir un palé para que sea igual a 16 unidades, siendo estas la unidad de medida base.  

Si desea establecer una cantidad máxima de un producto específico para almacenarlo en una ubicación individual y el producto tiene más de una unidad de medida, deberá definir la cantidad máxima para cada unidad de medida que exista en la ficha del producto. Por consiguiente, si un producto se ha configurado para gestionarse en unidades y palés, el campo **Cdad. máxima** de la página **Contenido ubicación** para ese producto deberá estar igualmente en unidades y palés. De lo contrario, la cantidad permitida para esa ubicación no se calculará correctamente.  

Antes de establecer restricciones de capacidad para contenidos de ubicación en una ubicación, primero deberá asegurarse de que la unidad de medida y las dimensiones del producto se hayan definido en la ficha del producto.  

> [!NOTE]  
> Solo es posible funcionar con varias unidades de medida en instalaciones SGA. En el resto de las configuraciones, los contenidos de ubicación solo pueden ir en la unidad de medida base. En todas las transacciones con un unidad de medida mayor que la unidad de medida base del producto, la cantidad se convierte a la unidad de medida base.  

## <a name="zone"></a>Zona

En la gestión avanzada del almacén, las ubicaciones se pueden agrupar en las zonas para controlar el direccionamiento del flujo de trabajo de las actividades de almacén.  

Una zona podría ser una zona de recepción o una zona de almacenamiento, y cada zona puede componerse de una o varias ubicaciones.  

La mayoría de las propiedades asignadas a una zona se asignarán de forma predeterminada a la ubicación que se cree para dicha zona.  

## <a name="class"></a>Clase
En la gestión avanzada del almacén se pueden asignar códigos de clase de almacén a productos, ubicaciones y zonas para controlar dónde se almacenan las distintas clases de producto, por ejemplo los productos congelados. Puede dividir una zona en varias clases de almacén. Por ejemplo, los productos en la zona de recepción se pueden almacenar como congelados, peligrosos u otra clase.  

Cuando trabaja con clases de almacén y una ubicación de recepción o envío predeterminada, debe rellenar manualmente las ubicaciones apropiadas en la recepción y en las líneas de albarán de almacén.  

En los flujos entrantes, el código de clase está resaltado con líneas de entrada cuando el código de clase del producto no coincide con la ubicación predeterminada de recepción. Si no se han asignado las ubicaciones predeterminadas correctas, la cantidad no puede recibirse.  

## <a name="location"></a>Almacén

Un almacén es una estructura física o un lugar donde se recibe, se almacena y se envía el inventario, potencialmente organizado en ubicaciones. Una ubicación puede ser un almacén, un vehículo de servicio, una sala de exposición, una planta o un área dentro de una planta.  

## <a name="first-expired-first-out"></a>Primero en caducar primero en salir

Si selecciona la casilla **Picking según FEFO (Primero en caducar, primero en salir)** en la ficha desplegable **Directivas ubicación** de la ficha de almacén, los productos con seguimiento se seleccionan según su fecha de vencimiento. Primero se realiza el picking de los productos con las fechas de vencimiento más tempranas.  

Las actividades de almacén en todos los documentos de picking y de movimientos se ordenan según FEFO, a menos que los productos en cuestión ya tengan asignados números de serie o de lote. Si solo una parte de la cantidad en la línea tiene ya asignados números de lote o de serie, la cantidad restante que seleccionar se ordena según el método FIFO.  

Cuando se realiza la selección por FEFO, el programa recopila los productos disponibles que caducan en primer lugar y el resultado es una lista temporal de seguimiento de productos basada en la fecha de vencimiento. Si dos productos tienen la misma fecha de caducidad, se selecciona primero aquel cuyo número de lote o de serie sea menor. Si los números de lote o de serie son iguales, entonces se selecciona primero el producto que se registró en primer lugar. Los criterios estándar para seleccionar productos en ubicaciones de selección, como Ranking ubicación y División bulto, se aplican a esta lista temporal de seguimiento de productos FEFO.  

## <a name="put-away-template"></a>Plantilla ubicar

La plantilla de ubicación se puede asignar a un producto y a una ubicación. La plantilla de ubicación especifica un conjunto de reglas con prioridad que se deben respetar al crear ubicaciones. Por ejemplo, una plantilla de ubicación puede requerir que el producto se coloque en una ubicación con contenido de ubicación que coincida con la unidad de medida y, si no se encuentra una ubicación similar con capacidad suficiente, el producto debe colocarse en una ubicación vacía.  

## <a name="see-also"></a>Consulte también

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Detalles de diseño: disponibilidad en el almacén](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
