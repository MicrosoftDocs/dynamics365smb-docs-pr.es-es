---
title: Configurar el intercambio de datos | Documentos de Microsoft
description: Configurar el marco de intercambio de datos en Dynamics 365 Business edition.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 593904835c55d4ce9b137d0af387ea897603795f
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-data-exchange"></a>Configuración del intercambio de datos
Para poder enviar y recibir documentos electrónicos o importar y exportar archivos de banco, debe configurar el marco de intercambio de datos para procesar los archivos correspondientes. Además, debe configurar áreas relacionadas, como los datos maestros de los clientes a los que envía facturas electrónicas o el servicio de conversión de datos bancarios en caso de usar el proveedor de servicios externo para convertir los archivos bancarios. Para obtener más información, vea [Intercambio de datos electrónicamente](across-data-exchange.md).  

 Cuando [!INCLUDE[d365fin](includes/d365fin_md.md)] se ha configurado para intercambiar datos con archivos externos, los usuarios pueden utilizar la configuración en tareas de negocio comunes, como enviar y recibir documentos electrónicos e importar y exportar archivos de banco.  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Configure el servicio de intercambio de documentos preconfigurado para permitir enviar y recibir documentos electrónicos a y desde [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Procedimiento: Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md)|  
|Configure el servicio de OCR preconfigurado para convertir documentos PDF o archivos de imagen a documentos electrónicos que se pueden convertir a registros de documento en [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Configurar documentos entrantes](across-how-setup-income-documents.md)|  
|Configure dos servicios preconfigurados para tipos de cambio actualizados para obtener los últimos tipos de cambio en la ventana **Divisa**.|[Actualizar los tipos de cambio de divisa](finance-how-update-currencies.md)|  
|Configure los distintos datos maestros, como la información de la empresa, los clientes, los proveedores, los productos y las unidades de medida relacionadas con la asignación de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Procedimiento: Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Configure un banco, un proveedor y un diario de pagos para la transferencia de crédito de SEPA.|[Configuración de transferencias de crédito SEPA](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Prepare los formatos de banco, las formas de pago y los acuerdos de cliente para el adeudo directo SEPA.|[Configuración de domiciliaciones de adeudo directo SEPA](finance-how-to-set-up-sepa-direct-debit.md)|  
|Configure la autenticación de usuario y la URL del proveedor de servicios de conversión de datos de banco que se requiere para que los archivos de banco se conviertan al formato de su banco.|[Procedimiento: Configuración del servicio de conversión de datos bancarios](bank-how-setup-bank-data-conversion-service.md)|  
|Configure y habilite un servicio externo que permita importar extractos bancarios directamente como fuentes de banco.|[Configurar el servicio de declaración bancaria](bank-how-setup-bank-statement-service.md)|  
|Una vez que el servicio de extractos bancarios esté activado, vincule las cuentas a [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Configurar cuentas bancarias](bank-how-setup-bank-accounts.md)|  
|Prepárese para configurar una definición de intercambio de datos nueva de un determinado archivo o flujo de datos usando el esquema XML del archivo para rellenar previamente la ficha desplegable **Definiciones de columna** en la ventana **Definiciones de intercambio de registro**.|[Procedimiento: Uso de esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Configure el marco de intercambio de datos para que los usuarios puedan recibir un formato de documento de compra nuevo, enviar un formato de documento de venta nuevo, importar un archivo bancario nuevo u otro intercambio de datos.|[Procedimiento: Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Consulte también  
[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Intercambio de datos](across-exchange-data.md)   
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

