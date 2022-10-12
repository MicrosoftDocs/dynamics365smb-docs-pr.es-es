---
title: Enviar informes de IVA a las autoridades fiscales
description: Obtenga más información sobre cómo preparar informes que registren el IVA de ventas durante un periodo, o durante vendas y compras, y enviarlo a las autoridades fiscales.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.search.form: 321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401
ms.date: 01/31/2022
ms.author: bholtorf
ms.openlocfilehash: bf0ea7f023eed4dced53477d72ff844d4da04e37
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617854"
---
# <a name="report-vat-to-tax-authorities"></a>Crear informes de IVA para las autoridades fiscales

En este tema se describen los informes de [!INCLUDE[prod_short](includes/prod_short.md)] que puede utilizar para enviar información sobre importes del IVA (IVA) para ventas y compras a las autoridades fiscales de su región. Según el país específico, los informes pueden incluir información específica o puede haber informes adicionales que deba enviar. Consulte los artículos de su país o región en la sección [Funcionalidad local](about-localization.md).  

Utilice los siguientes informes incluidos:

* El informe **Lista venta CE**  

    La Lista de ventas de la Comunidad Europea (CE) contiene listas de los importes del IVA que ha recaudado con las ventas a clientes con IVA dentro de los países de la Unión Europea.  
* Acerca del informe de **Devolución de IVA**  

    El informe Devolución de IVA incluye el IVA de las ventas y compras a clientes y de proveedores pertenecientes a todos los países que utilizan el IVA.  

En ambos casos, el IVA se calcula basándose en la configuración de grupos registro IVA y los grupos de tipo de registro de IVA que haya configurado. [!INCLUDE[prod_short](includes/prod_short.md)] muestra entradas de IVA basadas en su **Fecha de IVA**.

Si desea ver un historial completo de entradas de IVA, cada publicación que implica IVA crea una entrada en la página **Movs. IVA** . Estos movimientos se utilizan para calcular el importe de liquidación de IVA, como pago o devolución, de un determinado periodo. Para ver las entradas de IVA, elija el icono ![Bombilla que abre la función 1 Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de IVA** y luego elija el enlace relacionado.

> [!NOTE]
> Cada entorno [!INCLUDE[prod_short](includes/prod_short.md)] está destinado a gestionar la información reglamentaria en un solo país. Por ejemplo, la versión holandesa de [!INCLUDE[prod_short](includes/prod_short.md)] gestiona las declaraciones del IVA en los Países Bajos, pero no en otros países. Del mismo modo, la versión de Estados Unidos de [!INCLUDE[prod_short](includes/prod_short.md)] gestiona las declaraciones 1099 en los Estados Unidos y no admite la solicitud de declaraciones del IVA en otros países, a menos que sea posible a través de una extensión entregada por nuestro ecosistema de socios o una modificación de código específica del cliente.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Acerca del informe de la Lista venta CE

En la Unión Europea (UE) y el Reino Unido, todas las empresas que venden bienes y servicios a los clientes con IVA, incluidos los de los estados miembros de la Unión Europea (UE), deben presentar una versión electrónica de su informe de la lista de ventas de la Comunidad Europea a sus clientes y autoridades fiscales. El informe **Lista de ventas de RE** funciona solo para los países de la UE.

El informe incluye una línea para cada tipo de transacción con el cliente y muestra el importe total para cada tipo de transacción Existen tres tipos de transacciones que el informe puede incluir:  

* Mercancías B2B  
* Servicios B2B  
* Mercaderías trianguladas B2B  

Los bienes y servicios *B2B* especifican si se ha vendido un bien o un servicio y están controlados por la opción **Servicio de la UE** en la configuración de los grupos de registro de IVA. Las *Mercaderías trianguladas B2B* indican si se dedica al comercio con un tercero, y están controladas por el ajuste **Comercio con tercera parte de la UE** sobre los documentos de ventas, como órdenes de venta, facturas, notas de abono, etc.  

Después de que la autoridad fiscal revise su informe, enviará un correo electrónico a la persona de contacto de su empresa. En [!INCLUDE[prod_short](includes/prod_short.md)], la persona de contacto se especifica en la página **Información de la empresa**. Antes de enviar el informe, asegúrese de que ha elegido a una persona de contacto.  

### <a name="submit-an-ec-sales-list-report"></a>Enviar un informe de lista de ventas de CE

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Acerca del informe de devolución de IVA

Utilice este informe para enviar el IVA para los documentos de ventas y compras, como órdenes de compra y venta, facturas y abonos. La información en el informe está en el mismo formato que el formulario de declaración de las autoridades aduaneras y fiscales.  

Para la devolución de IVA, puede especificar los movimientos para incluir:

* Envíe solo transacciones abiertas o abiertas y cerradas. Por ejemplo, esto resulta de utilidad para preparar su devolución anual final del IVA.
* Envíe solo los movimientos de los períodos especificados o también incluya movimientos de los períodos previos. Esto es útil para actualizar una declaración de IVA que ya haya enviado, por ejemplo, si un proveedor le envía una factura tardía.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Conectarse al servicio web de su autoridad fiscal
[!INCLUDE[prod_short](includes/prod_short.md)] proporciona las conexiones de servicio a las páginas web de la autoridad fiscal. Por ejemplo, si está en el Reino Unido, puede habilitar la conexión de servicio **GovTalk** para enviar electrónicamente la lista de ventas de EC y los informes de devolución de IVA. Si desea enviar el informe manualmente, por ejemplo, ingresando sus datos en el sitio web de la autoridad tributaria, esto no es necesario.   

Para informar el IVA a una autoridad fiscal electrónicamente, debe conectar [!INCLUDE[prod_short](includes/prod_short.md)] al servicio web de la autoridad fiscal. Para ello es necesario que se configure una cuenta con su autoridad fiscal. Cuando tenga una cuenta, puede activar una conexión de servicio que proporcionamos en [!INCLUDE[prod_short](includes/prod_short.md)].

1. Elija el icono ![Bombilla que abre la característica Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conexiones de servicio** y luego elija el enlace correspondiente.
2. Rellene los campos requeridos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Conviene probar la conexión. Para ello, seleccione la casilla **Modo de prueba** y, a continuación, prepare y envíe su informe de IVA como se describe en la sección [Preparar y enviar un informe de IVA](#to-prepare-and-submit-a-vat-report). Mientras está en modo de prueba, el servicio comprueba si la autoridad tributaria puede recibir su informe y el estado del informe indicará si el envío de la prueba ha sido satisfactorio. Debe recordar que no es un envío real. Para enviar el informe de válido, debe desactivar la casilla de verificación **Ejecutar en modo de prueba** y, a continuación, repetir el proceso.

## <a name="to-set-up-vat-reports-in-prod_short"></a>Para configurar informes IVA en [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>Para configurar periodos de devolución de IVA

Opcionalmente, si su negocio no está ubicado en el Reino Unido, use la página **Períodos de devolución de IVA** para configurar devoluciones de IVA programadas. Si su empresa está ubicada en el Reino Unido, consulte [Digitalización de impuestos en el Reino Unido](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Periodos de devolución de IVA** y luego elija el vínculo relacionado.  
2. En la página **Períodos de devolución de IVA**, rellene los campos para configurar el primer período. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Repita el paso 2 para cualquier período adicional que desee agregar.  

Ahora, cuando haya llegado el momento de enviar un informe de IVA para un período de devolución de IVA, elija el período en la página **Períodos de devolución de IVA** y, a continuación, elija la acción **Crear devolución de IVA**. Entonces, en la tarjeta **Devolución de IVA**, elija la acción **Líneas de sugerencia** como se describe en el paso 3 del siguiente procedimiento.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Para preparar y enviar un informe de IVA

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Lista de ventas de la CE** o **Devolución de IVA** y, a continuación, elija el vínculo relacionado.  
2. Elija **Nuevo** y, a continuación, rellene los campos requeridos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para crear el contenido del informe, elija la acción **Proponer líneas** .  

    > [!NOTE]  
    >  Para el informe de Lista de ventas de EC, puede revisar las transacciones incluidas en las líneas de informe antes de enviarlo. Para hacerlo, seleccione la línea y, a continuación, seleccione la acción **Mostrar movs. IVA**.  

4. Para validar y preparar el informe para enviar, elija la acción **Enviar** .  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] valida si el informe está correctamente configurado. Si falla la validación, los errores se muestran en la ventana **Errores y advertencias** para que pueda corregirlos. Normalmente, si el mensaje se trata de una configuración que falta en [!INCLUDE[prod_short](includes/prod_short.md)], puede hacer clic en el mensaje para abrir la página que contiene la información para corregir.  
5. Para enviar el informe, elija la acción **Enviar** .  

Después de enviar el informe, [!INCLUDE[prod_short](includes/prod_short.md)] supervisa el servicio y mantiene un registro de sus comunicaciones. El campo **Estado** indica dónde se encuentra el informe en el proceso. Por ejemplo, cuando las autoridades procesan el informe, el estado del informe cambia a **Tenido éxito**. Si la autoridad tributaria encuentra errores en el informe que envió, el estado del informe aparecerán en **Erróneo**. Puede ver los errores en **Errores y advertencias**, corregirlos y volver a enviar el informe. Para ver una lista de todos sus informes de listas de ventas de CE, vaya a la página **Informes de la lista de ventas de CE**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Visualización de comunicaciones con la autoridad fiscal.
En algunos países, se intercambian mensajes con la autoridad fiscal cuando se envían informes. Puede ver el primer y último mensaje que envió o recibió mediante las acciones **Descargar mensaje de envío** y **Descargar mensaje de respuesta** .  

## <a name="submitting-vat-reports-manually"></a>Enviar informes de IVA manualmente
Si utiliza otro método para enviar el informe, por ejemplo, exportar el XML y cargarlo en un sitio web de autoridades fiscales, después puede elegir **Marcar como enviado** para cerrar el período del informe. Cuando marca el informe como enviado, se convierte en no editable. Si debe cambiar el informe después de marcarlo como enviado, debe volver a abrirlo.

## <a name="vat-settlement"></a>Liquidación IVA
De manera periódica, debe remitir la red IVA a las autoridades fiscales. Si tiene que liquidar el IVA con frecuencia, puede ejecutar el trabajo por lotes **Calc. y registrar liq. IVA** para cerrar los movimientos de IVA abiertos y transferir los importes del IVA de ventas y compras a la cuenta de liquidación del IVA.

Al transferir importes de IVA a la cuenta de liquidación, la cuenta de IVA soportado se contabiliza en el Haber y la cuenta de IVA repercutido se contabiliza en el Deber con los importes calculados en el periodo. El importe neto se contabiliza en el Haber, o en el Debe, si el importe de IVA soportado es superior, en la cuenta de liquidación del IVA. Puede registrar la liquidación inmediatamente o imprimir primero un informe.  

> [!Note]
> Cuando se utiliza el trabajo por lotes **Calc. y registrar liq. IVA**, si no especifica un **Grupo registro IVA neg.** y un **Grupo registro IVA prod.**, se incluirán los movimientos con todos los códigos de los grupos contables de negocio y los de grupos contables de producto.

## <a name="configuring-your-own-vat-reports"></a>Configuración de sus propios informes de IVA

Puede usar de forma inmediata el informe **Lista de ventas de la CE**. Sin embargo, también puede crear sus propios informes, si tiene una licencia de desarrollo, para que pueda crear unidades de código. Si necesita asistencia, póngase en contacto con un socio de Microsoft.  

En la tabla siguiente se describen las codeunits que debe crear para el informe.  

| Codeunit | Qué se debe hacer |
|----|-----|
|Proponer líneas| Obtener información de la tabla **Movimientos de IVA** y mostrarla en las líneas del informe de IVA.|
|Contenido | Controlar el formato del informe. Por ejemplo, si es XML o JSON. El formato que debe utilizarse depende de los requisitos del servicio web de la autoridad fiscal. |
|Envío | Controla cómo y cuándo enviar el informe en función de los requisitos de su autoridad fiscal. |
|Controlador de respuesta | Controla la devolución de la autoridad fiscal. Por ejemplo, puede registrar un correo electrónico al contacto de la empresa. |
|Cancelar | Registre cancelaciones de un informe de IVA enviada anteriormente a la administración fiscal. |  

> [!Note]
> Cuando cree las unidades de código para el informe, preste atención al valor del campo **Versión de informe de IVA**. Este campo debe reflejar la versión del informe que la autoridad tributaria requiere. Por ejemplo, puede introducir **2021** en el campo para indicar que el informe cumple con los requisitos que estaban en vigor ese año. Para buscar la versión actual, póngase en contacto con su autoridad fiscal.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/process-vat-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Configurar ventas](sales-setup-sales.md)  
[Facturar ventas](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
