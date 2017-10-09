---
title: Intercambio de datos | Documentos de Microsoft
description: "Puede intercambiar datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y secuencias o archivos externos en conexión con tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos bancarios."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 81781676adf27a4f1c1d478bb2b4bd8248551468
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="exchanging-data"></a>Intercambio de datos
Puede intercambiar datos entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y secuencias o archivos externos en conexión con tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos bancarios.  

Para poder enviar y recibir documentos electrónicos o importar y exportar archivos bancarios, debe configurar el marco de intercambio de datos para procesar las secuencias o los archivos de datos correspondientes. Además, debe configurar áreas relacionadas. Estos incluyen los datos maestros para los clientes a los que envían las facturas electrónicas y el servicio de la conversión de datos bancarios en los casos en que distribuya conversiones de archivos bancarios a un proveedor de servicios externo. Para obtener más información, consulte [Configuración del intercambio de datos](across-set-up-data-exchange.md).  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Convertir registros de documentos de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)] a un formato estándar y enviarlos como documentos electrónicos que los clientes pueden recibir en su sistema.|[Procedimiento: Enviar documentos electrónicos](sales-how-to-send-electronic-documents.md)|  
|Enviar un PDF o archivos de imagen a un proveedor de servicios de OCR y recibirlos como documentos electrónicos que se pueden convertir a registros de documento en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md)|  
|Recibir documentos electrónicos, del servicio OCR o del servicio de intercambio de documentos, en un formato estándar que usted convertirá a los registros de documento relevantes en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Procedimiento: recibir y convertir documentos electrónicos](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Importe un archivo de extracto bancario a la ventana **Diario de conciliación de pagos** como el primer paso para conciliar pagos o a la ventana **Conciliación banco** como el primer paso para conciliar cuentas bancarias.|[Configuración del servicio de fuentes de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)|  
|Exportar pagos desde la ventana **Diario de pagos** a un archivo bancario que se cargará en la cuenta bancaria electrónica para su procesamiento.|[Exportación de pagos a un archivo de banco](payables-how-export-payments-bank-file.md)|  
|Indique a su banco para que transfiera los importes de pago de los bancos de los clientes a la cuenta de su empresa según la configuración de adeudo directo SEPA.|[Creación de movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Utilice un proveedor de servicios de tipos de cambio de divisa para actualizar la ventana **Divisas**.|[Actualizar los tipos de cambio de divisa](finance-how-update-currencies.md)|  
|Ver qué elementos de archivo están asignados a campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] al importar archivos de extracto CAMT de SEPA.|[Asignación de campos al importar archivos CAMT de SEPA](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Ver qué campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] están asignados a elementos de archivo al exportar archivos de pago con la función de servicio de conversión de datos bancarios.|[Asignación de campos al exportar archivos de pago con el servicio de conversión de datos bancarios](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos como documentos electrónicos ](across-data-exchange.md)  
[Facturación de ventas](sales-how-invoice-sales.md)   
[Procedimiento: Registro de compras](purchasing-how-record-purchases.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

