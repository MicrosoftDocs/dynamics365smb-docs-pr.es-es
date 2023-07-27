---
title: Sincronizar artículos e inventario
description: Configurar y ejecutar sincronizaciones de artículos entre Shopify y Business Central
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30116, 30117, 30126, 30127,'
author: AndreiPanko
ms.author: andreipa
ms.reviewer: bholtorf
---

# Sincronizar artículos e inventario

Los **Artículos** en [!INCLUDE[prod_short](../includes/prod_short.md)] son equivalentes a los *productos* en Shopify, e incluyen bienes físicos, descargas digitales, servicios y tarjetas de regalo que usted vende. Hay dos razones principales para sincronizar artículos:

1. La gestión de datos se realiza principalmente en [!INCLUDE[prod_short](../includes/prod_short.md)]. Necesita exportar todos o algunos datos desde allí a Shopify y hacerlo visible. Puede exportar el nombre del artículo, la descripción, la imagen, los precios, la disponibilidad, las variantes, los detalles del proveedor y el código de barras. Una vez exportados, puede revisar los elementos o hacerlos visibles inmediatamente.
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
|**Crear artículos desconocidos automáticamente**|Cuando se importan productos y variantes de Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)], la función [!INCLUDE[prod_short](../includes/prod_short.md)] siempre intenta encontrar primero el registro coincidente en la lista de artículos. **Asignación de SKU** afecta a cómo se realiza la correspondencia y crea un nuevo artículo y/o variante de artículo. Habilite esta opción si desea crear un nuevo artículo o cuando no existe un registro correspondiente. El nuevo elemento se crea utilizando datos importados y el **Código de plantilla de artículos**. Si esta opción no está habilitada, deberá crear un artículo manualmente y usar la acción **Asignar producto** en la página **Productos de Shopify**.|
|**Código de plantilla de artículos**|Use este campo con la opción de alternancia **Creación automática de artículos desconocidos**.<br>Elija la plantilla que desea usar para los elementos creados automáticamente.|
|**Asignación de SKU**|Elige cómo quiere usar el valor de **SKU** importado de Shopify durante el mapeo y la creación de artículos/variantes. Obtenga más información en la sección [Efecto de los SKU y códigos de barras definidos del producto de Shopify en el mapeo y la creación de artículos y variantes en Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Separador de campo de SKU**|Use esto junto con **Asignación de SKU** ajustado a la opción **[N.º de artículo + Código de variante](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Defina un separador para usarlo para dividir la SKU.<br>Así, si en Shopify crea la variante con la SKU '1000/001', escribirá '/' en el campo **Separador de campo SKU** para crear el número de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] como '1000' y el código de variante del artículo como '001'.|
|**Prefijo de variante**|Se usa junto con **Asignación de SKU** ajustado a **Código de variante** o **N.º de articulo + Código de variante** como función alternativa cuando el SKU proveniente de Shopify esta vacío.<br>Si desea crear la variante de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] automáticamente, tendrá que introducir un valor en **Código**. Por defecto, se usa el valor definido en el campo SKU importado de Shopify. Sin embargo, si el SKU está vacío, generará un código que comenzará con el prefijo de variante definido y "001".|
|**Shopify puede actualizar artículo**|Elija esta opción si desea actualizar artículos y/o variantes automáticamente.|

### Efecto los SKU y códigos de barras del producto de Shopify en el mapeo y la creación de artículos y variantes en Business Central

Cuando los productos son importados desde Shopify a las tablas **Productos de Shopify** y **variantes de Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] intenta encontrar registros existentes.

La siguiente tabla describe las diferencias entre las opciones del campo **Asignación de SKU**.

|Opción|Efecto en el mapeo|Efecto en la creación|
|------|-----------------|------------------|
|**En blanco**|El campo SKU no se usa en la rutina de asignación de artículos.|Sin efecto en la creación del elemento.<br>Esta opción impide la creación de variantes. Cuando en el pedido de ventas, solo se usa el artículo principal. Una variante se sigue pudiendo mapear manualmente en la página **Productos de Shopify**.|
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

## Exportar elementos a Shopify

Elija los elementos de su lista de elementos que se exportarán a Shopify. Utilice la acción **Agregar artículo** en la página **Productos de Shopify** para agregar elementos a la lista de productos de Shopify. 

>[!IMPORTANT]
>El producto se agregará únicamente al canal de ventas **Tienda en línea**. Debe publicar productos en otros canales de venta, como el PDV de Shopify, desde Shopify.

Las siguientes configuraciones le permiten administrar el proceso de exportar artículos:

|Campo|Descripción|
|------|-----------|
|**Sincronizar texto adicional de artículo**|Seleccione este campo para sincronizar el texto extendido del elemento. Como se agregará al campo **Descripción**, puede contener código HTML. |
|**Sincronizar atributos de artículo**|Seleccione este campo para sincronizar los atributos del artículo. Los atributos tienen el formato de una tabla y se incluyen en el campo **Descripción** en Shopify.|
|**Sincronizar texto de marketing de producto**|Seleccione este campo para sincronizar el texto de marketing del producto. Aunque el texto de marketing es una especie de descripción, es diferente del campo **Descripción** del producto. El campo **Descripción** se utiliza normalmente como un nombre visible conciso para identificar rápidamente el producto. El texto de marketing, por otro lado, es más rico y descriptivo. Su propósito es agregar contenido promocional y de marketing. Este texto se puede publicar con el elemento en Shopify. Hay dos formas de crear el texto de marketing. Use Copilot, que sugiere texto generado por IA o comience desde cero.|
|**Código de idioma**|Seleccione este campo si desea que las versiones traducidas se utilicen para el título, los atributos y el texto ampliado.|
|**Asignación de SKU**|Elija cómo desea completar el campo SKU en Shopify. Las opciones admitidas son:<br> - **N.º de artículo** para usar el n.º de artículo tanto para productos como para variantes.<br> - **N.º de artículo + Código de variante** para crear un SKU concatenando valores de dos campos. Para artículos sin variantes, solo se usa el número de artículo.<br>- **N.º de proveedor de artículo** para utilizar el número de proveedor del artículo definido en **Tarjeta de artículo** tanto para productos como para variantes.<br> - **Código de barras** para usar el tipo código de barras de **Referencia del artículo**. Esta opción respeta las variantes.|
|**Separador de campo de SKU**|Defina un separador para la opción **N.º de articulo + Código de variante**.|
|**Inventario seguido**| Elija cómo el sistema debe llenar el campo **Seguimiento de inventario** para productos exportados a Shopify. Puede actualizar la información de disponibilidad desde [!INCLUDE[prod_short](../includes/prod_short.md)] para productos en Shopify cuyo inventario de seguimiento está habilitado. Obtenga más información en la sección [Inventario](synchronize-items.md#sync-inventory-to-shopify).|
|**Directiva de inventario predeterminada**|Escoja *Denegar* para evitar existencias negativas en el lado de Shopify.|
|**Puede actualizar productos de Shopify**|Defina este campo si [!INCLUDE[prod_short](../includes/prod_short.md)] solo puede crear productos o también puede actualizar productos. Seleccione esta opción si, después de la sincronización inicial desencadenada por la acción **Agregar artículo**, planea actualizar los productos manualmente usando la acción **Sincronizar producto** o usando la cola de trabajos para actualizaciones periódicas. Recuerde seleccionar **A Shopify** en el campo **Sincronización de elementos**.<br>**Puede actualizar productos de Shopify** no tiene impacto en la sincronización de precios, imágenes o niveles de inventario, que se configuran mediante controles independientes.<br>Si **Puede actualizar productos de Shopify** está habilitada, los siguientes campos en el lado de Shopify se actualizarán en el producto y, si es necesario, en el nivel de variante: **SKU**, **Código de barras**, **Peso**. El **Título**, **Tipo de producto**, **Proveedor**, **Descripción** del producto también se actualizará si los valores exportados no están vacíos. Para la descripción, esto significa que debe habilitar cualquiera de las opciones y atributos **Sincronizar texto extendido del elemento**, **Sincronizar texto de marketing del elemento**, **Sincronizar atributos del elemento** y el texto ampliado o de marketing deben tener valores. Si el producto usa variantes, la variante se agregará o eliminará si es necesario.|

### Información general de asignaciones de campos

|Shopify|Origen cuando se exporta desde [!INCLUDE[prod_short](../includes/prod_short.md)]|Destino cuando se importa a [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|De acuerdo con el campo **Estado de los productos creados** en la **Tarjeta de tienda de Shopify**. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Cargo | **Descripción**. Si el código de idioma está definido y existe una traducción del artículo correspondiente, se utilizará la traducción del artículo en lugar de la descripción.|**Descripción**|
|Descripción|Combina textos extendidos, texto de marketing y atributos si habilita las alternancias correspondientes en la tarjeta de tienda de Shopify. Respeta el código de idioma.|No utilizado.|
|Título de página SEO|Valor fijo: vacío. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Descripción meta de SEO|Valor fijo: vacío. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Medios|**Imagen**. Obtenga más información en la sección [Sincronizar imágenes de elementos](synchronize-items.md#sync-item-images)|**Imagen**|
|Precio|El cálculo del precio del cliente final incluye el precio unitario del producto, el grupo de precios del cliente, el grupo de descuento del cliente y el código de moneda. Obtenga más información en la sección [Sincronizar precios](synchronize-items.md#sync-prices-with-shopify)|**Precio unitario**. El precio solo se importa a los artículos recién creados, pero no se actualizará en sincronizaciones posteriores.|
|Comparar por precio|El cálculo del precio sin descuento.|No utilizado.|
|Coste por artículo|**Coste unitario**|**Coste unitario**. El coste unitario solo se importa a los artículos recién creados, y no se actualizará en sincronizaciones posteriores.|
|UA|Infórmese sobre esto en **Asignación de SKU** en la sección [Exportar elementos a Shopify](synchronize-items.md#export-items-to-shopify).|Obtenga más información sobre esto en la sección [Efecto de los SKU y códigos de barras definidos del producto de Shopify en la asignación y la creación de artículos y variantes en Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Código de barras|**Referencias de artículos** de tipo código de barras.|**Referencias de artículos** de tipo código de barras.|
|Seguimiento de cantidad|De acuerdo con el campo **Inventario seguido** en la página **Tarjeta de tienda de Shopify**. Obtenga más información en la sección [Inventario](synchronize-items.md#sync-inventory-to-shopify). Solo se usa cuando exporta un producto por primera vez.|No utilizado.|
|Continuar vendiendo cuando no haya existencias|De acuerdo con la **Directiva de inventario predeterminada** en la **Tarjeta de tienda de Shopify**. Solo se usa cuando exporta un producto por primera vez.|No utilizado.|
|Tipo|**Descripción** de **Código de categoría de artículos**. Si el tipo no está especificado en Shopify, se agrega como un tipo personalizado.|**Código de categoría de artículos**. Mapeo por descripción.|
|Proveedor|**Nombre** del proveedor según el **N.º de proveedor**|Asignación de **N.º de proveedor** por nombre.|
|Peso|**Peso bruto**.|No utilizado.|
|Gravable|Valor fijo: habilitado.|No utilizado.|
|Códigos impositivos|**Código de grupo de impuestos**. Solo relevante para los impuestos. Obtenga más información en [Configurar impuestos](setup-taxes.md).|No utilizado.|

### Etiquetas

Revise las etiquetas importadas en el cuadro informativo **Etiquetas** en la página **Producto de Shopify**. En la misma página, para editar etiquetas, seleccione la acción **Etiquetas**.
Si la opción **A Shopify** está seleccionada en el campo **Artículo de sincronización**, las etiquetas asignadas se exportan a Shopify en la próxima sincronización.

## Ejecutar sincronización de artículos

La sincronización total o parcial de elementos se puede realizar de muchas maneras diferentes.

### Sincronización inicial de elementos de Business Central a Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Agregar artículos**.
3. En el campo **Código de tienda**, escriba el código. Si abre la ventana **Producto de Shopify** de la página **Tarjeta de tienda**, el código de tienda se completará automáticamente.
4. Si configuró la sincronización de imágenes e inventario, puede incluirlos en el mismo proceso. Incluirlos en el mismo proceso es conveniente para escenarios de demostración o cuando se trata de una cantidad menor de datos. 
5. Defina filtros en artículos según sea necesario. Por ejemplo, puede filtrar por el n.º de artículo. o código de categoría de artículo.
6. Elija **Aceptar**.

Los artículos resultantes se crean automáticamente en Shopify con precios. En función de las elecciones que haya realizado, es posible que se incluyan imágenes y niveles de inventario. La operación puede tardar algún tiempo si se agrega una gran cantidad de elementos.

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

### Sincronzar imágenes de productos desde la página de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar imágenes para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar imágenes de productos**.

### Sincronzar imágenes de productos desde la página de productos de Shopify

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
|**Cód. divisa**|Introduzca un código de moneda solo si su tienda en línea utiliza una moneda diferente a la moneda local (LCY). La divisa especificada debe tener tipos de cambio configurados. Si su tienda en línea usa la misma divisa que [!INCLUDEprod_short], deje el campo vacío.|

Los precios para productos sincronizados puede exportarlos de las dos formas que se describen a continuación.

### Sincronzar precios desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Sincronizar precios con Shopify**.

### Observaciones de cálculo de precios

* Al determinar un precio, [!INCLUDE[prod_short](../includes/prod_short.md)] utiliza la lógica del "precio más bajo". Sin embargo, la lógica del precio más bajo ignora el precio unitario definido en la tarjeta del producto si se define un precio en el grupo de precios. Esto es cierto incluso si el precio unitario del precio de la tarjeta del producto es más bajo.
* Para calcular los precios, el conector crea una oferta de venta temporal para el producto con una cantidad de 1 y utiliza la lógica de cálculo de precios estándar. Solo se utilizan los precios y descuentos aplicables a la cantidad 1. No puede exportar diferentes precios o descuentos en función de la cantidad.

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

La sincronización de inventarios se puede inicializar de las dos maneras que se describen a continuación.

### Sincronzar inventario desde la página de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar el inventario para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Sincronizar inventario**.

### Sincronizar inventario desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Sincronizar inventario**.

### Consideraciones sobre inventarios

* El método estándar de cálculo de existencias es **Saldo disponible proyectado en la fecha**. Con la extensibilidad, puede agregar más opciones. Para obtener más información sobre la extensibilidad, vaya a los [ejemplos](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md). 
* Puede consultar la información de existencias recibida de Shopify en la página **Cuadro informativo de inventario de Shopify**. En este cuadro informativo, obtendrá una descripción general de las existencias de Shopify y el último inventario calculado en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay un registro por ubicación.
* Si la información de existencias en Shopify es diferente de **Saldo disponible proyectado** en [!INCLUDE[prod_short](../includes/prod_short.md)], entonces las existencias se actualizarán en Shopify.
* Cuando agrega una nueva ubicación en Shopify, también necesita agregar registros de inventario para ella. Shopify no lo hace automáticamente para los productos y variantes existentes y el conector no sincronizará los niveles de inventario para dichos productos en la nueva ubicación. Para obtener más información, vaya a [Asignación de inventario a ubicaciones](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* El inventario y el envío en **Business Central Fulfillment Services** no son compatibles; en su lugar, use ubicaciones normales.

#### Ejemplo de cálculo de saldo disponible proyectado

Hay 10 piezas del artículo A disponibles y dos órdenes de venta pendientes. Uno para el lunes con cantidad *Uno* y otro para el jueves con cantidad *Dos*. Dependiendo de cuándo sincronice el inventario, el sistema actualizará el nivel de existencias en Shopify con diferentes cantidades:

|Cuando se ejecuta el inventario sincronizado|Valor utilizado para actualizar el nivel de existencias|Comentario|
|------|-----------------|-----------------|
|Martes|9|Inventario 10 menos pedido de venta programado para enviarse el lunes|
|Viernes|7|Inventario 10 menos ambas órdenes de venta|

## Consulte también .

[Comenzar con el conector para Shopify](get-started.md)  
