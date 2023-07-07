---
title: Sincronizar clientes
description: Importar clientes desde o exportar a Shopify
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# Sincronizar clientes

Cuando un pedido se importa desde Shopify, es esencial obtener la información sobre el cliente para el procesamiento posterior del documento en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay dos opciones principales para ello y sus diversas combinaciones:

* Use un cliente especial para todos los pedidos.
* Importe la información real del cliente desde Shopify. Esta opción también está disponible cuando exporta clientes a Shopify primero desde [!INCLUDE[prod_short](../includes/prod_short.md)].

## Configuraciones importantes al importar clientes desde Shopify

Da igual si importa clientes desde Shopify de forma masiva o junto con la importación de pedidos, las siguientes configuraciones le permiten administrar el proceso:

|Campo|Descripción|
|------|-----------|
|**Importación de cliente desde Shopify**|Seleccione **Todos los clientes** si planea importar clientes desde Shopify de forma masiva; ya sea manualmente usando la acción **Sincronizar clientes** o a través de la cola de trabajos para actualizaciones periódicas. Independientemente de la selección, la información del cliente siempre se importará junto con el pedido. Sin embargo, el uso de esta información depende de las **Plantillas de clientes de Shopify** y los ajustes del campo **Tipo de asignación de cliente**.|
|**Tipo de asignación de cliente**|Defina cómo desea que el conector realice la asignación.<br>- **Por correo electrónico/teléfono** si desea que el conector asigne el cliente de Shopify importado a un cliente existente en [!INCLUDE[prod_short](../includes/prod_short.md)] utilizando el correo electrónico y el teléfono.</br>- **Por información de dirección de facturación** si desea que el conector use la dirección del destinatario de la factura para asignar el cliente de Shopify importado a un cliente existente en [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Seleccione **Tomar siempre el cliente predeterminado** si desea que el sistema utilice un cliente del campo **N.º de cliente predeterminado** . |
|**Shopify puede actualizar clientes**| Seleccione este campo si desea que el conector actualice los clientes que encuentra, cuando la opción **Por correo electrónico/teléfono** o **Por información de dirección de facturación** se ha seleccionado en el campo **Tipo de asignación de cliente**.|
|**Crear clientes desconocidos automáticamente**| Seleccione este campo si desea que el conector cree los clientes que falten cuando las opciones **Por correo electrónico/teléfono** o **Por información de dirección de facturación** se hayan seleccionado en el campo **Tipo de asignación de cliente**. Se creará un nuevo cliente usando datos importados y el **Código de plantilla de cliente** definido en las páginas **Ficha de tienda de Shopify** o **Plantilla de cliente de Shopify**. Tenga en cuenta que el cliente de Shopify debe tener al menos una dirección. A los pedidos creados a través del canal de ventas Shopify POS a menudo les faltan los detalles de la dirección. Si esta opción no está habilitada, deberá crear un cliente manualmente y vincularlo al cliente de Shopify.|
|**Código de plantilla de cliente**|Este campo se usa con **Creación automática de clientes desconocidos**.<br>- Elija la plantilla predeterminada que se utilizará para los clientes creados automáticamente. Asegúrese de que la plantilla seleccionada contenga los campos obligatorios, como los campos **Grupo de registro de negocio general**, **Grupo de registro de clientes**, y el IVA o los campos relacionados con impuestos.<br>- Puede definir plantillas por país o región en la página **Plantillas de clientes de Shopify**, que es útil para el cálculo de impuestos adecuado. <br>- Obtenga más información en [Configurar impuestos](setup-taxes.md).|

### Plantilla de cliente por país

Algunas configuraciones se pueden definir en el nivel de país o región, o en el nivel de estado o provincia. Los ajustes se pueden configurar en [Envío y entrega](https://www.shopify.com/admin/settings/shipping) en Shopify.

Puede hacer lo siguiente para cada cliente mediante la **Plantilla de cliente de Shopify**:

1. Especificar el **N.º de cliente genérico**, que tiene prioridad sobre la selección en los campos **Importación de clientes desde Shopify** y **Tipo de asignación de cliente**. Se utiliza en el pedido de venta importado.
2. Defina el **Código de plantilla de cliente**, que se utiliza para crear clientes que falten si se ha habilitado **Crear clientes desconocidos automáticamente**. Si el **Código de plantilla de cliente** está vacío, entonces la función usa el **Código de plantilla de cliente** definido en la **Ficha de tienda de Shopify**. El sistema primero intenta encontrar una plantilla para el **Código de país/región** para la dirección predeterminada. Si no encuentra una plantilla, utiliza la primera dirección.
3. En algunos casos, el **Código de plantilla de cliente** definido para un país no es suficiente para garantizar cálculos correctos de impuestos (por ejemplo, para países con impuesto sobre las ventas). En este caso, incluir **Área fiscal** podría ser una adición útil.
4. El campo **Zona fiscal** también contiene una pareja de **Código de país** y **Nombre de provincia**. Este par es útil cuando el conector necesita convertir un código en un nombre, o viceversa.

> [!NOTE]  
> Los códigos de país son códigos de país ISO 3166-1 alfa-2. Obtenga más información en [Código de país](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Exportar clientes a Shopify

Puede explotar los clientes existentes a Shopify de forma masiva. En cada caso, se crean un cliente y una dirección predeterminadas. Puede gestionar el proceso con las siguientes configuraciones:

|Campo|Descripción|
|------|-----------|
|**Exportar clientes a Shopify**|Seleccione esta opción si tiene previsto exportar todos los clientes de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify en masa. Puede hacerlo manualmente, usando la acción **Sincronizar clientes**, o automáticamente, usando una cola de trabajos para actualizaciones recurrentes.<br> Al exportar clientes con direcciones que incluyen provincias/estados, asegúrese de que **Código ISO** se rellena para países/regiones.|
|**Puede actualizar clientes de Shopify**|Se usa junto con el ajuste **Exportar cliente a Shopify**. Habilite esta opción si desea generar actualizaciones más tarde desde [!INCLUDE[prod_short](../includes/prod_short.md)] para los clientes que ya existen en Shopify.|

Los siguientes son requisitos para exportar un cliente:

* El cliente debe tener una dirección de correo electrónico válida.
* Se selecciona un país/región en la tarjeta de cliente, para clientes locales, con país/región en blanco el país/región especificado en la página **Información de la empresa** debe tener un código ISO definido.
* Si el cliente tiene un número de teléfono, el número debe ser único porque Shopify no aceptará un segundo cliente con el mismo número de teléfono.
* Si el cliente tiene un número de teléfono, debe estar en el formato E.164. Se admiten diferentes formatos si representan un número que se puede marcar desde cualquier parte del mundo. Los siguientes formatos son válidos:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Una vez que haya creado los clientes en Shopify, puedes enviarles invitaciones directas animándolos a activar sus cuentas.

### Rellenar la información del cliente en Shopify

Un cliente en Shopify tiene nombre, apellido, correo electrónico y número de teléfono. Puede introducir el nombre y los apellidos a partir de los datos de la ficha del cliente en [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioridad|Campo en la ficha de cliente|Descripción|
|------|------|-----------|
|1|**Nombre contacto**|Máxima prioridad, si el campo **Nombre de contacto** está lleno y el campo **Origen de contacto** en la **Ficha de tienda de Shopify** contiene la opción *Nombre y apellido* o *Apellido y nombre* para definir cómo dividir los valores.|
|2|**Nombre 2**|Si el campo **Nombre 2** está lleno y el campo **Origen de nombre 2** en la **Ficha de tienda de Shopify** contiene la opción *Nombre y apellido* o *Apellido y nombre* para definir cómo dividir los valores.|
|3|**Nombre**|Prioridad más baja, si el campo **Nombre** está lleno y el campo **Origen de nombre** en la **Ficha de tienda de Shopify** contiene la opción *Nombre y apellido* o *Apellido y nombre* para definir cómo dividir los valores.|

Un cliente en Shopify también tiene una dirección predeterminada. Esta dirección puede contener una empresa y dirección además de su nombre, apellido, correo electrónico o teléfono. Puede rellenar el campo **Empresa** en función de los datos de la ficha de cliente en [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioridad|Campo en la ficha de cliente|Descripción|
|------|------|-----------|
|1|**Nombre**|Máxima prioridad, si el campo **Origen de nombre** en la **Ficha de tienda de Shopify** contiene *Nombre de empresa*.|
|2|**Nombre 2**|Prioridad más baja, si el campo **Origen de nombre 2** en la **Ficha de tienda de Shopify** contiene *Nombre de empresa*.|

Para las direcciones en las que se utiliza la provincia, seleccione **Código** o **Nombre** en el campo **Origen de provincia**, en la página **Tarjeta de tienda de Shopify**. El código o el nombre especifica el tipo de datos almacenados en [!INCLUDE[prod_short](../includes/prod_short.md)], en el campo **Provincia**. Recuerde inicializar las plantillas de clientes por país, para que el mapeo de código/nombre de provincia esté listo. 


## Sincronizar clientes

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda específica para la que desea sincronizar los clientes.
3. Seleccione la acción **Sincronizar clientes**.

Como alternativa, use la acción **Iniciar sincronización de cliente** en la ventana **Clientes de Shopify** o buscar el trabajo por lotes **Sincronizar clientes**.

Puede programar la tarea para que se realice de forma automatizada. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

## Consulte también .

[Comenzar con el conector para Shopify](get-started.md)  
