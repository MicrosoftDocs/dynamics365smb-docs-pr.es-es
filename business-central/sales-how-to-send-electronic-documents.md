---
title: "Enviar documentos electrónicos | Documentos de Microsoft"
description: "Aprenda a enviar facturas electrónicamente."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: eac3422bade7b77ee0847d6a0f47fbcb4d41988a
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="send-electronic-documents"></a>Enviar documentos electrónicos
La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] admite el envío de facturas electrónicas y abonos en formato PEPPOL, admitido por los proveedores de servicios de intercambio de documentos más importantes. El proveedor de servicios de intercambio de documentos entrega documentos electrónicos de un socio comercial a otro. Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.  

 En la versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)], hay preconfigurado un servicio de intercambio de documentos listo para ser configurado según su empresa. Para obtener más información, vea [Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md).  

 Para enviar una factura de venta como un documento electrónico PEPPOL, seleccione la opción **Documento electrónico** en el cuadro de diálogo **Registrar y enviar** donde también puede configurarlo como el perfil de envío de documentos predeterminado del cliente. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de los campos de [Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)  

### <a name="to-send-an-electronic-sales-invoice"></a>Para enviar una factura de venta electrónica  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas venta** y, a continuación, seleccione el vínculo relacionado.  

2.  Cree una nueva factura de venta.  

3.  Cuando la factura de venta esté lista para facturarse, en la pestaña **Acciones**, en el grupo **Registro**, seleccione **Registrar y enviar**.  

     Si el perfil de envío predeterminado del cliente es **Documento electrónico**, se mostrará en el cuadro de diálogo **Registrar y enviar la confirmación** y solo tiene que elegir el botón **Sí** para registrar y enviar la factura electrónicamente en el formato seleccionado.  

4.  En el cuadro de diálogo **Registrar y enviar la confirmación**, seleccione el botón AssistEdit situado a la derecha del campo **Enviar documento a**.  

5.  En el cuadro de diálogo **Enviar documento a**, en el campo **Documento electrónico**, seleccione **A través del servicio de intercambio de documentos**.  

6.  En el campo **Formato**, seleccione **PEPPOL**.  

7.  Elija el botón **Aceptar**. Aparece el cuadro de diálogo **Registrar y enviar la confirmación**. **Documento electrónico (PEPPOL)** se agrega al campo **Enviar documento a**.  

8.  Elija el botón **Sí**.  

     Se registra la factura de venta y se envía al cliente como un documento electrónico en el formato PEPPOL.  

    > [!NOTE]  
    >  También puede enviar una factura de venta registrada como documento electrónico. El procedimiento es el mismo que el descrito en este tema para documentos de venta no registrada. En la ventana **Factura venta reg.**, en la pestaña **Acciones**, en el grupo **General**, seleccione **Registro de actividades** para ver el estado del documento electrónico. Para obtener más información, vea **Registro de actividades**.  

## <a name="see-also"></a>Consulte también  
[Facturar ventas](sales-how-invoice-sales.md)  
[Configurar perfiles de envío de documentos](sales-how-setup-document-send-profiles.md)  
[Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md)  
[Configurar definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

