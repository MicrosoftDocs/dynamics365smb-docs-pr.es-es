---
title: Experiencia contable en Financials | Documentos de Microsoft
description: "Obtenga más información sobre el portal contable de Dynamics 365 for Financials y el Área de trabajo Contable que admite a los contadores interno y externo en la empresa cliente."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b75c223b01690703b57c427ff00267ed5af7a13e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="accountant-experiences-in-included365finlongincludesd365finlongmdmd"></a>Experiencias contables en [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Los negocios deben crear sus libros y firmas de contabilidad. Algunas empresas emplean un contable externo, y otras lo tienen en plantilla. Independientemente del tipo de contable que sea, puede utilizar el Área de trabajo **Contable** como su página de inicio en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Desde aquí, puede acceder a todas las ventanas que necesita en su trabajo.  

## <a name="accountant-role-center"></a>Área de trabajo Contable
El Área de trabajo es un tablero de mandos con cuadros de actividad que le muestran cifras clave en tiempo real y le proporcionan un acceso rápido a los datos. En la cinta en la parte superior de la ventana tiene acceso a más acciones, como abrir los informes financieros y las declaraciones más utilizados en Excel. En el panel de navegación de la izquierda, puede cambiar rápidamente entre las listas que utiliza con mayor frecuencia. Si amplía el menú **Inicio** en el panel de navegación, verá otras áreas, como **Documentos registrados** con los diversos tipos de documentos que la empresa ha publicado.  

Si es nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede iniciar una lista de videos directamente desde su página de inicio. También puede abrir el paseo **Introducción** que se centra en las áreas clave.  

> [!NOTE]  
>  Esta funcionalidad requiere que la experiencia esté definida en **Suite**. Para obtener más información, consulte [Personalizar la experiencia de Financials](ui-experiences.md).  

### <a name="get-invited-to-a-clients-included365finincludesd365finmdmd"></a>Obtenga una invitación a un [!INCLUDE[d365fin](includes/d365fin_md.md)] de cliente
Una empresa que utiliza [!INCLUDE[d365fin](includes/d365fin_md.md)] puede invitarle a [!INCLUDE[d365fin](includes/d365fin_md.md)] como su contable externo. Para ello es necesario que se haya definido el correo SMTP, por lo que posible que dese ponerse en contacto con su socio [!INCLUDE[d365fin](includes/d365fin_md.md)] para obtener ayuda. Para obtener más información, consulte [Invitar al contable externo](finance-invite-external-accountant.md). Además, le recomendamos que proporcione la dirección de correo electrónico que va a utilizar para su trabajo de contabilidad; de esa manera, puede elegir si desea utilizar *me@accountant.com* o *me@client.com*.  

Como resultado, recibirá el correo electrónico del cliente con un vínculo a [!INCLUDE[d365fin](includes/d365fin_md.md)]  

A continuación, podrá acceder a sus datos financieros desde el **Área de trabajo Contable**. Si utiliza el portal contable, también puede añadir al cliente a la lista de clientes en el tablero del portal contable.  

## <a name="accountant-portal"></a>Portal para contables
Si es un contable con varios clientes, puede utilizar el portal como su panel de control para obtener una mejor visión general de sus clientes. Desde allí, puede acceder al suscriptor de cada cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)] y utilizar el Área de trabajo Contable como se describe anteriormente.  

El portal del contable es una versión dedicada de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede obtener acceso al tablero de mandos si se registra en [Financials para contables en Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]  
>  Cuando se registra en el portal contable, debe especificar su dirección de correo electrónico de empresa, como *me@accountant.com*. Recomendamos que utilice la misma dirección de correo electrónico cuando trabaje en el [!INCLUDE[d365fin](includes/d365fin_md.md)] de sus clientes, de modo que pueda cambiar fácilmente entre clientes.  

Cuando inicia sesión por primera vez en el portal contable, el panel muestra un ejemplo de cliente para ayudarle a empezar. Una vez que se sienta cómodo, puede eliminar ese cliente de ejemplo.  

### <a name="working-with-individual-clients"></a>Trabajar con clientes individuales
El panel muestra la información más importante sobre cada cliente.  
[![Portal para contables](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)

La columna **Nombre de la empresa** muestra todas las empresas que el cliente tiene en [!INCLUDE[d365fin](includes/d365fin_md.md)] y la columna **Nombre del cliente** muestra los nombres de sus clientes. Puede personalizar el panel para mostrar los puntos de datos que desea ver añadiendo o eliminando columnas. Por ejemplo, es posible que desee ver los impuestos que se deben, cuántos documentos de ventas abiertos tiene cada cliente, o el número de facturas de compra que vencen la próxima semana. Puede configurar la vista para adaptarla a sus necesidades. Si tiene varios clientes, puede utilizar filtros para ordenar la vista.  

Junto al nombre de la empresa, los puntos suspensivos (...) revelan un menú corto:

* Actualizar la empresa actual y obtener nuevos datos para el cliente  
* Vaya a la empresa del cliente  
* Seleccione más empresas  

De manera similar, por ejemplo, puede utilizar el menú desplegable **Resumen de cliente** para actualizar todas las empresas o abrir la empresa actual seleccionada.  

### <a name="company-details"></a>Detalles empresa
Puede ver más información acerca de los datos de sus clientes eligiendo el nombre de la empresa sobre la que desea saber más. Se abrirá el panel **Detalles empresa**, donde podrá ver la información adicional siguiente:  

* Saldos de cuentas de efectivo  
* Previsión flujos efectivo  
* Facturas compra vencidas  
* Facturas venta vencidas  

![Los detalles de la empresa cliente en el portal contable](./media/finance-accounting/accountant-company-details.png)

Técnicamente, ahora se ha registrado en su [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente y los datos que se ven son datos reales. Si desea estudiar atentamente los datos, como una factura de compra vencida, elija el vínculo y se le redireccionará a la empresa cliente.  

> [!TIP]  
>  Puede lanzar los libros de Excel predefinidos de la pestaña **Informes** en la cinta de opciones. Estos libros de Excel están diseñadas para estar listos para imprimir los informes financieros e informes clave, pero también puede modificarlos en función de sus necesidades. Para obtener más información, consulte [Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md).  

En caso contrario, cierre el panel de detalles y continúe con el cliente siguiente.  

### <a name="working-in-the-client-company"></a>Trabajar en la empresa cliente
Si desea hacer más trabajo para un cliente, puede hacerlo en el Área de trabajo Contable en su [!INCLUDE[d365fin](includes/d365fin_md.md)], elija simplemente el elemento de menú **Ir al cliente** e iniciará sesión automáticamente.  

En la empresa del cliente, puede ver y modificar los datos que necesita en su trabajo. Para obtener más información, consulte la parte superior de esta página.

> [!NOTE]  
>  Si no tiene la intención de regresar a este cliente en unos minutos, le recomendamos que cierre la pestaña del navegador.  

### <a name="adding-clients"></a>Añadir clientes
Puede agregar un cliente mediante la ventana **Clientes** que puede abrir con la acción **Administrar clientes** de la cinta. Simplemente, elija **Nuevo** y, a continuación, rellene los campos.  

Los datos de la tarjeta para cada cliente los especifica el usuario, y puede cambiarlos según sea necesario. Sin embargo, el campo **Dirección URL del cliente** es fundamental ya que así es como puede acceder al [!INCLUDE[d365fin](includes/d365fin_md.md)] de cada cliente. Utilice la acción **URL de prueba del cliente** de la cinta para comprobar que ha introducido el vínculo correcto. La dirección URL que debe introducir apunta en el [!INCLUDE[d365fin](includes/d365fin_md.md)] del cliente, como *https://mybusiness.financials.dynamics.com*. A continuación, esta URL se utiliza cuando elige el elemento de menú **Ir a empresa**.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Análisis de estados financieros en Excel](finance-analyze-excel.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Invitar a contable externo a [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-invite-external-accountant.md)  
[Financials for Accountants en Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
[Configuración del análisis de flujo de efectivo](finance-setup-cash-flow-analyses.md)  

