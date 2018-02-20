---
title: "Procedimiento: Configurar el envío y la recepción de documentos electrónicos | Documentos de Microsoft"
description: "Como alternativa al envío de correos electrónicos con archivos adjuntos, puedes enviar y recibir documentos empresariales de forma electrónica."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f597ce7dc0d4cda526da00d9aac5b1178c5e7a14
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-electronic-document-sending-and-receiving"></a>Configurar el envío y la recepción de documentos electrónicos
Como alternativa al envío de correos electrónicos con archivos adjuntos, puedes enviar y recibir documentos empresariales de forma electrónica. Se entiende por documento electrónico un archivo compatible con el estándar que representa un documento empresarial, como una factura de un proveedor que se puede recibir y convertir en una factura de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El intercambio de los documentos electrónicos entre dos socios comerciales se realiza a través de un proveedor externo de servicios de intercambio de datos. La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] admite el envío y la recepción de facturas electrónicas y abonos en formato PEPPOL, admitido por los proveedores de servicios de intercambio de documentos más importantes. Hay preconfigurado un proveedor de servicios de intercambio de documentos principal listo para ser configurado según su empresa.  

Puedes hacer que un servicio de OCR (Reconocimiento óptico de caracteres) externo cree documentos electrónicos desde PDF o desde archivos de imagen que representen documentos entrantes que después puedas convertir a registros de documentos en [!INCLUDE[d365fin](includes/d365fin_md.md)], como en documentos electrónicos PEPPOL. Por ejemplo, cuando recibes una factura de un proveedor en formato PDF, la puedes enviar al servicio de OCR desde la ventana **Documentos entrantes**. Al de unos segundos recibirás el archivo devuelto como una factura electrónica que se puede convertir en una factura de compra para el proveedor. Si envías el archivo al servicio de OCR por correo electrónico, se creará un documento entrante nuevo automáticamente cuando recibas el documento electrónico devuelto.  

El formato de documento electrónico **PEPPOL** se ha preconfigurado para permitirle enviar facturas y abonos electrónicos en formato PEPPOL. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en elementos en el archivo de documento saliente. Por último, debe seleccionar el formato en la ventana **Formato documento electrónico** para cada cliente al que enviará documentos electrónicos PEPPOL. Para obtener más información, vea [Enviar documentos electrónicos](sales-how-to-send-electronic-documents.md).  

Las definiciones de intercambio de datos **PEPPOL - Factura** y **PEPPOL - Abono** se han preconfigurado para permitirle recibir facturas electrónicas y abonos en formato PEPPOL. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los proveedores, los productos y las unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de elementos del archivo de documento entrante en campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por último, debe seleccionar la definición de intercambio de datos en la ventana **Documentos entrantes** para cada documento electrónico entrante que desee convertir a un documento de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

La definición de intercambio de datos **OCR - Factura** está preconfigurada para permitirle recibir documentos electrónicos generados por el servicio de OCR. Para recibir, por ejemplo, una factura como documento electrónico de OCR, configure una fecha maestra y después procese el documento como si recibiera un documento electrónico de PEPPOL. Para obtener más información, vea [Usar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md).  

Los servicios preconfigurados para intercambio de documentos y OCR se deben activar antes de enviar o recibir. Para obtener más información, vea [Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md).  

El tema incluye los siguientes procedimientos:  

* Para configurar la empresa para el envío y la recepción de documentos electrónicos  
* Para configurar el registro de IVA para el envío y la recepción de documentos electrónicos  
* Para configurar países o regiones para el envío y la recepción de documentos electrónicos  
* Para configurar productos para el envío y la recepción de documentos electrónicos  
* Para configurar unidades de medida para el envío y la recepción de documentos electrónicos  
* Para configurar clientes para enviar documentos electrónicos  
* Para seleccionar el formato de documento electrónico **PEPPOL** para enviar documentos electrónicos  
* Para configurar proveedores para recibir documentos electrónicos  
* Para seleccionar la definición de intercambio de datos **PEPPOL - Factura** para recibir documentos electrónicos  
* Para configurar la cuenta que utilizar en las líneas de la nueva factura de compra para productos y no productos no identificables  

### <a name="to-set-up-the-company-for-electronic-document-sending-and-receiving"></a>Para configurar la empresa para el envío y la recepción de documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Información de la empresa** y, a continuación, elija el vínculo relacionado.  
2. En la ficha desplegable **General**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifique a su empresa.<br /><br /> Por ejemplo, al enviar facturas electrónicas en formato PEPPOL, el valor de este campo se utiliza para rellenar el elemento **EndPointID** bajo el nodo **AccountingSupplierParty** en el archivo. El número se basa en el GS1 estándar, que es compatible con ISO 6523.|  
    |**CIF/NIF**|Especifique el CIF/NIF de la empresa.|  
    |**Centro responsabilidad**|Si la empresa se ha configurado con un centro de responsabilidad, asegúrese de que el campo **Código país/región** se haya rellenado.|  

### <a name="to-set-up-vat-posting-for-electronic-document-sending-and-receiving"></a>Para configurar el registro de IVA para el envío y la recepción de documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Configuración registro de IVA** y, a continuación, elija el vínculo relacionado.  
2. Para cada línea de configuración de registro de IVA que utilizará para los documentos electrónicos, rellene el campo tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Categoría de impuesto**|Especifique la categoría de IVA.<br /><br /> Por ejemplo, al enviar facturas electrónicas en formato PEPPOL, el valor de este campo se utiliza para rellenar el elemento **TaxApplied** bajo el nodo **AccountingSupplierParty** en el archivo. El número se basa en el UNCL5305 estándar.|  

### <a name="to-set-up-countriesregions-for-electronic-document-sending-and-receiving"></a>Para configurar países o regiones para el envío y la recepción de documentos electrónicos  
1. En el cuadro **Buscar**, escriba **País/Regiones** y, a continuación, elija el vínculo relacionado.  
2. Para cada país/región que utilizará para intercambiar documentos electrónicos, rellene el campo tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Esquema de IVA**|Identifica al organismo nacional que emite el CIF\/NIF en el país o la región en relación con el envío de documentos electrónicos.<br /><br /> Por ejemplo, al enviar facturas electrónicas en formato PEPPOL, el valor de este campo se utiliza para rellenar el atributo **SchemeID** para el elemento **EndPointID** bajo el nodo **AccountingSupplierParty** y el nodo **AccountingCustomerParty** en el archivo.<br /><br /> El campo **Esquema de IVA** solo se utiliza si el campo **GLN** en la ventana **Información empresa** no se rellena. **Nota**: El valor del campo **Código** en la ventana **Países\/Regiones** debe cumplir con 3166\-1 ISO: Alpha2.|  

### <a name="to-set-up-items-for-electronic-document-sending-and-receiving"></a>Para configurar productos para el envío y la recepción de documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Productos** y, a continuación, elija el vínculo relacionado.  
2. Para cada producto que compre o venda en documentos electrónicos, rellene el campo tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Identifica el producto en conexión con el envío y recepción de documentos electrónicos. Para el formato PEPPOL se utiliza el campo de la siguiente forma:<br /><br /> Si el elemento **StandardItemIdentification\/ID** tiene el atributo **SchemeID** establecido en **GTIN**, el elemento se asigna al campo **GTIN** en la ficha de producto.|  

### <a name="to-set-up-units-of-measure-for-electronic-document-sending-and-receiving"></a>Para configurar unidades de medida para el envío y la recepción de documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Unidades de medida** y, a continuación, elija el vínculo relacionado.  
2. Para cada unidad de medida que utilizará para productos en documentos electrónicos, rellene el campo tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Código estándar internacional**|Especifique el código de unidad de medida expresado como el estándar UNECERec20 en relación con el envío de documentos electrónicos.<br /><br /> Por ejemplo, al enviar facturas electrónicas en formato PEPPOL, el valor de este campo se utiliza para rellenar el atributo **unitCode** del elemento **InvoicedQuantity** bajo el nodo **InvoiceLine**. **Nota**: Si el campo **Unidad de medida** de la línea de venta está vacío, el valor estándar UNECERe20 para “Unidad” \(H87\) se inserta de manera predeterminada. Para obtener más información y una lista de códigos de unidad de medida válidos, vea [Recomendación n.º 20 \- Unidades de medida utilizadas en comercio internacional](http://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### <a name="to-set-up-customers-for-electronic-document-sending"></a>Para configurar clientes para enviar documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Clientes**, y a continuación, elija el vínculo relacionado.  
2. Para cada cliente al que enviará documentos electrónicos, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifique al cliente.<br /><br /> Por ejemplo, al enviar facturas electrónicas en formato PEPPOL, el valor de este campo se utiliza para rellenar el elemento **EndPointID** bajo el nodo **AccountingCustomerParty** en el archivo. El número se basa en el GS1 estándar, que es compatible con ISO 6523.<br /><br /> Si el campo **GLN** está vacío, se usa el valor en el campo **CIF/NIF**.|  
    |**CIF/NIF**|Especifique el número CIF/NIF del cliente. **Sugerencia**: Seleccione el botón Análisis para utilizar el servicio web que comprueba si el número existe en el registro de empresas del país.|  
    |**Centro responsabilidad**|Si el cliente se ha configurado con un centro de responsabilidad, asegúrese de que el campo **Código país/región** se haya rellenado.|  

    Puede configurar cada cliente con un método preferido de enviar los documentos empresariales, para que no tenga que seleccionar una opción de envío cada vez que deba enviar un documento al cliente. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  

### <a name="to-select-the-peppol-electronic-document-format-for-electronic-document-sending"></a>Para seleccionar el formato de documento electrónico PEPPOL para enviar documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Perfiles de envío de documentos** y, a continuación, elija el vínculo relacionado.  
2. Abra un perfil de envío de documentos existente o cree uno nuevo. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  
3. En la ventana **Perfil de envío de documentos**, elija **Formato electrónico**, seleccione la línea de PEPPOL y, a continuación, elija **Aceptar**.  
4. En el campo **Documento electrónico**, seleccione **Sí (A través del servicio de intercambio de documentos)**.  

    > [!NOTE]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)]  detecta automáticamente si el documento es una factura o un abono y aplica el formato PEPPOL según corresponda.  

5. Para aplicar este perfil de envío de documentos a todos los clientes, seleccione la casilla **Por defecto** en la ficha desplegable **General**. Para aplicarlo solo a clientes específicos, rellene el campo **Perfil de envío de documentos** en las fichas cliente en cuestión. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  

    Ahora puede enviar datos convertidos dentro del documento electrónico. Para obtener más información, vea [Enviar documentos electrónicos](sales-how-to-send-electronic-documents.md).  

### <a name="to-set-up-vendors-for-electronic-document-receiving"></a>Para configurar proveedores para recibir documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Proveedores** y, a continuación, elija el vínculo relacionado.  
2. Para cada proveedor desde el que recibirá documentos electrónicos, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifique al proveedor.<br /><br /> Por ejemplo, al recibir facturas electrónicas en formato PEPPOL, el valor de este campo se utiliza para rellenar el elemento **EndPointID** bajo el nodo **AccountingSupplierParty** en el archivo. El número se basa en el GS1 estándar, que es compatible con ISO 6523.<br /><br /> Si el campo **GLN** está vacío, se usa el valor en el campo **CIF/NIF**.|  
    |**CIF/NIF**|Especifique el número CIF/NIF del proveedor. **Sugerencia**: Seleccione el botón Análisis para utilizar el servicio web que comprueba si el número existe en el registro de empresas del país.|  
    |**Centro responsabilidad**|Si el proveedor se ha configurado con un centro de responsabilidad, asegúrese de que el campo **Código país/región** se haya rellenado.|  

### <a name="to-select-the-peppol---invoice-data-exchange-definition-for-electronic-document-receiving"></a>Para seleccionar la definición de intercambio de datos PEPPOL - Factura para recibir documentos electrónicos  
1. En el cuadro **Buscar**, escriba **Documentos entrantes** y, a continuación, elija el vínculo relacionado.  
2. En la línea del documento electrónico que desea recibir y convertir, elija el campo **Tipo de intercambio de datos** y seleccione **PEPPOLINVOICE**.  

     Si el documento que recibir es un abono, seleccione **PEPPOLCREDITMEMO**.  

    Ahora puede recibir el documento electrónico iniciando el proceso de conversión de datos en la ventana **Documentos entrantes**. Para obtener más información, consulte [Recibir y convertir documentos electrónicos](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### <a name="to-set-up-the-gl-account-to-use-on-new-purchase-invoice-lines-for-non-identifiable-items-and-non-items"></a>Para configurar la cuenta que utilizar en las líneas de la nueva factura de compra para productos y no productos no identificables  
1. En el cuadro **Buscar**, escriba **Compras y pagos** y, a continuación, elija el vínculo relacionado.  
2. En la ficha desplegable **Intercambio de datos**, rellene el campo tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Cuenta para líneas que no son artículos físicos**|Especifica la cuenta que se inserta automáticamente en las líneas de compra creadas a partir de los documentos electrónicos cuando la línea de documento entrante no contiene un producto identificable. Cualquier línea del documento entrante que no tenga un GTIN o el número de producto del proveedor se convierte en una línea de compra de tipo **Cuenta**, y el campo **Nº** de la línea de compra contendrá la cuenta seleccionada en el campo **Cuenta para líneas que no son artículos físicos**.<br /><br /> Si dejas el campo **Cuenta para líneas que no son artículos físicos** en blanco y el documento entrante contiene líneas sin artículos identificables, no se creará el documento de compra. Entonces, aparecerá un mensaje de error que te indicará que rellenes el campo **Cuenta para líneas que no son artículos físicos** antes de completar la tarea.|  

## <a name="see-also"></a>Consulte también  
[Intercambio de datos electrónicamente](across-data-exchange.md)   
[Facturar ventas](sales-how-invoice-sales.md)   
[Registrar compras](purchasing-how-record-purchases.md)

