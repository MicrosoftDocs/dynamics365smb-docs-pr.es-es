---
title: 'Procedimiento: recibir y convertir documentos electrónicos | Documentos de Microsoft'
description: Puede recibir documentos electrónicos directamente desde sus socios colaboradores o desde un servicio de OCR.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fcc8e97a61c777a7857e95db04fe16973c4c7b07
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918818"
---
# <a name="receive-and-convert-electronic-documents"></a>Recibir y convertir documentos electrónicos
La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] admite la recepción de facturas electrónicas y abonos en formato PEPPOL, admitido por los proveedores de servicios de intercambio de documentos más importantes. Para recibir una factura de un proveedor como un documento electrónico PEPPOL, debe procesarse el documento en la página Documentos entrantes para luego convertirlo en una factura de compra o en una línea de diario general en [!INCLUDE[d365fin](includes/d365fin_md.md)].

 Además de recibir documentos electrónicos directamente de los socios comerciales, puede recibir documentos electrónicos de un servicio OCR que haya convertido sus archivos PDF o de imagen en documentos electrónicos.  

 Antes de que pueda recibir documentos electrónicos a través del servicio de intercambio de documentos, debe configurar los distintos datos maestros, como la información de empresa, proveedores, artículos y unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de elementos del archivo de documento entrante en campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md).  

 Antes de que pueda recibir documentos electrónicos a través del servicio OCR, debe configurar y habilitar la conexión de servicio preconfigurada. Para obtener más información, vea [Configurar documentos entrantes](across-how-setup-income-documents.md).  

 El tráfico de documentos electrónicos hacia y desde [!INCLUDE[d365fin](includes/d365fin_md.md)] lo administra la característica Cola proyecto. Antes de que pueda recibir documentos electrónicos, debe iniciarse la cola de proyectos correspondiente.  

 Puede iniciar la conversión de documentos electrónicos manualmente, tal como se describe en este procedimiento, o puede activar un flujo de trabajo para convertir los documentos electrónicos automáticamente cuando se reciban. La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye una plantilla de flujo de trabajo, *Flujo de trabajo desde Documento electrónico entrante hasta Abrir factura de compra*, que está listo para copiarse en un flujo de trabajo y activarse. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

> [!NOTE]  
>  Cuando conviertes documentos electrónicos recibidos del servicio de OCR o de líneas del diario de [!INCLUDE[d365fin](includes/d365fin_md.md)], se suman varias líneas en el documento de origen en una línea. La línea única será del tipo Cuenta del libro mayor y los campos de **Descripción** y **Número** (de cuenta del libro mayor) estarán vacíos. El valor del campo **Importe** se igualará al importe total (IVA excluído) de todas las líneas del documento de origen.  
>   
>  Para asegurarse de que los campos **Descripción** y **N.º** se rellenan, puede elegir el botón **Asignar texto a cuenta** en la página **Documentos entrantes** para definir que un determinado texto de factura se asigne siempre a una cuenta Debe o Haber determinada en la contabilidad. En adelante, el campo **Descripción** del documento o de las líneas de diario creados a partir de un documento electrónico para el proveedor o cliente en concreto se rellenarán con el texto en cuestión y el campo **N.º** (cuenta libro mayor) con la cuenta en cuestión.  
>   
>  En lugar de asignar a una cuenta, también se puede asignar a una cuenta bancaria. Esto resulta práctico, por ejemplo, en los documentos electrónicos para los gastos que ya se han pagado, donde desea crear una línea de diario general que esté lista para registrarse en una cuenta bancaria.  

 El procedimiento siguiente describe cómo recibir una factura de proveedor y convertirla en una factura de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El procedimiento es el mismo cuando se convierte una factura de proveedor en una línea de diario general.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Para recibir y convertir una factura electrónica en una factura de compra  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Documentos entrantes** y luego elija el enlace relacionado.  

2.  Seleccione la línea del registro del documento entrante que representa una factura electrónica entrante nueva y, a continuación, elija la acción **Editar**.  

     En la página **Ficha de documento entrante**, está adjunto el archivo XML relacionado, y la mayor parte de los campos se prellenan con la información de la factura electrónica. Para obtener más información, vea [Crear registros de documentos entrantes](across-how-create-income-document-records.md).  

3.  En el campo **Tipo de intercambio de datos**, seleccione **PEPPOL - Factura** o **OCR - Factura** según el origen del documento electrónico.  

4.  Para asignar el texto de la factura de proveedor a una cuenta Debe específica, en la pestaña **Acciones**, en el grupo **General**, seleccione **Asignar texto a cuenta** y, a continuación rellene la página **Hoja asignación de texto a cuenta**.  

5.  Seleccione la acción **Crear documento**.  

     Se creará una factura de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)] basándose en la información del documento electrónico.  

     Los errores de validación, normalmente relacionados con datos maestros incorrectos o no presentes en [!INCLUDE[d365fin](includes/d365fin_md.md)], se mostrarán en la ficha desplegable **Mensajes de error**.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también  
[Administrar pagos](payables-manage-payables.md)  
[Documentos entrantes](across-income-documents.md)  
[Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)   
[Funciones empresariales generales](ui-across-business-areas.md)  
