---
title: Adquirir activos fijos
description: 'Puede configurar un activo fijo, asignar un libro de amortización y registrar el coste de adquisición del activo fijo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="acquire-fixed-assets"></a>Adquirir activos fijos

Utilice la página **Tarjeta de activos fijos** para ingresar información sobre un activo. Puede configurar los edificios o los bienes de producción como activos principales con una lista de componentes y puede agruparlos de diferentes maneras como, por ejemplo, por clase, departamento o ubicación. Debe configurar y asignar un libro de depreciación a cada activo fijo antes de poder adquirirlo.

Después de configurar un activo fijo y asignar un libro de depreciación, debe adquirir el activo fijo. Para adquirir un activo, registre el coste en la cuenta de contabilidad, la cuenta bancaria o el proveedor correspondiente registrando una transacción de adquisición desde la página **A/F Diario general**. Puede utilizar la página **Adquisición activos asistida** para crear y registrar las líneas del diario general requeridas automáticamente.

Utilice la indexación para ajustar los valores según los cambios generales en el nivel de precios. Utilice el trabajo por lotes **Indexar activos fijos** para calcular los costos de adquisición y los costos de reemplazo.

## <a name="add-a-fixed-asset-to-your-list-of-fixed-assets"></a>Agregue un activo fijo a su lista de activos fijos

Antes de poder adquirir un activo fijo, debe agregarlo a su lista de activos. Hay varias formas de agregar activos fijos a su lista:

* Ingrese información sobre los activos en la página  **Tarjeta de activos fijos** .
* Utilice la acción **Editar en Excel** para descargar su lista de activos a una hoja de cálculo, agregar nuevos activos a la lista y luego publicar la actualización en [!INCLUDE [prod_short](includes/prod_short.md)].
* Utilice una orden de compra para agregar activos.
* Utilice la acción **Copiar activo fijo** .

Después de agregar activos fijos a su lista, el siguiente paso es adquirirlos para poder usarlos en transacciones. Obtenga más información en [Adquirir un activo fijo](#acquire-fixed-assets).

### <a name="add-a-fixed-asset-on-the-fixed-asset-card-page"></a>Agregar un activo fijo en la página Tarjeta de activo fijo

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Activos fijos** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos de la ficha desplegable **General** como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En la ficha desplegable **Ficha libros amortización**, rellene los campos según sea necesario. Este paso asigna un libro de amortización al activo.  
4. Si necesita asignar más de un libro de amortización al activo, elija la acción **Añadir más libros amortización**. Para obtener más información, vaya a [Para asignar un libro de depreciación a un activo fijo](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Después de completar los campos obligatorios, **Está listo para adquirir el activo fijo.** La notificación aparece en la parte superior de la página. Si está listo para adquirir el activo ahora, elija la acción **Adquirir** . Siga los pasos en la página **Adquisición asistida de activos fijos** para completar la adquisición. Si no está listo, siempre puede adquirir el activo más tarde.

### <a name="use-edit-in-excel-to-add-assets"></a>Utilice Editar en Excel para agregar activos

Si desea agregar numerosos activos fijos, Editar en Excel es una excelente herramienta. La herramienta descarga su lista actual de activos en una hoja de trabajo que incluye la mayoría de los campos disponibles en la página Tarjeta de activos fijos. Puede completar algunos o todos los campos en una fila para cada activo y publicar sus cambios para agregarlos a su lista en [!INCLUDE [prod_short](includes/prod_short.md)]. Si no puede completar todos los campos obligatorios, está bien. Puedes actualizarlos en [!INCLUDE [prod_short](includes/prod_short.md)] cuando estés listo.

> [!NOTE]
> Para utilizar la acción Editar en Excel, debe tener instalado el complemento Microsoft Dynamics Office. El complemento crea la conexión entre Excel y [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, vaya a [Obtener el complemento Business Central para Excel](admin-deploy-excel-addin.md).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Elija el ícono :::image type="content" source="media/share-icon.png" alt-text="Compartir esta página con otros usuarios o aplicaciones."::: Y luego elija **Editar en Excel**.
3. Abra el archivo descargado e ingrese información sobre los nuevos activos fijos.

   > [!TIP]
   > No es necesario introducir un identificador en el campo **No.** . Cuando publica su actualización, [!INCLUDE [prod_short](includes/prod_short.md)] asigna un identificador según la serie numérica que utiliza para los activos fijos.

4. Para actualizar [!INCLUDE [prod_short](includes/prod_short.md)], en el panel **Microsoft Dynamics**, elija **Publicar**.

### <a name="add-a-fixed-asset-from-a-purchase-order-or-invoice"></a>Agregar un activo fijo desde una orden de compra o factura

Los siguientes pasos describen cómo agregar un activo fijo desde una orden de compra. Los pasos son similares para una factura de compra.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. Elija **Nuevo** para crear una nueva orden de compra.
3. En la ficha desplegable **General**, rellene los campos como sea necesario. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4. En la ficha desplegable **Líneas**, en el campo **Tipo**, elija **Activo fijo**.
5. En el campo **N.º**, , elija un activo fijo existente para agregar un gasto o elija **Nuevo** para agregar un nuevo activo.
6. Después de ingresar la información del nuevo activo y la orden de compra, elija **Publicar**.

## <a name="acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal"></a>Adquirir un activo fijo utilizando un diario del L/M de activos fijos

El siguiente procedimiento describe cómo adquirir mediante la creación y contabilización de las líneas de diario del Libro Mayor de activos fijos requeridas. También puede crear y registrar las líneas de diario manualmente. Para obtener más información, vaya a [Adquirir un activo fijo mediante un diario del libro mayor de activos fijos](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
1. Elija el activo que desea adquirir y luego elija la acción **Adquirir** .
1. Siga los pasos en la página **Adquisición asistida de activos fijos** para completar la adquisición.

> [!NOTE]  
> Puede registrar los costes como abonos. En ese caso, recuerde que el valor del campo **Coste con IVA** debe tener el símbolo menos que indica un abono.

Cuando elige **Terminar**, el campo **Valor contable** en la **Tarjeta de activos fijos**  se completa, lo que indica que el activo fijo fue adquirido al costo de adquisición especificado.  

## <a name="to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal"></a>Para registrar una adquisición de activos fijos manualmente con un diario del L/M de activos fijos

El procedimiento siguiente describe cómo adquirir un activo manualmente creando y registrando líneas en la página **A/F Diario general**. También puede adquirir un activo fijo automáticamente en la página **Tarjeta de Activo Fijo** eligiendo la acción **Adquirir activo fijo** . Para obtener más información, vaya a [Adquirir un activo fijo](#acquire-fixed-assets).

> [!NOTE]  
> Puede registrar los costes como abonos. En ese caso, recuerde que el valor del campo **Importe** debe tener el símbolo menos que indica un abono.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales de activos fijos** y luego elija el enlace relacionado.
2. En la página **A/F Diario general**, en el campo **A/F Tipo registro**, seleccione **Coste**.
3. Rellene los campos restantes según sea necesario.
4. Seleccione la acción **Registrar**.  

> [!TIP]  
> Si completa el campo **Nº de seguro**, [!INCLUDE[prod_short](includes/prod_short.md)] también contabiliza el costo de adquisición del activo fijo en el libro mayor de cobertura de seguro. Para obtener más información, vaya a [Asegurar activos fijos](fa-how-insure.md).

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Para configurar una lista de componentes para un activo principal

Puede agrupar sus activos en principales y sus componentes. Por ejemplo, es posible que tenga una máquina de producción que consta de varias piezas que desee agrupar de esta manera.  

Debe configurar el activo principal y todos sus componentes como activo fijo individual. Después de configurar una lista de componentes, [!INCLUDE[prod_short](includes/prod_short.md)] completa automáticamente los **Activos/componentes principales** y **Componentes del activo principal** campos en los activos fijos.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo principal y, a continuación, elija la acción **Componentes activo ppal**.
3. En la página **Componentes activo ppal.**, seleccione el campo **A/F Nº** y, a continuación, seleccione el activo que desea agregar como componente del activo principal.
4. Cierre la página.
5. Repita los pasos 3 y 4 para cada componente que desee agregar.
6. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de activos fijos** y luego elija el enlace relacionado.
7. Active la opción **Permitir publicación en activos principales** .

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Para anular un coste del registro de un activo

Si se equivoca al registrar un coste, puede eliminar el movimiento mediante el proceso **Cancelar movs. A/F** y registrar seguidamente el movimiento de adquisición correcto. Los movimientos incorrectos se transfieren a la página **A/F Movs. anulados**.

Por ejemplo, si registra una adquisición con la fecha incorrecta, debe corregirla lo más pronto posible porque la fecha de registro de un activo se utiliza para realizar muchos cálculos.

> [!IMPORTANT]  
> No puede utilizar la acción **Transacciones inversas** para entradas de activos fijos.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movs. Activos**, y luego elija el enlace relacionado.  
2. En la página **Movs. Activos**, seleccione la entrada o entradas que desea cancelar.  
3. Seleccione el menú **Acciones** y, a continuación, seleccione la acción **Cancelar movs.**.
4. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Elija el botón **Aceptar** para iniciar el trabajo por lotes.
6. Cuando se hayan cancelado el movimiento o movimientos incorrectos, registre el coste correcto.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Para registrar el valor residual junto con el coste

El valor residual es el valor restante de un activo cuando ya no se puede utilizar. Puede registrar el valor residual en el momento de registrar el coste. Para obtener más información, vaya a [Depreciar o amortizar activos fijos](fa-how-depreciate-amortize.md).

Puede registrar el valor residual junto con el coste a partir del diario de activos.

> [!NOTE]
> Este proceso puede requerir que personalice la página A/F Diario activos agregando el campo Valor residual. El campo Para no se muestra de forma predeterminada en la página. Para obtener más información, vaya a [Personalice su espacio de trabajo](ui-personalization-user.md).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Diario activos** y luego elija el enlace relacionado.
2. En la página **Diarios de activos fijos**, cree la línea de adquisición. Para obtener más información, vaya a [Para registrar una adquisición de activos fijos manualmente con un diario del L/M de activos fijos](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. En el campo **Valor residual** de la línea del diario, escriba el importe del valor residual como abono (prefije la cantidad con un signo menos, por ejemplo, **-** 100).
4. Seleccione la acción **Registrar**.

> [!NOTE]
> Si existe un valor de rescate para un activo fijo, ese valor se utiliza en la contabilización de la depreciación en lugar del valor en el campo **Valor contable final** en el **Libros de depreciación FA** página. Para obtener más información, vaya a [Para administrar el valor contable final](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Consulte también

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Detalles de diseño sobre el impacto del IVA no deducible en Activos Fijos](design-details-nondeductible-vat.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
