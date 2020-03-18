---
title: Intercambio de datos | Documentos de Microsoft
description: Puede intercambiar datos entre Business Central y secuencias o archivos externos en conexión con tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos bancarios.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e6466690fb4be462f20cd967c35b2aee39486b61
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076760"
---
# <a name="exchanging-data"></a>Intercambio de datos
Puede intercambiar datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y secuencias o archivos externos en conexión con tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos bancarios.  

Para poder enviar y recibir documentos electrónicos o importar y exportar archivos bancarios, debe configurar el marco de intercambio de datos para procesar las secuencias o los archivos de datos. Además, debe configurar áreas relacionadas, como los clientes a los que envía facturas electrónicas y la extensión AMC Banking 365 Fundamentals si distribuye conversiones de archivos bancarios a un proveedor de servicios externo. Para obtener más información, consulte [Configurar el intercambio de datos](across-set-up-data-exchange.md).  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Convertir registros de documentos de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)] a un formato estándar y enviarlos como documentos electrónicos que los clientes pueden recibir en su sistema.|[Enviar documentos electrónicos](sales-how-to-send-electronic-documents.md)|  
|Enviar un PDF o archivos de imagen a un proveedor de servicios de OCR y recibirlos como documentos electrónicos que se pueden convertir a registros de documento en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md)|  
|Recibir documentos electrónicos, del servicio OCR o del servicio de intercambio de documentos, en un formato estándar que usted convertirá a los registros de documento relevantes en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Recibir y convertir documentos electrónicos](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Prepare la importación de un archivo de extracto bancario a la página **Diario de conciliación de pagos** como el primer paso para conciliar pagos o a la página **Conciliación banco** como el primer paso para conciliar cuentas bancarias.|[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Exportar pagos desde la página **Diario de pagos** a un archivo bancario que se cargará en la cuenta bancaria electrónica para su procesamiento.|[Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Realizar pagos electrónicos en función del estándar de transferencia de crédito SEPA de la UE.|[Realizar pagos con la extensión AMC Banking 365 Fundamentals o transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Indique a su banco para que transfiera los importes de pago de los bancos de los clientes a la cuenta de su empresa según la configuración de adeudo directo SEPA.|[Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Utilice un proveedor de servicios de tipos de cambio de divisa para actualizar la página **Divisas**.|[Actualizar tipos cambio divisa](finance-how-update-currencies.md)|  
|Ver qué elementos de archivo están asignados a campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] al importar archivos de extracto CAMT de SEPA.|[Asignación de campos al importar archivos CAMT de SEPA](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Ver qué campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] están asignados a elementos de archivo al exportar archivos de pago con la extensión AMC Banking 365 Fundamentals.|[Asignación de campos al exportar archivos de pago utilizando la extensión AMC Banking 365 Fundamentals](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Facturar ventas](sales-how-invoice-sales.md)   
[Registrar compras](purchasing-how-record-purchases.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
