---
title: Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas
description: Las transacciones entre empresas vinculadas que recibe de los socios IC se muestran en la bandeja de entrada IC donde se procesan manual o automáticamente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.date: 03/09/2022
ms.author: edupont
---
# Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas
Todas las transacciones de empresas vinculadas que se reciben electrónicamente aparecen en la bandeja de entrada de empresas vinculadas.  

Sin embargo, dependiendo de cómo se configuren las empresas vinculadas para su empresa, algunas transacciones se replican automáticamente a los socios de empresas vinculadas pertinentes. A partir del primer lanzamiento de versiones de 2022, puede configurar la empresa para la creación automática de transacciones recibidas entre empresas vinculadas de socios de empresas vinculadas, registradas a través del diario general entre empresas vinculadas. Para obtener más información, consulte [Para rellenar y registrar un diario de empresas vinculadas](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal).  

## Organizar la bandeja de entrada  
 Para determinar qué transacciones se mostrarán en la página de bandeja de entrada, puede utilizar los campos de filtro de la parte superior de la página. Por ejemplo, si únicamente desea ver transacciones creadas por una empresa asociada determinada, puede definir los filtros **Origen de la transacción** y **Código socio empresa vinculada**.  

### Origen de la transacción  
Las acciones que se pueden realizar con una transacción dependen de:  

- Si la empresa vinculada asociada la creó  
- Si la empresa vinculada asociada la rechazó y se la devolvió  

Puede utilizar el campo **Mostrar origen de transacción** para filtrar la página **Trans. band. ent. empresa vinculada** de modo que sólo se muestre uno de estos tipos de transacciones. (También puede filtrar por socio empresa vinculada o por los contenidos del campo **Acción de línea**.)  

#### Si el socio de la empresa vinculada la creó  
 Si recibe una nueva transacción creada por su socio, puede elegir entre:

- Aceptar la transacción  
- Rechazar la transacción (devolvérsela al socio)  
- Cancelar la transacción (eliminarla pero sin devolvérsela al socio)  

#### Si el socio de la empresa vinculada devolvió la transacción  
 Si el socio de la empresa vinculada rechaza la transacción, la única opción es cancelar ésta en la bandeja de entrada. Después, deberá crear líneas de corrección o revertir el diario o el documento en su empresa.  

## Volver a crear movimientos en la bandeja de entrada  
 Si ha aceptado una transacción en la bandeja de entrada pero ha eliminado el documento o el diario en lugar de registrarlo, puede volver a crear el movimiento en la bandeja de entrada y aceptarlo de nuevo.  

## Panorama de transacciones de empresas vinculadas durante un periodo  
 Puede obtener una descripción general de todas las transacciones de empresas vinculadas que ha enviado y recibido en el periodo. Las listas de informe de **Transacciones de empresa vinculada** enumera todos los movimientos de empresas vinculadas, movimientos de cliente y movimientos de proveedor de contabilidad.

 > [!NOTE]  
 > Si los socios de empresas vinculadas se encuentran en la misma base de datos, las transacciones se transfieren sin necesidad de un archivo o correo electrónico. Consulte el campo **Tipo transferencia** de la página **Socio empresa vinculada**. <br /><br />
En ese caso, puede configurar el sistema para que evite las bandeja de entrada y de salida seleccionando la opción **Aceptar auto. transacciones** en la página **Socio empresa vinculada** y en la ventana **Enviar auto. transacciones** en la página **Config. empr. vincul.**, respectivamente. Las transacciones entrantes entre empresas vinculadas se pueden aceptar automáticamente solo si el programador de tareas está habilitado. Para obtener más información, consulte [Configuración de Business Central Server - Configuración del programador de tareas](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## Importar transacciones entre empresas vinculadas desde un archivo

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Si tiene alguna empresa vinculada asociada que no está incluida en la misma base de datos que su empresa, puede recibir transacciones entre empresas vinculadas de ese socio en un archivo .xml. Después, deberá importar las transacciones en su bandeja de entrada.  

1. Guarde el archivo en la ubicación que especificó en el campo **Detalles de bandeja de entrada de las empresas vinculadas** cuando configure empresas vinculadas.  
2. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones de bandeja de entrada entre empresas vinculadas** y luego elija el enlace relacionado.
3. En la página **Transacciones de bandeja de entrada entre empresas vinculadas**, seleccione la acción **Importar archivo transacción**.  
4. En la página que aparece, seleccione el archivo .xml que contiene las transacciones y seleccione el botón **Abrir**.  

Las transacciones se importan en la bandeja de entrada y quedan listas para ser procesadas.

## Procesar transacciones entrantes entre empresas vinculadas  
Cuando sus socios le envían transacciones entre empresas vinculadas, estas transacciones van a parar a su bandeja de entrada de empresas vinculadas. Debe evaluar cada transacción en la bandeja de entrada y emprender las acciones que estime convenientes.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones de bandeja de entrada entre empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Transacciones de bandeja de entrada entre empresas vinculadas**, seleccione una línea y, a continuación, elija una acción, como **Aceptar**, para procesar la línea.
3. En la página **Completa acc. band. entrada IC**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija el botón **Aceptar**.  

Para las líneas procesadas con la acción **Aceptar**, se crearán líneas de diario o documentos en su empresa. Abra cada documento o diario, haga los cambios necesarios y regístrelos.  

Las líneas que procesó con la acción **Devolvérsela al socio** se moverán a la bandeja de salida desde donde se pueden enviar a su socio.

Para las líneas que procesó con la acción **Devolvérsela al socio**, debe registrar una corrección de la transacción original registrada en su empresa.

## Procesar transacciones salientes entre empresas vinculadas  
Al registrar un diario o un documento de empresas vinculadas, o al enviar una confirmación de pedido de empresas vinculadas, las transacciones se envían a su bandeja de salida de empresas vinculadas. Para que se envíen a las empresas asociadas, debe abrir la bandeja de salida y procesarlas.  

1.  Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones de bandeja de salida entre empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Transacciones de bandeja de salida entre empresas vinculadas**, seleccione una línea y, a continuación, elija una acción, como **Devolver a bandeja de entrada**, para procesar la línea.

Las líneas que procesó con la acción **Enviar a socio de empresa vinculada** se enviarán a la bandeja de entrada del socio correspondiente.

Las líneas que procesó con la acción **Devolver a bandeja de entrada** se moverán a la bandeja de entrada donde podrá aceptarlas para crear documentos o líneas de diario en su empresa.  

Para las líneas que procesó con la acción **Cancelar**, debe registrar una corrección de la transacción original registrada en su empresa.  

## Para volver a crear transacciones entre empresas vinculadas en la bandeja de entrada  
De vez en cuando, es posible que desee volver a crear una transacción en la bandeja de entrada o bandeja de salida. Por ejemplo, si ha aceptado una transacción en la bandeja de entrada pero ha eliminado el documento o el diario en lugar de registrarlo, puede volver a crear el movimiento en la bandeja de entrada y aceptarlo de nuevo.  

Este siguiente procedimiento describe el método para volver a crear transacciones en la bandeja de entrada, pero para la bandeja de salida el procedimiento es el mismo.

  1.  Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones bandeja entrada IC procesadas** y luego elija el enlace de salida.  

  2.  En la página **Transacciones bandeja entrada IC procesadas**, seleccione la línea que contiene la transacción que desea volver a crear en la bandeja de entrada y elija la acción **Volver a crear transacción en bandeja de entrada**.  

## Consulte también
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
