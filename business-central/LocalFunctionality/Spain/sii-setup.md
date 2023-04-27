---
title: 'Configurar SII para informes de IVA [ES]'
description: Descubre cómo configurar Business Central para enviar documentos a través del SII en la versión en español.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10751, 10752, 10753, 10770, 10771, 747, 473'
ms.date: 07/12/2022
ms.author: edupont
---
# Configurar SII para informes de IVA en la versión en español

[!INCLUDE[prod_short](../../includes/prod_short.md)] admite los requisitos del SII españoles para la declaración del IVA (suministro de información inmediato).  

## Habilitar el módulo SII en la versión española

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de SII** y luego elija el enlace relacionado.  
2. En la ficha desplegable **General**, seleccione el campo **Habilitado**.  

   El campo **Habilitado** se selecciona automáticamente si importa un certificado en el campo **Código de certificado** en la ficha desplegable **Certificado**.  
3. En el campo **Fecha operación**, especifique si desea utilizar *Fecha registro* o *Fecha emisión documento* como fecha de operación en el archivo XML que se envía a través del SII a las autoridades fiscales.  
4. Si desea enviar documentos en lotes, seleccione el campo **Habilitar envío de lotes**.

   Si no habilita los envíos por lotes, cada documento se envía cuando lo registra y el resultado se muestra en la página **Historial SII**.

   Si utiliza envíos por lotes de documentos, puede enviar documentos por lotes de forma manual o automática. Con el envío automático por lotes, los documentos se transfieren a la página **Historial SII** con un estado de *Pendiente* cuando los registra y envía en lotes cuando se alcanza o supera el valor umbral. Obtenga más información en la sección [Umbral de envíos de lotes de proyectos](#job-batch-submission-thresholds).
5. Configure los otros campos, importe un certificado válido y especifique los puntos finales relevantes con la URL de destino. [!INCLUDE[tooltip-inline-tip](../../includes/tooltip-inline-tip_md.md)]

## Umbral de envíos de lotes de proyectos

Si desea utilizar el envío automático por lotes, el campo **Umbral de envío de lotes de proyectos** especifica el número de umbral de documentos con el estado *Pendiente* y eso activará un envío automático por lotes.

> [!IMPORTANT]
> Los campos **Habilitado** y **Envíos de lotes habilitados** deben seleccionarse para que el valor de umbral tenga efecto.  

Si el umbral se establece en *0*, los documentos se enviarán cuando se registren.

Si el umbral se establece en *1* o más, los documentos se envían automáticamente en lotes. Si el número de entradas pendientes supera el valor del umbral, todas las entradas pendientes se envían automáticamente.  

Siempre puede enviar documentos manualmente con un estado *Pendiente* eligiendo las acciones **Reintentar** o **Reintentar todo** de la página **Historial SII**.

## Especificar clientes sin NIF registrado en la AEAT

Si el NIF de un cliente aún no está registrado en la base de datos de la AEAT, se rechazará la presentación de documentos. En este caso, puede seleccionar la opción **No está en la AEAT** y volver a enviar el documento.

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2. Elija el cliente relevante para abrir la **Ficha de cliente**.
3. Seleccione el campo **No está en la AEAT**.

## Establecer exenciones de IVA

Para indicar las exenciones del impuesto sobre el valor añadido (IVA) en el esquema SII, puede seleccionar un código de exención para una cláusula del IVA en la página **Cláusulas de IVA** o bien crear una nueva cláusula que se corresponda con la exención y elegir el código adecuado en el campo **Código de excepción SII**.

>[!IMPORTANT]
>Los valores predeterminados se proporcionan para cubrir escenarios estándar. Su negocio y el tipo de transacciones comerciales y cualquier personalización que pueda tener pueden requerir que seleccione un valor diferente para cumplir con los requisitos de presentación de informes bajo el SII.

Para habilitar la presentación de informes en los escenarios **No sujeto a impuestos debido a reglas de localización**, establezca la **Ficha config. registro IVA** correspondiente en la página **Config. grupos registro IVA** eligiendo la opción en el campo **No es un tipo imponible**.

## Consulte también .

[SII - Tipos de factura y abonos en documentos de compra y venta](SII-invoice-types-sales-purchase-documents.md)  
[Funcionalidad local para España](spain-local-functionality.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
