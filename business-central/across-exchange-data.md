---
title: Intercambio de datos
description: 'Intercambie documentos comerciales electrónicos, por ejemplo, archivos bancarios, entre Business Central y terceros.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'exchange data, external files, electronic documents, AMC Banking, OCT, SEPA'
ms.date: 06/10/2021
ms.author: edupont
---
# <a name="exchanging-data" />Intercambio de datos
Puede intercambiar datos entre [!INCLUDE[prod_short](includes/prod_short.md)] y secuencias o archivos externos en conexión con tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos bancarios.  

Para poder enviar y recibir documentos electrónicos o importar y exportar archivos bancarios, debe configurar el marco de intercambio de datos para procesar las secuencias o los archivos de datos. Además, debe configurar áreas relacionadas, como los clientes a los que envía facturas electrónicas y la extensión AMC Banking 365 Fundamentals si distribuye conversiones de archivos bancarios a un proveedor de servicios externo. Para obtener más información, consulte [Configurar el intercambio de datos](across-set-up-data-exchange.md).  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Convertir registros de documentos de venta en [!INCLUDE[prod_short](includes/prod_short.md)] a un formato estándar y enviarlos como documentos electrónicos que los clientes pueden recibir en su sistema.|[Enviar documentos electrónicos](sales-how-to-send-electronic-documents.md)|  
|Enviar un PDF o archivos de imagen a un proveedor de servicios de OCR y recibirlos como documentos electrónicos que se pueden convertir a registros de documento en [!INCLUDE[prod_short](includes/prod_short.md)].|[Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md)|  
|Recibir documentos electrónicos, del servicio OCR o del servicio de intercambio de documentos, en un formato estándar que usted convertirá a los registros de documento relevantes en [!INCLUDE[prod_short](includes/prod_short.md)].|[Recibir y convertir documentos electrónicos](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Prepare la importación de un archivo de extracto bancario a la página **Diario de conciliación de pagos** como el primer paso para conciliar pagos o a la página **Conciliación banco** como el primer paso para conciliar cuentas bancarias.|[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)|  
|Exportar pagos desde la página **Diario de pagos** a un archivo bancario que se cargará en la cuenta bancaria electrónica para su procesamiento.|[Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Realizar pagos electrónicos en función del estándar de transferencia de crédito SEPA de la UE.|[Realizar pagos con la extensión AMC Banking 365 Fundamentals o transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Indique a su banco para que transfiera los importes de pago de los bancos de los clientes a la cuenta de su empresa según la configuración de adeudo directo SEPA.|[Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Utilice un proveedor de servicios de tipos de cambio de divisa para actualizar la página **Divisas**.|[Actualizar tipos cambio divisa](finance-how-update-currencies.md)|  
|Ver qué elementos de archivo están asignados a campos de [!INCLUDE[prod_short](includes/prod_short.md)] al importar archivos de extracto CAMT de SEPA.|[Asignación de campos al importar archivos CAMT de SEPA](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Exportar datos para informes de Intrastat en formato [!INCLUDE[prod_short](includes/prod_short.md)].|[Configuración de informes de Intrastat](finance-how-setup-report-intrastat.md)|
|Ver qué campos de [!INCLUDE[prod_short](includes/prod_short.md)] están asignados a elementos de archivo al exportar archivos de pago con la extensión AMC Banking 365 Fundamentals.|[Asignación de campos al exportar archivos de pago utilizando la extensión AMC Banking 365 Fundamentals](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also" />Consulte también
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Facturar ventas](sales-how-invoice-sales.md)   
[Registrar compras](purchasing-how-record-purchases.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
