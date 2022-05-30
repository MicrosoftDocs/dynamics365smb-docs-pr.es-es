---
title: Configurar SII para informes de IVA [ES]
description: Descubre cómo configurar Business Central para enviar documentos a través del SII en la versión en español.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 10751, 10752, 10753, 10770, 10771
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: a81a6c53ac00585d241afcfa2269fb1fd1b89ffd
ms.sourcegitcommit: bc645e7ecb1940a85b2c433aa894d3494c9b10df
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743744"
---
# <a name="set-up-sii-for-vat-reporting-in-the-spanish-version"></a>Configurar SII para informes de IVA en la versión en español

[!INCLUDE[prod_short](../../includes/prod_short.md)] admite los requisitos del SII españoles para la declaración del IVA (suministro de información inmediato).  

## <a name="to-use-the-sii-module-in-the-spanish-version"></a>Para usar el módulo SII en la versión española

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de SII** y luego elija el enlace relacionado.  
2. En la ficha desplegable **General**, seleccione el campo **Habilitado**.  

  El campo **Habilitado** se selecciona automáticamente si importa un certificado en el campo **Código de certificado** en la ficha desplegable **Certificado**.  
2. En el campo **Fecha operación**, especifique si desea utilizar *Fecha registro* o *Fecha emisión documento* como fecha de operación en el archivo XML que será enviado a través del SII a las autoridades fiscales.  
3. Si desea enviar documentos en lotes, seleccione el campo **Habilitar envío de lotes**.  

  <!--You must also specify how you want to submit them in the **Job Batch Submission Threshold** field, where you can specify the minimum number of pending history records for the batch submission.  -->

  Si no configura envíos por lotes, cada documento se envía cuando lo registra y el resultado se muestra en la página **Historial SII**.  

  Si utiliza envíos por lotes de documentos, puede enviar documentos por lotes de forma manual o automática. Con el envío automático por lotes, los documentos se transfieren a **Historial SII** con un estado de *Pendiente* cuando los registra y envía en lotes cuando se alcanza o supera el valor umbral, consulte la sección [Umbral de envíos de lotes de proyectos](#job-batch-submission-thresholds).  
4. Configure otros campos, importe un certificado válido y especifique los puntos finales relevantes con la URL de destino.

## <a name="job-batch-submission-thresholds"></a>Umbral de envíos de lotes de proyectos

Si desea utilizar el envío automático por lotes, el campo **Umbral de envío de lotes de proyectos** especifica el número de umbral de documentos con el estado *Pendiente* y eso activará un envío automático por lotes.

> [!IMPORTANT]
> Los campos **Habilitado** y **Envíos de lotes habilitados** deben seleccionarse para que el valor de umbral tenga efecto.  

Si el umbral se establece en *0*, los documentos se enviarán cuando registre el documento.  

Si el umbral se establece en *1* o más, los documentos se envían automáticamente en lotes. Si el número de entradas pendientes supera el valor del umbral, todas las entradas pendientes se envían automáticamente.  

Siempre puede enviar documentos manualmente con un estado de *Pendiente* eligiendo la acción **Reintentar** o **Reintentar todo**.

## <a name="see-also"></a>Consulte también

[SII - Tipos de factura y abonos en documentos de compra y venta](SII-invoice-types-sales-purchase-documents.md)  
[Funcionalidad local para España](spain-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
