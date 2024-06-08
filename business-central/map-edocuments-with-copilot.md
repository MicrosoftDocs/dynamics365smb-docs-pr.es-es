---
title: Asignar documentos electrónicos a líneas de pedido de compra con Copilot
description: Obtenga información sobre cómo utilizar Copilot para asignar documentos electrónicos a líneas de órdenes de compra.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/10/2024
ms.custom: bap-template
---

# <a name="map-e-documents-to-purchase-order-lines-with-copilot-preview"></a>Asignar documentos electrónicos a líneas de pedido de compra con Copilot (versión preliminar)

A medida que los procesos de adquisiciones se vuelven más digitales, la función de documentos electrónicos en Business Central desempeña un papel clave en la automatización de la recepción y el procesamiento de facturas de proveedores. Copilot puede ayudar en este proceso mejorando la asignación y la correspondencia de las facturas de los proveedores con los pedidos de compra. Esto reduce las tareas que consumen mucho tiempo y que normalmente incluirían búsquedas, consultas e introducción de datos exhaustivas. El beneficio se ve agravado por el hecho de que las facturas de los proveedores a menudo no se relacionan exactamente con los pedidos de compra, en cuyo caso Copilot está mejor posicionado para identificar los pedidos de compra correspondientes. Las capacidades de comparación mejoradas benefician particularmente a las organizaciones pequeñas y medianas que necesitan un seguimiento eficiente de documentos para líneas de órdenes de compra. Copilot es el asistente de trabajo con tecnología de IA que impulsa la creatividad y mejora la productividad de los usuarios de Business Central.

> [!IMPORTANT]
> - Esta es una característica de Vista previa lista para producción para entornos de producción y sandbox en cualquier localización de país o región, con excepción de Canadá.
> - Las vistas previas listas para producción están sujetas a términos de uso complementarios. Más información: [Términos de uso complementarios para la vista previa de Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)
> - El contenido generado por IA puede ser incorrecto.

En la versión inicial de la aplicación **documento electrónico**, introdujimos escenarios fundamentales para documentos electrónicos para todo el proceso de ventas. Sin embargo, existe la necesidad de mejoras y automatización en el manejo de los documentos recibidos, especialmente en el contexto de los procesos de compra. Copilot perfecciona la forma de gestionar los documentos electrónicos en el proceso de compra, especialmente con respecto a las órdenes de compra. El marco de documentos electrónicos le permite especificar el tipo de documento de compra que creará para cada proveedor cuando reciba facturas electrónicas de ellos. Anteriormente, la única opción era crear una factura de compra, ya sea como documento o como diario del libro mayor.

Ahora puede actualizar una orden de compra existente en Business Central con la información recibida en la factura electrónica.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->

## <a name="to-activate-copilot"></a>Para activar Copilot

Si no ha activado Copilot de **Ayuda de correspondencia de documentos electrónicos**, deberá hacerlo manualmente. Para habilitar el copiloto de **Ayuda de correspondencia de documentos electrónicos**, siga estos pasos: 

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Copilot y capacidades de IA** y, a continuación, elija el vínculo relacionado. 
2. En la lista de capacidades, elija **Ayuda de correspondencia de documentos electrónicos** y cambie el estado a **Activo**.  

Puede empezar a usar Copilot tan pronto como esté activado. 

## <a name="identify-purchase-orders"></a>Identificar pedidos compra

Primero, puede identificar los pedidos de compra que puede corresponder automáticamente. Si su **Proveedor** ha configurado el campo **Recibir documento electrónico en** para trabajar con **Pedidos de Compra**, una vez creado el documento electrónico en [!INCLUDE[prod_short](includes/prod_short.md)] (manualmente o desde un punto final externo), [!INCLUDE[prod_short](includes/prod_short.md)] hará lo siguiente:

1. Si el **Pedido de compra** para este proveedor en particular *existe y hay un número de pedido de compra* en el archivo de **documento electrónico**, [!INCLUDE[prod_short](includes/prod_short.md)] vinculará automáticamente este **Documento electrónico** con el **Pedido de compra** especificado. El **Estado del documento** de este **Documento electrónico** será **En curso** y el **Estado del documento electrónico** en la subpágina **Estado del servicio** será **Pedido vinculado**.  
Este vínculo será visible en el campo **Documento** de este **Documento electrónico** específico. Si necesita cambiar el **Pedido de compra** vinculado automáticamente, puede hacerlo usando la acción **Actualizar vínculo de pedido de compra** y eligiendo manualmente uno de los pedidos de compra existentes para este proveedor. Puede hacerlo solo antes de hacer coincidir las líneas entre **Documento electrónico** y **Pedido de compra**.  
2. Si el **Pedido de compra** para este proveedor específico *existe pero no hay ningún número de pedido de compra* en el archivo de **documento electrónico** recibido, si ha cargado este documento manualmente, [!INCLUDE[prod_short](includes/prod_short.md)] permite elegir uno de los pedidos de compra existentes cuando y si cargó este documento manualmente, abriendo la lista **Pedidos de compra** de los pedidos que ha obtenido de proveedores que contienen solo el **Documento electrónico**, donde debe seleccionar **Pedido de compra** que desea y seleccionar **Aceptar**. Si no seleccionó el **Pedido de compra** correcto u obtuvo el **Documento electrónico** automáticamente desde un extremo externo utilizando la **Cola de trabajos**, el nuevo **Documento electrónico** no se vinculará con ningún documento de compra, el **Estado del documento** será **Error** y el **Estado del documento electrónico** en la subpágina **Estado del servicio** será **Error de procesamiento de documento importado**. Para finalizar la vinculación con el **Pedido de compra**, seleccione la acción **Actualizar vínculo de pedido de compra** y elija uno de los pedidos de compra existentes para este proveedor.  

## <a name="map-lines"></a>Asignar líneas

Copilot le ayuda a hacer coincidir automáticamente líneas de facturas electrónicas con líneas de órdenes de compra y ofrece inteligencia de comparación adicional para mejorar las coincidencias.

Después de compararlos y asignarlos, [!INCLUDE [prod_short](includes/prod_short.md)] actualiza la orden de compra coincidente con la información de recibo relevante para garantizar que se reciban las cantidades correctas en las líneas de pedido.

Podrá cotejar tus documentos electrónicos recibidos con líneas de pedidos de compra desde dos lugares diferentes, desde la página **Documentos electrónicos** o desde la página **Pedido de compra**. La forma más sencilla de localizar los **Pedidos de compra** ya vinculados es utilizar el mosaico **Pedidos de compra vinculados** como parte de **Actividades de documentos electrónicos**. Todos los documentos no vinculados se pueden encontrar usando el mosaico **Facturas electrónicas de compra en espera** donde tiene una lista de **Documentos electrónicos** que debe revisar.  

> [!NOTE]
> Las **Actividades de documentos electrónicos** con estos dos mosaicos se puede encontrar en las siguientes Áreas de trabajo: **Evaluación de administrador de negocio**, **Administrador de negocios**, **Contable**, **Administrador de Inventario** y **Envío y recepción**.

Cuando desee ejecutar la comparación del pedido de compra, elija la acción **Asignar líneas de documento electrónico**, que existe tanto en la página de pedido de compra como en la de lista de pedidos de compra. Pero, si desea ejecutar la comparación desde la página **Documentos electrónicos**, elija la acción **Conciliar pedido de compra** desde esta página. Para procesar con comparación, siga estos pasos:

1. Elija la acción **Asignar líneas de documentos electrónicos** o **Conciliar pedido de compra**, para documentos ya vinculados.  
2. Puede observar que la solicitud **Líneas de pedido de correspondencia de documentos electrónicos con Copilot** está funcionando y tiene la página **Conciliación de pedidos de compra** en segundo plano. Eso significa que está ocurriendo el mismo proceso pero con el apoyo automático de **Copilot**, que ejecuta el proceso de emparejamiento en su lugar. 
3. Después de unos segundos, la **Líneas de pedido de correspondencia de documentos electrónicos con Copilot** sugerirán líneas para combinar con algunos detalles más: 

    1. En el encabezado del mensaje, puede encontrar la siguiente información: 

    |Nombre del campo |Descripción |
    |--------|-----------------|
    |Coincidencia automática | Especifica el número de coincidencias propuestas por Copilot. Esto se basa en una comparación de cadenas y si hay un 80 % o más de descripciones superpuestas, el sistema hará coincidir estas descripciones automáticamente sin utilizar las capacidades de GPT. |
    |Coincidencia por Copilot | Especifica el número de coincidencias propuestas por Copilot mediante comparación semántica y de cadenas. |
    |N.º documento electrónico | Especifica el número del documento electrónico vinculado. |
    |Importe total sin IVA | Permite especificar el importe total de la factura sin IVA. |
    |Importe total incl. IVA | Especifica el importe conciliado sin IVA. |
    
    2. Si todas las líneas coinciden, verá el texto verde en la esquina superior derecha: **Coincidencia de todas las líneas (100 %). Revise las propuestas de coincidencia**.  
    3. En las líneas **Propuesta coincidente**, puede encontrar la siguiente información:  

    |Nombre del campo |Descripción |
    |--------|-----------------|
    |N.º línea documento electrónico | Especifica el número de línea del documento electrónico (procedente del archivo del documento electrónico original). |
    |Descripción de la línea del documento electrónico | Especifica la descripción de línea del documento electrónico (procedente del archivo del documento electrónico original). |
    |Cantidad conciliada | Especifica la cantidad que se liquidará a la línea del pedido de compra. |
    |Propuesta | Especifica la acción propuesta por la IA y estas acciones sugeridas están relacionadas con la comparación de las líneas del pedido de compra. |

    4. Todas las líneas totalmente sugeridas y coincidentes están marcadas en color verde. Si hay algún problema, es decir, precio diferente, pero dentro del rango de precios permitido, esta línea se marcará en color amarillo, y si hay alguna similitud entre los campos de descripción pero la diferencia de precio es mayor de lo permitido, esta línea se marcará en color rojo. 
    5. Si no está satisfecho con algunas sugerencias, puede eliminarlas usando la acción **Eliminar línea**.  
    6. Si desea ver las coincidencias de propuestas, puede seleccionar el enlace en la columna **Propuesta** para abrir la página **Detalles de coincidencia de documentos electrónicos**. 
    7. En la página **Detalles de coincidencia de documentos electrónicos** puede comparar los detalles del **Documentos electrónicos** y del **Pedido de compra** para estar seguro de la coincidencia sugerida antes de confirmarla. 
    8. Después de revisar, cierre la página.   

4. Si no está satisfecho con la mayoría de las sugerencias, o en caso de que no desee utilizar la característica **Líneas de pedido de correspondencia de documentos electrónicos con Copilot**, seleccione **Descartarlo** y podrá continuar con la [comparación manual](finance-how-use-edocuments-purchase.md).  
5. Si desea conservar las sugerencias, elija el botón **Mantenerlo** y el sistema guardará todas las sugerencias realizadas por **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] cierra la solicitud de Copilot y las líneas en la página **Conciliación de pedidos de compra** se marcan en verde, ya que ya están coincidentes.  
7. A partir de ahora, puede continuar trabajando mientras está realizando comparaciones manuales, y eso significa que puede eliminar correspondencias, correspondencias manuales, restablecer correspondencias o si no hay cambios que quiera hacer, simplemente elegir la acción **Aplicar a pedido de compra** y continuar trabajando con el **Pedido de compra**. 

> [!NOTE]
> Puede elegir la acción **Coincidencia con Copilot** en la página **Conciliación de pedidos de compra** nuevamente, pero en este caso se le preguntará si desea sobrescribir las coincidencias existentes, ya que todas las líneas ya han sido cotejadas.  

> [!NOTE]
> El análisis de precio/coste y la verificación de la cantidad disponible son parte de la actividad de preprocesamiento. 

## <a name="see-also"></a>Consulte también

[Información general de documentos electrónicos](finance-edocuments-overview.md)    
[Usar documentos electrónicos en ventas](finance-how-use-edocuments.md)    
[Usar documentos electrónicos en compras](finance-how-use-edocuments-purchase.md)   
[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)    
[Preguntas frecuentes para IA responsable para asistencia de conciliación bancaria](faqs-bank-reconciliation.md)    
