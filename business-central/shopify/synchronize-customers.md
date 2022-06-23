---
title: Sincronizar clientes
description: Importar clientes desde o exportar a Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 75c4de7736572ff923c74464dc33b218d0665e3f
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808870"
---
# <a name="synchronize-customers"></a>Sincronizar clientes

Cuando un pedido se importa desde Shopify, la información sobre los clientes es esencial para el procesamiento posterior del documento en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay dos opciones principales y sus combinaciones:

* Use el cliente especial para todos los pedidos.
* Importe la información real del cliente desde Shopify. Esta opción también está disponible cuando exporta clientes a Shopify desde [!INCLUDE[prod_short](../includes/prod_short.md)] primero.

## <a name="how-connector-chooses-which-customer-to-use"></a>Cómo el conector elige qué cliente usar

La función *Importar pedido de Shopify* intenta seleccionar el cliente en el siguiente orden:

1. Si el **N.º de cliente genérico** el campo se define en la **Plantilla de cliente de Shopify** para el país correspondiente, se usa el **N.º de cliente genérico** independientemente de los ajustes en **Importación de cliente desde Shopify** y **Tipo de asignación de cliente**. Para obtener más información, consulte [Plantilla de clientes por país](synchronize-customers.md#customer-template-per-country).
2. Si **Importación de clientes desde Shopify** está establecido como *Ninguno* y **N.º de cliente genérico** se define en la **Shopify Tarjeta de tienda**, luego el **N.º de cliente genérico** .

Los próximos pasos dependen del **Tipo de asignación de cliente**.

* **Tomar siempre el cliente predeterminado**, luego use el cliente definido en el campo **N.º de cliente génerico** en la ventana **Ficha de tienda de Shopify**.
* **Por correo electrónico/teléfono**, el conector intenta encontrar el cliente existente primero por id., luego por correo electrónico y luego por teléfono. Si no se encuentra el cliente, el conector crea un nuevo cliente.
* **Por info. de dirección de facturación**, el conector intenta encontrar el cliente existente primero por id. y luego por información de dirección de facturación. Si no se encuentra, el conector crea un nuevo cliente.

> [!NOTE]  
> El conector utiliza la información de la dirección de facturación y crea el cliente de facturación en [!INCLUDE[prod_short](../includes/prod_short.md)]. El cliente de venta es igual al cliente de facturación.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Configuraciones importantes al importar clientes desde Shopify

Da igual si importa clientes desde Shopify de forma masiva o junto con la importación de pedidos, las siguientes configuraciones le permiten administrar el proceso:

|Campo|Descripción|
|------|-----------|
|**Importación de cliente desde Shopify**|Seleccione **Todos los clientes** si planea importar clientes desde Shopify de forma masiva; ya sea manualmente usando la acción **Sincronizar clientes** o a través de la cola de trabajos para actualizaciones periódicas. Independientemente de la selección, la información del cliente siempre se importará junto con el pedido. Sin embargo, el uso de esta información depende de las **Plantillas de clientes de Shopify** y los ajustes en el campo **Tipo de asignación de cliente**.|
|**Tipo de asignación de cliente**|Defina cómo desea que el conector realice la asignación.<br>- **Por correo electrónico/teléfono** si desea que el conector asigne el cliente de Shopify importado a un cliente existente en [!INCLUDE[prod_short](../includes/prod_short.md)] utilizando el correo electrónico y el teléfono.</br>- **Por info. de dirección de facturación** si desea que el conector asigne el cliente de Shopify importado a un cliente existente en [!INCLUDE[prod_short](../includes/prod_short.md)] utilizando la información de la dirección que recibe la factura.</br>Seleccione **Tomar siempre el cliente predeterminado** si desea que el sistema utilice un cliente del campo **N.º de cliente genérico** . |
|**Shopify puede actualizar clientes**| Seleccione si desea que el conector actualice los clientes que se encuentran, cuando las opciones **Por correo electrónico/teléfono** o **Por info. de dirección de facturación** se han seleccionado en el campo **Tipo de asignación de cliente**.|
|**Crear clientes desconocidos automáticamente**| Seleccione si desea que el conector cree los clientes que falten cuando las opciones **Por correo electrónico/teléfono** o **Por info. de dirección de facturación** se han seleccionado en el campo **Tipo de asignación de cliente**. Se creará un nuevo cliente usando datos importados y el **Código de plantilla de cliente** definido en las páginas **Ficha de tienda de Shopify** o **Plantilla de cliente de Shopify**. Tenga en cuenta que el cliente de Shopify debe tener al menos una dirección. Si esta opción no está habilitada, deberá crear el cliente manualmente y vincularlo al cliente de Shopify. Siempre puede iniciar la creación de un cliente manualmente desde la página **Pedido de Shopify**.|
|**Código de plantilla de cliente**|Se usa con **Creación automática de clientes desconocidos**.<br> Elija la plantilla predeterminada que se utilizará para los clientes creados automáticamente. Puede definir plantillas por país o región en la ventana **Plantillas de clientes de Shopify**, que es útil para el cálculo de impuestos adecuado. Para obtener más información, consulte [Observaciones sobre impuestos](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Plantilla de cliente por país

Algunas configuraciones se pueden definir a nivel de país o región, o a nivel de estado o provincia. Los ajustes se pueden configurar en [Envío y entrega](https://www.shopify.com/admin/settings/shipping) en Shopify.

La **Plantilla de cliente de Shopify** le permite hacer lo siguiente para cada país:

1. Especificar el **N.º de cliente genérico**, que tiene prioridad sobre la selección en los campos **Importación de clientes desde Shopify** y **Tipo de asignación de cliente**. Se utiliza en el pedido de venta importado.
2. Definir el **Código de plantilla de cliente**, que se utiliza para crear clientes que falten si se ha habilitado **Crear clientes desconocidos automáticamente**. Si el **Código de plantilla de cliente** está vacío, entonces la función usa el **Código de plantilla de cliente** definido en la **Ficha de tienda de Shopify**.
3. En algunos casos, el **Código de plantilla de cliente** por país no es suficiente para garantizar el cálculo correcto de los impuestos. Por ejemplo, para países con impuesto sobre las ventas.

> [!NOTE]  
> Los códigos de país son códigos de país ISO 3166-1 alfa-2. Para obtener más información, consulte [Código de país](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Exportar clientes a Shopify

Los clientes existentes se pueden exportar a Shopify de forma masiva. Como resultado, se crean un cliente y una dirección predeterminadas. Puede administrar el proceso con la ayuda de los siguientes ajustes:

|Campo|Descripción|
|------|-----------|
|**Exportar clientes a Shopify**|Seleccione si planea importar todos clientes con una dirección de correo electrónico válida desde [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify de forma masiva usando la acción **Sincronizar clientes** o mediante una cola de trabajos para actualizaciones periódicas.|
|**Puede actualizar clientes de Shopify**|Se usa junto con **Exportar cliente a Shopify**. Habilite la opción si desea generar actualizaciones más tarde desde [!INCLUDE[prod_short](../includes/prod_short.md)] para los clientes que ya existen en Shopify.|

> [!NOTE]  
> Una vez que hayan creado clientes en Shopify, es posible que desee enviar invitaciones directas a los clientes. Les animará a activar su cuenta.

### <a name="populate-customer-information-in-shopify"></a>Rellenar la información del cliente en Shopify

Un cliente en Shopify tiene nombre, apellido, correo electrónico y número de teléfono. Puede completar el nombre y el apellido a partir de los datos de la ficha del cliente en [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioridad|Campo en la ficha cliente|Descripción|
|------|------|-----------|
|1|**Nombre contacto**|Máxima prioridad, si el campo **Nombre de contacto** está lleno y el campo **Origen de contacto** en la **Ficha de tienda de Shopify** contiene las opciones *Nombre y apellido* o *Apellido y nombre*, lo que define cómo dividir los valores.|
|2|**Nombre 2**|Si el campo **Nombre 2** está lleno y el campo **Origen de nombre 2** en la **Ficha de tienda de Shopify** contiene las opciones *Nombre y apellido* o *Apellido y nombre*, lo que define cómo dividir los valores.|
|3|**Nombre**|Prioridad más baja, si el campo **Nombre** está lleno y el campo **Origen de nombre** en la **Ficha de tienda de Shopify** contiene las opciones *Nombre y apellido* o *Apellido y nombre*, lo que define cómo dividir los valores.|

Un cliente en Shopify también tiene una dirección predeterminada, que además del nombre, apellido, correo electrónico o teléfono puede contener empresa y dirección. Puede rellenar el campo **Empresa** en función de los datos de la ficha cliente en [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioridad|Campo en la ficha cliente|Descripción|
|------|------|-----------|
|1|**Nombre**|Máxima prioridad, si el campo **Origen de nombre** en la **Ficha de tienda de Shopify** contiene *Nombre de empresa*.|
|2|**Nombre 2**|Prioridad más baja, si el campo **Origen de nombre 2** en la **Ficha de tienda de Shopify** contiene *Nombre de empresa*.|

Para las direcciones en las que se utiliza el país o la provincia, seleccione *Código* o *Nombre* en el campo **Origen de país** en la **Ficha de tienda de Shopify** para especificar qué tipo de datos se almacenan en [!INCLUDE[prod_short](../includes/prod_short.md)] en el campo **País**.

## <a name="sync-customers"></a>Sincronizar clientes

1. Vaya al icono de búsqueda ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer"). , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar los clientes para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar clientes**.

Como alternativa, puede usar la acción **Iniciar sincronización de cliente** en la ventana **Clientes de Shopify** o buscar el trabajo por lotes **Sincronizar clientes**.

Puede programar la tarea para que se realicen de forma automatizada. Para obtener más información, consulte [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
