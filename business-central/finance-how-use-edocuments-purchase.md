---
title: Usar documentos electrónicos en el proceso de compra
description: Aprenda a utilizar la funcionalidad de documentos electrónicos relacionada con las facturas de compra y pedidos.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="use-e-documents-in-the-purchases-process"></a>Usar documentos electrónicos en el proceso de compra

Puede utilizar documentos electrónicos configurados (documentos electrónicos) con los documentos de compra.

Se pueden usar los siguientes documentos de compra con la función de documentos electrónicos:  

- Facturas de compra
- Pedidos de compra (desde la versión 24.0)
- Notas de abono de compra
- Diarios generales

> [!NOTE]
> Desde [!INCLUDE[prod_short](includes/prod_short.md)] versión 24.0, se pueden conectar **Pedidos de compra** con los **Documentos electrónicos** recibidos.  

## <a name="e-documents-in-purchases"></a>Documentos electrónicos en compras

La recepción de documentos electrónicos de compra en Dynamics 365 Business Central puede realizarse como un trabajo por lotes o manualmente.  

### <a name="how-to-set-up-vendors-to-work-with-different-purchase-documents"></a>Cómo configurar proveedores para que trabajen con diferentes documentos de compra

Siga estos pasos para configurar proveedores para que funcionen correctamente con facturas electrónicas entrantes: 

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego seleccione el vínculo relacionado. 
2. Elija el proveedor que quiere configurar.   
3. En la pestaña desplegable **Recepción**, busque el campo **Recibir documento electrónico en** para especificar el documento de compra por defecto que se generará a partir del documento electrónico recibido. 

   > [!NOTE]
   > En el campo **Recibir documento electrónico para**, los usuarios pueden seleccionar una **Factura de compra** o un **Pedido de compra** basándose en lo que les gustaría haber creado a partir de la factura electrónica recibida. Esta selección no afecta a la creación de documentos correctores; en ambos escenarios, el sistema generará una **Nota de abono**.  

   > [!NOTE]
   > Si el usuario elige la opción **Pedido de compra** en el campo **Recibir documento electrónico en**, el sistema intentará actualizará uno de los pedidos de compra existentes, pero si el pedido de compra de un proveedor en el **documento electrónico** no existe, [!INCLUDE[prod_short](includes/prod_short.md)] creará un nuevo **Pedido de compra**, utilizando el mismo enfoque que se utiliza para crear las nuevas **Facturas de compra** como se explica más adelante en esta página.  

4. Elija una de las opciones que desee utilizar para el proveedor seleccionado. 
5. Cierre la página.   

### <a name="to-work-with-purchase-invoices"></a>Para trabajar con facturas de compra

#### <a name="run-the-batch-job"></a>Ejecutar el trabajo por lotes

> [!NOTE]
> Este trabajo por lotes es para el cobro automatizado de sus facturas entrantes. Solo puede funcionar en un país o región donde exista la funcionalidad.  

Cada vez que se selecciona la ejecución de una **Cola de trabajos**, si el servicio externo tiene facturas entrantes enviadas por su proveedor, el sistema recopila e importa esas facturas. Para completar el proceso, siga estos pasos: 

1. Una vez finalizada la ejecución del trabajo por lotes, las facturas recién importadas se enumeran en la página **Documentos electrónicos**, junto con su información detallada básica. 
2. Para ver más detalles, abra un documento electrónico específico.   
3. Si no hubo errores o problemas en el documento electrónico, el campo **Registro** muestra el número de documento de la factura de compra, si se configura en la página **Ficha proveedor** (que el sistema creó automáticamente). Seleccione el enlace para abrir el documento.
 
   > [!NOTE]
   > Este documento creado por el sistema no es el documento contabilizado. 

4. Para ir directamente al documento de compra, seleccione el campo **Registro**. Después de abrir la página **Factura de compra**, verifique el documento. Si todo está correcto, contabilice el documento.  
5. Al contabilizar el documento de compra, el campo **Registro** del **Documento electrónico** se actualiza de **Factura** a **Factura de compra** y el número del documento de compra contabilizado está disponible. Puede seleccionar el número para abrir la factura de compra contabilizada. 

Los detalles sobre los registros son los mismos que en el proceso de venta de documentos electrónicos.  

Debido a que los errores en el proceso de ventas están relacionados principalmente con la disponibilidad del servicio, el documento entrante puede contener múltiples motivos. El motivo más común de un error es que el sistema no puede reconocer las líneas del documento electrónico que recibió de su proveedor. Por lo tanto, no puede introducir líneas en su factura de compra. 

Hay dos errores comunes:  

- Si desea utilizar esta línea específica de su factura de proveedor que se registró directamente en la cuenta del libro mayor (G/L), debe haber configurado correctamente el valor **Texto de asignación**. Para evitar este error si desea utilizar cuentas de mayor, seleccione **Asignar texto a cuenta** para crear una asignación específica del valor de **Texto de asignación** con el valor de **N.º cta. débito** que desea utilizar. 
- Si desea realizar un seguimiento del inventario y utilizar líneas de su factura de proveedor para completar artículos en las líneas de su documento, debe haber configurado correctamente el valor de **N.º de referencia de producto** . Para evitar este error, asigne el artículo externo con sus números de artículo utilizando la lista de referencia de artículos. Para obtener más información, consulte [Usar referencias de producto](inventory-how-use-item-cross-refs.md). 

Después de corregir los errores y advertencias, puede especificar manualmente cuándo el sistema debe crear una factura de compra según su configuración seleccionando **Crear documento**.   

#### <a name="manually-import-invoices"></a>Importar facturas manualmente

Para importar manualmente documentos electrónicos externos, siga estos pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicio de documentos electrónicos** y luego seleccione el enlace relacionado. 
2. En la página **Servicio de documentos electrónicos**, seleccione el servicio activo.   
3. Seleccione **Recibir** y cargue el archivo de documento electrónico que recibió del proveedor. 
4. Si aparece un mensaje de error, abra el documento electrónico para solucionar los problemas. 
5. Cuando haya terminado de solucionar los problemas, en el grupo **Importar manualmente**, seleccione **Crear documento**.  
6. Una vez creado el documento en [!INCLUDE[prod_short](includes/prod_short.md)], el uso de un trabajo por lotes no cambia la forma en que lo ve. 

### <a name="e-documents-with-purchase-orders"></a>Documentos electrónicos con pedidos de compra

#### <a name="to-link-purchase-orders-with-the-received-e-documents"></a>Vincular los pedidos de compra con los documentos electrónicos recibidos

Si su **Proveedor** ha configurado el campo **Recibir documento electrónico en** para trabajar con **Pedidos de Compra**, una vez creado un documento electrónico en [!INCLUDE[prod_short](includes/prod_short.md)] (manualmente o desde un punto final externo), [!INCLUDE[prod_short](includes/prod_short.md)] hará lo siguiente:  

1. Si el **Pedido de compra** para este proveedor en particular existe y hay un número de pedido de compra en el archivo **Documento electrónico** de recepción, [!INCLUDE[prod_short](includes/prod_short.md)] vinculará automáticamente este **Documento electrónico** con el **Pedido de compra** mencionado, el **Estado del documento** de este **Documento electrónico** será **En curso**, y el **Estado del documento electrónico** en la subpágina **Estado del servicio** será **Pedido vinculado**. Este vínculo será visible en el campo **Documento** de este **Documento electrónico** específico. Si necesita cambiar el **Pedido de compra** vinculado automáticamente, puede hacerlo usando la acción **Actualizar vínculo de pedido de compra** y eligiendo manualmente uno de los pedidos de compra existentes para este proveedor. Puede hacerlo solo antes de hacer coincidir las líneas entre **Documento electrónico** y **Pedido de compra**.  

2. Si existe el **Pedido de compra** para este proveedor en particular pero no hay ningún número de pedido de compra en el archivo de **Documento electrónico** recibido, [!INCLUDE[prod_short](includes/prod_short.md)] ofrecerá la posibilidad de elegir uno de los pedidos de compra existentes cuando y si cargó este documento manualmente. Esto abre la lista **Pedidos de compra** con pedidos solo para el proveedor del que recibió el **Documento electrónico**. Debe seleccionar el **Pedido de compra** que desea y después seleccionar **Aceptar**. Si no pudo seleccionar el **Pedido de compra** correcto u obtuvo el **Documento electrónico** automáticamente desde un punto final externo usando la **Cola de trabajos**, no se vinculará un nuevo **Documento electrónico** a ningún documento de compra. El **Estado del documento** mostrará **Error** y el **Estado del documento electrónico** en la subpágina **Estado del servicio** también mostrará **Error de procesamiento de documento importado**. Para finalizar la vinculación con el **Pedido de compra**, seleccione la acción **Actualizar vínculo de pedido de compra** y elija uno de los pedidos de compra existentes para este proveedor. 

3. Si el **Pedido de compra** para este proveedor en particular cuando se crea un nuevo **Documento electrónico**, [!INCLUDE[prod_short](includes/prod_short.md)] creará un nuevo **Pedido de compra**, utilizando el mismo modelo de creación que ya existe para las nuevas **Facturas de compra**. El **Estado del documento** de este **Documento electrónico** será **Procesado** y el **Estado del documento electrónico** en la subpágina **Estado del servicio** será **Documento importado creado**. Este vínculo será visible en el campo **Documento** de este **Documento electrónico** específico.   

#### <a name="matching-lines-from-received-e-document-with-purchase-order"></a>Líneas coincidentes del documento electrónico recibido con el pedido de compra

Podrá cotejar tus documentos electrónicos recibidos con líneas de pedidos de compra desde dos lugares diferentes, desde la página **Documento electrónico** o desde la página **Pedido de compra**. La forma más sencilla de localizar los **Pedidos de compra** ya vinculados es utilizar el mosaico **Pedidos de compra vinculados** como parte de **Actividades de documentos electrónicos**. Todos los documentos no vinculados se pueden encontrar usando el mosaico **Facturas electrónicas de compra en espera** donde tiene una lista de **Documentos electrónicos** que necesita revisar.  

> [!NOTE]
> Las **Actividades de documentos electrónicos** con estos dos mosaicos se puede encontrar en las siguientes **Áreas de trabajo**: Evaluación de administrador de negocio, Administrador de negocio, Contable, Administrador de Inventario y Envío y recepción.  

> [!NOTE]
> Si el porcentaje de IVA difiere entre el documento entrante y el porcentaje de IVA de la empresa, los documentos coincidentes no se pueden utilizar en un entorno de varios países o regiones.  

##### <a name="matching-lines-from-purchase-order"></a>Líneas coincidentes del pedido de compra

Puede hacer coincidir las líneas de la lista **Pedidos de compra** o de uno de los **Pedidos de compra** abiertos. Para empezar, siga los pasos que se detallan a continuación:  

1. Seleccione el mosaico **Pedidos de compra vinculados** en el Área de trabajo si hay un número. 
2. Elija una de las dos opciones de correspondencia: 

   - Si desea hacer coincidir las líneas de la lista **Pedidos de compra**, seleccione la línea **Pedido de compra** que desea unir y elija la acción **Asignar líneas de documentos electrónicos**.  
   - Si desea abrir primero el **Pedido de compra**, abra el documento y luego elija la acción **Asignar líneas de documentos electrónicos**. 

3. Como ambas opciones tienen el mismo proceso, abrirá la página **Conciliación de pedidos de compra** con el siguiente contenido: 

    1. En el encabezado puede encontrar la siguiente información, que puede ayudarle a asignar las líneas más fácilmente: 

       |Nombre del campo |Descripción |
       |--------|-----------------|
       |Nombre del proveedor |Especifica el nombre del proveedor del documento electrónico. |
       |N.º documento electrónico |Especifica el número de documento electrónico vinculado. |
       |Fecha del documento electrónico |Especifica la fecha del documento electrónico vinculado.  |
       |Importe del documento electrónico |Especifica el importe total del documento electrónico vinculado con IVA. |

    2. En las líneas, puede encontrar las líneas importadas desde el archivo de **Documento electrónico** en el lado izquierdo y las líneas de **Pedido de compra** existentes a la derecha.  
    3. Todas las líneas en ambos lados tienen números de artículo y descripciones, junto con el **Coste unitario directo** y el **% de descuento de línea**.  
    4. En el lado **Líneas importadas**, también puede ubicar el campo **Cantidad** como una cantidad total de la factura electrónica y el campo **Cantidad coincidente** que especifica la cantidad que ya coincidió con las líneas del pedido de compra. 
    5. En el lado **Líneas de pedidos de compra**, también puede encontrar la **Cantidad disponible** como la cantidad que se puede igualar esta línea (cantidad recibida, pero no facturada) y **Cdad. a facturar**, especificando la cantidad que ya coincide con esta línea. 
    6. Para hacer coincidir líneas, seleccione las líneas en ambos lados que desea hacer coincidir y elija la acción **Conciliar manualmente**. Las líneas coincidentes se marcarán en verde. 
    7. Es posible hacer coincidir una con una, pero también es posible hacer coincidir muchas con una o una con muchas, seleccionando más líneas en uno u otro lado antes de elegir la acción **Conciliar manualmente**. 
    8. También puede elegir la acción **Conciliar manualmente** para hacer coincidir automáticamente todas las líneas con el mismo **Tipo**, **Nº**, **Precio unitario**, **Descuento** y **Unidad de medida**. 
    9. Si comete un error, puede elegir la acción **Eliminar conciliación** para eliminar las líneas coincidentes en el lado del pedido de compra o elegir la acción **Restablecer correspondencia** para restablecer todo lo que coincide. 
    10. Si su **Documento electrónico** tiene muchas líneas, durante el proceso de comparación, puede elegir la acción **Mostrar líneas pendientes** para eliminar todas las líneas del documento electrónico si ya coinciden completamente. Si necesita ver todas las líneas, siempre puede elegir la acción **Mostrar todas las líneas**. 

4. Una vez que termine con la correspondencia, debe elegir la acción **v**.   
5. Una vez que aplique la coincidencia al **Pedido de compra**, [!INCLUDE[prod_short](includes/prod_short.md)] actualizará los siguientes campos:

    1. **N.º factura proveedor** y **Fecha emisión documento** en el encabezado del documento se actualizarán con los valores del documento electrónico que recibió y vinculó. 
    2. **Cdad. a facturar** en las líneas se actualizará con los valores de **Cdad. a facturar** de la página **Conciliación de pedidos de compra** según la coincidencia que haya realizado. 
    3. Ahora puede registrar el documento eligiendo la acción **Registrar**.  
    4. Una vez que publique el documento, el campo **Documento** en la página **Documento electrónico** cambiará el valor y se relacionan con la **Factura de compra publicada**. 
    5. Cierre la página.  

> [!IMPORTANT]
> De manera predeterminada, puede hacer coincidir solo las líneas que tengan el mismo importe total en ambos documentos. Eso significa que el **Coste unitario directo** junto con la línea aplicada **% de descuento** deben ser iguales, ya que en un documento puede tener un importe sin descuento y en otro con descuento.  

Si desea agregar algo de tolerancia y permitir la diferencia entre líneas en **Factura electrónica** y **Pedido de compra**, siga estos pasos:   

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de compras y pagos** y luego seleccione el vínculo relacionado.  
2. Desea permitir una tolerancia en el campo **% diferencia correspondencia doc. elect.** especificando el porcentaje máximo permitido de diferencia de costes al cotejar una línea **Documento electrónico** con la línea **Pedido de compra**. 
3. Esta configuración se aplicará a todas las líneas coincidentes, pero nuevamente considerando la tolerancia para el importe total, como para el **Coste unitario directo** junto con el **% de descuento en línea** aplicado.  
4. Cierre la página.   

##### <a name="matching-lines-from-e-document"></a>Para hacer coincidir líneas de un documento electrónico

Puede hacer coincidir las líneas en la página  **Documento electrónico**. Para empezar, siga los pasos que se detallan a continuación:  

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documentos electrónicos** y luego seleccione el vínculo relacionado. 
2. Seleccione el **Documento electrónico** que desee hacer coincidir.   
3. Elija la acción **Conciliar pedido de compra** para abrir la página **Conciliación de pedidos de compra**.  
4. Repita los mismos pasos que utilizó cuando comenzó a emparejar los pedidos de compra.

### <a name="e-document-matching-assistance-copilot"></a>Copiloto de ayuda de correspondencia de documentos electrónicos

> [!NOTE]
> Actualmente el **Copiloto de ayuda de correspondencia de documentos electrónicos** se encuentra en estado de versión preliminar listo para producción y está disponible en todo el mundo, excepto en Canadá. Solo funciona en inglés. 

> [!NOTE]
> Copilot es el asistente con tecnología de IA que ayuda a personas de su organización a desatar su creatividad y automatizar las tareas tediosas. El copiloto de **Ayuda de correspondencia de documentos electrónicos** ayuda a los usuarios a cotejar fácilmente sus facturas electrónicas recibidas con líneas de pedido de compra existentes, utilizando el modelo LLM para cotejar líneas entre dos documentos diferentes. 

#### <a name="to-activate-the-copilot"></a>Para activar el copiloto

En caso de que no haya activado el copiloto de **Ayuda de correspondencia de documentos electrónicos**, deberá hacerlo manualmente. Para habilitar el copiloto de **Ayuda de correspondencia de documentos electrónicos**, siga estos pasos: 

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Copilot y capacidades de IA** y, a continuación, elija el vínculo relacionado. 
2. En la lista de capacidades, elija **Ayuda de correspondencia de documentos electrónicos** y cambie el estado a **Activo**.  

Una vez que el copiloto esté activado, podrá comenzar a usarlo.

#### <a name="use-the-e-document-matching-assistance-copilot"></a>Usar el copiloto de ayuda de correspondencia de documentos electrónicos

Si el copiloto está activado, las acciones existentes **Asignar líneas de documentos electrónicos** en pedidos comprados y **Conciliar pedido de compra** en la página **Documento electrónico** obtendrá diferentes iconos, que simbolizan la capacidad de IA. Puedes ejecutar estas acciones (iguales que en ejemplos anteriores del listado de pedidos de compra), desde uno de los **Pedidos de compra** o de **Documento electrónico**. Todos los pasos para ejecutar son iguales, pero cuando ejecuta esta acción, el resultado será diferente y deberá seguir estos pasos:  

1. Elija la acción **Asignar líneas de documentos electrónicos** o **Conciliar pedido de compra**, para documentos ya vinculados.  
2. Observe que la solicitud **Líneas de pedido de correspondencia de documentos electrónicos con Copilot** está funcionando y la página **Conciliación de pedidos de compra** está en segundo plano. Eso significa que está ocurriendo el mismo proceso pero con el apoyo automático de **Copilot**, que ejecuta el proceso de emparejamiento en su lugar. 
3. Después de unos segundos, la **Líneas de pedido de correspondencia de documentos electrónicos con Copilot** sugerirán líneas para combinar con algunos detalles adicionales: 

    1. En el encabezado del mensaje, puede encontrar la siguiente información: 

       |Nombre del campo |Descripción |
       |--------|-----------------|
       |Coincidencia automática | Especifica el número de coincidencias propuestas por Copilot. Esto se basa en una comparación de cadenas y si hay un 80 % o más de descripciones superpuestas, el sistema hará coincidir estas descripciones automáticamente sin utilizar las capacidades de GPT. |
       |Coincidencia por Copilot | Especifica el número de coincidencias propuestas por el copiloto mediante comparación semántica y de cadenas. |
       |N.º documento electrónico | Especifica el número del documento electrónico vinculado. |
       |Importe total sin IVA | Permite especificar el importe total de la factura sin IVA. |
       |Importe total incl. IVA | Especifica el importe conciliado con IVA. |
    
    2. Si todas las líneas coinciden, verá el texto verde en la esquina superior derecha: **Coincidencia de todas las líneas (100 %). Revise las propuestas de coincidencia**.  
    3. En las líneas **Propuesta coincidente**, puede encontrar la siguiente información:  

       |Nombre del campo |Descripción |
       |--------|-----------------|
       |N.º línea documento electrónico | Especifica el número de línea del documento electrónico (procedente del archivo del documento electrónico original). |
       |Descripción de la línea del documento electrónico | Especifica la descripción de línea del documento electrónico (procedente del archivo del documento electrónico original). |
       |Cantidad conciliada | Especifica la cantidad que se liquidará a la línea del pedido de compra. |
       |Propuesta | Especifica la acción propuesta por la IA y estas acciones sugeridas están relacionadas con la comparación de las líneas del pedido de compra. |

    4. Todas las líneas totalmente sugeridas y coincidentes están marcadas en color verde. Si hay algún problema, es decir, precio diferente, pero dentro del rango de precios permitido, esta línea se marcará en amarillo, y si hay alguna similitud entre los campos de descripción pero la diferencia de precio es mayor de lo permitido, esta línea se marcará en rojo. 
    5. Si no está satisfecho con algunas sugerencias, puede eliminarlas usando la acción **Eliminar línea**.  
    6. Si desea ver las coincidencias de propuestas, puede seleccionar el enlace en la columna **Propuesta** para abrir la página **Detalles de coincidencia de documentos electrónicos**. 
    7. En la página **Detalles de coincidencia de documentos electrónicos** puede comparar los detalles del **Documento electrónico** y del **Pedido de compra** para estar seguro de la coincidencia sugerida antes de confirmarla. 
    8. Después de revisar, cierre la página.   

4. Si no está satisfecho con la mayoría de las sugerencias, o si no desea utilizar la característica **Líneas de pedido de correspondencia de documentos electrónicos con Copilot**, seleccione **Descartarlo** y podrá continuar con la comparación manual como se explicó anteriormente.  
5. Si desea conservar las sugerencias, elija el botón **Mantenerlo** y el sistema guardará todas las sugerencias realizadas por **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] cerrará la solicitud de Copilot y las líneas en la página **Conciliación de pedidos de compra** se marcarán en verde, ya que ya están coincidentes. 
7. Ahora puede continuar trabajando mientras realiza la comparación manual; eso significa que puede eliminar coincidencias, conciliar manualmente o restablecer las coincidencias. Si no desea realizar cambios, simplemente elija la acción **Aplicar a pedido de compra** y continúe trabajando con el **Pedido de compra**. 

> [!NOTE]
> Puede elegir la acción **Coincidencia con Copilot** en la página **Conciliación de pedidos de compra** nuevamente, pero en este caso se le preguntará si desea sobrescribir las coincidencias existentes, ya que todas las líneas ya han sido cotejadas.  

> [!NOTE]
> El análisis de precio/coste y la verificación de la cantidad disponible son parte de la actividad de preprocesamiento.   

## <a name="overview-of-e-document-statuses"></a>Descripción general de los estados de los documentos electrónicos

Para obtener una mejor descripción general de todos los documentos electrónicos de la empresa, puede seleccionar el centro de funciones **Contable** donde existen estados de documentos electrónicos. Allí podrá encontrar actividades de documentos electrónicos que tengan los siguientes estados:

- **Documentos electrónicos entrantes:**

    - Procesado
    - En curso
    - Error


## <a name="see-also"></a>Consulte también

[Configurar documentos electrónicos](finance-how-setup-edocuments.md)    
[Usar un documento electrónico en el proceso de venta](finance-how-use-edocuments.md)   
[Ampliar la funcionalidad de documentos electrónicos](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Gestión financiera](finance.md)    
[Facturar ventas](sales-how-invoice-sales.md)    
[Registrar compras con facturas de compra y pedidos](purchasing-how-record-purchases.md)    
[Trabajar con Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

