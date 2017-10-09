---
title: "Documentos electrónicos en Dynamics 365 for Financials | Documentos de Microsoft"
description: "Introducción al envío y recepción de documentos electrónicos en [!INCLUDE[d365fin](includes/d365fin_md.md)]."
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
ms.openlocfilehash: 0c0ca1b5da823d31bba4961e8724dfb98e842317
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
## <a name="exchanging-data-as-electronic-documents"></a>Intercambio de datos como documentos electrónicos  
Como alternativa al envío de correos electrónicos con archivos adjuntos, puede enviar y recibir documentos de forma electrónica. Por documento electrónico se entiende un archivo estándar y compatible que representa un documento empresarial, como una factura de un proveedor que pueda recibirse y convertirse a una factura de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El intercambio de los documentos electrónicos entre dos socios comerciales se realiza a través de un proveedor externo de servicios de intercambio de datos. La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] admite el envío y la recepción de facturas electrónicas y abonos en formato PEPPOL, admitido por los proveedores de servicios de intercambio de documentos más importantes. Hay preconfigurado un proveedor de servicios de intercambio de documentos principal listo para ser configurado según su empresa. Para proporcionar compatibilidad para otros formatos de documentos electrónicos, debe crear nuevas definiciones de intercambio de datos utilizando el marco de intercambio de datos.  

Puedes hacer que un servicio de OCR (Reconocimiento óptico de caracteres) externo cree documentos electrónicos desde PDF o desde archivos de imagen que representen documentos entrantes que después puedas convertir a registros de documentos en [!INCLUDE[d365fin](includes/d365fin_md.md)], como en documentos electrónicos PEPPOL. Por ejemplo, cuando recibes una factura de un proveedor en formato PDF, la puedes enviar al servicio de OCR desde la ventana **Documentos entrantes**. Al de unos segundos recibirás el archivo devuelto como una factura electrónica que se puede convertir en una factura de compra para el proveedor. Si envías el archivo al servicio de OCR por correo electrónico, se creará un documento entrante nuevo automáticamente cuando recibas el documento electrónico devuelto.  

Para enviar, por ejemplo, una factura de venta como documento electrónico de PEPPOL, seleccione la opción **Documento electrónico** en el cuadro de diálogo **Registrar y enviar**. Desde aquí puede configurar también perfil de envío de documentos predeterminado del cliente. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida. Se utilizan para identificar los socios comerciales y los productos al convertir los datos de los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en elementos en el archivo de documento saliente. La conversión de datos y el envío de las facturas de venta PEPPOL se realizan mediante unidades de código dedicadas y objetos XMLport, representados por el formato de documento electrónico **PEPPOL**.  

Para recibir, por ejemplo, una factura de un proveedor como un documento electrónico PEPPOL, debe procesarse el documento en la ventana **Documentos entrantes** para luego convertirlo en una factura de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede configurar la función de cola de proyectos para procesar estos archivos periódicamente o puede iniciar el proceso manualmente. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los proveedores, los productos y las unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de elementos del archivo de documento entrante en campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. La recepción y la conversión de datos de las facturas PEPPOL las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **PEPPOL - Factura**.  

 Para recibir, por ejemplo, una factura como documento electrónico de OCR, se procesa como cuando se recibe un documento electrónico de PEPPOL. La recepción y la conversión de documentos electrónicos de OCR las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **OCR - Factura**.  

## <a name="bank-files"></a>Archivos bancarios  
 Los formatos de los archivos para el intercambio de datos bancarios con sistemas ERP varían en función del proveedor del archivo y del país o la región. La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] permite importar y exportar archivos bancarios SEPA (zona única de pagos en euros) y un servicio de conversión de datos bancarios facilitado por el proveedor externo, AMC Consult. Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.  

Para exportar transferencias de crédito SEPA, se elige el botón **Exportar pagos a archivo** en la ventana **Diario de pagos** y después se carga el archivo para procesar pagos en el banco. Primero debe configurar distintos datos maestros, como la cuenta bancaria, proveedores y formas de pago. La conversión de datos y la exportación de datos bancarios SEPA se realizan a través de una unidad de código y un XMLport dedicados, representados por la configuración de exportación/importación **Transferencia de crédito SEPA**. Alternativamente, puede configurar el servicio de conversión de datos bancarios para realizar la exportación, representada en la definición de intercambio de datos **Servicio de conversión de datos bancarios - Transferencia de crédito**.  

Para exportar las instrucciones de adeudo directo SEPA, debe elegirse el botón **Exportar archivo de adeudo directo** de la ventana **Cobros por adeudo directo** y después enviarlo al banco para cobrar automáticamente los pagos al cliente en cuestión. Primero debe configurar cuentas bancarias, clientes, órdenes de adeudo directo y formas de pago. La conversión de datos y la exportación de los datos bancarios SEPA se realizan a través de una unidad de código y un XMLport dedicados, representados por la configuración de exportación/importación **Adeudo directo SEPA**.  

Para importar extractos bancarios SEPA, debe elegir el botón Importar extracto bancario en las ventanas **Diario de conciliación de pagos** y **Conciliación banco** y, a continuación, aplicar cada movimiento de extracto bancario a pagos o movimientos de contabilidad bancaria, manual o automáticamente. Primero debe configurar cuentas bancarias. La importación y la conversión de datos bancarios SEPA las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **CAMT de SEPA**. Alternativamente, puede configurar el servicio de conversión de datos bancarios para realizar la importación, representada en la definición de intercambio de datos **Servicio de conversión de datos bancarios - Extracto banco**.  

 Además, las versiones locales de [!INCLUDE[d365fin](includes/d365fin_md.md)] admiten otros formatos de archivo para importar y exportar datos bancarios, transacciones de nóminas y otros datos. Para obtener más información, consulte la sección de ayuda sobre funcionalidad local en la versión de [!INCLUDE[d365fin](includes/d365fin_md.md)] para su país.  

## <a name="currency-exchange-rates"></a>Tipos cambio divisa  
Puede configurar un servicio externo para mantener actualizados los tipos de cambio de divisa. El servicio que proporciona tipos de cambio de divisa actualizados se habilita mediante una definición de intercambio de datos. Por consiguiente, la ventana **Tarjeta de configuración de actualización de tipo de cambio** es una visión condensada de la ventana **Definición de intercambio de datos** para la definición de intercambio de datos en cuestión.  

Para todos los intercambios de datos en archivos XML, puede preparar la configuración de intercambio de datos cargando el archivo relacionado de esquema XML en la ventana **Visor de esquema XML**. Aquí se seleccionan los elementos de datos que se desea intercambiar con [!INCLUDE[d365fin](includes/d365fin_md.md)] y, a continuación, se inicializa una definición de intercambio de datos o se genera un XMLport.  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|Para|Vea|  
|--------|---------|  
|Conocer el funcionamiento del marco de intercambio de datos.|[Acerca del marco de intercambio de datos](across-about-the-data-exchange-framework.md)|  
|Preparar el intercambio de datos en un archivo reutilizando el esquema XML del archivo. Configurar definiciones de intercambio de datos. Configurar datos maestros para enviar documentos electrónicos. Configurar diversos campos de importación y exportación bancaria.|[Configuración del intercambio de datos](across-set-up-data-exchange.md)|  
|Basándose en las definiciones de intercambio de datos, enviar facturas PEPPOL, recibir facturas PEPPOL, importar extractos bancarios y exportar archivos de pago por banco.|[Intercambio de datos](across-exchange-data.md)|  

## <a name="see-also"></a>Consulte también  
[Acerca del marco de intercambio de datos](across-about-the-data-exchange-framework.md)  
[Procedimiento: Uso de esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos](across-exchange-data.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

