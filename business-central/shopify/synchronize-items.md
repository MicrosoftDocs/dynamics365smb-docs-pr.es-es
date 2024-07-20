---
title: Sincronizar artículos e inventario
description: Configurar y ejecutar sincronizaciones de artículos entre Shopify y Business Central
ms.date: 04/28/2024
ms.topic: article
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# Sincronizar artículos e inventario

**Los productos** en [!INCLUDE[prod_short](../includes/prod_short.md)] son equivalentes a **productos** en Shopify. Son los bienes físicos, las descargas digitales, los servicios y las tarjetas regalo que usted vende. Hay dos razones principales para sincronizar artículos:

1. Cuando administra principalmente datos en [!INCLUDE[prod_short](../includes/prod_short.md)]. Necesita exportar todos o algunos datos desde allí a Shopify y hacerlo visible. Puede exportar el nombre del artículo, la descripción, la imagen, los precios, la disponibilidad, las variantes, los detalles del proveedor y el código de barras. Una vez exportados, puede revisar los elementos o hacerlos visibles inmediatamente.
2. Cuando un pedido de Shopify se importa, la información sobre los artículos es vital para el procesamiento posterior del documento en [!INCLUDE[prod_short](../includes/prod_short.md)].

Los dos escenarios anteriores siempre están habilitados.

Un tercer escenario es administrar datos en Shopify pero importar esos productos a granel para [!INCLUDE[prod_short](../includes/prod_short.md)]. Este escenario puede ser útil para eventos de migración de datos, como cuando quiere conectar una tienda en línea existente con un entorno [!INCLUDE[prod_short](../includes/prod_short.md)] nuevo.

## Definir las sincronizaciones de artículos

1. Elija el icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. y entre en la **Tienda Shopify**. Abra la tienda para la que quiera configurar la sincronización de artículos.
2. En el campo **Sincronizar artículo**, seleccione la opción requerida.

   La siguiente tabla esboza las opciones.

   |Opción|Descripción|
   |------|-----------|
   |**En blanco**| Los productos se importan junto con la importación de pedidos. Los productos se exportan a Shopify si un usuario ejecuta la acción **Agregar artículo** desde la página **Productos de Shopify**. Esta opción es el proceso predeterminado.|
   |**A Shopify**| Seleccione esta opción si, después de la sincronización inicial desencadenada por la acción **Agregar artículo**, planea actualizar los productos manualmente usando la acción **Sincronizar producto** o usando la cola de trabajos para actualizaciones periódicas. Recuerde habilitar el campo **Puede actualizar producto de Shopify**. Si no está habilitado, es igual a la opción **Vacío** (proceso predeterminado). Obtenga más información en la sección [Exportar artículos a Shopify](synchronize-items.md#export-items-to-shopify).|
   |**Desde Shopify**| Elija esta opción si planea importar productos de Shopify de forma masiva, ya sea manualmente usando la acción **Sincronizar producto** o a través de la cola de trabajos para actualizaciones periódicas. Obtenga más información en la sección [Importar artículos de Shopify](synchronize-items.md#import-items-from-shopify).|

   > [!NOTE]
   > Cambiar **Elemento de sincronización** de **De Shopify** a **A Shopify** no tendrá ningún efecto a menos que habilite **Puede actualizar productos de Shopify**.

## Importar artículos desde Shopify

Primero, importe artículos de Shopify de forma masiva o junto con pedidos para agregarlos a las tablas **Producto de Shopify** y **Variante de Shopify**. A continuación, asigne productos y variantes importados a productos y variantes en [!INCLUDE[prod_short](../includes/prod_short.md)]. Administre el proceso con las siguientes configuraciones:

|Campo|Descripción|
|------|-----------|
|**Crear artículos desconocidos automáticamente**|Cuando se importan productos y variantes de Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)], la función [!INCLUDE[prod_short](../includes/prod_short.md)] siempre intenta encontrar primero el registro coincidente en la lista de artículos. **Asignación de SKU** afecta a cómo se realiza la correspondencia y crea un nuevo artículo y/o variante de artículo. Habilite esta opción si desea crear un nuevo artículo o cuando no existe un registro correspondiente. El nuevo elemento se crea utilizando datos importados y el **Código de plantilla de artículos**. Si esta opción no está habilitada, cree un artículo manualmente y usar la acción **Asignar producto** en la página **Productos de Shopify**.|
|**Código de plantilla de artículos**|Use este campo con la opción de alternancia **Creación automática de artículos desconocidos**.<br>Elija la plantilla que desea usar para los elementos creados automáticamente.|
|**Asignación de SKU**|Elige cómo quiere usar el valor de **SKU** importado de Shopify durante el mapeo y la creación de artículos/variantes. Obtenga más información en la sección [Efecto de los SKU y códigos de barras definidos del producto de Shopify en el mapeo y la creación de artículos y variantes en Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Separador de campo de SKU**|Use esto junto con **Asignación de SKU** ajustado a la opción **[N.º de artículo + Código de variante](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Defina un separador para usarlo para dividir la SKU.<br>Así, si en Shopify crea la variante con la SKU '1000/001', escribirá '/' en el campo **Separador de campo SKU** para crear el número de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] como '1000' y el código de variante del artículo como '001'. Si crea la variante con la SKU "1000/001/111" en Shopify, el número de producto en [!INCLUDE[prod_short](../includes/prod_short.md)] es "1000" y el código de variante de producto es "001". La parte "111" se ignora. |
|**Prefijo de variante**|Se usa junto con **Asignación de SKU** ajustado a **Código de variante** o **N.º de articulo + Código de variante** como función alternativa cuando el SKU proveniente de Shopify esta vacío.<br>Si desea crear la variante de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] automáticamente, tiene que introducir un valor en **Código**. Por defecto, se usa el valor definido en el campo SKU importado de Shopify. Sin embargo, si el SKU está vacío, genera un código que comenzará con el prefijo de variante definido y "001".|
|**Shopify puede actualizar artículo**|Elija esta opción si desea actualizar artículos y/o variantes automáticamente.|
|**UdM como variante**| Elija esta opción si desea que todas las unidades de medida de los artículos se exporten como variantes separadas. Para agregar el campo, personalice la página. Obtenga más información en la sección [Unidad de medida como variante](synchronize-items.md#unit-of-measure-as-variant).|
|**Nombre de opción de variante para UdM**| Utilice este campo con **UM como variante** para especificar bajo qué opción agregar variantes que representen unidades de medida. El valor predeterminado es *Unidad de medida*. Utilice la personalización para agregar el campo a la página.|

## Exportar elementos a Shopify

Hay varias formas de exportar elementos a Shopify:

* Utilice la acción **Agregar artículo a Shopify** directamente desde la página **Tarjeta de artículo**.
* Utilice la acción **Agregar artículo**  en la página  **Productos de Shopify** .
* Ejecute la sincronización de elementos una o varias veces con la automatización.

No importa cómo exporte los artículos, la información específica del artículo se transfiere a la lista de productos de Shopify según su elección de configuración para la sincronización de artículos.

Antes de exportar un elemento a Shopify, el conector comprueba si ya existe un elemento. Primero, verifica si hay un producto o variante con un código de barras, porque está definido en la entrada **Referencias de artículos** de un tipo de código de barras. Si el campo **Asignación de SKU** está completo, el conector verifica si hay un producto o variante con el SKU completo. Para obtener más información, vaya a [Efecto de los SKU y códigos de barras definidos del producto de Shopify en la asignación y la creación de artículos y variantes en Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).

> [!IMPORTANT]
> El producto se agrega únicamente al canal de ventas **Tienda en línea**. Debe publicar productos en otros canales de venta, como el PDV de Shopify, desde Shopify.

Las siguientes configuraciones le permiten administrar el proceso de exportar artículos:

|Campo|Descripción|
|------|-----------|
|**Sincronizar texto adicional de producto**|Seleccione este campo para sincronizar el texto extendido del elemento. Como se agregará al campo **Descripción**, puede contener código HTML. |
|**Sincronizar atributos de artículo**|Seleccione este campo para sincronizar los atributos del artículo. Los atributos tienen el formato de una tabla y se incluyen en el campo **Descripción** en Shopify.|
|**Sincronizar texto de marketing de producto**|Seleccione este campo para sincronizar el texto de marketing del producto. Aunque el texto de marketing es una especie de descripción, es diferente que el campo **Descripción** del producto. El campo **Descripción** se utiliza normalmente como un nombre visible conciso para identificar rápidamente el producto. El texto de marketing, por otro lado, es más rico y descriptivo. Su propósito es agregar contenido promocional y de marketing. Este texto se puede publicar con el elemento en Shopify. Hay dos formas de crear el texto de marketing. Use Copilot, que sugiere texto generado por IA o comience desde cero.|
|**Código de idioma**|Seleccione este campo si desea que las versiones traducidas se utilicen para el título, los atributos y el texto ampliado.|
|**Asignación de SKU**|Elija cómo desea completar el campo SKU en Shopify. Las opciones admitidas son:<br> - **N.º de artículo** para usar el número de artículo tanto para productos como para variantes.<br> - **N.º de artículo + Código de variante** para crear un SKU concatenando valores de dos campos. Para artículos sin variantes, solo se usa el número de artículo.<br>- **N.º de proveedor de artículo** para utilizar el número de proveedor del artículo definido en **Tarjeta de artículo** tanto para productos como para variantes.<br> - **Código de barras** para usar el tipo código de barras de **Referencia del artículo**. Esta opción respeta las variantes.<br>Si está habilitado **Puede actualizar productos Shopify**, los cambios en el campo **Asignación de SKU** se propagan a Shopify después de la siguiente sincronización para todos los productos y variantes enumerados en la página **Productos de Shopify** de la tienda seleccionada.|
|**Separador de campo de UA**|Defina un separador para la opción **N.º de articulo + Código de variante**.|
|**Inventario seguido**| Elija cómo el sistema debe llenar el campo **Seguimiento de inventario** para productos exportados a Shopify. Puede actualizar la información de disponibilidad desde [!INCLUDE[prod_short](../includes/prod_short.md)] para productos en Shopify cuyo inventario de seguimiento está habilitado. Obtenga más información en la sección [Inventario](synchronize-items.md#sync-inventory-to-shopify).|
|**Directiva de inventario predeterminada**|Escoja *Denegar* para evitar existencias negativas en el lado de Shopify. <br>Si está habilitado **Puede actualizar productos Shopify**, los cambios en el campo **Directiva de inventario predeterminada** se propagan a Shopify después de la siguiente sincronización para todos los productos y variantes enumerados en la página **Productos de Shopify** de la tienda seleccionada.|
|**Puede actualizar productos de Shopify**|Defina este campo si [!INCLUDE[prod_short](../includes/prod_short.md)] solo puede crear productos o también puede actualizar productos. Seleccione esta opción si, después de la sincronización inicial desencadenada por la acción **Agregar artículo**, planea actualizar los productos manualmente usando la acción **Sincronizar producto** o usando la cola de trabajos para actualizaciones periódicas. Recuerde seleccionar **A Shopify** en el campo **Sincronización de elementos**.<br>**Puede actualizar productos de Shopify** no tiene impacto en la sincronización de precios, imágenes o niveles de inventario, que se configuran mediante controles independientes.<br>Si **Puede actualizar productos de Shopify** está habilitada, los siguientes campos en el lado de Shopify se actualizarán en el producto y, si es necesario, en el nivel de variante: **SKU**, **Código de barras**, **Peso**. El **Título**, **Tipo de producto**, **Proveedor** y **Descripción** del producto también se actualizará si los valores exportados no están vacíos. Para la descripción, esto significa que debe habilitar cualquiera de las opciones y atributos **Sincronizar texto extendido del elemento**, **Sincronizar texto de marketing del elemento** y **Sincronizar atributos del elemento** y el texto ampliado o de marketing deben tener valores. Si el producto usa variantes, la variante se agrega o elimina si es necesario. <br>Si el producto en Shopify está configurado para usar una matriz de variantes que combina dos o más opciones, el conector Shopify no puede crear una variante para ese producto. En [!INCLUDE[prod_short](../includes/prod_short.md)] no hay forma de definir la matriz de opciones, por eso el conector utiliza el **Código de variante** como única opción. Sin embargo Shopify espera varias opciones y se niega a crear una variante si falta información sobre una segunda y otras opciones. |
|**UdM como variante**| Elija esta opción si desea que algunas opciones se exporten como importadas como unidades de medida en lugar de variantes. Personalice la página para agregar el campo. Obtenga más información en la sección [Unidad de medida como variante](synchronize-items.md#unit-of-measure-as-variant).|
|**Nombre de opción de variante para UdM**| Utilice este campo con **UM como variante** para especificar qué contiene variantes que representen unidades de medida. El valor predeterminado es *Unidad de medida*. Personalice la página para agregar el campo.|

> [!NOTE]
> Cuando desee exportar muchos artículos y variantes, es posible que algunos estén bloqueados. No puede incluir artículos bloqueados ni variantes en los cálculos de precios, por lo que no se exportan. El Conector omite esos elementos y variantes, por lo que no es necesario filtrarlos en la página de solicitud **Agregar elemento a Shopify**.

## Detalles avanzados

### Efecto los SKU y códigos de barras del producto de Shopify en el mapeo y la creación de artículos y variantes en Business Central

Cuando los productos son importados desde Shopify a las tablas **Productos de Shopify** y **variantes de Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] intenta encontrar registros existentes.

La siguiente tabla describe las diferencias entre las opciones del campo **Asignación de SKU**.

|Opción|Efecto en el mapeo|Efecto en la creación|
|------|-----------------|------------------|
|**En blanco**|El campo SKU no se usa en la rutina de asignación de artículos.|Sin efecto en la creación del elemento.<br>Esta opción impide la creación de variantes. En un pedido de ventas, solo se usa el artículo principal. Una variante se sigue pudiendo mapear manualmente en la página **Productos de Shopify**.|
|**Nº producto**|Elíjalo si el campo SKU contiene el número de artículo.|Sin efecto en la creación de un elemento sin variantes. Para un artículo con variantes, cada variante se crea como un artículo separado.<br>Si Shopify tiene un producto con dos variantes y sus SKU son '1000' y '2000', en [!INCLUDE[prod_short](../includes/prod_short.md)], el sistema creará dos productos numerados '1000' y '2000'.|
|**Cód. variante**|El campo SKU no se usa en la rutina de asignación de artículos.|Sin efecto en la creación del elemento. Cuando se crea una variante de artículo, el valor del campo SKU se usa como código. Si el SKU está vacío, se genera un código usando el campo **Prefijo de variante**.|
|**N.º artículo + Código de variante**|Seleccione esto si el campo SKU contiene un número de artículo y el código de variante del artículo se separa por el valor definido en el campo **Separador de campos SKU**.|Cuando se crea un artículo, la primera parte del valor del campo SKU se designa como **N.º**. Si el campo SKU está vacío, un número de artículo se genera utilizando las series numéricas definidas en el campo **Código de plantilla de artículo** o **Números de artículo** de la página **Configuración de inventario**.<br>Cuando se crea un artículo, la función variante usa la segunda del valor del campo SKU se usa como **Código**. Si el campo de SKU está vacío, se genera un código usando el campo **Prefijo de variante**.|
|**N.º de artículo de proveedor**|Elíjalo si el campo SKU contiene el número de artículo de proveedor. En este caso, el **Número de proveedor de artículo** no se usa en la página **Tarjeta de artículo**; más bien se usa el **Número de artículo del proveedor** del **Catálogo de proveedores de artículos**. Si el registro encontrado de *Catálogo de proveedores de artículos* contiene un código de variante, este código se utiliza para mapear la variante de Shopify.|Si existe un proveedor correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)], el valor de SKU se usará como **Número de artículo del proveedor** en la página **Tarjeta de artículo** y como **Referencia del artículo** de tipo *proveedor*. <br>Impide la creación de variantes. Es útil cuando desea usar el artículo principal solo en el pedido de ventas. Todavía puodrá asignar una variante manualmente desde la página **Productos de Shopify**.|
|**Código de barras**|Elíjalo si el campo SKU contiene un código de barras. Se realiza una búsqueda entre **Referencias de artículos** del tipo de *código de barras*. Si el registro encontrado de Referencia de artículo contiene un código de variante, este código de variante se utiliza para mapear la variante de Shopify.|Sin efecto en la creación del elemento. <br>Impide la creación de variantes. Es útil cuando desea usar el artículo principal solo en el pedido de ventas. Todavía puodrá asignar una variante manualmente desde la página **Productos de Shopify**.|

En la tabla siguiente se describe los efectos del campo **Código de barras**.

|Efecto en el mapeo|Efecto en la creación|
|-----------------|------------------|
|Se realiza una búsqueda en las **Referencias de artículos** que contienen un tipo de código de barras para el valor definido en el campo **Código de barras** en Shopify. Si el registro encontrado de Referencia de artículo contiene un código de variante, este código de variante se utiliza para mapear la variante de Shopify.|El código de barras se guarda como **Referencia del artículo** para el artículo y variante de artículo.|

> [!NOTE]  
> Puede desencadenar el mapeo del producto/variantes seleccionados o todos los productos importados no mapeados seleccionando **Intentar buscar mapeo de producto** o **Intentar buscar asignaciones**.

### Información general de asignaciones de campos

|Shopify|Origen cuando se exporta desde [!INCLUDE[prod_short](../includes/prod_short.md)]|Destino cuando se importa a [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|De acuerdo con el campo **Estado de los productos creados** en la **Tarjeta de tienda de Shopify**. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Cargo | **Descripción**. Si el código de idioma está definido y existe una traducción del artículo correspondiente, se utilizará la traducción del artículo en lugar de la descripción.|**Descripción**|
|Título variante | **Cód. variante**.<br>La razón para usar **Código** y no **Descripción** es porque Shopify requiere títulos de variantes únicos por producto. En [!INCLUDE[prod_short](../includes/prod_short.md)] el **Código** es único, mientras que la **Descripción** no lo es. Las descripciones no únicas generarán problemas durante la exportación del producto.|**Descripción** de variante|
|Descripción|Combina textos extendidos, texto de marketing y atributos si habilita las alternancias correspondientes en la tarjeta de tienda de Shopify. Respeta el código de idioma.|No utilizado.|
|Título de página SEO|Valor fijo: vacío. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Descripción meta de SEO|Valor fijo: vacío. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Medios|**Imagen**. Obtenga más información en la sección [Sincronizar imágenes de elementos](synchronize-items.md#sync-item-images)|**Imagen**|
|Precio|El cálculo del precio del cliente final incluye el precio unitario del producto, el grupo de precios del cliente, el grupo de descuento del cliente y el código de moneda. Obtenga más información en la sección [Sincronizar precios](synchronize-items.md#sync-prices-with-shopify)|**Precio unitario**. El precio solo se importa a los artículos recién creados, pero no se actualizará en sincronizaciones posteriores.|
|Comparar por precio|El cálculo del precio sin descuento. Si el valor es menor o igual a **Precio**, el conector envía 0 (nulo) en lugar del valor real.|No utilizado.|
|Coste por artículo|**Coste unitario**|**Coste unitario**. El coste unitario solo se importa a los artículos recién creados, y no se actualizará en sincronizaciones posteriores.|
|UA|Infórmese sobre esto en **Asignación de SKU** en la sección [Exportar elementos a Shopify](synchronize-items.md#export-items-to-shopify).|Obtenga más información sobre esto en la sección [Efecto de los SKU y códigos de barras definidos del producto de Shopify en la asignación y la creación de artículos y variantes en Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Código de barras|**Referencias de artículos** de tipo código de barras.|**Referencias de artículos** de tipo código de barras.|
|El inventario se almacenará en| Depende de Ubicaciones de las tiendas Shopify. Si **Business Central Fulfillment Services** tiene el campo **Ubicación de producto predeterminada** habilitado, el inventario se almacena y se envía desde **Business Central Fulfillment Services**. De lo contrario, se usa la ubicación principal de Shopify o varias ubicaciones. Obtenga más información en la sección [Dos enfoques para gestionar los cumplimientos](synchronize-items.md#two-approaches-to-manage-fulfillments)| No utilizado.|
|Seguimiento de cantidad|De acuerdo con el campo **Inventario seguido** en la página **Tarjeta de tienda de Shopify**. Obtenga más información en la sección [Inventario](synchronize-items.md#sync-inventory-to-shopify). Solo se usa cuando exporta un producto por primera vez.|No utilizado.|
|Continuar vendiendo cuando no haya existencias|De acuerdo con la **Directiva de inventario predeterminada** en la **Tarjeta de tienda de Shopify**.|No utilizado.|
|Tipo|**Descripción** de **Código de categoría de artículos**. Si el tipo no está especificado en Shopify, se agrega como un tipo personalizado.|**Código de categoría de artículos**. Mapeo por descripción.|
|Proveedor|**Nombre** del proveedor según el **N.º de proveedor**|Asignación de **N.º de proveedor** por nombre.|
|Peso|**Peso bruto**.|No utilizado.|
|Gravable|Valor fijo: habilitado.|No utilizado.|
|Códigos impositivos|**Código de grupo de impuestos**. Solo relevante para los impuestos. Obtenga más información en [Configurar impuestos](setup-taxes.md).|No utilizado.|

### Etiquetas

Revise las etiquetas importadas en el cuadro informativo **Etiquetas** en la página **Producto de Shopify**. En la misma página, para editar etiquetas, seleccione la acción **Etiquetas**.

Si la opción **A Shopify** está seleccionada en el campo **Artículo de sincronización**, las etiquetas asignadas se exportan a Shopify en la próxima sincronización.

### Unidad de medida como variante

Shopify no admite múltiples unidades de medida. Si desea vender el mismo producto como, por ejemplo, pieza y establecer y utilizar diferentes precios o descuentos, debe crear unidades de medida como variantes del producto.
El conector Shopify se puede configurar para exportar unidades de medida como variantes o importar variantes como unidades de medida.

Para habilitar esta capacidad, utilice los campos **UMO como variante** y **Nombre de opción de variante** en la **Tarjeta de compra Shopify**. Los campos están ocultos de forma predeterminada; utilice la personalización para agregarlos a la página.

**Unidad de medida como comentarios de variante**

* Cuando se trata de una matriz de variantes, por ejemplo Color y UM, y desea importar productos en [!INCLUDE[prod_short](../includes/prod_short.md)], debe configurar *N.º de artículo + Código de variante* en el campo **Asignación de SKU** y asegúrese de que el campo **SKU** en Shopify tenga el mismo valor para todas las unidades de medida e incluya número de artículo y código de variante.
* En [!INCLUDE[prod_short](../includes/prod_short.md)] la disponibilidad se calcula por artículo/variante de artículo y no por unidad de medida. Significa que se asignará la misma disponibilidad a cada variante que represente la unidad de medida (con respecto a **Cantidad por unidad de medida**), lo que puede llevar a casos en que la cantidad disponible en Shopify no es exacto. Ejemplo: Artículo que se vende en PCS y Caja de 6. El inventario en [!INCLUDE[prod_short](../includes/prod_short.md)] es de 6 unidades. Artículo exportado a Shopify como Producto con dos variantes. Una vez ejecutada la sincronización del inventario, el nivel de inventario en Shopify será 6 para la variante unidades y 1 para la variante caja. El comprador puede explorar solo la tienda y ver que el producto está disponible en ambas opciones y realizar el pedido por 1 CAJA. El próximo comprador verá que CAJA no está disponible, pero todavía quedan 6 UNIDADES. Esto se solucionará con la próxima sincronización del inventario.
* No podrá agregar la opción Unidad de medida a productos existentes con variantes (el resultado específico depende de otra configuración, como **Asignación de SKU**).

### URL y URL de vista previa

Un producto añadido a Shopify o importado de Shopify podría tener la **URL** o **URL de vista previa** previamente rellenas. El campo **URL** estará vacío si el producto no se publica en la tienda en línea, por ejemplo porque su estado es borrador. La **URL** estará vacía si el almacén está protegido con contraseña, por ejemplo, porque se trata de un almacén de desarrollo. En la mayoría de los casos, puede utilizar **URL de vista previa** para comprobar cómo se verá el producto una vez publicado.

## Ejecutar sincronización de artículos

La sincronización total o parcial de elementos se puede realizar de muchas maneras diferentes.

### Sincronización inicial de elementos de Business Central a Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Agregar artículos**.
3. En el campo **Código de tienda**, escriba el código. Si abre la ventana **Producto de Shopify** de la página **Tarjeta de tienda**, el código de tienda se completará automáticamente.
4. Si configuró la sincronización de imágenes e inventario, puede incluirlos en el mismo proceso. Incluirlos en el mismo proceso es conveniente para escenarios de demostración o cuando se trata de una cantidad menor de datos.
5. Defina filtros en artículos según sea necesario. Por ejemplo, puede filtrar por el número de artículo. o código de categoría de artículo.
6. Elija **Aceptar**.

Los artículos resultantes se crean automáticamente en Shopify con precios. En función de las elecciones que haya realizado, es posible que se incluyan imágenes y niveles de inventario. La operación puede tardar algún tiempo si se agrega una gran cantidad de elementos.

Alternativamente, puede sincronizar un producto eligiendo la acción **Agregar a Shopify** en la página **Ficha producto**.  

> [!NOTE]  
> La sincronización inicial de productos de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify no tiene en cuenta los ajustes **Sincronizar producto** y **Puede actualizar productos de Shopify**. 

### Sincronizar productos de Shopify a Business Central

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar artículos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar productos**.

Como alternativa, utilice la acción **Sincronizar productos** en la página **Productos de Shopify** o busque el trabajo por lotes **Sincronizar productos**.

Puede programar la tarea para que se realice de forma automatizada. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

### Actualizaciones ad hoc de productos de Shopify

Cuando se actualizan los registros en la tabla **Productos de Shopify**, los siguientes cambios se sincronizan con Shopify.

Actualizar:

* **Estado**: puede elegir entre activo, archivado o borrador.
* **Título de SEO**
* **Descripción de SEO**

Eliminación:

Según el valor de **Acción para productos eliminados** en la página **Tarjeta de tienda de Shopify**, el producto se actualiza en Shopify cuando se elimina el registro de la página **Productos de Shopify**.

* **En blanco**: no sucederá nada. Si es necesario, deberá realizar la acción requerida desde el **administrador de Shopify**.
* **Estado a Borrador**: el estado del producto en Shopify se establece en *Borrador*.
* **Estado a archivado**: el producto se archiva en Shopify.

## Sincronizar imágenes de artículo

La sincronización de imágenes se puede configurar para elementos sincronizados. Elija entre las siguientes opciones:

* **Deshabilitado**: la sincronización de imágenes se desactiva.
* **A Shopify**: las imágenes de los artículos se exportan a Shopify
* **Desde Shopify**: las imágenes de Shopify se importan a [!INCLUDE[prod_short](../includes/prod_short.md)]

La sincronización de imágenes se puede inicializar de las dos maneras que se describen a continuación.

### Sincronizar imágenes de productos desde la página de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar imágenes para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar imágenes de productos**.

### Sincronizar imágenes de productos desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Sincronizar imágenes de productos**.

### Observaciones de sincronización de imágenes

* Cuando exporta imágenes de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, las imágenes reemplazan a las que exportó anteriormente. Las imágenes anteriores ya no están disponibles.
* Si elimina una imagen en [!INCLUDE[prod_short](../includes/prod_short.md)], la imagen en Shopify tampoco se elimina. Deberá eliminar manualmente las imágenes antiguas en el **Administrador de Shopify**.
* Las imágenes que exporte a Shopify deben cumplir con los requisitos de Shopify. De lo contrario, no podrá importarlas. Para más información sobre los requisitos de los medios, vaya a [Tipos de medios de productos en help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## Sincronizar precios con Shopify

Las siguientes configuraciones le permiten administrar el proceso de exportar precios:

|Campo|Descripción|
|------|-----------|
|**Grupo de precios de cliente**|Determine el precio de un artículo en Shopify. Se toma el precio de venta de este grupo de precios de cliente. Si no se especifica ningún grupo, se utiliza el precio de la tarjeta del producto.|
|**Grupo de descuentos de cliente**|Determine el descuento que se utilizará para calcular el precio de un producto en Shopify. Los precios con descuento se almacenan en el campo **Precio** y el precio completo se almacena en el campo **Comparar por precio**.|
|**Permitir dto. línea**|Especifica si se permite el descuento de línea al calcular precios para Shopify. Esta configuración se aplica solo a los precios del producto. Los precios para el grupo de precios del cliente tienen sus propias líneas de activación.|
|**Precio IVA incluido**|Especifica si los cálculos de precio para Shopify incluyen el IVA. Obtenga más información en [Configurar impuestos](setup-taxes.md).|
|**Grupo registro IVA negocio**|Especifica el grupo contable de negocio de IVA que se usa para calcular los precios en Shopify. Este debería ser el grupo que utilice para clientes nacionales. Obtenga más información en [Configurar impuestos](setup-taxes.md).|
|**Cód. divisa**|Introduzca un código de moneda solo si su tienda en línea utiliza una moneda diferente a la moneda local (LCY). La divisa especificada debe tener tipos de cambio configurados. Si su tienda en línea usa la misma divisa que [!INCLUDE[prod_short](../includes/prod_short.md)], deje el campo vacío.|

Los precios para productos sincronizados puede exportarlos de las dos formas que se describen a continuación.

### Sincronizar precios desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Sincronizar precios con Shopify**.

### Observaciones de cálculo de precios

* Al determinar un precio, [!INCLUDE[prod_short](../includes/prod_short.md)] utiliza la lógica del "precio más bajo". Sin embargo, la lógica del precio más bajo ignora el precio unitario definido en la tarjeta del producto si se define un precio en el grupo de precios. Esto es cierto incluso si el precio unitario del precio de la tarjeta del producto es más bajo.
* Para calcular los precios, el conector crea una oferta de venta temporal para el producto con una cantidad de 1 y utiliza la lógica de cálculo de precios estándar. Solo se utilizan los precios y descuentos aplicables a la cantidad 1. No puede exportar diferentes precios o descuentos en función de la cantidad.
* El conector envía una solicitud para actualizar los precios en Shopify si el precio en [!INCLUDE[prod_short](../includes/prod_short.md)] ha cambiado. Por ejemplo, si ha sincronizado productos y precios y luego ha cambiado el precio en Shopify, elegir la acción **Sincronizar precios con Shopify** no tendrá ningún impacto en el precio en Shopify ya que el nuevo precio calculado por el conector es el mismo que el precio almacenado en la variante de Shopify de la sincronización anterior. El campo **Comparar al precio** se actualiza solo si el precio principal ha cambiado.

## Sincronizar inventario a Shopify

La sincronización de inventario se puede configurar para elementos ya sincronizados. Hay dos condiciones que se deben cumplir:

1. El seguimiento de inventario debe estar habilitado para un producto en Shopify. Si los artículos se exportan a Shopify, considere habilitar la alternancia **Inventario seguido** en la página **Tarjeta Shopify**. Obtenga más información en la sección [Exportar artículos a Shopify](synchronize-items.md#export-items-to-shopify).
2. La sincronización de inventario debe estar habilitada para **Ubicaciones de Shopify**.

### Para habilitar la sincronización de inventario

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar el inventario para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Ubicaciones** para abrir **Ubicaciones de tienda de Shopify**.
4. Elija la acción **Obtener ubicaciones de Shopify** para importar todas las ubicaciones definidas en Shopify. Puede encontrarlas en la configuración de [**Ubicaciones**](https://www.shopify.com/admin/settings/locations) del **Administrador de Shopify**.
5. En el campo **Filtro de ubicación**, agregue ubicaciones si desea incluir inventario solo de ubicaciones específicas. Por lo tanto, podría introducir *ESTE|OESTE* para que el inventario solo de estas dos ubicaciones esté disponible para la venta a través de la tienda en línea.
6. Seleccione el método de cálculo de existencias que se usará para las ubicaciones seleccionadas de Shopify.
7. Habilite **Ubicación de producto predeterminada** si desea que la ubicación se utilice para la creación de registros de inventario y participe en la sincronización del inventario.

La sincronización de inventarios se puede inicializar de las dos maneras que se describen a continuación.

### Sincronizar inventario desde la página de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar el inventario para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Sincronizar inventario**.

### Sincronizar inventario desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Sincronizar inventario**.

### Consideraciones sobre inventarios

* Hay dos métodos estándar de cálculo de existencias: **Saldo disponible proyectado en la fecha** e **Inventario libre (no reservado)**. Con la extensibilidad, puede agregar más opciones. Para obtener más información sobre la extensibilidad, vaya a los [ejemplos](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* Puede consultar la información de existencias recibida de Shopify en la página **Cuadro informativo de inventario de Shopify**. En este cuadro informativo, obtendrá una descripción general de las existencias de Shopify y el último inventario calculado en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay un registro por ubicación.
* Si la información de existencias en Shopify es diferente de **Saldo disponible proyectado** en [!INCLUDE[prod_short](../includes/prod_short.md)], entonces las existencias se actualizarán en Shopify.
* Cuando agrega una nueva ubicación en Shopify, también necesita agregar registros de inventario para ella. Shopify no lo hace automáticamente para los productos y variantes existentes y el conector no sincronizará los niveles de inventario para dichos productos en la nueva ubicación. Para obtener más información, vaya a [Asignación de inventario a ubicaciones](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* Se admiten tanto **Servicios de cumplimiento de Business Central** como ubicaciones normales y se pueden usar para envíos y el inventario.

#### Ejemplo de cálculo de saldo disponible proyectado

Hay 10 piezas del artículo A disponibles y dos órdenes de venta pendientes. Uno para el lunes con cantidad *Uno* y otro para el jueves con cantidad *Dos*. Dependiendo de cuándo sincronice el inventario, el sistema actualizará el nivel de existencias en Shopify con diferentes cantidades:

|Cuando se ejecuta el inventario sincronizado|Valor utilizado para actualizar el nivel de existencias|Comentario|
|------|-----------------|-----------------|
|Martes|9|Inventario 10 menos pedido de venta programado para enviarse el lunes|
|Viernes|7|Inventario 10 menos ambas órdenes de venta|

####  Ejemplo de cálculo de inventario libre (no reservado)

Hay 10 piezas del artículo A disponibles y tres pedidos de venta pendientes. Un pedido con cantidad *1* reservado desde el asiento contable de artículo, uno con cantidad *2* no reservado y otro con cantidad *3* reservado de un pedido de compra. Para este método, la fecha de sincronización no es importante.

|Valor utilizado para actualizar el nivel de existencias|Comentario|
|-----------------|-----------------|
|9|Inventario 10 menos el pedido de venta con inventario reservado del movimiento del producto. Se ignoran otros pedidos de ventas.|

### Dos enfoques para gestionar los cumplimientos

Hay dos formas de abordar el cumplimiento en Shopify:

* Cumplimiento y seguimiento de inventario de Shopify "integrados"
* Cumplimiento y seguimiento de inventario de terceros

El inventario de cada producto en Shopify puede ser almacenado por Shopify o por 3PL.

Si utiliza cumplimiento de Shopify, también puede definir varias ubicaciones en Shopify. Una vez creado el pedido, Shopify selecciona la ubicación según la disponibilidad y la prioridad. También puede especificar en qué ubicaciones planea realizar un seguimiento de un producto específico, por ejemplo, nunca vender desde la ubicación *ShowRoom*.

Si utiliza 3PL, el proveedor 3PL se encarga de la gestión física, por lo que no se necesitan ubicaciones. Para 3PL el campo SKU se vuelve obligatorio.

Cuando decide en qué ubicación realizar el seguimiento del artículo, Shopify crea registros en la tabla **Niveles de inventario** , que se pueden actualizar manualmente con la disponibilidad del inventario.

El conector admite ambos modos. Puede enviar inventario a múltiples ubicaciones de Shopify o funcionar como servicio de cumplimiento.

Desde la perspectiva [!INCLUDE[prod_short](../includes/prod_short.md)] cuando crea un artículo y quiere enviarlo a Shopify también desea:

* Use la opción **Ubicación predeterminada del producto** para especificar si este artículo será cumplido por cumplimiento de Shopify o por 3PL. Siempre hay **Servicio de cumplimiento de Business Central**, pero puede haber más servicios de cumplimiento si se instalan más aplicaciones. Puede habilitar **Ubicación predeterminada del producto** solo en un registro si desea utilizar el servicio de cumplimiento. 
* use la opción **Ubicación predeterminada del producto** para especificar qué ubicaciones desea usar para realizar un seguimiento del inventario. Puede activar la **Ubicación predeterminada del producto** para varias ubicaciones donde **El servicio de cumplimiento** está deshabilitado. Tenga en cuenta que siempre se realizará un seguimiento del inventario para su ubicación principal.

#### ¿Cuál es la diferencia?

El proceso de entrega de Shopify es útil cuando se utiliza Shopify PDV y existen múltiples tiendas físicas. Quiere que los empleados de la tienda física conozcan su inventario actual. En este caso, crea varias ubicaciones en Shopify, múltiples ubicaciones en [!INCLUDE[prod_short](../includes/prod_short.md)] y active **Ubicación predeterminada del producto** para todas estas ubicaciones.  

Si la logística se gestiona en [!INCLUDE[prod_short](../includes/prod_short.md)] donde puede tener tantas ubicaciones como sea necesario representando centros de distribución, no crea ubicaciones en Shopify, el conector crea automáticamente los servicios de cumplimiento de Business Central y puede vincular el inventario mediante filtros de ubicación desde varias ubicaciones a un registro de servicios de proceso de entrega. Como resultado, en Shopify no hay información sobre desde dónde se envían los productos; solo tiene información de seguimiento, mientras que en [!INCLUDE[prod_short](../includes/prod_short.md)], puedes seleccionar según la disponibilidad y la proximidad al destino.

#### Ejemplo de uso del conmutador de ubicación predeterminada del producto

Después de elegir la acción **Obtener ubicaciones de Shopify** en la página **Ubicaciones de Shopify** verá las siguientes ubicaciones:

|Nombre|Es servicio de proceso de entrega|Es principal|
|------|-----------------|-----------------|
|Principal| |**Sí**|
|Segundo| | |
|Servicio de cumplimiento de Business Central|**Sí**| |

Repasemos el impacto de habilitar la opción de ubicación predeterminada del producto:

|Nombre de las ubicaciones donde está activada la opción Ubicación predeterminada del producto|Impacto en cómo se crea el producto en Shopify|
|------|-----------------|
|Principal| El inventario se almacenará en: Múltiples ubicaciones; Ubicaciones seleccionadas: Principal (primaria) |
|Principal y Segundo| El inventario se almacenará en: Múltiples ubicaciones; Ubicaciones seleccionadas: Principal y segunda |
|Servicio de cumplimiento de Business Central|El inventario se almacenará en: Servicio de cumplimiento de Business Central; Ubicaciones seleccionadas: (Aplicación) Servicio de cumplimiento de Business Central|
|Servicio de cumplimiento de Business Central y principal| Error: No puede usar almacenes de Shopify estándar con almacenes de servicio de proceso de entrega|

## Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
