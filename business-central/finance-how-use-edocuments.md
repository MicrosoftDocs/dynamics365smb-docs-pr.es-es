---
title: Usar documentos electrónicos en ventas
description: Aprenda a utilizar la funcionalidad de documentos electrónicos relacionada con las ventas.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 03/29/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-sales-process"></a>Usar documentos electrónicos en el proceso de venta

Puede utilizar documentos electrónicos configurados (documentos electrónicos) con los documentos de ventas.

Puede usar los siguientes documentos de ventas con la función de documentos electrónicos:  

- Facturas de venta
- Pedidos de venta
- Notas de abono de venta
- Facturas de servicios
- Notas de abono de servicio
- Documentos de interés
- Recordatorios

## <a name="e-documents-in-sales"></a>Documentos electrónicos en ventas

Para crear y enviar una factura electrónica a un cliente, debe crear y registrar la factura de venta. Para obtener más información sobre el proceso estándar, consulte [Ventas con facturas](sales-how-invoice-sales.md).

Después de contabilizar el documento de ventas, abra la página **Factura de ventas registrada** para obtener a la página **Documento electrónico** relacionada.

### <a name="view-e-documents"></a>Ver documentos electrónicos

Para ver documentos electrónicos existentes, siga estos pasos.

1. En la página **Factura de ventas registrada**, seleccione **Documento electrónico** \> **Abrir documento electrónico**.
2. En la página **Documento electrónico** , en el encabezado, puede ver información básica sobre la factura registrada.
3. El campo **Registro** muestra el número del documento de la factura de venta registrada. Seleccione el enlace para abrir el documento.
4. En el campo **Estado del documento electrónico** , puede ver el estado en tiempo real del documento y su ubicación en el proceso. Si el documento está contabilizado, el estado es **Procesado**.

### <a name="e-document-statuses-and-logs"></a>Estados y registros de documentos electrónicos

Para obtener detalles sobre el nivel de estado del servicio de su documento electrónico, consulte la pestaña desplegable **Estado del servicio de documento electrónico** . En las líneas, el sistema muestra uno o más servicios que el documento utilizó. En el escenario más común, cada documento utiliza solo un servicio. Sin embargo, un documento puede utilizar varios servicios.

- Marque el campo **Código de servicio de documentos electrónicos** para determinar qué servicio se utilizó.
- Marque el campo **Estado de documento electrónico** para determinar el estado actual del servicio para este documento.
- Si desea más información, seleccione el campo **Registros** para el servicio de la página **Registros de documentos electrónicos**. Se muestra una descripción cronológica de los diferentes estados del documento.
- Marque los campos **N.º de movimiento** y **Hora de creación** y otra información en la página **Registros de documentos electrónicos**. En el campo **Estado de documento electrónico**, el primer estado es **Exportado**, que indica que se ha creado el archivo del documento electrónico. El siguiente estado es **Enviado**, que indica que el documento se envió al proveedor de servicios, si está configurado.

Para obtener más información, seleccione la entrada que tiene el estado **Exportado** y luego ejecute una de las siguientes acciones:

- **Abrir registros de asignación**: Obtenga una descripción general de todos los campos exportados de las tablas de origen en el campo **Valor original**. Si utilizó reglas de transformación en el proceso de exportación, también puede obtener el valor final en el campo **Nuevo valor**.
- **Exportar archivo**: Exportar el archivo XML para revisión manual.

Para ver la comunicación entre usted y el servicio al que envía su documento, utilice el campo **Registros de comunicación**. Abra la página **Registros de comunicación de documentos electrónicos** para ver detalles sobre la solicitud y los motivos del mensaje con ese servicio.

Si hay un problema con el proveedor de servicios y el documento no se puede enviar, busque los siguientes indicadores en la página **Documento electrónico**:

- El campo **Estado de documento electrónico** del encabezado muestra el estado **Error**.
- El campo **Estado de documento electrónico** de la ficha desplegable **Estado del servicio de documentos electrónicos** muestra el estado **Error de envío**.
- La ficha desplegable **Errores y advertencias** contiene uno o más mensajes que proporcionan la causa del problema.

Una vez solucionado el problema, ejecute manualmente las acciones **Enviar documento**. Si necesita diferentes acciones, como **Documento recreado**, **Cancelar documento** u **Obtener aprobación**, puede ejecutarlos.

## <a name="overview-of-e-document-statuses"></a>Descripción general de los estados de los documentos electrónicos

Para obtener una mejor descripción general de todos los documentos electrónicos de la empresa, puede seleccionar el centro de funciones **Contable** donde existen estados de documentos electrónicos. Allí podrá encontrar actividades de documentos electrónicos que tengan los siguientes estados:

- **Documentos electrónicos salientes:**

    - Procesado
    - En curso
    - Error


## <a name="see-also"></a>Consulte también

[Cómo configurar documentos electrónicos en Business Central](finance-how-setup-edocuments.md)  
[Cómo ampliar documentos electrónicos en Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestión financiera](finance.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Registrar compras con facturas de compra y pedidos](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
