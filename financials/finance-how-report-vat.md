---
title: Gestionar los informes de IVA a las autoridades fiscales | Documentos de Microsoft
description: "Obtenga más información sobre cómo preparar un informe que registre el IVA de ventas durante un periodo y enviarlo a las autoridades fiscales."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Crear informes de IVA para las autoridades fiscales.
La lista de ventas de la Comunidad Europea (CE) contiene listas de los importes del IVA que ha recaudado con las ventas dentro de la UE, por lo que puede enviar los importes del IVA al servicio web de una autoridad fiscal.

> [!NOTE]  
>   En el Reino Unido, todas las empresas que venden más de un determinado valor cada año a los clientes de los estados miembros de la UE deben presentar una versión electrónica de su informe de la lista de ventas de la Comunidad Europea en formato XML a través del sitio web Her Majesty's Revenue and Customs (HMRC).

El informe de la lista de ventas de la CE solo funciona para los países de la UE. Por ejemplo, no incluye el IVA por ventas a países como China o los Estados Unidos.

Para informar el IVA a una autoridad fiscal electrónicamente, debe conectar [!INCLUDE[d365fin](includes/d365fin_md.md)] al servicio web de la autoridad fiscal. Para ello es necesario que se configure una cuenta con su autoridad fiscal. Cuando tenga una cuenta, puede activar una conexión de servicio que proporcionamos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, en el Reino Unido puede utilizar la conexión de servicio **GovTalk** .

El informe incluye una línea para cada tipo de transacción con el cliente y muestra el importe total para cada tipo de transacción Existen tres tipos de transacciones que el informe puede incluir:  
  
* Mercancías B2B  
* Servicios B2B  
* Mercaderías trianguladas B2B  
  
Los bienes y servicios B2B especifican si se ha vendido un bien o un servicio y están controlados por el servicio **EU Service** en la configuración de los grupos de registro de IVA. Las mercaderías trianguladas B2B inciden en si se dedica al comercio con un tercero, y están controladas por el ajuste **Op. triangular UE** sobre los documentos de ventas, tales como órdenes de venta, facturas, abonos, etc.  
  
Después de enviar el informe, [!INCLUDE[d365fin](includes/d365fin_md.md)] supervisa el servicio y mantiene un registro de sus comunicaciones. El campo **Estado** indica dónde se encuentra el informe en el proceso. Por ejemplo, cuando las autoridades procesan el informe, el estado del informe cambia a **Tenido éxito**. Si la autoridad tributaria encuentra errores en el informe que envió, el estado del informe aparecerán en **Erróneo**. Puede ver los errores en **Errores y advertencias,** corregirlos y volver a enviar el informe. Para ver una lista de todos sus informes de listas de ventas de CE, vaya a la página **Informes de la lista de ventas de CE**.  
  
> [!NOTE]  
>   Si utiliza otro método para enviar el informe, por ejemplo, exportar el XML y cargarlo en un sitio web de autoridades fiscales, después puede elegir **Marcar como enviado** para cerrar el período del informe. Cuando marca el informe como enviado, se convierte en no editable. Si debe cambiar el informe después de marcarlo como enviado, debe volver a abrirlo. 
  
Después de que la autoridad fiscal revise su informe, enviará un correo electrónico a la persona de contacto de su empresa. En [!INCLUDE[d365fin](includes/d365fin_md.md)], la persona de contacto se especifica en la página **Información de la empresa**. Antes de enviar el informe, asegúrese de que ha elegido a una persona de contacto.

<!--> [!NOTE]  
>   El informe Lista de ventas de CE puede contener hasta 1000 líneas. Si tiene más líneas, debe enviar otro informe. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Conectarse al servicio web de su autoridad fiscal
[!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona las conexiones de servicio que se conectan a las páginas web de la autoridad fiscal. Por ejemplo, si se encuentra en el Reino Unido, debe habilitar la conexión de servicio **GovTalk** .  

1. En el campo **Buscar por páginas o informes** , introduzca **Conexiones de servicio** y, a continuación, seleccione el vínculo apropiado. <!-- remember to get the updated text for this-->  
2. Rellene los campos requeridos.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Configurar el informe Informe de lista de ventas de CE
1. En el campo **Buscar por páginas o informes** , introduzca **Configuración informe IVA** y, a continuación, elija el vínculo relacionado*.  
2. Si desea permitir que los usuarios cambien y vuelvan a enviar este informe, seleccione la casilla de verificación **Modificar informes enviados**.  
3. Especifique la serie de numeración que desee usar para los informes Lista de ventas de CE.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Preparar y enviar el informe de la lista de ventas de CE
1. En el campo **Buscar por páginas o informes** , introduzca **Lista venta CE** y, a continuación, elija el vínculo relacionado*.  
2. Elija **Nuevo** y, a continuación, rellene los campos requeridos.  
3. Para crear el contenido del informe, elija la acción **Proponer líneas** .  

    > [!NOTE]  
>   Puede revisar las transacciones incluidas en la línea antes de que envíe el informe. Para hacerlo, seleccione la línea y, a continuación, seleccione la acción **Mostrar movs. IVA**.  
4. Para preparar el informe para enviar, elija la acción **Enviar** .  
5. Para enviar el informe, elija la acción **Enviar** .  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] valida si el informe está correctamente configurado. Si falla la validación, los errores se muestran en la ventana **Errores y advertencias** de forma que pueda realizar los cambios necesarios.

## <a name="viewing-communications-with-your-tax-authority"></a>Visualización de comunicaciones con la autoridad fiscal.
En algunos países, se intercambian mensajes con la autoridad fiscal cuando se envían informes. Puede ver el primer y último mensaje que envió o recibió mediante las acciones **Descargar mensaje de envío** y **Descargar mensaje de respuesta** .  

## <a name="configuring-your-own-vat-reports"></a>Configuración de sus propios informes de IVA
Puede utilizar el informe de listas de ventas de CE original, sin embargo, también puede crear sus propios informes. Para ello es necesario crear algunas unidades de código. Si necesita ayuda, póngase en contacto con un socio de Microsoft.  
    
En la tabla siguiente se describen las unidades de código que debe crear para el informe.

| Codeunit | Qué se debe hacer |
|----|-----|
|Proponer líneas| Obtener información de la tabla de movimientos de IVA y mostrarla en las líneas del informe de IVA.|
|Contenido | Controlar el formato del informe. Por ejemplo, si es XML o JSON. El formato que debe utilizarse depende de los requisitos del servicio web de la autoridad fiscal. |
|Envío | Controla cómo y cuándo enviar el informe en función de los requisitos de su autoridad fiscal. |
|Controlador de respuesta | Controla la devolución de la autoridad fiscal. Por ejemplo, puede registrar un correo electrónico al contacto de la empresa. |
|Cancelar | Registre cancelaciones de un informe de IVA enviada anteriormente a la administración fiscal. |

> [!NOTE]  
>   Cuando cree las unidades de código para el informe, ponga atención al valor del campo **Versión de informe de IVA**. Este campo debe reflejar la versión del informe que la autoridad tributaria requiere. Por ejemplo, puede introducir **2017** en el campo para indicar que el informe cumple con los requisitos que estaban en vigor ese año. Para buscar la versión actual, póngase en contacto con su autoridad fiscal.  

## <a name="see-also"></a>Consulte también .
[Configurar IVA](finance-setup-vat.md)  
[Configurar ventas](sales-setup-sales.md)  
[Facturación de ventas](sales-setup-sales.md)  

