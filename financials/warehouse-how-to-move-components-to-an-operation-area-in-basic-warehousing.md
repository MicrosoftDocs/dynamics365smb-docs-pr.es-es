---
title: "Procedimiento: mueva componentes a un área de operaciones en configuraciones básicas de almacén | Documentos de Microsoft"
description: "Si el artículo que procesa las operaciones tiene lugar en su ubicación de almacén, puede tener que mover los artículos entre las ubicaciones internas para responder a los documentos de origen interno, como producción, ensamblado o pedidos de servicio en la ubicación."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 146e113931384e8bc9ba01d5ae7ddb626d18050f
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Procedimiento: mueva componentes a un área de operaciones en configuraciones básicas de almacén
Si el artículo que procesa las operaciones tiene lugar en su ubicación de almacén, puede tener que mover los artículos entre las ubicaciones internas para responder a los documentos de origen interno, como producción, ensamblado o pedidos de servicio en la ubicación.  

> [!NOTE]  
>  Para obtener información acerca de los artículos entre las ubicaciones sin documentos de origen, consulte Movimiento interno.  

En configuraciones avanzadas de almacén, que son los almacenes que utilizan el campo de instalación **Ubicac. y pick. directo**, puede utilizar la ventana **Hoja trabajo movimiento** para mover los artículos entre las ubicaciones. Para obtener más información, vea [Mover productos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md).  

En configuraciones de almacén básico, es decir en ubicaciones que utilizan el campo de instalación **Ubicac. obligatoria** y posiblemente los campos de configuración **Picking requerido**, puede registrar los movimientos de los artículos para áreas de operación internas basándose en documentos de origen de las siguientes formas:  

-   Con la ventana **Movimiento inventario**.  
-   Con la ventana **Picking existencias**.  

> [!NOTE]  
>  Los picking de inventario también registran los movimientos de producto negativos como consumo y sólo se utilizan para los componentes de producción. Para obtener más información, consulte la ventana Picking inventario.  

Para obtener información detallada acerca de los movimientos de inventario, consulte la ventana Movimiento inventario.  

Dos diferentes funciones pueden crear el movimiento de inventario inicial. Un trabajador de ensamblado, por ejemplo, puede crearlo desde un pedido de ensamblado lanzado de modo que aparezca en la lista del trabajador de almacén de trabajo para crear. Para crear un movimiento de inventario para las líneas del pedido de ensamblado que están preparadas para mover los componentes a sus ubicaciones especificadas, el trabajador del ensamblado utiliza la función **Crear movimiento de inventario**.  

Alternativamente, un trabajador de almacén puede crearla apuntando al pedido de ensamblado lanzado en cuestión. Esto se describe en el procedimiento siguiente:  

> [!NOTE]  
>  Si el movimiento es para un pedido de ensamblado donde el artículo se ensambla para un pedido de venta, puede definir que el documento de movimiento de inventario esté creado automáticamente cuando se cree el documento del picking de existencias que toma el artículo de montaje final y registra el envío. Para configurarlo, seleccione el campo **Crear movimientos automáticamente** en la ventana **Conf. ensamblado**  
>   
>  Para obtener más información acerca de los pedidos de endamblaje y configuraciones básicas de almacén, vea la sección “Gestionar productos de ensamblar para pedido con picking de existencias” en [Procedimiento: Selección de producción o ensamblaje](warehouse-how-to-pick-for-production.md).  

Este procedimiento muestra cómo crear un movimiento de inventario de la ventana **Movimiento inventario** haciendo referencia un pedido de ensamblado lanzado como documento de origen. El procedimiento es el mismo cuando se mueven los componentes para las órdenes de producción y los pedidos de servicio.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Para mover componentes a un área de operaciones en configuraciones básicas de almacén  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Movimiento inventario** y, a continuación, seleccione el vínculo correspondiente.  
2.  En la ficha desplegable **General**, rellene el campo **Nº** . Puede pulsar la tecla Entrar para seleccionar entre las series numéricas.  
3.  En el campo **Cód. almacén**, escriba la ubicación donde tiene lugar el movimiento.  
4.  Seleccione la acción **Traer doc. origen**. Alternativamente, rellene el campo **Documento origen** y, a continuación, elija el botón **AssistEdit** en el campo **Cód. procedencia mov.**  
5.  En la ventana **Documentos origen**, seleccione el pedido de ensamblado al que desea mover los componentes y, a continuación seleccione el botón **Aceptar**.  

    Para cada componente necesario que se pueda mover, se generan una línea Toma y una línea Plaza en la ventana **Movimientos de inventario**. Todos los campos excepto **Cdad. a manipular** se prellenan según las líneas del documento de origen. El campo **Cdad. a manipular** se establece en cero hasta que se introduzca la cantidad que realmente ha movido.  

    Puede modificar el código de ubicación en una línea de Toma pero sólo según la disponibilidad. Si elige el botón **AssistEdit** en el campo **Cód. ubicación** en una línea Toma, se abre la ventana **Contenidos ubicación** y sólo muestra ubicaciones donde está disponible el componente.  

    No puede modificar el código de ubicación en una línea Plaza. Sólo se valida el código de ubicación que se define en la línea de componente del documento de origen. Esto soporta el principio de que la función que solicita un componente, que es un trabajador de ensamblado en este procedimiento, sabe dónde debe situarse el componente. Si desea situar los componentes en otra ubicación, primero deberá modificar el código de ubicación en la línea de componente y después volver a crear las líneas del movimiento de inventario.  
6.  En el campo **Cdad. a manipular**, introduzca la cantidad completa o parcial cantidad que ha movido realmente. El valor de Toma y las líneas de Plaza deben iguales. Si no, no podrá registrar el movimiento.  

    > [!NOTE]  
    >  Como en otras actividades de almacén, puede dividir la línea del apartado seleccionando **Acciones** y **Dividir línea**. En ese caso, la suma de las dos líneas divididas de Plaza debe ser igual a la cantidad en la línea de Toma.  

7.  Cuando vaya para registrar los movimientos realizados, seleccione la acción **Registro Invent. movimiento**.  

    Los movimientos de almacén se crean reflejando que los componentes ahora existen en las ubicaciones especificadas en las líneas del pedido de ensamblado.  

    > [!NOTE]  
    >  A diferencia de cuando se mueven los componentes con un picking de inventario, el consumo no se registra cuando se registra un movimiento de inventario. Ese el paso puede realizarse por separado registrando la salida y el consumo del pedido de ensamblado. Para obtener más información, consulte Pedido de ensamblado.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

