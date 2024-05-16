---
title: 'Configurar SII para informes de IVA [ES]'
description: Este artículo explica cómo enviar documentos a través del SII en la versión en español de Microsoft Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '10740, 10751, 10752, 10753, 10770, 10771, 747, 473, 472'
ms.date: 04/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-sii-for-vat-reporting-in-the-spanish-version"></a>Configurar SII para informes de IVA en la versión en español

[!INCLUDE[prod_short](../../includes/prod_short.md)] admite los requisitos del SII españoles para la declaración del IVA (suministro de información inmediato).  

## <a name="enable-the-sii-module-in-the-spanish-version-of-business-central"></a>Habilitar el módulo SII en la versión en español de Business Central

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de SII** y luego seleccione el enlace relacionado.  
2. En la ficha desplegable **General**, seleccione el campo **Habilitado**.  

   El campo **Habilitado** se selecciona automáticamente si importa un certificado en el campo **Código de certificado** en la ficha desplegable **Certificado**.  

3. En el campo **Fecha operación**, especifique si desea utilizar la fecha registro o la fecha de emisión del documento como fecha de operación en el archivo XML que se envía a través del SII.  
4. Si desea enviar documentos en lotes, seleccione el campo **Habilitar envío de lotes**. Si habilita envíos por lotes de documentos, puede enviar documentos por lotes de forma manual o automática. Para el envío automático por lotes, los documentos se transfieren a la página **Historia SII** en estado *Pendiente* cuando los registra. Luego, cuando se alcanza o supera el valor umbral, los documentos se envían por lotes. Obtenga más información en la sección [Umbral de envíos de lotes de proyectos](#job-batch-submission-thresholds).

   Si no habilita los envíos por lotes, cada documento se envía cuando lo registra y el resultado se muestra en la página **Historial SII**.
   
5. Configure los otros campos, importe un certificado válido y especifique los puntos finales relevantes con la URL de destino. [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]

## <a name="job-batch-submission-thresholds"></a>Umbral de envíos de lotes de proyectos

Si desea utilizar el envío automático por lotes, el campo **Umbral de envío de lotes de proyectos** especifica el número de umbral de documentos con el estado *Pendiente* y eso activará un envío automático por lotes.

> [!IMPORTANT]
> Los campos **Habilitado** y **Envíos de lotes habilitados** deben seleccionarse para que el valor de umbral tenga efecto.  

Si el umbral se establece en cero (0), los documentos se enviarán cuando se registren.

Si el umbral se establece en uno o más, los documentos se envían automáticamente en lotes. Si el número de entradas pendientes supera el valor del umbral, todas las entradas pendientes se envían automáticamente.  

Siempre puede enviar documentos manualmente que tienen un estado *Pendiente* seleccionando **Reintentar** o **Reintentar todo** de la página **Historial SII**.

## <a name="specify-customers-without-a-registered-nif-with-aeat"></a>Especificar clientes sin NIF registrado en la AEAT

Si el NIF de un cliente aún no está registrado en la base de datos de la AEAT, se rechazará la presentación de documentos. En este caso, puede seleccionar la opción **No está en la AEAT** y volver a enviar el documento.

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2. Elija el cliente relevante para abrir la **Ficha de cliente**.
3. Seleccione el campo **No está en la AEAT**.

## <a name="set-vat-exemptions"></a>Establecer exenciones de IVA

Para indicar las exenciones del impuesto sobre el valor añadido (IVA) en el esquema SII, puede seleccionar un código de exención para una cláusula del IVA en la página **Cláusulas de IVA** o bien crear una nueva cláusula que se corresponda con la exención y elegir el código adecuado en el campo **Código de excepción SII**.

>[!IMPORTANT]
>Los valores predeterminados se proporcionan para cubrir escenarios estándar. Su negocio y el tipo de transacciones comerciales y cualquier personalización que pueda tener pueden requerir que seleccione un valor diferente para cumplir con los requisitos de presentación de informes bajo el SII.

Para habilitar la presentación de informes en los escenarios **No sujeto a impuestos debido a reglas de localización**, establezca la **Ficha config. registro IVA** correspondiente en la página **Config. grupos registro IVA** seleccionando la opción en el campo **No es un tipo imponible**. Para asegurar que funciona **Config. grupos registro IVA** de esta manera, el valor del campo **% IVA** debe ser igual a **0** (cero). 

Cuando contabiliza el documento y el IVA está configurado con el campo **No es un tipo imponible** activo, este campo junto con el campo **Mov. IVA** creará un nuevo **No es un movimiento imponible** que tiene detalles sobre esta exención de impuestos.

### <a name="vat-reporting-based-on-vat-exemption"></a>Informes de IVA basados en exención del IVA

El informe **Calc. y registrar liq. IVA** procesa **No son movimientos imponibles** de manera similar a **Movimientos de IVA**. Puede publicar algunos documentos con **No imponible** seleccionado por un período específico para tres movimientos **Config. grupos registro IVA** diferentes no imponibles y ejecutar el informe **Proceso Calc. y registrar liq. IVA**. La sección **No imponible** se imprimirá debajo de la sección **Movimientos de IVA** del informe.

Si decide cerrar algunos movimientos para **Config. grupos registro IVA**, el sistema cierra automáticamente **No son movimientos imponibles** que están conectados con este **Mov. IVA**. Si ejecuta el informe **Calc. y registrar liq. IVA** , se muestran todos los demás movimientos, pero sin incluir lo movimientos liquidados para el mismo período.

> [!NOTE]
> Puede generar la **Declaración de IVA** en la página **Declaraciones de IVA**. Seleccione **Vista previa** en la página **Declaraciones de IVA** para ver el resultado de la opción **Incluye movs. IVA** = **Abierto**. Esta opción también funciona para **No son movimientos imponibles**. La impresión del informe **Declaración de IVA** también es compatible con la opción **Incluir movimientos IVA** para los mismos valores (**Abierto**, **Cerrado** y **Abierto y cerrado**) tanto para **Movimientos IVA** como para **No son movimientos imponibles**.

## <a name="ignoring-invoice-lines-for-sii"></a>Ignorar líneas de factura para SII

En algunas situaciones, el usuario debe utilizar una línea de la factura, pero no reportarla al SII. Para realizar una configuración para este requisito, siga estos pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego seleccione el vínculo relacionado. 
1. Abra la **Tarjeta de configuración de grupos de registro de IVA** donde desea configurar esta exención y elija el campo **Ignorar en SII** para este grupo de registro.  

Cuando haya configurado **Configuración de registro de IVA** y después de crear la factura de compra o venta, puede seleccionar **Producto** y /o **Cuenta C/G** con la **Configuración de registro de IVA** y la línea con esta configuración se ignorará cuando la notifique a SII. Esta línea existe en **Movimiento de IVA**, pero esta entrada tendrá *Sí* en el campo **Ignorar en SII**.  

## <a name="see-also"></a>Consulte también

[SII - Tipos de factura y abonos en documentos de compra y venta](SII-invoice-types-sales-purchase-documents.md)    
[Funcionalidad local para España](spain-local-functionality.md)    

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
