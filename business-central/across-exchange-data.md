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
ms.openlocfilehash: 0ed17b601df17ae85424013b6053ef1901082c10
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300550"
---
# <a name="exchanging-data"></a>Intercambio de datos
Puede intercambiar datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y secuencias o archivos externos en conexión con tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos bancarios.  

Para poder enviar y recibir documentos electrónicos o importar y exportar archivos bancarios, debe configurar el marco de intercambio de datos para procesar las secuencias o los archivos de datos correspondientes. Además, debe configurar áreas relacionadas. Estos incluyen los datos maestros para los clientes a los que envían las facturas electrónicas y el servicio de la conversión de datos bancarios en los casos en que distribuya conversiones de archivos bancarios a un proveedor de servicios externo. Para obtener más información, consulte [Configurar el intercambio de datos](across-set-up-data-exchange.md).  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Convertir registros de documentos de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)] a un formato estándar y enviarlos como documentos electrónicos que los clientes pueden recibir en su sistema.|[Enviar documentos electrónicos](sales-how-to-send-electronic-documents.md)|  
|Enviar un PDF o archivos de imagen a un proveedor de servicios de OCR y recibirlos como documentos electrónicos que se pueden convertir a registros de documento en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md)|  
|Recibir documentos electrónicos, del servicio OCR o del servicio de intercambio de documentos, en un formato estándar que usted convertirá a los registros de documento relevantes en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Recibir y convertir documentos electrónicos](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Prepare la importación de un archivo de extracto bancario a la página **Diario de conciliación de pagos** como el primer paso para conciliar pagos o a la página **Conciliación banco** como el primer paso para conciliar cuentas bancarias.|[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Exportar pagos desde la página **Diario de pagos** a un archivo bancario que se cargará en la cuenta bancaria electrónica para su procesamiento.|[Exportar pagos a un archivo bancario](payables-how-export-payments-bank-file.md)|
|Realizar pagos electrónicos en función del estándar de transferencia de crédito SEPA de la UE.|[Realizar pagos con Servicio de conversión de datos del banco o Transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Indique a su banco para que transfiera los importes de pago de los bancos de los clientes a la cuenta de su empresa según la configuración de adeudo directo SEPA.|[Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Utilice un proveedor de servicios de tipos de cambio de divisa para actualizar la página **Divisas**.|[Actualizar tipos cambio divisa](finance-how-update-currencies.md)|  
|Ver qué elementos de archivo están asignados a campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] al importar archivos de extracto CAMT de SEPA.|[Asignación de campos al importar archivos CAMT de SEPA](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Ver qué campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] están asignados a elementos de archivo al exportar archivos de pago con la función de servicio de conversión de datos bancarios.|[Asignación de campos al exportar archivos de pago con el servicio de conversión de datos bancarios](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Facturar ventas](sales-how-invoice-sales.md)   
[Registrar compras](purchasing-how-record-purchases.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
