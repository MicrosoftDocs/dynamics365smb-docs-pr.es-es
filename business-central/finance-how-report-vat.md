---
title: Enviar informes de IVA a las autoridades fiscales | Documentos de Microsoft
description: "Obtenga más información sobre cómo preparar informes que registren el IVA de ventas durante un periodo, o durante vendas y compras, y enviarlo a las autoridades fiscales."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 07/17/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b88b714e380155f1da089c3549d9533ceea0624e
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---

# <a name="how-to-report-vat-to-a-tax-authority"></a>Crear informes de IVA para una autoridad fiscal
En este tema se describen los informes de [!INCLUDE[d365fin](includes/d365fin_md.md)] que puede utilizar para enviar información sobre importes del IVA (IVA) para ventas y compras a las autoridades fiscales de su región.

Utilice los siguientes informes:

* El informe **Lista venta CE** (Lista de ventas de la Comunidad Europea (CE)) contiene listas de los importes del IVA que ha recaudado con las ventas a clientes con IVA dentro de los países de la Unión Europea.  
* El informe **Devolución de IVA** incluye el IVA de las ventas y compras a clientes pertenecientes a todos los países que utilizan el IVA.

Si desea ver un historial completo de entradas de IVA, cada publicación que implica IVA crea una entrada en la página **Movs. IVA** . Estos movimientos se utilizan para calcular el importe de liquidación de IVA, como pago o devolución, de un determinado periodo. Para ver las entradas del IVA, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Movs. IVA** y, a continuación, seleccione el vínculo relacionado.

## <a name="about-the-ec-sales-list-report"></a>Acerca del informe de la Lista venta CE
En el Reino Unido, todas las empresas que venden bienes y servicios a los clientes con IVA, incluidos los de los estados miembros de la UE, deben presentar una versión electrónica de su informe de la lista de ventas de la Comunidad Europea en formato XML a través del sitio web Her Majesty's Revenue and Customs (HMRC). El informe de la lista de ventas de la CE funciona solo para los países de la UE.

El informe incluye una línea para cada tipo de transacción con el cliente y muestra el importe total para cada tipo de transacción Existen tres tipos de transacciones que el informe puede incluir:  

* Mercancías B2B  
* Servicios B2B  
* Mercaderías trianguladas B2B  

Los bienes y servicios B2B especifican si se ha vendido un bien o un servicio y están controlados por el servicio **EU Service** en la configuración de los grupos de registro de IVA. Las mercaderías trianguladas B2B indican si se dedica al comercio con un tercero, y están controladas por el ajuste **Op. triangular UE** sobre los documentos de ventas, tales como órdenes de venta, facturas, abonos, etc.  

Después de que la autoridad fiscal revise su informe, enviará un correo electrónico a la persona de contacto de su empresa. En [!INCLUDE[d365fin](includes/d365fin_md.md)], la persona de contacto se especifica en la página **Información de la empresa**. Antes de enviar el informe, asegúrese de que ha elegido a una persona de contacto.

## <a name="about-the-vat-return-report"></a>Acerca del informe de devolución de IVA
Utilice este informe para enviar el IVA para los documentos de ventas y compras, como órdenes de compra y venta, facturas y abonos. La información en el informe está en el mismo formato que el formulario de declaración de las autoridades aduaneras y fiscales.  

El IVA se calcula basándose en la configuración de grupos registro IVA y los grupos de registro de IVA que haya configurado.

Para la devolución de IVA, puede especificar los movimientos para incluir:

* Envíe solo transacciones abiertas o abiertas y cerradas. Por ejemplo, esto resulta de utilidad para preparar su devolución anual final del IVA.
* Envíe solo los movimientos de los períodos especificados o también incluya movimientos de los períodos previos. Esto es útil para actualizar una declaración de IVA que ya haya enviado, por ejemplo, si un proveedor le envía una factura tardía.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Conectarse al servicio web de su autoridad fiscal
[!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona las conexiones de servicio a las páginas web de la autoridad fiscal. Por ejemplo, si está en el Reino Unido, puede habilitar la conexión de servicio **GovTalk** para enviar electrónicamente la lista de ventas de EC y los informes de devolución de IVA. Si desea enviar el informe manualmente, por ejemplo, ingresando sus datos en el sitio web de la autoridad tributaria, esto no es necesario.   

Para informar el IVA a una autoridad fiscal electrónicamente, debe conectar [!INCLUDE[d365fin](includes/d365fin_md.md)] al servicio web de la autoridad fiscal. Para ello es necesario que se configure una cuenta con su autoridad fiscal. Cuando tenga una cuenta, puede activar una conexión de servicio que proporcionamos en [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Conexiones de servicio** y, a continuación, seleccione el vínculo apropiado.
2. Rellene los campos requeridos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >   Conviene probar la conexión. Para ello, seleccione la casilla de verificación **Ejecutar en modo de prueba** y, a continuación, prepare y envíe su informe de IVA como se describe en la sección _Preparar y enviar un informe de IVA_. Mientras está en modo de prueba, el servicio comprueba si la autoridad tributaria puede recibir su informe y el estado del informe indicará si el envío de la prueba ha sido satisfactorio. Debe recordar que no es un envío real. Para enviar el informe de válido, debe desactivar la casilla de verificación **Ejecutar en modo de prueba** y, a continuación, repetir el proceso.

## <a name="to-set-up-vat-reports-in-included365finincludesd365finmdmd"></a>Para configurar informes IVA en [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración informe IVA** y, a continuación, seleccione el vínculo relacionado.  
2. Para permitir que los usuarios cambien y vuelvan a enviar este informe, seleccione la casilla de verificación **Modificar informes enviados**.  
3. Elija el código de serie que desee usar para cada informe.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Para preparar y enviar un informe de IVA
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Lista venta CE** o **Devolución de IVA** y, a continuación, seleccione el vínculo relacionado.  
2. Elija **Nuevo** y, a continuación, rellene los campos requeridos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para crear el contenido del informe, elija la acción **Proponer líneas** .  

    > [!NOTE]  
    >   Para el informe de Lista de ventas de EC, puede revisar las transacciones incluidas en las líneas de informe antes de enviarlo. Para hacerlo, seleccione la línea y, a continuación, seleccione la acción **Mostrar movs. IVA**.  
4. Para validar y preparar el informe para enviar, elija la acción **Enviar** .  

    >  [!NOTE]  
    >   [!INCLUDE[d365fin](includes/d365fin_md.md)] valida si el informe está correctamente configurado. Si falla la validación, los errores se muestran en la ventana **Errores y advertencias** para que pueda corregirlos. Normalmente, si el mensaje se trata de una configuración que falta en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede hacer clic en el mensaje para abrir la página que contiene la información para corregir.  
5. Para enviar el informe, elija la acción **Enviar** .  

Después de enviar el informe, [!INCLUDE[d365fin](includes/d365fin_md.md)] supervisa el servicio y mantiene un registro de sus comunicaciones. El campo **Estado** indica dónde se encuentra el informe en el proceso. Por ejemplo, cuando las autoridades procesan el informe, el estado del informe cambia a **Tenido éxito**. Si la autoridad tributaria encuentra errores en el informe que envió, el estado del informe aparecerán en **Erróneo**. Puede ver los errores en **Errores y advertencias**, corregirlos y volver a enviar el informe. Para ver una lista de todos sus informes de listas de ventas de CE, vaya a la página **Informes de la lista de ventas de CE**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Visualización de comunicaciones con la autoridad fiscal.
En algunos países, se intercambian mensajes con la autoridad fiscal cuando se envían informes. Puede ver el primer y último mensaje que envió o recibió mediante las acciones **Descargar mensaje de envío** y **Descargar mensaje de respuesta** .  

## <a name="submitting-vat-reports-manually"></a>Enviar informes de IVA manualmente
Si utiliza otro método para enviar el informe, por ejemplo, exportar el XML y cargarlo en un sitio web de autoridades fiscales, después puede elegir **Marcar como enviado** para cerrar el período del informe. Cuando marca el informe como enviado, se convierte en no editable. Si debe cambiar el informe después de marcarlo como enviado, debe volver a abrirlo.

## <a name="vat-settlement"></a>Liquidación IVA
De manera periódica, debe remitir la red IVA a las autoridades fiscales. Si tiene que liquidar el IVA con frecuencia, puede ejecutar el trabajo por lotes **Calc. y registrar liq. IVA** para cerrar los movimientos de IVA abiertos y transferir los importes del IVA de ventas y compras a la cuenta de liquidación del IVA.

Al transferir importes de IVA a la cuenta de liquidación, la cuenta de IVA soportado se contabiliza en el Haber y la cuenta de IVA repercutido se contabiliza en el Deber con los importes calculados en el periodo. El importe neto se contabiliza en el Haber, o en el Debe, si el importe de IVA soportado es superior, en la cuenta de liquidación del IVA. Puede registrar la liquidación inmediatamente o imprimir primero un informe.

>    [!NOTE]  
>    Cuando se utiliza el trabajo por lotes **Calc. y registrar liq. IVA**, si no especifica un **Grupo registro IVA neg.** y un **Grupo registro IVA prod.**, se incluirán los movimientos con todos los códigos de los grupos contables de negocio y los de grupos contables de producto.

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
[Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Facturar ventas](sales-setup-sales.md)  

