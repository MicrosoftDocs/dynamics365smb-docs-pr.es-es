---
title: Configurar documentos electrónicos
description: Aprenda a configurar la funcionalidad de documentos electrónicos.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# <a name="set-up-e-documents"></a>Configurar documentos electrónicos

> [!IMPORTANT]
> El módulo principal de E-Documents es un marco. De forma predeterminada, no hay ningún campo **Formato de documento** o **Integración de servicio**. Estos detalles forman parte de las aplicaciones de localización, porque ambos son específicos de los requisitos locales.

> [!NOTE]
> A partir de la versión 23.1 se añade un formato de documento estándar PEPPOL como formato global en el campo **Formato de documento**.

El primer paso en la configuración de documentos electrónicos (e-documents) es configurar el Servicio de documentos electrónicos donde se define el comportamiento completo de su sistema en relación con la comunicación de documentos electrónicos.

## <a name="set-up-the-e-document-service"></a>Configurar el servicio de documentos electrónicos

Siga estos pasos para configurar el Servicio de documentos electrónicos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios de documentos electrónicos** y luego seleccione el enlace relacionado.
2. Seleccione **Nuevo** y, a continuación, en la página **Servicio de documentos electrónicos**, en la ficha desplegable **General**, configure los campos tal y como se describen en la siguiente tabla.

    | Campo | Descripción |
    |-------|-------------|
    | Código | Seleccione el código de configuración de la exportación electrónica. |
    | Descripción | Especifique una breve descripción de la configuración de la exportación electrónica. |
    | Formato de documento | <p>El formato de exportación de la configuración de exportación electrónica.</p><p>De forma predeterminada, no hay opciones en este campo en el lanzamiento 1.</p> |
    | Integración de servicio | Seleccione el código de integración de la configuración de exportación electrónica. En el lanzamiento 1, la única opción es **Sin integración**. |
    | Usar procesamiento por lotes | Especifique si el servicio usa procesamiento por lotes para la exportación. |

4. En la ficha desplegable **Parámetros importados**, configure los campos tal como se describe en la tabla siguiente.

    | Campo | Descripción |
    |-------|-------------|
    | Validar empresa receptora | Especifique si se debe validar la información de la empresa de recepción durante la importación. |
    | Resolver unidad medida | Especifique si la unidad de medida debe resolverse durante la importación. |
    | Buscar referencia de producto | Especifique si un artículo debe buscarse por la referencia del artículo durante la importación. |
    | Buscar GTIN de producto | Especifique si un artículo debe buscarse por Número Global de Artículo Comercial (GTIN) durante la importación. |
    | Buscar asignación de cuentas | Especifique si debe buscarse una cuenta en **Asignación de cuentas** por texto entrante durante la importación. |
    | Validar dto. línea | Especifique si se debe validar un descuento de línea durante la importación. |
    | Aplicar dto. factura | Especifique si se debe aplicar un descuento de línea durante la importación. |
    | Comprobar totales | Especifique si el total de una factura debe verificarse durante la importación. |
    | Actualizar pedido | Especifique si se debe actualizar el pedido de compra correspondiente. |
    | Crear líneas de diario | Especifique si se debe crear una línea de diario en lugar de un documento de compra. Seleccione esta opción cuando desee utilizar diarios como destino de sus facturas. |
    | Nombre libro diario general | Especifique el nombre de la plantilla de diario general que se utiliza para la creación de líneas de diario. Este campo es aplicable cuando desee utilizar diarios como destino de sus facturas. |
    | Nombre sección diario general | Especifique el nombre del lote de diario general que se utiliza para la creación de líneas de diario. Este campo es aplicable cuando desee utilizar diarios como destino de sus facturas. |
    | Importación automática | Especifique si los documentos deben importarse automáticamente desde el servicio. |
    | Hora Inicio lote | Especifique la hora de inicio de los trabajos de importación. |
    | Minutos entre ejecuciones | Especifique el número de minutos entre ejecuciones de trabajos de importación. |

Si ha configurado el formato **Definición de intercambio de datos** en su localización, puede añadir una línea para cada tipo de documento que necesite. Sin embargo, primero debe seleccionar la opción **Tipo de Documento** para cada línea que necesite. Para cada tipo de datos, seleccione el valor de **Importar código de def. de intercambio de datos** o **Exportar código de def. de intercambio de datos** que desee usar.

Finalmente, si no utiliza el formato de **Definición de intercambio de datos** , puede configurar los formatos a través de las líneas **Exportar asignación** e **Importar asignación** , donde puede ubicar las tablas y campos para usar y configurar reglas de transformación, si corresponde.

## <a name="set-up-a-document-sending-profile"></a>Configurar un perfil de envío de documentos

Puede configurar un método preferido de envío de documentos de ventas para cada cliente. De esta manera, no tiene que seleccionar una opción de envío cada vez que selecciona la acción **Registrar y enviar** . En la página **Perfiles de envío de documentos**, puede establecer diferentes perfiles de envío y después seleccionar entre ellos en el campo **Perfil de envío de documentos** de una ficha de cliente. Puede seleccionar la casilla **Predeterminado** para especificar que un perfil de envío de documentos es el perfil predeterminado para todos los clientes, excepto para los clientes en los que el campo **Perfil de envío de documentos** esté configurado con un perfil de envío diferente.

Esta funcionalidad se utiliza para configurar la automatización de la facturación electrónica. Cuando selecciona **Registrar y enviar** en un documento de venta, el cuadro de diálogo **Registrar y enviar confirmación** muestra el perfil de envío usado, tanto el configurado para el cliente como el predeterminado para todos los clientes.

Siga estos pasos para configurar un perfil de envío de documentos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Perfil de envío de documentos** y luego seleccione el enlace relacionado.
2. En la página **Perfiles de envío de documentos**, seleccione **Nuevo**.
3. En la ficha desplegable **General**, introduzca cualquier información necesaria.
4. En la ficha desplegable **Opciones de envío**, configure los campos tal como se describe en la tabla siguiente.

    | Campo | Descripción |
    |-------|-------------|
    | Documento electrónico | Especifique si el documento se envía como un documento electrónico que el cliente puede importar en el sistema cuando selecciona **Registrar y enviar**. Para utilizar esta opción, también debe configurar el campo **Formato** o **Código de flujo de servicio de documentos electrónicos**. El archivo también se puede guardar en el disco. |
    | Formato | Especifique el formato que se utilizará para enviar un documento electrónico. Este campo es necesario si selecciona **A través del intercambio de documentos** en el campo **Documento electrónico**. |
    | Código flujo servicio documento electrónico | Especifique el flujo de servicio electrónico que se utiliza para enviar documentos. Este campo es necesario si selecciona **Flujo de servicio de documentos electrónicos ampliado** en el campo **Documento electrónico**. |

    > [!NOTE]
    > Si selecciona **Flujo de servicio de documentos electrónicos ampliado** en el campo **Documento electrónico** , debe tener ya configurado el flujo de trabajo para sus documentos electrónicos.

## <a name="set-up-the-workflow"></a>Configurar el flujo de trabajo

Siga estos pasos para configurar el flujo de trabajo que se utiliza en la funcionalidad de documentos electrónicos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plantillas de flujo de trabajo** y luego seleccione el enlace relacionado.
2. Si no encuentra **Plantillas de flujo de trabajo de documentos electrónicos** en la página **Plantillas de flujo de trabajo**, seleccione **Restablecer plantillas de Microsoft**. Debería aparecer **Plantillas de flujo de trabajo de documentos electrónicos**. Cierre la página.
3. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego seleccione el enlace relacionado.
4. Ejecute la acción **Nuevo flujo de trabajo desde plantilla** para seleccionar una plantilla para el proceso de documentos electrónicos. Las plantillas disponibles son **Enviar a un servicio** y **Enviar a varios servicios**.
5. Seleccione **Aceptar** para finalizar la configuración del flujo de trabajo.
6. En el campo **Respuesta entonces** , seleccione **Enviar documento electrónico usando la configuración** para configurar las respuestas del flujo de trabajo.
7. Seleccione el servicio de documentos electrónicos que creó como opción, seleccione **Aceptar** y luego habilite el flujo de trabajo.

> [!NOTE]
> Puede crear su propio flujo de trabajo para documentos electrónicos sin utilizar plantillas de flujo de trabajo predefinidas. Si tiene más servicios, puede utilizar diferentes flujos de trabajo.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Configurar una política de retención de documentos electrónicos

Los documentos electrónicos pueden estar sujetos a diferentes legislaciones locales relacionadas con el período de conservación de los documentos electrónicos. Por lo tanto, hemos agregado una configuración de política de retención para toda la información importante relacionada con los documentos electrónicos. Los administradores pueden definir políticas de retención que especifiquen con qué frecuencia Dynamics 365 Business Central elimina registros obsoletos relacionados con documentos electrónicos. Para obtener más información sobre las directivas de retención en, consulte [Definir directivas de retención](admin-data-retention-policies.md).

Para configurar políticas de retención relacionadas con documentos electrónicos, siga estos pasos.

1. En la página **Servicios de documentos electrónicos** , ejecute la acción **Directiva de retención** .
2. Cuando se complete la acción, seleccione una de las siguientes políticas de retención para configurar:

    - Registro documento electrónico
    - Registro de integración de documentos electrónicos
    - Registro de asignación de documentos electrónicos
    - Almacenamiento de datos de documentos electrónicos

## <a name="see-also"></a>Consulte también .

[Cómo usar documentos electrónicos en Business Central](finance-how-use-edocuments.md)  
[Cómo ampliar documentos electrónicos en Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestión financiera](finance.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Registrar compras con facturas de compra y pedidos](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
