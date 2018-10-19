---
title: Procesar transacciones IC entrantes y salientes | Documentos de Microsoft
description: "Las transacciones entre empresas vinculadas que recibe de los socios IC se muestran en la bandeja de entrada IC donde se procesan manual o automáticamente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 19a426c4fc163e66c85f2ec3df19a9619d38106e
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas
Todas las transacciones de empresas vinculadas que se reciben electrónicamente aparecen en la bandeja de entrada de empresas vinculadas.  

## <a name="organizing-the-inbox"></a>Organizar la bandeja de entrada  
 Para determinar qué transacciones se mostrarán en la bandeja de entrada, puede utilizar los campos de filtro de la parte superior de la ventana. Por ejemplo, si únicamente desea ver transacciones creadas por una empresa asociada determinada, puede definir los filtros **Origen de la transacción** y **Código socio empresa vinculada**.  

### <a name="transaction-source"></a>Origen de la transacción  
Las acciones que se pueden realizar con una transacción dependen de:  

- Si la empresa vinculada asociada la creó  
- Si la empresa vinculada asociada la rechazó y se la devolvió  

Puede utilizar el campo **Mostrar origen de transacción** para filtrar la ventana **Trans. band. ent. empresa vinculada** de modo que sólo se muestre uno de estos tipos de transacciones. (También puede filtrar por socio empresa vinculada o por los contenidos del campo **Acción de línea**.)  

#### <a name="created-by-intercompany-partner"></a>Si el socio de la empresa vinculada la creó  
 Si recibe una nueva transacción creada por su socio, puede elegir entre:

- Aceptar la transacción  
- Rechazar la transacción (devolvérsela al socio)  
- Cancelar la transacción (eliminarla pero sin devolvérsela al socio)  

#### <a name="returned-from-intercompany-partner"></a>Si el socio de la empresa vinculada devolvió la transacción  
 Si el socio de la empresa vinculada rechaza la transacción, la única opción es cancelar ésta en la bandeja de entrada. Después, deberá crear líneas de corrección o revertir el diario o el documento en su empresa.  

## <a name="re-creating-inbox-entries"></a>Volver a crear movimientos en la bandeja de entrada  
 Si ha aceptado una transacción en la bandeja de entrada pero ha eliminado el documento o el diario en lugar de registrarlo, puede volver a crear el movimiento en la bandeja de entrada y aceptarlo de nuevo.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Panorama de transacciones de empresas vinculadas durante un periodo  
 Puede obtener una descripción general de todas las transacciones de empresas vinculadas que ha enviado y recibido en el periodo. Las listas de informe de **Transacciones de empresa vinculada** enumera todos los movimientos de empresas vinculadas, movimientos de cliente y movimientos de proveedor de contabilidad.

 > [!NOTE]  
 > Si los socios de empresas vinculadas se encuentran en la misma base de datos, las transacciones se transfieren sin necesidad de un archivo o correo electrónico. Consulte el campo **Tipo transferencia** de la ventana **Socio empresa vinculada**. <br /><br />
En ese caso, puede configurar el sistema para que evite las bandeja de entrada y de salida seleccionando la opción **Aceptar auto. transacciones** en la ventana **Socio empresa vinculada** y en la ventana **Enviar auto. transacciones** en la ventana **Config. empr. vincul.**, respectivamente.

## <a name="to-import-intercompany-transactions-from-a-file"></a>Importar transacciones entre empresas vinculadas desde un archivo  
Si tiene alguna empresa vinculada asociada que no está incluida en la misma base de datos que su empresa, puede recibir transacciones entre empresas vinculadas de ese socio en un archivo .xml. Después, deberá importar las transacciones en su bandeja de entrada.  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.
2. Guarde el archivo en la ubicación que especificó en el campo **Detalles buzón empresa vinculada** en la ventana **Información empresa**.  
3. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transacciones de bandeja de entrada entre empresas vinculadas** y luego elija el enlace relacionado.
4. En la ventana **Transacciones de bandeja de entrada entre empresas vinculadas**, seleccione la acción **Importar archivo transacción**.  
5. En la ventana que aparece, seleccione el archivo .xml que contiene las transacciones y seleccione el botón **Abrir**.  

Las transacciones se importan en la bandeja de entrada y quedan listas para ser procesadas.

## <a name="to-process-incoming-intercompany-transactions"></a>Procesar transacciones entrantes entre empresas vinculadas  
Cuando sus socios le envían transacciones entre empresas vinculadas, estas transacciones van a parar a su bandeja de entrada de empresas vinculadas. Debe evaluar cada transacción en la bandeja de entrada y emprender las acciones que estime convenientes.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transacciones de bandeja de entrada entre empresas vinculadas** y luego elija el enlace relacionado.  
2. En la ventana **Transacciones de bandeja de entrada entre empresas vinculadas**, seleccione una línea y, a continuación, elija una acción, como **Aceptar**, para procesar la línea.
3. En la ventana **Completa acc. band. entrada IC**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija el botón **Aceptar**.  

Para las líneas procesadas con la acción **Aceptar**, se crearán líneas de diario o documentos en su empresa. Abra cada documento o diario, haga los cambios necesarios y regístrelos.  

Las líneas que procesó con la acción **Devolvérsela al socio** se moverán a la bandeja de salida desde donde se pueden enviar a su socio.

Para las líneas que procesó con la acción **Devolvérsela al socio**, debe registrar una corrección de la transacción original registrada en su empresa.

## <a name="to-process-outgoing-intercompany-transactions"></a>Procesar transacciones salientes entre empresas vinculadas  
Al registrar un diario o un documento de empresas vinculadas, o al enviar una confirmación de pedido de empresas vinculadas, las transacciones se envían a su bandeja de salida de empresas vinculadas. Para que se envíen a las empresas asociadas, debe abrir la bandeja de salida y procesarlas.  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transacciones de bandeja de salida entre empresas vinculadas** y luego elija el enlace relacionado.  
2. En la ventana **Transacciones de bandeja de salida entre empresas vinculadas**, seleccione una línea y, a continuación, elija una acción, como **Devolver a bandeja de entrada**, para procesar la línea.

Las líneas que procesó con la acción **Enviar a socio de empresa vinculada** se enviarán a la bandeja de entrada del socio correspondiente.

Las líneas que procesó con la acción **Devolver a bandeja de entrada** se moverán a la bandeja de entrada donde podrá aceptarlas para crear documentos o líneas de diario en su empresa.  

Para las líneas que procesó con la acción **Cancelar**, debe registrar una corrección de la transacción original registrada en su empresa.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Para volver a crear transacciones entre empresas vinculadas en la bandeja de entrada  
De vez en cuando, es posible que desee volver a crear una transacción en la bandeja de entrada o bandeja de salida. Por ejemplo, si ha aceptado una transacción en la bandeja de entrada pero ha eliminado el documento o el diario en lugar de registrarlo, puede volver a crear el movimiento en la bandeja de entrada y aceptarlo de nuevo.  

Este siguiente procedimiento describe el método para volver a crear transacciones en la bandeja de entrada, pero para la bandeja de salida el procedimiento es el mismo.

  1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transacciones bandeja entrada IC procesadas** y luego elija el enlace relacionado.  

  2.  En la ventana **Transacciones bandeja entrada IC procesadas**, seleccione la línea que contiene la transacción que desea volver a crear en la bandeja de entrada y elija la acción **Volver a crear transacción en bandeja de entrada**.  

## <a name="see-also"></a>Consulte también
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

