---
title: Configurar documentos electrónicos
description: Aprenda a configurar la funcionalidad de documentos electrónicos.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 04/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Configurar documentos electrónicos

> [!IMPORTANT]
> El módulo principal de E-Documents es un marco. De forma predeterminada, no hay ningún campo **Integración de servicio**. Si encuentra las opciones de **Formato de documento** de forma predeterminada, tenga en cuenta que se ofrecen a modo de ejemplo y que la localización debe proporcionar un formato detallado. Estos detalles forman parte de las aplicaciones de localización, porque son específicos de los requisitos locales.

> [!NOTE]
> A partir de la versión 23.2 se añade un formato de documento estándar PEPPOL como formato global en el campo **Formato de documento**. Tenga en cuenta que probablemente no pueda utilizar este formato tal como está. Se trata de un formato W1 que se proporciona para mostrar cómo usar esta característica. Le recomendamos que pruebe el formato PEPPOL existente antes de empezar a usar este formato.

El primer paso en la configuración de documentos electrónicos (e-documents) es configurar el Servicio de documentos electrónicos donde se define el comportamiento completo de su sistema en relación con la comunicación de documentos electrónicos.

## Configurar el servicio de documentos electrónicos

Siga estos pasos para configurar el Servicio de documentos electrónicos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios de documentos electrónicos** y luego seleccione el enlace relacionado.
2. Seleccione **Nuevo** y, a continuación, en la página **Servicios de documentos electrónicos**, en la ficha desplegable **General**, configure los campos tal y como se describen en la siguiente tabla.

    | Campo | Descripción |
    |-------|-------------|
    | Código | Seleccione el código de configuración de la exportación electrónica. |
    | Descripción | Especifique una breve descripción de la configuración de la exportación electrónica. |
    | Formato de documento | <p>El formato de exportación de la configuración de exportación electrónica.</p><p>De forma predeterminada, hay dos opciones en este campo. Puede seleccionar **PEPPOL BIS 3** como formato genérico basado en códigos o **Intercambio de datos** cuando deba configurar documentos previos de formatos específicos en la ficha desplegable **Definición de intercambio de datos**.</p> |
    | Integración de servicio | Seleccione el código de integración de la configuración de exportación electrónica. En el lanzamiento 1, la única opción es **Sin integración**. |
    | Usar procesamiento por lotes | Especifique si el servicio usa procesamiento por lotes para la exportación. |

3. En la ficha desplegable **Parámetros importados**, configure los campos tal como se describe en la tabla siguiente.

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

4. Si ha seleccionado **Intercambio de datos** en el campo **Formato de documento** de la ficha desplegable **General**, use la ficha desplegable **Definición de intercambio de datos** para configurar los siguientes campos.

    | Campo | Descripción |
    |-------|-------------|
    | Tipo documento | Especifique el tipo de documento que usa el intercambio de datos para importar y exportar los datos. Los ejemplos incluyen **Factura de venta**, **Nota de abono de venta** y **Factura de compra**. |
    | Importar cód. def. intercambio datos | Especifique el código de intercambio de datos que se usa para importar los datos. Solo use este campo para recibir un documento en el proceso de compra. |
    | Exportar código def. intercambio datos | Especifique el código de intercambio de datos que se usa para exportar los datos. Solo use este campo para entregar documentos en el proceso de venta. |

> [!NOTE]
> Existen definiciones de intercambio de datos preparadas para el formato PEPPOL que están relacionadas con el documento estándar de venta y compra. Sin embargo, es probable que no pueda usar estas definiciones tal cual. Todos son formatos W1 que se proporcionan para mostrar cómo usar esta característica. Le recomendamos que pruebe el formato PEPPOL existente antes de empezar a usarlo.

Si ha configurado el formato **Definición de intercambio de datos** en su localización, puede añadir una línea para cada tipo de documento que necesite. Agregue líneas que coincidan con el ejemplo de intercambio de datos predeterminado para el formato W1 PEPPOL. Sin embargo, primero seleccione la opción **Tipo de Documento** para cada línea que necesite. Para cada tipo de datos, seleccione el valor de **Importar código de def. de intercambio de datos** o **Exportar código de def. de intercambio de datos** que desee usar.

Si no usa el formato **Definición de intercambio de datos**, puede crear y configurar formatos utilizando la [interfaz](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments). Ajuste la información en las líneas **Asignación de exportación** y **Asignación de importación**, donde encontrará las tablas y los campos para configurar las reglas de transformación. En este caso, debe agregar una nueva opción en el campo **Formato de documento** que esté relacionada con su formato.  

### Tipos de documento admitidos 

Los tipos de documentos admitidos se basan en el **formato de documento**. Para comprobar qué tipos de documentos son compatibles, en la página **Servicios de documentos electrónicos**, elija la acción **Tipos de documentos admitidos**. Se abre **Tipos de documentos de origen admitidos por el servicio de documentos electrónicos** y en la columna **Tipo de documento de origen**, podrá elegir diferentes tipos de documentos para que sean compatibles con el formato que piensa utilizar. Asegúrese de no utilizar el tipo de documento si ese documento no está seleccionado en esta página.   

## Configurar un perfil de envío de documentos

Puede configurar un método preferido de envío de documentos de ventas para cada cliente. De esta manera, no tiene que elegir una opción de envío cuando elige la acción **Registrar y enviar**. En la página **Perfiles de envío de documentos**, puede establecer diferentes perfiles de envío y después seleccionar entre ellos en el campo **Perfil de envío de documentos** de una ficha de cliente. Puede seleccionar la casilla **Predeterminado** para especificar que un perfil de envío de documentos es el perfil predeterminado para todos los clientes, excepto para los clientes en los que el campo **Perfil de envío de documentos** esté configurado con un perfil de envío diferente.

Esta funcionalidad se utiliza para configurar la automatización de la facturación electrónica. Cuando elige **Registrar y enviar** en un documento de venta, el cuadro de diálogo **Registrar y enviar confirmación** muestra el perfil de envío usado, tanto el configurado para el cliente como el predeterminado para todos los clientes.

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

## Configurar el flujo de trabajo

Siga estos pasos para configurar el flujo de trabajo que se utiliza en la funcionalidad de documentos electrónicos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plantillas de flujo de trabajo** y luego seleccione el enlace relacionado.
2. Si no encuentra **Plantillas de flujo de trabajo de documentos electrónicos** en la página **Plantillas de flujo de trabajo**, seleccione **Restablecer plantillas de Microsoft**. Debería aparecer **Plantillas de flujo de trabajo de documentos electrónicos**. Cierre la página.
3. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego seleccione el enlace relacionado.
4. Elija la acción **Nuevo flujo de trabajo desde plantilla** para seleccionar una plantilla para el proceso de documentos electrónicos. Las plantillas disponibles son **Enviar a un servicio** y **Enviar a varios servicios**.
5. Seleccione **Aceptar** para finalizar la configuración del flujo de trabajo.
6. En el campo **Respuesta entonces** , seleccione **Enviar documento electrónico usando la configuración** para configurar las respuestas del flujo de trabajo.
7. Seleccione el servicio de documentos electrónicos que creó como opción, elija **Aceptar** y luego habilite el flujo de trabajo.

> [!NOTE]
> Puede crear su propio flujo de trabajo para documentos electrónicos sin utilizar plantillas de flujo de trabajo predefinidas. Si tiene más servicios, puede utilizar diferentes flujos de trabajo.

Para usar más flujos de trabajo, configúrelos a través de los perfiles de envío de documentos para distintos clientes. Cuando configure el flujo de trabajo, especifique el perfil de envío de documentos en la columna **Condición On** de la ficha desplegable **Pasos del flujo de trabajo**, porque no puede tener dos servicios que usen el mismo perfil de envío de documentos en los flujos de trabajo.

Cuando configure su flujo de trabajo en la página **Flujos de trabajo**, señale el campo **Condición On** en la ficha desplegable **Pasos de flujo de trabajo**. En la página **Condiciones del evento**, en el campo **Filtro**, seleccione el perfil de envío de documentos que desea usar.

## Configurar una política de retención de documentos electrónicos

Los documentos electrónicos pueden estar sujetos a diferentes legislaciones locales relacionadas con el período de conservación de los documentos electrónicos. Por lo tanto, hemos agregado una configuración de política de retención para toda la información importante relacionada con los documentos electrónicos. Los administradores pueden definir políticas de retención que especifiquen con qué frecuencia Dynamics 365 Business Central elimina registros obsoletos relacionados con documentos electrónicos. Para obtener más información sobre las directivas de retención en, consulte [Definir directivas de retención](admin-data-retention-policies.md).

Para configurar políticas de retención relacionadas con documentos electrónicos, siga estos pasos.

1. En la página **Servicios de documentos electrónicos**, elija la acción **Directiva de retención** .
2. Cuando se complete la acción, seleccione una de las siguientes políticas de retención para configurar:

    - Registro documento electrónico
    - Registro de integración de documentos electrónicos
    - Registro de asignación de documentos electrónicos
    - Almacenamiento de datos de documentos electrónicos

## Datos de demostración de documentos electrónicos  

> [!NOTE]
> A partir de Business Central 24.0, es posible configurar datos de demostración para documentos electrónicos.

Para proporcionar formas más sencillas de probar y demostrar las capacidades de **Documentos electrónicos**, Microsoft creó un nuevo módulo de demostración para documentos electrónicos. Para habilitar este módulo, siga los pasos:  

1.  Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Herramienta de demostración de Contoso** y luego seleccione el vínculo relacionado.  
2.  Antes de habilitar el **Módulo Contoso de documentos electrónicos**, debido a las dependencias, debe haber habilitado los siguientes módulos: **Módulo común** y **Módulo de Almacén**. 
3.  Después de habilitar estos módulos, seleccione el **Módulo Contoso de documentos electrónicos** y luego elija la acción **Generar**. 
4.  Siga los pasos.  
5.  Cierre la página.   

Una vez que tenga un módulo habilitado, habrá creado nuevos elementos de demostración, habrá importado seis documentos electrónicos (basados ​​en Peppol BIS 3) y ya habrá configurado el **Servicios de documentos electrónicos** con los flujos de trabajo creados.  

## Consulte también

[Cómo usar documentos electrónicos en ventas](finance-how-use-edocuments.md)    
[Cómo usar documentos electrónicos en compras](finance-how-use-edocuments-purchase.md)  
[Cómo ampliar documentos electrónicos en Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Gestión financiera](finance.md)    
[Facturar ventas](sales-how-invoice-sales.md)    
[Registrar compras con facturas de compra y pedidos](purchasing-how-record-purchases.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
