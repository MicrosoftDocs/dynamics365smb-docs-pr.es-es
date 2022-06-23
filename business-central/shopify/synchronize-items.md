---
title: Sincronizar artículos e inventario
description: Configurar y ejecutar sincronizaciones de artículos entre Shopify y Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ad69d58a84926041df1125809f748b9129cc64e2
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808964"
---
# <a name="synchronize-items-and-inventory"></a>Sincronizar artículos e inventario

Los **Artículos** en [!INCLUDE[prod_short](../includes/prod_short.md)] son equivalentes a los *productos* en Shopify, lo que incluye bienes físicos, descargas digitales, servicios y tarjetas de regalo que vende. Hay dos razones principales para sincronizar los artículos:

1. Principalmente, la gestión de datos se realiza en [!INCLUDE[prod_short](../includes/prod_short.md)], necesita exportar todos o algunos datos a Shopify y hacerlos visible. Puede exportar el nombre del artículo, la descripción, la imagen, los precios, la disponibilidad, las variantes, los detalles del proveedor y el código de barras. Una vez importados, los artículos pueden volverse visibles inmediatamente o pueden ser revisados y mejorados por una persona responsable primero.
2. Cuando un pedido de Shopify se importa, la información sobre los artículos es esencial para el procesamiento posterior del documento en [!INCLUDE[prod_short](../includes/prod_short.md)].

Estos dos escenarios siempre están habilitados.

Un tercer escenario es administrar datos en Shopify pero importar esos productos a granel para [!INCLUDE[prod_short](../includes/prod_short.md)]. Este escenario puede ser útil para eventos de migración de datos, cuando quiere conectar una tienda en línea existente con un entorno [!INCLUDE[prod_short](../includes/prod_short.md)] nuevo.

## <a name="to-define-item-synchronizations"></a>Para definir las sincronizaciones de artículos

1. Elija el icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , entre en la **Tienda Shopify**. Abra una tienda para la que quiera configurar la sincronización de artículos.
2. En el campo **Sincronizar artículo**, seleccione la opción requerida. <br>La siguiente tabla describe las diferencias entre las opciones.

|Opción|Descripción|
|------|-----------|
|**En blanco**| Los productos se importan junto con la importación de pedidos. Los productos se exportan a Shopify si un usuario ejecuta la acción **Agregar artículo** desde la página **Productos de Shopify**. Este proceso es el comportamiento predeterminado. |
|**A Shopify**| Seleccione esta opción si, después de la sincronización inicial desencadenada por la acción **Agregar artículo**, planea actualizar los productos manualmente usando la acción **Sincronizar producto** o a través de la cola de trabajos para actualizaciones periódicas. Recuerde habilitar el campo **Puede actualizar producto de Shopify**. Si no está habilitado, es igual a la opción **En blanco**. Para obtener más información, consulte [Exportar artículos a Shopify](synchronize-items.md#export-items-to-shopify).|
|**Desde Shopify**| Elija esta opción, si planea importar productos de Shopify de forma masiva; ya sea manualmente usando la acción **Sincronizar producto** o a través de la cola de trabajos para actualizaciones periódicas. Si no se selecciona ninguna opción, es igual a la opción **En blanco**. Para obtener más detalles sobre la importación de artículos, consulte [Importar artículos desde Shopify](synchronize-items.md#import-items-from-shopify)|

## <a name="import-items-from-shopify"></a>Importar artículos desde Shopify

Si importa artículos de Shopify de forma masiva o junto con la importación de pedidos, estos artículos se agregan primero a las tablas **Producto de Shopify** y **Variante de Shopify**. Las siguientes configuraciones le permiten administrar el proceso:

|Campo|Descripción|
|------|-----------|
|**Crear artículos desconocidos automáticamente**|Cuando se importan productos y variantes de Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)], la función [!INCLUDE[prod_short](../includes/prod_short.md)] siempre intenta encontrar primero el registro coincidente en la lista de artículos. **Asignación de SKU** afecta a cómo se realiza la correspondencia y crea un nuevo artículo y/o variante de artículo. Habilite esta opción si desea crear un nuevo artículo o cuando no existe un registro correspondiente. El nuevo elemento se creará utilizando datos importados y **Código de plantilla de artículos**. Si esta opción no está habilitada, deberá crear un artículo manualmente y usar la acción **Asignar producto** desde la página **Productos de Shopify**.|
|**Código de plantilla de artículos**|Se usa con **Creación automática de artículos desconocidos**. <br> Elija la plantilla que se utilizará para los elementos creados automáticamente.|
|**Asignación de SKU**|Elige cómo quiere usar el valor de **SKU** importado de Shopify durante el mapeo y la creación de artículos/variantes. Para más información, vea [Cómo el SKU y código de barras definidos en el producto de Shopify afecta el mapeo y la creación de artículos y variantes](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**Separador de campo de SKU**|Se usa junto con **Asignación de SKU** ajustado a la opción **N.º de artículo + Código de variante**.<br> Defina un separador que debe usarse para dividir SKU. <br>Por ejemplo, si en Shopify crea la variante con SKU '1000/001', escriba '/' en el campo **Separador de campo SKU** para obtener el número de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] como '1000' y el código de variante del artículo como '001'.
|**Prefijo de variante**|Se usa junto con **Asignación de SKU** ajustado a **Código de variante** o **N.º de articulo + Código de variante** como una estrategia alternativa cuando el SKU proveniente de Shopify esta vacío.<br>Si desea crear la variante de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] automáticamente, tendrá que introducir un valor en **Código**. Por defecto, se usa el valor definido en el campo SKU importado de Shopify. Sin embargo, si el SKU está vacío, generará un código que comenzará con el prefijo de variante definido y "001".|
|**Shopify puede actualizar artículo**| Elija esta opción si desea actualizar artículos y/o variantes automáticamente.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Cómo los SKU y códigos de barras definidos en el producto de Shopify afectan al mapeo y la creación de artículos y variantes en Business Central

Cuando los productos son importados desde Shopify a las tablas **Productos de Shopify** y **variantes de Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] intenta encontrar registros existentes. La siguiente tabla describe las diferencias entre las opciones del campo **Asignación de SKU**.

|Opción|Efecto en el mapeo|Efecto en la creación|
|------|-----------------|------------------|
|**En blanco**|El campo SKU no se usa en la rutina de mapeo de artículos.|Sin efecto en la creación del elemento. <br>Impide la creación de variantes. Es útil cuando en el pedido de ventas solo se usa el artículo principal. Una variante se sigue pudiendo mapear manualmente desde la ventana **Productos de Shopify**.|
|**Nº producto**|Elíjalo si el campo SKU contiene el número de artículo.|Sin efecto en la creación del elemento sin variantes. Para un artículo con variantes, cada variante se crea como un artículo separado.<br> Por ejemplo, si Shopify tiene un producto con dos variantes y sus SKU son '1000' y '2000', en [!INCLUDE[prod_short](../includes/prod_short.md)] el sistema creará dos artículos con los números '1000' y '2000'.|
|**Cód. variante**|El campo SKU no se usa en la rutina de mapeo de artículos.|Sin efecto en la creación del elemento. Cuando se crea una variante de artículo, el valor del campo SKU se usa como código. Si el SKU está vacío, se genera un código usando el campo **Prefijo de variante**.|
|**N.º artículo + Código de variante**| Seleccione si el campo SKU contiene un número de artículo. y el código de variante del artículo separados por el valor definido en el campo **Separador de campos SKU**.|Cuando se crea un artículo, la primera parte del valor del campo SKU se usa como **N.º**. Si el SKU está vacío, un número de artículo se genera utilizando series numéricas definidas en el **Código de plantilla de artículo** o **Números de artículo** de la ventana **Configuración de inventario**.<br>Cuando se crea un artículo, la función variante usa la segunda del valor del campo SKU se usa como **Código**. Si el SKU está vacío, se genera un código usando el campo **Prefijo de variante**.|
|**N.º de artículo de proveedor**| Elija si el campo SKU contiene el número de artículo del proveedor. En este caso, el **Número de proveedor de artículo** no se usa en la ventana **Tarjeta de artículo**, sino **Número de artículo del proveedor** del **Catálogo de proveedores de artículos**. Si el registro encontrado *Catálogo de proveedores de artículos* contiene un código de variante, este código de variante se utiliza para mapear la variante de Shopify.|Si existe un proveedor correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)], el valor de SKU se usará como **Número de artículo del proveedor** en **Tarjeta de artículo** y como **Referencia del artículo** de tipo proveedor. <br>Impide la creación de variantes. Es útil cuando desea usar el artículo principal solo en el pedido de ventas. Debería seguir pudiendo asignar una variante manualmente desde la ventana **Productos de Shopify**.|
|**Código de barras**| Elíjalo si el campo SKU contiene un código de barras. Se realiza una búsqueda entre **Referencias de artículos** de tipo proveedor. Si el registro encontrado Referencia de artículo contiene un código de variante, este código de variante se utilizará para mapear la variante de Shopify.|Sin efecto en la creación del elemento. <br>Impide la creación de variantes. Puede ser útil cuando en el pedido de ventas solo se usa el artículo principal. Una variante se sigue pudiendo mapear manualmente desde la ventana **Productos de Shopify**.|

En la tabla siguiente se describe el efecto del campo **Código de barras**.

|Efecto en el mapeo|Efecto en la creación|
|-----------------|------------------|
|Se realiza una búsqueda entre **Referencias de artículos** del tipo código de barras para el valor definido en el campo Código de barras en Shopify. Si el registro encontrado Referencia de artículo contiene un código de variante, este código de variante se utilizará para mapear la variante de Shopify.|El código de barras se guarda como **Referencia del artículo** para artículo y variante de artículo.|

> [!NOTE]  
> Puede desencadenar el mapeo para el producto/variantes seleccionados o todos los productos importados no mapeados seleccionando **Intentar buscar mapeo de producto** (para el seleccionado) o **Intentar buscar asignaciones** (para todos).

## <a name="export-items-to-shopify"></a>Exportar elementos a Shopify

Elija los elementos de su lista de elementos, que se exportarán a Shopify. Utilice la acción **Agregar artículo** en la ventana **Productos de Shopify** para agregar elementos a la lista de productos de Shopify.

Las siguientes configuraciones le permiten administrar el proceso de exportar artículos:

|Campo|Descripción|
|------|-----------|
|**Grupo de precios de cliente**|Determine el precio de un artículo en Shopify. Se toma el precio de venta de este grupo de precios de cliente. Si no se ingresa ningún grupo, se utiliza el precio de la ficha del artículo.|
|**Grupo de descuentos de cliente**|Determinar el descuento que se utilizará para calcular el precio de un artículo en Shopify. Los precios con descuento se almacenan en el campo **Precio** y el precio completo se almacena en el campo **Comparar en el precio**.|
|**Sincronizar texto adicional de artículo**|Seleccione para sincronizar el texto extendido del elemento. Como se agregará a *Descripción*, puede contener código HTML. |
|**Sincronizar atributos de artículo**|Seleccione para sincronizar los atributos del artículo. Los atributos tienen el formato de una tabla y se incluyen en el campo *Descripción* en Shopify.|
|**Código de idioma**|Si se selecciona, las versiones traducidas se utilizan para el título, los atributos y el texto ampliado.|
|**Asignación de SKU**|Elija cómo desea completar el campo SKU en Shopify. Las opciones admitidas son:<br> - **N.º de artículo** para usar el n.º de artículo tanto para productos como para variantes.<br> - **N.º de artículo + Código de variante** para crear un SKU concatenando valores de dos campos. Para artículos sin variantes, el n.º de artículo se usa solo.<br>- **N.º de proveedor de artículo** para utilizar el número de proveedor del artículo definido en *Tarjeta de artículo* tanto para productos como para variantes.<br> - **Código de barras**: usa **Referencia del artículo** de tipo código de barras. Esta opción respeta las variantes. |
|**Separador de campo de SKU**|Defina un separador para la opción **N.º de articulo + Código de variante**.|
|**Inventario seguido**|Elija cómo el sistema debe llenar el campo **Seguimiento de inventario** para productos exportados a Shopify. Puede actualizar la información de disponibilidad desde [!INCLUDE[prod_short](../includes/prod_short.md)] para productos en Shopify cuyo inventario de seguimiento está habilitado. Para obtener más información, vea [Inventario](synchronize-items.md#sync-inventory-to-shopify).|
|**Directiva de inventario predeterminada**|Escoja *Denegar* para evitar existencias negativas del lado de Shopify. |
|**Puede actualizar productos de Shopify**|Defina si [!INCLUDE[prod_short](../includes/prod_short.md)] solo puede crear elementos o también puede actualizar elementos. Seleccione esta opción si, después de la sincronización inicial desencadenada por la acción **Agregar artículo**, planea actualizar los productos manualmente usando la acción **Sincronizar producto** o a través de la cola de trabajos para actualizaciones periódicas. Recuerde seleccionar **A Shopify** en el campo **Sincronización de elementos**.|

### <a name="fields-mapping-overview"></a>Información general de asignaciones de campos

|Shopify|Origen cuando se exporta desde [!INCLUDE[prod_short](../includes/prod_short.md)]|Destino cuando se importa a [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|De acuerdo con **Estado de los productos creados** en la **Tarjeta de tienda de Shopify**. Para más información, vea [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hock-updates-of-shopify-products).|No utilizado.|
|Cargo|**Descripción**. Si el código de idioma está definido y existe la traducción del artículo correspondiente, se utilizará la traducción del artículo en lugar de la descripción.|**Descripción**|
|Descripción|Combina textos extendidos y atributos silas alternancias correspondientes de la tarjeta de Shopify están habilitadas. Respeta el código de idioma.|No utilizado.|
|Título de página SEO|Valor fijo: vacío, vea [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hock-updates-of-shopify-products). |No utilizado.|
|Descripción meta de SEO|Valor fijo: vacío, vea [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hock-updates-of-shopify-products). |No utilizado.|
|Medios|**Imagen**, para más información, vea [Sincronizar imágenes de artículos](synchronize-items.md#sync-item-images)|**Imagen**|
|Precio|El cálculo del precio del cliente final incluye el grupo de precios del artículo, el grupo de descuento del artículo, el código de moneda y el código de plantilla de cliente. |No utilizado.|
|Comparar por precio|El cálculo del precio sin descuento incluye el grupo de precios del artículo, el grupo de descuento del artículo, el código de moneda y el código de plantilla de cliente. |No utilizado.|
|Coste por artículo|**Coste unitario**|**Coste unitario**|
|UA|Vea **Asignación de SKU** en [Exportar elementos a Shopify](synchronize-items.md#export-items-to-shopify)| Vea [Cómo el SKU y el código de barras definidos en el producto de Shopify afectan al mapeo y la creación de artículos y variantes](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|Código de barras|**Referencias de artículos** de tipo código de barras|**Referencias de artículos** de tipo código de barras|
|Seguimiento de cantidad|De acuerdo con el **Inventario seguido** en la **Tarjeta de tienda de Shopify**. Para obtener más información, vea [Inventario](synchronize-items.md#sync-inventory-to-shopify).|No utilizado.|
|Continuar vendiendo cuando no haya existencias|De acuerdo con la **Directiva de inventario predeterminada** en la **Tarjeta de tienda de Shopify**. No importado.|No utilizado.|
|Tipo|**Descripción** de **Código de categoría de artículos**. Si el tipo no está especificado en Shopify, se agregará como un tipo personalizado.|**Código de categoría de artículos**. Mapeo por descripción.|
|Proveedor|**Nombre** del proveedor según el **N.º de proveedor** |Asignación de **N.º de proveedor** por nombre.|
|Peso|**Peso bruto**.|No utilizado.|
|Gravable|Valor fijo: habilitado.|No utilizado.|
|Códigos impositivos|**Código de grupo de impuestos**. Solo relevante para los impuestos. Para obtener más información, consulte [impuesto](synchronize-orders.md#tax-remarks). |No utilizado.|

### <a name="tags"></a>Etiquetas

Revise las etiquetas importadas en el cuadro informativo **Etiquetas** en la página del **Producto de Shopify**. Para editar etiquetas, seleccione la acción **Etiquetas** en la página **Producto de Shopify**.
Si la opción **A Shopify** está seleccionada en el campo **Artículo de sincronización**, las etiquetas asignadas se exportan a Shopify en la próxima sincronización.

## <a name="run-item-synchronization"></a>Ejecutar sincronización de artículos

La sincronización total o parcial de elementos se puede realizar de muchas maneras diferentes.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Sincronización inicial de elementos de Business Central a Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Agregar artículos**.
3. En el campo **Código de tienda**, escriba el código. Si abre la ventana **Producto de Shopify** de la ventana **Tarjeta de tienda**, el código de la tienda se completará automáticamente.
4. Defina filtros en artículos según sea necesario. Por ejemplo, puede filtrar por n.º de artículo. o código de categoría de artículo.
5. Elija **Aceptar**.

Los elementos resultantes se crean automáticamente en Shopify con precios, pero las imágenes y los niveles de inventario no están incluidos. La operación puede tardar algún tiempo si se agrega una gran cantidad de elementos.

### <a name="sync-products-from-shopify-to-business-central"></a>Sincronizar productos de Shopify a Business Central

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar artículos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar productos**.

Como alternativa, utilice la acción **Sincronizar productos** en la ventana **Productos de Shopify** o busque el trabajo por lotes **Sincronizar productos**.

Puede programar la tarea para que se realicen de forma automatizada. Para obtener más información, consulte [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

### <a name="ad-hock-updates-of-shopify-products"></a>Actualizaciones ad hoc de productos de Shopify

Cuando se actualizan los registros en la tabla **Productos de Shopify**, los siguientes cambios se sincronizan con Shopify.

Actualizar:

* **Estado**: puede elegir entre activo, archivado o borrador.
* **Título de SEO**
* **Descripción de SEO**

Eliminación:

Según el valor de **Acción para productos eliminados** en **Tarjeta de tienda de Shopify**, el producto se actualiza en Shopify cuando se elimina el registro de la página **Productos de Shopify**.

* **En blanco**: nada pasará. Si es necesario, el usuario debe realizar la acción requerida desde el administrador de Shopify.
* **Estado a Borrador**: el estado del producto en Shopify se establece en *Borrador*.
* **Estado a archivado**: el producto se archiva en Shopify.

## <a name="sync-item-images"></a>Sincronizar imágenes de artículo

La sincronización de imágenes se puede configurar para elementos sincronizados. Elija una de las opciones siguientes:

* **En blanco**: la sincronización de imágenes se desactiva.
* **A Shopify**: las imágenes de los artículos se exportan a Shopify
* **Desde Shopify**: las imágenes de Shopify se importan a [!INCLUDE[prod_short](../includes/prod_short.md)]

La sincronización de imágenes se puede inicializar de dos maneras.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Sincronzar imágenes de productos desde la ventana de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar imágenes para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar imágenes de productos**.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Sincronzar imágenes de productos desde la ventana de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Sincronizar imágenes de productos**.

### <a name="image-synchronization-remarks"></a>Observaciones de sincronización de imágenes

* Al exportar imágenes de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, las nuevas imágenes se añaden a Shopify, manteniendo intactas las imágenes antiguas. Si una imagen se actualiza en [!INCLUDE[prod_short](../includes/prod_short.md)], deberá eliminar las imágenes antiguas en el administrador de Shopify.
* Las imágenes que se exportan a Shopify y no cumplen con los requisitos definidos por Shopify no se importarán. Para más información, vea [Tipos de medios de productos en help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Sincronizar precios con Shopify

Los precios se pueden exportar para artículos sincronizados de las formas que se describen a continuación.

### <a name="sync-prices-from-the-shopify-products-window"></a>Sincronzar precios desde la ventana de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Sincronizar precios con Shopify**.

### <a name="price-calculation-remarks"></a>Observaciones de cálculo de precios

* Para el cálculo del precio, es importante tener un valor en el campo **Plantilla de cliente predeterminada**. [!INCLUDE[prod_short](../includes/prod_short.md)] utiliza el valor del campo **Grupo empresarial IVA** para calcular el precio con IVA incluido. Es posible que desee crear un grupo de precios de clientes en el que seleccione el campo **Precio con IVA incluido** y especifique el valor relevante en el campo **(Precio) gr. publicación comercial IVA**.
* Introduzca un **Código de moneda** si su tienda en línea utiliza una moneda diferente a LCY. La divisa especificada debe tener tipos de cambio configurados. Si su tienda en línea usa la misma divisa que [!INCLUDE[prod_short](../includes/prod_short.md)], deje el campo vacío.
* Al determinar un precio, [!INCLUDE[prod_short](../includes/prod_short.md)] utiliza la lógica del "Precio más bajo". Significa que si el precio unitario definido en la ficha del artículo es inferior al definido en el grupo de precios, se utiliza el precio unitario de la ficha del artículo.

## <a name="sync-inventory-to-shopify"></a>Sincronizar inventario a Shopify

La sincronización de inventario se puede configurar para elementos ya sincronizados. Hay dos condiciones que se deben cumplir:

1. El seguimiento de inventario debe estar habilitado para un producto en Shopify. Si los artículos se exportan a Shopify, considere habilitar la alternancia **Inventario seguido** en la **Tarjeta Shopify**. Para obtener más información, consulte [Exportar artículos a Shopify](synchronize-items.md#export-items-to-shopify).
2. La sincronización de inventario debe estar habilitada para **Ubicaciones de Shopify**.

### <a name="to-enable-inventory-sync"></a>Para habilitar la sincronización de inventario

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar el inventario para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Ubicaciones** para abrir **Ubicaciones de tienda de Shopify**.
4. Elija la acción **Conseguir unicaciones de Shopify** para importar todas las ubicaciones definidas en Shopify. Puedes encontrarlas en la configuración de [**Ubicaciones**](https://www.shopify.com/admin/settings/locations) del **Administrador de Shopify**.
5. En el campo **Filtro de ubicación**, agregue ubicaciones, si desea incluir inventario solo de ubicaciones específicas. Por ejemplo, puede introducir *ESTE|OESTE*, de modo que el inventario solo de estas dos ubicaciones esté disponible para la venta a través de la tienda en línea.
6. Deseleccione la alternancia **Desactivado** para habilitar la sincronización de inventario para ubicaciones de Shopify seleccionadas.

La sincronización de inventarios se puede inicializar de dos maneras.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Sincronzar inventario desde la ventana de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar el inventario para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Sincronizar inventario**.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Sincronzar inventario desde la ventana de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Sincronizar inventario**.

### <a name="inventory-remarks"></a>Consideraciones sobre inventarios

* El conector calcula el **Saldo disponible proyectado** y lo exporta a Shopify.
* Puede consultar la información de existencias recibida de Shopify en la página **Cuadro informativo de inventario de Shopify**. En este cuadro informativo, obtendrá una descripción general de las existencias de Shopify y el último inventario calculado en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay un registro por ubicación.
* Si la información de existencias en Shopify es diferente de **Saldo disponible proyectado** en [!INCLUDE[prod_short](../includes/prod_short.md)], entonces las existencias se actualizarán en Shopify.

## <a name="see-also"></a>Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
