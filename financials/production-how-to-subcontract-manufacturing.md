---
title: "Cómo subcontratadas fabricación | Documentos de Microsoft"
description: "Cuando el pedido de compra se haya creado en la hoja de subcontratación, se puede registrar."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2796da1b41569c8c950dc844fc31eaf4f0179efa
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="subcontract-manufacturing"></a>Subcontratación de fabricación
La subcontratación de operaciones seleccionadas al proveedor es común de muchas empresas de fabricación. La subcontratación puede ser esporádica o puede formar parte integrante de todos los procesos de producción.

El programa ofrece varias herramientas para gestionar el trabajo subcontratado:  

- Centros de trabajo con proveedor asignado: esta característica le permite configurar un centro de trabajo asociado a un proveedor (subcontratista). Se denomina centro de trabajo subcontratado. Puede especificar un centro de trabajo subcontratado en una operación de ruta, con lo que le resultará muy sencillo procesar la actividad subcontratada. Además, el coste de la operación se puede indicar en el nivel de la ruta o del centro de trabajo.  
- Coste del centro de trabajo basado en unidades o tiempo: esta característica le permite especificar si los costes asociados al centro de trabajo se basan en el tiempo de producción o en una tarifa plana por unidad. Si bien los subcontratistas suelen usar una tarifa plana por unidad en sus servicios, el programa puede manejar las dos opciones (tiempo de producción y tarifa plana por unidad).  
- Hoja de subcontratación: esta característica le permite buscar las órdenes de producción cuyo material esté listo para el envío a un subcontratista y para crear automáticamente pedidos de compra para las operaciones subcontratadas a partir de rutas de órdenes de producción. A continuación, el programa registra automáticamente los cargos del pedido de compra en la orden de producción al proceder al registro del pedido de compra. En las hojas de subcontratación sólo se pueden ver y utilizar las órdenes de producción que tengan el estado de lanzadas.  

## <a name="subcontract-work-centers"></a>Subcontratar centros de trabajo  
Los centros de trabajo subcontratados se configuran igual que los centros de trabajo normales que tienen información adicional. Se asignan a rutas de la misma forma que los demás centros de trabajo.  

### <a name="subcontract-work-center-fields"></a>Subcontratar campos de centros de trabajo  
El campo **Nº subcontratista** indica que el centro de trabajo es un centro de trabajo subcontratado. Puede escribir el número de un subcontratista que suministra el centro de trabajo. Este campo se puede usar para administrar los centros de trabajo que no están dentro de la empresa, sino que realizan procesos por contrato.  

Si subcontrata al proveedor a una tarifa distinta para cada proceso, puede seleccionar el campo **Coste unitario específico**. De esta forma, puede configurar un coste en cada línea de la ruta y no tener que volver a introducir la información en cada pedido de compra. El coste de la línea de ruta se usa en el procesamiento en lugar del coste de los campos de coste del centro de trabajo. Si activa el campo **Coste unitario específico**, el programa puede calcular los costes del proveedor por operación de ruta.  

Si subcontrata a cada proveedor a una única tarifa, deje en blanco el campo **Coste unitario específico**. Los costes se configurarán rellenando los campos **Coste unit. directo**, **% Coste indirecto** y **Tasa costes generales**.  

### <a name="routings-that-use-subcontract-work-centers"></a>Rutas que usan centros de trabajo subcontratados  
Los centros de trabajo subcontratados se pueden usar para las operaciones de las rutas de la misma forma que los centros de trabajo normales.  

Puede configurar una ruta que use un centro de trabajo externo como paso operativo estándar. Si lo prefiere, puede modificar la ruta de una orden de producción concreta para que incluya una operación externa. Ello podría ser necesario en una situación de urgencia, por ejemplo en el caso de que una máquina no funcione correctamente, o durante una temporada de mayor demanda, en que el trabajo que normalmente se realiza en la empresa se tiene que enviar a un subcontratista.  

Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).  

## <a name="subcontracting-worksheet"></a>Hoja subcontratación  
Una vez que ha calculado la hoja de subcontratación, se crea el documento correspondiente, en este caso un pedido de compra.  

# <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Calcular las hojas de cálculo de la subcontratación y cree los pedidos de compra de subcontratación
Las funciones de ventana de **Hoja subcontratación** como **Hoja planificación** calculando el suministro necesario, en este caso los pedidos de compra, que se revisa en la hoja de cálculo y después crea con la función de **Ejecutar mensajes acción**.  

> [!NOTE]  
>  En las hojas de subcontratación, sólo se pueden ver y utilizar las órdenes de producción que tengan el estado de **Lanzadas**.  

### <a name="to-calculate-the-subcontracting-worksheet"></a>Para calcular la hoja de subcontratación  
1.  Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja de subcontratación** y, a continuación, seleccione el vínculo relacionado.  
2.  Para calcular la hoja, seleccione la acción **Calcular subcontratos**.  
3.  En la ventana de **Calcular subcontratos**, defina filtros para operaciones subcontratadas, o los centros de trabajo donde se realizan, para calcular solo las órdenes de producción correspondientes.  
4.  Elija el botón **Aceptar**.  

    Revise las líneas en la ventana de **Hoja subcontratación**. La información de esta hoja de cálculo proviene de la orden de producción y de las líneas de ruta y flujos de la orden de producción del pedido de compra cuando se crea el documento. Puede eliminar una fila de la hoja de cálculo sin asignar a la información original, tal como puede hacer con las otras hojas de cálculo. La información reaparecerá la siguiente vez que ejecute la función de **Calcular subcontratos**.  

### <a name="to-create-the-subcontract-purchase-order"></a>Para generar el pedido de compra subcontratado  
1.  Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja de subcontratación** y, a continuación, seleccione el vínculo relacionado.  
2.  En la pestaña **Acciones**, en el grupo **Procesar**, elija **Ejecutar mensajes acción**.  
3.  Seleccione el campo **Imprimir pedidos** para imprimir el pedido de compra al crearlo.  
4.  Elija el botón **Aceptar**.  

Si todas las operaciones subcontratadas se van a enviar a un solo proveedor, se crea un solo pedido de compra.  

La línea de la hoja de trabajo que se convirtió en pedido de compra se elimina de la hoja. Una vez que se crea un pedido de compra, no volverá a aparecer en la hoja de cálculo.  

## <a name="posting-subcontract-purchase-orders"></a>Registrar pedidos de compra de subcontratación  
Una vez que se han creado los pedidos de compra del subcontratista, se pueden registrar. La recepción del pedido registra un movimiento de capacidad en la orden de producción y la facturación del pedido registra el coste directo del pedido de compra en la orden de producción.  

Cuando la compra se registra como recibida, se registra automáticamente un movimiento de diario de salida para la orden de producción. Esto se aplica solo si la operación de subcontratación es la última operación en la ruta de la orden de producción.  

> [!CAUTION]  
>  Es posible que no desee realizar el registro de salida automático para una orden de producción en curso cuando se reciben productos subcontratados. Los motivos de esto podrían ser que la cantidad de salida esperada que se registra puede ser diferente de la cantidad real y que la fecha de registro de la salida automática es engañosa.  
>   
>  Para evitar que se registra la salida esperada de una orden de producción cuando se reciban compras de subcontratados, asegúrese de que la operación subcontratada no sea la última. También, inserte una nueva última operación para la cantidad de salida final.

## <a name="to-post-a-subcontract-purchase-order"></a>Para registrar un pedido de compra de subcontratación  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de compra** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra un pedido de compra creado en la hoja de subcontratación.  

    En las líneas del pedido de compra, puede ver la misma información que estaba en la hoja de cálculo. Los campos **Nº orden producción**, **Nº lín. orden producc.**, **Nº operación** y **Nº centro trabajo** se rellenan con la información del pedido de producción de origen.  

3.  Seleccione la acción **Registrar**.  

Cuando la compra se registra como recibida, se registra automáticamente un movimiento de diario de salida para la orden de producción. Esto se aplica solo si la operación de subcontratación es la última operación en la ruta de la orden de producción.  

> [!CAUTION]  
>  Es posible que no desee realizar el registro de salida automático para una orden de producción en curso cuando se reciben productos subcontratados. Los motivos de esto podrían ser que la cantidad de salida esperada que se registra puede ser diferente de la cantidad real y que la fecha de registro de la salida automática es engañosa.  
>   
>  Para evitar que se registra la salida esperada de una orden de producción cuando se reciban compras de subcontratados, asegúrese de que la operación subcontratada no sea la última. También, inserte una nueva última operación para la cantidad de salida final.  

Cuando se registra el pedido de compra como facturado, el coste directo de dicho pedido se registra en producción  

## <a name="see-also"></a>Consulte también  
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

