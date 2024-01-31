---
title: Acerca del marco de intercambio de datos
description: Este artículo explica cómo usar el Marco de intercambio de datos para administrar el intercambio de datos en documentos comerciales como facturas con sus socios comerciales.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR'
ms.search.form: '189,'
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Acerca del marco de intercambio de datos

Puede usar Marco de intercambio de datos para gestionar documentos empresariales, archivos bancarios, tipos de cambio de divisa y cualquier otro archivo de datos con sus socios o autoridades comerciales.

Como administrador o socio de Microsoft, puede usar el marco en nuevas funciones de integración configurando qué datos intercambiar y cómo. Por ejemplo, el formato de archivos para intercambio de datos en archivos bancarios, documentos electrónicos, tipos de cambio de divisa y otros con los sistemas ERP varía en función del proveedor del archivo de datos o de secuencia y el país o la región. [!INCLUDE[prod_short](includes/prod_short.md)] utiliza varios formatos de archivo bancario y estándares de servicio de datos. Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.

 En los diagramas siguientes se muestra la arquitectura del marco de intercambio de datos.  

 ![Marco de intercambio de datos &#45; Importar.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Marco de intercambio de dato &#45; Exportar.](media/across-data-exchange/dataexchangeframework_export.png)  

## Documentos electrónicos

Como alternativa al envío por correo electrónico de documentos de negocios con archivos adjuntos, puede enviarlos y recibirlos de forma electrónica. Un "documento electrónico" es un archivo estándar y compatible que representa un documento empresarial, como una factura de un proveedor que pueda recibirse y convertirse a una factura de compra en [!INCLUDE[prod_short](includes/prod_short.md)]. Los socios comerciales intercambian documentos electrónicos a través de servicios de intercambio de documentos externos. De forma predeterminada, [!INCLUDE[prod_short](includes/prod_short.md)] admite el envío y la recepción de facturas electrónicas y abonos en formato PEPPOL, admitido por los proveedores de servicios de intercambio de documentos más importantes. Hay preconfigurado un proveedor de servicios de intercambio de documentos principal, Tradeshift, listo para ser configurado según su empresa. Para proporcionar compatibilidad para otros formatos de documentos electrónicos, debe crear nuevas definiciones de intercambio de datos.  

Puedes hacer que un servicio de OCR (Reconocimiento óptico de caracteres) externo cree documentos electrónicos desde PDF o desde archivos de imagen que representen documentos entrantes que después puedas convertir a registros de documentos en [!INCLUDE[prod_short](includes/prod_short.md)], como en documentos electrónicos PEPPOL. Por ejemplo, cuando recibes una factura de un proveedor en formato PDF, la puedes enviar al servicio de OCR desde la página **Documentos entrantes**. Al de unos segundos recibirás el archivo devuelto como una factura electrónica que se puede convertir en una factura de compra para el proveedor. Si envías el archivo al servicio de OCR por correo electrónico, se creará un documento entrante nuevo automáticamente cuando recibas el documento electrónico devuelto.  

Para enviar, por ejemplo, una factura de venta como documento electrónico de PEPPOL, seleccione la opción **Documento electrónico** en el cuadro de diálogo **Registrar y enviar**. Desde aquí puede configurar también perfil de envío de documentos predeterminado del cliente. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida. Se utilizan para identificar los socios comerciales y los productos al convertir los datos de los campos de [!INCLUDE[prod_short](includes/prod_short.md)] en elementos en el archivo de documento saliente. La conversión de datos y el envío de las facturas de venta PEPPOL se realizan mediante codeunits dedicadas y objetos XMLport, representados por el formato de documento electrónico **PEPPOL**.  

Para recibir, por ejemplo, una factura de un proveedor como un documento electrónico PEPPOL, debe procesarse el documento en la página **Documentos entrantes** para luego convertirlo en una factura de compra en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede configurar la función de cola de proyectos para procesar estos archivos periódicamente o puede iniciar el proceso manualmente. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los proveedores, los productos y las unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de elementos del archivo de documento entrante en campos de [!INCLUDE[prod_short](includes/prod_short.md)]. La recepción y la conversión de datos de las facturas PEPPOL las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **PEPPOL - Factura**.  

  Para recibir, por ejemplo, una factura como documento electrónico de OCR, se procesa como cuando se recibe un documento electrónico de PEPPOL. La recepción y la conversión de documentos electrónicos de OCR las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **OCR - Factura**.  

## Archivos bancarios

Los formatos de los archivos para intercambiar datos bancarios con aplicaciones de administración de empresas varían en función del proveedor del archivo y del país o la región. [!INCLUDE[prod_short](includes/prod_short.md)] admite la importación y exportación de archivos bancarios de la Zona única de pagos en euros (SEPA). Además, la extensión AMC Banking 365 Fundamentals le permite conectarse a una extensión AMC Banking 365 Fundamentals proporcionada por un proveedor externo, AMC Consult. Para obtener más información, consulte [Hacer pagos con la extensión AMC Banking 365 Fundamentals o Transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.  

Para exportar transferencias de crédito SEPA, se elige el botón **Exportar pagos a archivo** en la página **Diario de pagos** y después se carga el archivo para procesar pagos en el banco. Primero debe configurar distintos datos maestros, como la cuenta bancaria, proveedores y formas de pago. La conversión de datos y la exportación de datos bancarios SEPA se realizan a través de una codeunit y un XMLport dedicados, representados por la configuración de exportación/importación **Transferencia de crédito SEPA**. Alternativamente, puede configurar la extensión AMC Banking 365 Fundamentals para realizar la exportación, representada en la definición de intercambio de datos de la extensión **AMC Banking 365 Fundamentals - Transferencia de crédito**.  

 Para exportar las instrucciones de adeudo directo SEPA, debe elegirse el botón **Exportar archivo de adeudo directo** de la página **Cobros por adeudo directo** y después enviarlo al banco para cobrar automáticamente los pagos al cliente en cuestión. Primero debe configurar cuentas bancarias, clientes, órdenes de adeudo directo y formas de pago. La conversión de datos y la exportación de los datos bancarios SEPA se realizan a través de una codeunit y un XMLport dedicados, representados por la configuración de exportación/importación **Adeudo directo SEPA**.  

 Para importar extractos bancarios SEPA, debe elegir el botón Importar extracto bancario en las páginas **Diario de conciliación de pagos** y **Conciliación banco** y, a continuación, aplicar cada movimiento de extracto bancario a pagos o movimientos de contabilidad bancaria, manual o automáticamente. Primero debe configurar cuentas bancarias. La importación y la conversión de datos bancarios SEPA las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **CAMT de SEPA**. Alternativamente, puede configurar la extensión AMC Banking 365 Fundamentals para realizar la importación, representada en la definición de intercambio de datos de la extensión **AMC Banking 365 Fundamentals - Extracto de cuenta**.  

 Además, las versiones locales de [!INCLUDE[prod_short](includes/prod_short.md)] admiten otros formatos de archivo para importar y exportar datos bancarios, transacciones de nóminas y otros datos. Para obtener más información, consulte la página de aterrizaje [Funcionalidad local](about-localization.md) para su su país o región en la Ayuda.  

## Tipos cambio divisa

Puede configurar un servicio externo para mantener actualizados los tipos de cambio de divisa. El servicio que proporciona tipos de cambio de divisa actualizados se habilita mediante una definición de intercambio de datos. Por consiguiente, la página **Tarjeta de configuración de actualización de tipo de cambio** es una visión condensada de la página **Definición de intercambio de datos** para la definición de intercambio de datos en cuestión.  

Para todos los intercambios de datos en archivos XML, puede preparar la configuración de intercambio de datos cargando el archivo relacionado de esquema XML en la página **Visor de esquema XML**. Aquí se seleccionan los elementos de datos que se desea intercambiar con [!INCLUDE[prod_short](includes/prod_short.md)] y, a continuación, se inicializa una definición de intercambio de datos o se genera un XMLport.

## Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] utiliza el marco de intercambio de datos para informes de Intrastat, donde puede crear fácilmente archivos con marca de tiempo en diferentes formatos para exportar. [!INCLUDE[prod_short](includes/prod_short.md)] contiene formatos preparados para países o regiones localizados, y para la versión predeterminada. Pero puede cambiar el informe original o crear uno propio.

## Consulte también

[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Usar esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
