---
title: Acerca del marco de intercambio de datos | Documentos de Microsoft
description: El formato de archivos para intercambio de datos en archivos bancarios, documentos electrónicos, tipos de cambio de divisa y otros con los sistemas ERP varía en función del proveedor del archivo de datos o de secuencia y el país o la región.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fc01b4a0d04cf21ae2ede3a3a98aa928446fa4d1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385004"
---
# <a name="about-the-data-exchange-framework"></a>Acerca del marco de intercambio de datos

Puede usar Marco de intercambio de datos para gestionar documentos empresariales, archivos bancarios, tipos de cambio de divisa y cualquier otro archivo de datos con sus socios comerciales.

Como administrador o socio de Microsoft, puede usar el marco en nuevas funciones de integración configurando qué datos intercambiar y cómo. Por ejemplo, el formato de archivos para intercambio de datos en archivos bancarios, documentos electrónicos, tipos de cambio de divisa y otros con los sistemas ERP varía en función del proveedor del archivo de datos o de secuencia y el país o la región. [!INCLUDE[prod_short](includes/prod_short.md)] utiliza varios formatos de archivo bancario y estándares de servicio de datos. Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.

 En los diagramas siguientes se muestra la arquitectura del marco de intercambio de datos.  

 ![&#45; Importación de marco de intercambio de datos](media/across-data-exchange/dataexchangeframework_import.png)  

 ![&#45; Exportación de marco de intercambio de datos](media/across-data-exchange/dataexchangeframework_export.png)  

## <a name="electronic-documents"></a>Documentos electrónicos

Como alternativa al envío de correos electrónicos con archivos adjuntos, puedes enviar y recibir documentos empresariales de forma electrónica. Por documento electrónico se entiende un archivo estándar y compatible que representa un documento empresarial, como una factura de un proveedor que pueda recibirse y convertirse a una factura de compra en [!INCLUDE[prod_short](includes/prod_short.md)]. El intercambio de los documentos electrónicos entre dos socios comerciales se realiza a través de un proveedor externo de servicios de intercambio de datos. La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] admite el envío y la recepción de facturas electrónicas y abonos en formato PEPPOL, admitido por los proveedores de servicios de intercambio de documentos más importantes. Hay preconfigurado un proveedor de servicios de intercambio de documentos principal listo para ser configurado según su empresa. Para proporcionar compatibilidad para otros formatos de documentos electrónicos, debe crear nuevas definiciones de intercambio de datos utilizando el marco de intercambio de datos.  

 Puedes hacer que un servicio de OCR (Reconocimiento óptico de caracteres) externo cree documentos electrónicos desde PDF o desde archivos de imagen que representen documentos entrantes que después puedas convertir a registros de documentos en [!INCLUDE[prod_short](includes/prod_short.md)], como en documentos electrónicos PEPPOL. Por ejemplo, cuando recibes una factura de un proveedor en formato PDF, la puedes enviar al servicio de OCR desde la página **Documentos entrantes**. Al de unos segundos recibirás el archivo devuelto como una factura electrónica que se puede convertir en una factura de compra para el proveedor. Si envías el archivo al servicio de OCR por correo electrónico, se creará un documento entrante nuevo automáticamente cuando recibas el documento electrónico devuelto.  

 Para enviar, por ejemplo, una factura de venta como documento electrónico de PEPPOL, seleccione la opción **Documento electrónico** en el cuadro de diálogo **Registrar y enviar**. Desde aquí puede configurar también perfil de envío de documentos predeterminado del cliente. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida. Se utilizan para identificar los socios comerciales y los productos al convertir los datos de los campos de [!INCLUDE[prod_short](includes/prod_short.md)] en elementos en el archivo de documento saliente. La conversión de datos y el envío de las facturas de venta PEPPOL se realizan mediante codeunits dedicadas y objetos XMLport, representados por el formato de documento electrónico **PEPPOL**.  

 Para recibir, por ejemplo, una factura de un proveedor como un documento electrónico PEPPOL, debe procesarse el documento en la página **Documentos entrantes** para luego convertirlo en una factura de compra en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede configurar la función de cola de proyectos para procesar estos archivos periódicamente o puede iniciar el proceso manualmente. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los proveedores, los productos y las unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de elementos del archivo de documento entrante en campos de [!INCLUDE[prod_short](includes/prod_short.md)]. La recepción y la conversión de datos de las facturas PEPPOL las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **PEPPOL - Factura**.  

  Para recibir, por ejemplo, una factura como documento electrónico de OCR, se procesa como cuando se recibe un documento electrónico de PEPPOL. La recepción y la conversión de documentos electrónicos de OCR las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **OCR - Factura**.  

## <a name="bank-files"></a>Archivos bancarios

Los formatos de los archivos para intercambiar datos bancarios con sistemas ERP varían en función del proveedor del archivo y del país o la región. [!INCLUDE[prod_short](includes/prod_short.md)] permite importar y exportar archivos bancarios SEPA (zona única de pagos en euros) y la extensión AMC Banking 365 Fundamentals le permite conectar una extensión AMC Banking 365 Fundamentals facilitada por el proveedor externo, AMC Consult. Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.  

Para exportar transferencias de crédito SEPA, se elige el botón **Exportar pagos a archivo** en la página **Diario de pagos** y después se carga el archivo para procesar pagos en el banco. Primero debe configurar distintos datos maestros, como la cuenta bancaria, proveedores y formas de pago. La conversión de datos y la exportación de datos bancarios SEPA se realizan a través de una codeunit y un XMLport dedicados, representados por la configuración de exportación/importación **Transferencia de crédito SEPA**. Alternativamente, puede configurar la extensión AMC Banking 365 Fundamentals para realizar la exportación, representada en la definición de intercambio de datos de la extensión **AMC Banking 365 Fundamentals - Transferencia de crédito**.  

 Para exportar las instrucciones de adeudo directo SEPA, debe elegirse el botón **Exportar archivo de adeudo directo** de la página **Cobros por adeudo directo** y después enviarlo al banco para cobrar automáticamente los pagos al cliente en cuestión. Primero debe configurar cuentas bancarias, clientes, órdenes de adeudo directo y formas de pago. La conversión de datos y la exportación de los datos bancarios SEPA se realizan a través de una codeunit y un XMLport dedicados, representados por la configuración de exportación/importación **Adeudo directo SEPA**.  

 Para importar extractos bancarios SEPA, debe elegir el botón Importar extracto bancario en las páginas **Diario de conciliación de pagos** y **Conciliación banco** y, a continuación, aplicar cada movimiento de extracto bancario a pagos o movimientos de contabilidad bancaria, manual o automáticamente. Primero debe configurar cuentas bancarias. La importación y la conversión de datos bancarios SEPA las realiza el marco de intercambio de datos, representado por la definición de intercambio de datos **CAMT de SEPA**. Alternativamente, puede configurar la extensión AMC Banking 365 Fundamentals para realizar la importación, representada en la definición de intercambio de datos de la extensión **AMC Banking 365 Fundamentals - Extracto de cuenta**.  

 Además, las versiones locales de [!INCLUDE[prod_short](includes/prod_short.md)] admiten otros formatos de archivo para importar y exportar datos bancarios, transacciones de nóminas y otros datos. Para obtener más información, consulte la página de aterrizaje [Funcionalidad local](about-localization.md) para su su país o región en la Ayuda.  

## <a name="currency-exchange-rates"></a>Tipos cambio divisa

Puede configurar un servicio externo para mantener actualizados los tipos de cambio de divisa. El servicio que proporciona tipos de cambio de divisa actualizados se habilita mediante una definición de intercambio de datos. Por consiguiente, la página **Tarjeta de configuración de actualización de tipo de cambio** es una visión condensada de la página **Definición de intercambio de datos** para la definición de intercambio de datos en cuestión.  

Para todos los intercambios de datos en archivos XML, puede preparar la configuración de intercambio de datos cargando el archivo relacionado de esquema XML en la página **Visor de esquema XML**. Aquí se seleccionan los elementos de datos que se desea intercambiar con [!INCLUDE[prod_short](includes/prod_short.md)] y, a continuación, se inicializa una definición de intercambio de datos o se genera un XMLport.

## <a name="see-also"></a>Consulte también

[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Uso de esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]