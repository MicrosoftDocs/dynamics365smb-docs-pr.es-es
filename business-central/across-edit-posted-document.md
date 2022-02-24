---
title: Editar documentos de venta y compra registrados | Documentos de Microsoft
description: Obtenga información sobre las diferentes funciones de registro para registrar documentos de compra y cómo puede actualizar los documentos registrados.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1041dda83552af3c2c805c08518600d89f0467fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188737"
---
# <a name="edit-posted-documents"></a>Editar documentos registrados
A veces tiene que actualizar un documento registrado porque la información relevante para el documento ha cambiado. En un documento de venta publicado, puede ser el número de seguimiento del paquete del transportista, por ejemplo. En un documento de compra registrado, puede ser un texto de referencia de pago.

Realice el cambio en una versión editable del documento original, indicado por "**- Actualización**" en el título de la página. La página contiene un subconjunto de los campos en el documento original, de los cuales algunos son campos no editables que se muestran solo con fines informativos.

La funcionalidad está disponible para los siguientes documentos en todas las versiones de país:
- Histórico albaranes venta
- Factura compra reg.
- Histórico envío devolución
- Histórico de recepción de devolución

Los siguientes documentos adicionales se pueden editar en versiones de país seleccionadas:
- ES: histórico de facturas de venta, histórico de abonos de venta, abono de compra registrado
- APAC: histórico de abonos de venta, abono de compra registrado
- RU: histórico de abonos de venta
- IT: histórico envío transferencia, envío de servicio registrado

## <a name="to-edit-a-posted-sales-shipment"></a>Para editar un histórico de albaranes de venta
A continuación se explica cómo editar un histórico de albaranes de venta. Los pasos son similares para los demás documentos admitidos.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Histórico albaranes venta** y luego elija el enlace relacionado.
2. Seleccione el documento que desea editar y, a continuación, seleccione la acción **Actualizar documento**. También puede abrir el documento y, a continuación, elegir la acción.
3. En la página **Histórico albaranes venta - Actualiz.**, edite el campo **Nº seguimiento bulto** , por ejemplo.
4. Elija el botón **Aceptar**.

Se actualiza el histórico de albaranes de venta.

## <a name="see-also"></a>Consulte también
[Funciones empresariales generales](ui-across-business-areas.md)  
[Compras](purchasing-manage-purchasing.md)  
[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
