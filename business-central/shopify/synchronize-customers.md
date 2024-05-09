---
title: Sincronizar clientes
description: Importar clientes desde o exportar a Shopify
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# Sincronizar clientes y empresas

Cuando un pedido se importa desde Shopify, es esencial obtener la información sobre el cliente para el procesamiento posterior del documento en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay dos opciones principales para ello y sus diversas combinaciones:

* Use un cliente especial para todos los pedidos.
* Importe la información del cliente desde Shopify. Esta opción también está disponible cuando exporta clientes a Shopify desde [!INCLUDE[prod_short](../includes/prod_short.md)].

Shopify le permite administrar su negocio B2B y DTC desde un solo lugar con el poder y la facilidad de la plataforma todo en uno de Shopify. El conector de Shopify también funciona con diferentes tipos de comercio electrónico.

Shopify tiene dos entidades, cliente y empresa, pero [!INCLUDE[prod_short](../includes/prod_short.md)] solo tiene la entidad del cliente, lo que afecta el funcionamiento de la sincronización.

Cuando ejecuta DTC, el comprador se crea en Shopify como cliente. Luego, el cliente es importado a [!INCLUDE[prod_short](../includes/prod_short.md)] como un cliente de Shopify y vinculado o convertido a un cliente.

Si ejecuta B2B, el comprador se crea en Shopify como cliente vinculado a una empresa. El cliente es importado a [!INCLUDE[prod_short](../includes/prod_short.md)] como un cliente de Shopify, y la empresa es importada a [!INCLUDE[prod_short](../includes/prod_short.md)] como una empresa de Shopify y vinculado o convertido a un cliente.

Para exportar un cliente desde [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, los pasos son ligeramente diferentes dependiendo de lo que quiera hacer:

* Exportar un cliente como cliente Shopify para DTC.
* Exporte un cliente como par de empresa y cliente para el flujo B2B.

## Configuraciones importantes al importar clientes DTC desde Shopify

Da igual si importa clientes desde Shopify de forma masiva o junto con la importación de pedidos, las siguientes configuraciones le permiten administrar el proceso:

|Campo|Descripción|
|------|-----------|
|**Importación de cliente desde Shopify**|Seleccione **Todos los clientes** si planea importar clientes desde Shopify de forma masiva; ya sea manualmente usando la acción **Sincronizar clientes** o a través de la cola de trabajos para actualizaciones periódicas. Independientemente de la selección, la información del cliente siempre se importará junto con el pedido. Sin embargo, el uso de esta información depende de las **Plantillas de clientes de Shopify** y los ajustes del campo **Tipo de asignación de cliente**.|
|**Tipo de asignación de cliente**|Defina cómo desea que el conector realice la asignación.</br></br>- **Por correo electrónico/teléfono** si desea que el conector use la información de la cuenta de correo electrónico y teléfono para asignar el cliente importado de Shopify a un cliente en Business Central.</br></br>- **Por información de dirección de facturación** si desea que el conector use la dirección del destinatario de la factura para asignar el cliente de Shopify importado a un cliente existente en Business Central.</br></br>Seleccione **Tomar siempre el cliente predeterminado** si desea que el sistema utilice un cliente del campo **N.º de cliente predeterminado** . |
|**Shopify puede actualizar clientes**| Seleccione este campo si desea que el conector actualice los clientes que encuentra, cuando la opción **Por correo electrónico/teléfono** o **Por información de dirección de facturación** se ha seleccionado en el campo **Tipo de asignación de cliente**.|
|**Crear clientes desconocidos automáticamente**| Seleccione este campo si desea que el conector cree los clientes que falten cuando las opciones **Por correo electrónico/teléfono** o **Por información de dirección de facturación** se hayan seleccionado en el campo **Tipo de asignación de cliente**. Se creará un nuevo cliente usando datos importados y el **Código de plantilla de cliente** definido en las páginas **Ficha de tienda de Shopify** o **Plantilla de cliente de Shopify**. Tenga en cuenta que el cliente de Shopify debe tener al menos una dirección. A los pedidos creados a través del canal de ventas Shopify POS a menudo les faltan los detalles de la dirección. Si esta opción no está habilitada, deberá crear un cliente manualmente y vincularlo al cliente de Shopify.|
|**Código plantilla cliente/empresa**|Este campo se usa con **Creación automática de clientes desconocidos**.</br></br> Elija la plantilla predeterminada que se utilizará para los clientes creados automáticamente. Asegúrese de que la plantilla seleccionada contenga los campos obligatorios, como los campos **Grupo de registro de negocio general**, **Grupo de registro de clientes**, y el IVA o los campos relacionados con impuestos.</br></br>Puede definir plantillas por país o región en la página **Plantillas de clientes de Shopify**, que es útil para el cálculo de impuestos adecuado.</br></br>Obtenga más información en [Configurar impuestos](setup-taxes.md).|

### Plantilla de cliente por país o región

Algunas configuraciones se pueden definir en el nivel de país o región, o en el nivel de estado o provincia. Los ajustes se pueden configurar en [Envío y entrega](https://www.shopify.com/admin/settings/shipping) en Shopify.

Puede hacer lo siguiente para cada cliente mediante la **Plantilla de cliente de Shopify**:

1. Especificar el **N.º de cliente genérico**, que tiene prioridad sobre la selección en los campos **Importación de clientes desde Shopify** y **Tipo de asignación de cliente**. Se utiliza en el pedido de venta importado.
2. Defina el **Código de plantilla de cliente**, que se utiliza para crear clientes que falten si se ha habilitado **Crear clientes desconocidos automáticamente**. Si el **Código de plantilla de cliente** está vacío, entonces la función usa el **Código de plantilla de cliente** definido en la **Ficha de tienda de Shopify**. El sistema primero intenta encontrar una plantilla para el **Código de país/región** para la dirección predeterminada. Si no encuentra una plantilla, utiliza la primera dirección.
3. En algunos casos, el **Código de plantilla de cliente** definido para un país o región no es suficiente para garantizar cálculos correctos de impuestos (por ejemplo, para países o regiones con impuesto sobre las ventas). En este caso, incluir **Área fiscal** podría ser una adición útil.
4. El campo **Zona fiscal** también contiene una pareja de **Código de país** y **Nombre de provincia**. Este par es útil cuando el conector necesita convertir un código en un nombre, o viceversa.

> [!NOTE]  
> Los códigos de país son códigos de país ISO 3166-1 alfa-2. Obtenga más información en [Código de país](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Configuraciones importantes al exportar clientes de DTC a Shopify

Puede explotar los clientes existentes a Shopify de forma masiva. En cada caso, se crean un cliente y una dirección predeterminadas. Puede gestionar el proceso con las siguientes configuraciones:

|Campo|Descripción|
|------|-----------|
|**Puede actualizar clientes de Shopify**| Habilite la opción si desea generar actualizaciones más tarde desde Business Central para los clientes que ya existen en Shopify.|

Los siguientes son requisitos para exportar un cliente:

* El cliente debe tener una dirección de correo electrónico válida.
* Al exportar clientes con direcciones que incluyen provincias/estados, asegúrese de que **Código ISO** se rellena para países/regiones.|
* Para el país/región seleccionado en la tarjeta de cliente, asegúrese de que **Código ISO**. Para clientes locales, con país o región en blanco, el conector Shopify utiliza el país o región especificado en la **Información de la empresa**.
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

Para las direcciones en las que se utiliza la provincia, seleccione **Código** o **Nombre** en el campo **Origen de provincia**, en la página **Tarjeta de tienda de Shopify**. El código o el nombre especifica el tipo de datos almacenados en [!INCLUDE[prod_short](../includes/prod_short.md)], en el campo **Provincia**. Recuerde inicializar las plantillas de clientes por país o región, para que la asignación de código/nombre de provincia esté listo. 

## Exportar clientes DTC a Shopify

### Sincronización inicial de clientes de Business Central a Shopify

1. Vaya al icono de búsqueda ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer"). , escriba **Clientes de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Agregar cliente**.
3. En el campo **Código de tienda**, escriba el código. Si abre la ventana **Clientes de Shopify** de la página **Tarjeta de tienda**, el código de tienda se completará automáticamente.
4. Defina filtros en clientes según sea necesario. Por ejemplo, puede filtrar por código de país o región.
5. Elija **Aceptar**.

Los clientes resultantes se crean automáticamente en Shopify con direcciones.

> [!NOTE]  
> La sincronización inicial de clientes de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify no tiene en cuenta la configuración **Puede actualizar clientes de Shopify**.

### Sincronizar clientes

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda específica para la que desea sincronizar los clientes.
3. Seleccione la acción **Sincronizar clientes**.

Como alternativa, use la acción **Iniciar sincronización de cliente** en la ventana **Clientes de Shopify** o buscar el trabajo por lotes **Sincronizar clientes**.

Puede programar la tarea para que se realice de forma automatizada. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

## Empresas B2B

Si utilizas B2B en Shopify, además de clientes también puedes crear empresas. Puede vincular uno o más clientes individuales a una empresa. También puede definir condiciones de pago, ubicaciones y catálogos.

## Configuraciones importantes al importar empresas B2B desde Shopify

Da igual si importa clientes desde Shopify de forma masiva o junto con la importación de pedidos, use la configuración de la tabla siguiente para administrar el proceso.

|Campo|Descripción|
|------|-----------|
|**Importación de empresa desde Shopify**|Seleccione **Todas las empresas** si planea importar clientes desde Shopify de forma masiva; ya sea manualmente usando la acción **Sincronizar empresas** o a través de la cola de trabajos para actualizaciones periódicas. Independientemente de la selección, la información del cliente siempre se importará junto con el pedido. Sin embargo, el uso de esta información depende de las **Plantillas de empresa de Shopify** y los ajustes del campo **Tipo de asignación de empresa**.|
|**Tipo de asignación de empresa**|Defina cómo desea que el conector realice la asignación.</br></br>- **Por correo electrónico/teléfono** si desea que el conector asigne las empresas importadas de Shopify a un cliente existente en Business Central utilizando el correo electrónico y el teléfono para el contacto principal.</br></br>- Seleccione **Tomar siempre la empresa predeterminada** si desea que el sistema utilice una empresa del campo **N.º de empresa predeterminada** . |
|**Shopify puede actualizar empresa**| Seleccione este campo si desea que el conector actualice los clientes que encuentra, cuando la opción **Por correo electrónico/teléfono** está seleccionada en el campo **Tipo de asignación de empresa**.|
|**Crear empresas desconocidas automáticamente**| Seleccione este campo si desea que el conector cree nuevos clientes, cuando la opción **Por correo electrónico/teléfono** está seleccionada en el campo **Tipo de asignación de empresa**. Se creará un nuevo cliente usando datos importados y el **Código de plantilla de cliente/empresa** definido en las páginas **Ficha de tienda de Shopify** o **Plantilla de cliente de Shopify**.|
|**Código plantilla cliente/empresa**|Este campo se usa con **Creación automática de empresas desconocidas**.</br></br>- Elija la plantilla predeterminada que se utilizará para los clientes creados automáticamente. Asegúrese de que los campos obligatorios de la plantilla estén rellenados, como los campos **Grupo de registro de negocio general**, **Grupo de registro de clientes**, y el **Impuesto del valor añadido (IVA)** u otros campos relacionados con impuestos.</br></br>- Puede definir plantillas por país o región en la página **Plantillas de clientes de Shopify**, que es útil para el cálculo de impuestos adecuado.</br></br>Obtenga más información en [Configurar impuestos](setup-taxes.md).|

> [!NOTE]  
> La empresa debe tener un contacto principal. De lo contrario, el conector salta a la empresa.
> Solo se importa una ubicación más antigua.
> Sólo se importa el contacto principal.

## Configuraciones importantes al exportar empresas B2B a Shopify

Puede explotar los clientes existentes a Shopify de forma masiva como empresa. En cada caso se crea una empresa y una ubicación predeterminada y un contacto principal. También es posible crear un catálogo.

|Campo|Descripción|
|------|-----------|
|**Puede actualizar empresas de Shopify**| Habilite la opción si desea generar actualizaciones más tarde desde Business Central para las empresas que ya existen en Shopify.|
|**Permisos de contacto predeterminado**| Especifique qué permisos deben asignarse al contacto principal. Puede elegir entre **Ninguno**, **Sólo pedidos** y **Administrador de ubicación**.|
|**Creación automática de catálogos**| Habilite esta opción si desea crear un catálogo que incluya todos los productos. Se crea un catálogo para cada empresa exportada.|

## Exportar empresa B2B a Shopify

### Sincronización inicial de empresas B2B de Business Central a Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Empresa de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Agregar empresa**.
3. En el campo **Código de tienda**, escriba el código. Si abre la ventana **Empresa de Shopify** de la página **Tarjeta de tienda**, el código de tienda se completará automáticamente.
4. Defina filtros en clientes según sea necesario. Por ejemplo, puede filtrar por código de país o región.
5. Elija **Aceptar**.

La empresa y clientes resultantes se crean automáticamente en Shopify.

> [!NOTE]  
> La sincronización inicial de empresas de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify no tiene en cuenta la configuración **Puede actualizar empresas de Shopify**.

### Sincronizar empresas B2B

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda específica para la que desea sincronizar los clientes.
3. Elija la acción **Sincronizar empresa**.

Como alternativa, utilice la acción **Iniciar sincronización de empresa** en la página **Empresa de Shopify** o busque el trabajo por lotes **Sincronizar empresa**.

Puede programar la tarea para que se ejecuten de forma automatizada. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

## Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
