---
title: Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas
description: 'Las transacciones entre empresas vinculadas que recibe de los socios se muestran en la bandeja de entrada de empresas vinculadas, donde se procesan manual o automáticamente.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a><a name="manage-the-intercompany-inbox-and-outbox"></a><a name="manage-the-intercompany-inbox-and-outbox"></a>Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas

Las transacciones de empresas vinculadas que se reciben de los socios aparecen en la página **Bandeja de entrada de empresas vinculadas**. Para obtener información sobre cómo procesar transacciones entrantes entre empresas, vaya a [Procesar transacciones entrantes entre empresas](#process-incoming-intercompany-transactions). Las transacciones de empresas vinculadas que envía a los socios aparecen en la página **Bandeja de salida de empresas vinculadas**. Para obtener información sobre cómo procesar transacciones salientes entre empresas, vaya a [Procesar transacciones salientes entre empresas](#to-process-outgoing-intercompany-transactions).

Sin embargo, dependiendo de su configuración de empresas vinculadas, algunas transacciones se manejan automáticamente. Puede configurar la empresa de origen y las empresas asociadas para crear automáticamente documentos y diarios que correspondan a las transacciones que los socios contabilizan a través del diario general de empresas vinculadas. Para obtener información sobre el uso de diarios de empresas vinculadas, vaya a [Rellenar y publicar un diario de empresas vinculadas](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox"></a><a name="organizing-the-inbox"></a><a name="organizing-the-inbox"></a>Organizar la bandeja de entrada

Para determinar qué transacciones se mostrarán en la parte superior de la página Bandeja de entrada, puede utilizar los campos de filtro. Por ejemplo, si únicamente desea explorar creadas por un socio determinado, use los filtros **Origen de la transacción** y **Código de socio de empresas vinculadas**.  

### <a name="transaction-source"></a><a name="transaction-source"></a><a name="transaction-source"></a>Origen de la transacción

Las acciones que se pueden realizar con una transacción dependen de:  

* Si la empresa vinculada asociada la creó  
* Si la empresa vinculada asociada la rechazó y se la devolvió  

Use el campo **Mostrar origen de transacción** para filtrar la página **Transacciones de bandeja de entrada de empresa vinculada**, de modo que sólo se muestre uno de estos tipos de transacciones. También puede filtrar por socio de empresas vinculadas o por los contenidos del campo **Acción de línea**.  

#### <a name="created-by-intercompany-partner"></a><a name="created-by-intercompany-partner"></a><a name="created-by-intercompany-partner"></a>Creado por socio de empresas vinculadas

 Si recibe una nueva transacción creada por su socio, puede elegir entre:

* Aceptar la transacción  
* Rechazar la transacción (devolvérsela al socio)  
* Cancelar la transacción (eliminarla pero sin devolvérsela al socio)  

#### <a name="returned-from-intercompany-partner"></a><a name="returned-from-intercompany-partner"></a><a name="returned-from-intercompany-partner"></a>Devuelto por socio de empresas vinculadas

Si el socio de empresas vinculadas rechaza una transacción, debe cancelar ésta en la bandeja de entrada y luego crear líneas de corrección o revertir el diario o el documento.  

## <a name="recreating-inbox-entries"></a><a name="recreating-inbox-entries"></a><a name="recreating-inbox-entries"></a>Volver a crear movimientos en la bandeja de entrada

Si ha aceptado una transacción en la bandeja de entrada pero ha eliminado el documento o el diario en lugar de registrarlo, puede volver a crear el movimiento en la bandeja de entrada y aceptarlo de nuevo.  

## <a name="get-an-overview-of-intercompany-transactions-for-a-period"></a><a name="get-an-overview-of-intercompany-transactions-for-a-period"></a><a name="get-an-overview-of-intercompany-transactions-for-a-period"></a>Obtener un panorama de transacciones de empresas vinculadas durante un periodo

Puede obtener una descripción general de todas las transacciones de empresas vinculadas que ha enviado y recibido en el periodo. Las listas de informe de **Transacciones de empresa vinculada** enumera todos los movimientos de empresas vinculadas, movimientos de cliente y movimientos de proveedor de contabilidad.

> [!NOTE]  
> Si los socios de empresas vinculadas están en la misma base de datos, los socios pueden aceptar transacciones automáticamente. Vaya directamente a las páginas **Transacciones de bandeja de entrada entre empresas gestionadas** y **Transacciones de bandeja de salida entre empresas gestionadas**. Para obtener más información sobre la aceptación automática de transacciones, vaya a [Aceptación automática de transacciones de socios de empresas vinculadas](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Para el socio de sincronización, en la página **Configuración de empresas vinculadas** , active la opción **Enviar automáticamente transacciones** .
> * Para empresas de socios, en la página **Socio de empresas vinculadas** , active la opción **Aceptar automáticamente transacciones** .  

## <a name="import-intercompany-transactions-from-a-file"></a><a name="import-intercompany-transactions-from-a-file"></a><a name="import-intercompany-transactions-from-a-file"></a>Importar transacciones entre empresas vinculadas desde un archivo

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Si tiene alguna empresa vinculada asociada que no está incluida en la misma base de datos que su empresa, puede recibir transacciones entre empresas vinculadas de ese socio en un archivo .xml. Después, deberá importar las transacciones en su bandeja de entrada.  

1. Guarde el archivo en la ubicación que especificó en el campo **Detalles de bandeja de entrada de las empresas vinculadas** cuando configure empresas vinculadas.  
2. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones de bandeja de entrada entre empresas vinculadas** y luego elija el enlace relacionado.
3. En la página **Transacciones de bandeja de entrada entre empresas vinculadas**, seleccione la acción **Importar archivo transacción**.  
4. En la página que aparece, seleccione el archivo .xml que contiene las transacciones y seleccione el botón **Abrir**.  

Las transacciones se importan en la bandeja de entrada y quedan listas para ser procesadas.

## <a name="process-incoming-intercompany-transactions"></a><a name="process-incoming-intercompany-transactions"></a><a name="process-incoming-intercompany-transactions"></a>Procesar transacciones entrantes entre empresas vinculadas

Cuando sus socios le envían transacciones entre empresas vinculadas, estas transacciones van a parar a su bandeja de entrada de empresas vinculadas. Debe evaluar cada transacción en la bandeja de entrada y emprender las acciones que estime convenientes.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones de bandeja de entrada entre empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Transacciones de bandeja de entrada entre empresas vinculadas**, seleccione una línea y, a continuación, elija una acción, como **Aceptar**, para procesar la línea.
3. En la página **Completa acc. band. entrada IC**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija el botón **Aceptar**.  

Para las líneas que acepte, se crearán líneas de diario o documentos en su empresa. Abra cada documento o diario, haga los cambios necesarios y regístrelos.  

Las líneas que rechaza y devuelve a su socio van a su bandeja de salida de empresas vinculadas, donde puede enviárselas a su socio.

Para las líneas que un socio rechazó y se las devolvió, debe registrar una corrección de la transacción original registrada en su empresa.

## <a name="to-process-outgoing-intercompany-transactions"></a><a name="to-process-outgoing-intercompany-transactions"></a><a name="to-process-outgoing-intercompany-transactions"></a>Procesar transacciones salientes entre empresas vinculadas

Al registrar un diario o un documento de empresas vinculadas, o al enviar una confirmación de pedido de empresas vinculadas, las transacciones se envían a su bandeja de salida de empresas vinculadas. Para enviarlas a los socios de empresas vinculadas, debe abrir la bandeja de salida y procesarlas.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones de bandeja de salida entre empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Transacciones de bandeja de salida entre empresas vinculadas**, seleccione una línea y, a continuación, elija una acción, como **Devolver a bandeja de entrada**, para procesar la línea.

Use la acción **Enviar a socio de empresas vinculadas** para enviar líneas a la bandeja de entrada del socio correspondiente.

Use la acción **Devolver a bandeja de entrada** para mover líneas a la bandeja de entrada, donde podrá aceptarlas para crear documentos o líneas de diario en su empresa.  

Si usa la acción **Cancelar**, debe registrar una corrección de la transacción original registrada originalmente en su empresa.  

## <a name="recreate-intercompany-inbox-transactions"></a><a name="recreate-intercompany-inbox-transactions"></a><a name="recreate-intercompany-inbox-transactions"></a>Volver a crear transacciones entre empresas vinculadas en la bandeja de entrada

Es posible que desee volver a crear una transacción en la bandeja de entrada o la bandeja de salida. Por ejemplo, si ha aceptado una transacción en la bandeja de entrada pero ha eliminado el documento o el diario en lugar de registrarlo, puede volver a crear el movimiento en la bandeja de entrada y aceptarlo de nuevo.  

Este siguiente procedimiento describe el método para volver a crear transacciones en la bandeja de entrada, pero para la bandeja de salida el procedimiento es el mismo.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones bandeja entrada IC procesadas** y luego elija el enlace de salida.  
2. En la página **Transacciones bandeja entrada IC procesadas**, seleccione la línea que contiene la transacción que desea volver a crear en la bandeja de entrada y elija la acción **Volver a crear transacción en bandeja de entrada**.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
