---
title: Usar documentos electrónicos en ventas y compras
description: Aprenda a utilizar la funcionalidad de documentos electrónicos relacionada con las facturas de compra y venta.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
---

# Usar documentos electrónicos en ventas y compras

Puede utilizar documentos electrónicos configurados (documentos electrónicos) con documentos de compras y ventas.

Puede usar los siguientes documentos con la función de documentos electrónicos:  

- Ventas: 
    - Facturas de venta
    - Pedidos de venta
    - Notas de abono de venta
    - Facturas de servicios
    - Notas de abono de servicio
    - Documentos de interés
    - Recordatorios
- Compras: 
    - Facturas de compra
    - Pedidos de compra (solo crear documento nuevo)
    - Notas de abono de compra
    - Diarios generales

> [!NOTE]
> Actualmente, una orden de compra solo se puede utilizar cuando crea el documento a partir del documento electrónico de su proveedor. Sin embargo, no puede actualizar el documento existente con líneas que recibió de su proveedor.  

## Documentos electrónicos en ventas

Para crear y enviar una factura electrónica a un cliente, debe crear y registrar la factura de venta. Para obtener más información sobre el proceso estándar, consulte [Ventas con facturas](sales-how-invoice-sales.md).

Después de contabilizar el documento de ventas, abra la página **Factura de ventas registrada** para obtener a la página **Documento electrónico** relacionada.

### Ver documentos electrónicos

Para ver documentos electrónicos existentes, siga estos pasos.

1. En la página **Factura de ventas registrada**, seleccione **Documento electrónico** \> **Abrir documento electrónico**.
2. En la página **Documento electrónico** , en el encabezado, puede ver información básica sobre la factura registrada.
3. El campo **Registro** muestra el número del documento de la factura de venta registrada. Seleccione el enlace para abrir el documento.
4. En el campo **Estado del documento electrónico** , puede ver el estado en tiempo real del documento y su ubicación en el proceso. Si el documento está contabilizado, el estado es **Procesado**.

### Estados y registros de documentos electrónicos

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

## Documentos electrónicos en compras

La recepción de facturas electrónicas de compra en Dynamics 365 Business Central puede realizarse como un trabajo por lotes o manualmente.

### Ejecutar el trabajo por lotes

> [!NOTE]
> Este trabajo por lotes es para el cobro automatizado de sus facturas entrantes. Solo puede funcionar en un país o región donde exista la funcionalidad.

Cada vez que se ejecuta una cola de trabajos, si el servicio externo tiene facturas entrantes enviadas por su proveedor, el sistema recopila e importa esas facturas. Para completar el proceso, siga estos pasos.

1. Una vez finalizada la ejecución del trabajo por lotes, las facturas recién importadas se enumeran en la página **Documentos electrónicos**, junto con su información detallada básica.
2. Para ver más detalles, abra un documento electrónico específico.
3. Si no hubo errores o problemas en el documento electrónico y su mapeo, el campo **Registro** muestra el número de documento de la factura de compra que el sistema creó automáticamente. Seleccione el enlace para abrir el documento. Este documento creado por el sistema no es el documento contabilizado.
4. Para ir directamente al documento de compra, seleccione el campo **Registro**. Después de abrir la página **Factura de compra**, verifique el documento. Luego, si todo está correcto, contabilice el documento.
5. Al contabilizar el documento de compra, el campo **Registro** del **Documento electrónico** se actualiza de **Factura** a **Factura de compra** y el número del documento de compra contabilizado está disponible. Puede seleccionar el número para abrir la factura de compra contabilizada.

Los detalles sobre los registros son los mismos que en el proceso de venta de documentos electrónicos.

Debido a que los errores en el proceso de ventas están relacionados principalmente con la disponibilidad del servicio, el documento entrante puede contener múltiples motivos. El motivo más común de un error es que el sistema no puede reconocer las líneas del documento electrónico que recibió de su proveedor. Por lo tanto, no puede introducir líneas en su factura de compra.

Hay dos errores comunes:

- Si desea utilizar esta línea específica de su factura de proveedor que se registró directamente en la cuenta del libro mayor (G/L), debe haber configurado correctamente el valor **Texto de asignación**. Para evitar este error si desea utilizar cuentas de mayor, seleccione **Asignar texto a cuenta** para crear una asignación específica del valor de **Texto de asignación** con el valor de **N.º cta. débito** que desea utilizar.
- Si desea realizar un seguimiento del inventario y utilizar líneas de su factura de proveedor para completar artículos en las líneas de su documento, debe haber configurado correctamente el valor de **N.º de referencia de producto** . Para evitar este error, asigne el artículo externo con sus números de artículo utilizando la lista de referencia de artículos. Para obtener más información, consulte [Usar referencias de producto](inventory-how-use-item-cross-refs.md).

Después de corregir los errores y advertencias, puede especificar manualmente cuándo el sistema debe crear una factura de compra según su configuración seleccionando **Crear documento**.

### Importar facturas manualmente

Para importar manualmente documentos electrónicos externos, siga estos pasos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicio de documentos electrónicos** y luego seleccione el enlace relacionado.
2. En la página **Servicio de documentos electrónicos**, seleccione el servicio activo. 
3. Seleccione **Recibir** y cargue el archivo de documento electrónico que recibió del proveedor.
4. Si aparece un mensaje de error, abra el documento electrónico para solucionar los problemas.
5. Cuando haya terminado de solucionar los problemas, en el grupo **Importar manualmente**, seleccione **Crear documento**.
6. Una vez creado el documento en Business Central, podrá verlo tal como lo haría si utiliza un trabajo por lotes.

## Descripción general de los estados de los documentos electrónicos

Para obtener una mejor descripción general de todos los documentos electrónicos de la empresa, puede seleccionar el centro de funciones **Contable** donde existen estados de documentos electrónicos. Allí podrá encontrar actividades de documentos electrónicos que tengan los siguientes estados:

- **Documentos electrónicos salientes:**

    - Procesado
    - En curso
    - Error

- **Documentos electrónicos entrantes:**

    - Procesado
    - En curso
    - Error

## Consulte también

[Cómo configurar documentos electrónicos en Business Central](finance-how-setup-edocuments.md)  
[Cómo ampliar documentos electrónicos en Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestión financiera](finance.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Registrar compras con facturas de compra y pedidos](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
