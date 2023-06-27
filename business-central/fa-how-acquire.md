---
title: Activos fijos adquiridos
description: 'Puede configurar un activo fijo, asignar un libro de amortización y registrar el coste de adquisición del activo fijo.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="acquire-fixed-assets"></a><a name="acquire-fixed-assets"></a>Activos fijos adquiridos

Deberá configurar una ficha con la información de cada activo. Puede configurar los edificios o los bienes de producción como activos principales con una lista de componentes y puede agruparlos de diferentes maneras como, por ejemplo, por clase, departamento o ubicación. Un libro de amortización debe estar configurado y asignado a cada activo fijo antes de que pueda adquirirlo.

Cuando se ha configurado un activo y se le ha asignado un libro de amortización, debe adquirirlo. Para adquirir un activo, registre el coste en la cuenta de contabilidad, la cuenta bancaria o el proveedor correspondiente registrando una transacción de adquisición desde la página **A/F Diario general**. Puede utilizar la página **Adquisición activos asistida** para crear y registrar las líneas del diario general requeridas automáticamente.

El valor residual es el valor restante de un activo cuando ya no se puede utilizar. Puede registrar el valor residual en el momento de registrar el coste. Para obtener más información, consulte [Depreciar o amortizar activos fijos](fa-how-depreciate-amortize.md).

El ajuste de valores se utiliza para ajustar los valores a los cambios de niveles generales de precio. El proceso **Ajustar valores activos** puede utilizarse para calcular los costes de adquisición como de sustitución.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a><a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Para crear un activo y adquirirlo automáticamente

El procedimiento siguiente describe cómo crear un activo y después adquirirlo utilizando la página **Adquisición activos asistida** para crear y registrar las líneas necesarias del diario general de activos. También puede crear y registrar las líneas de diario manualmente. Para obtener más información, consulte [Para registrar una adquisición de un activo manualmente con el diario general de activos](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos de la ficha desplegable **General** como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En la ficha desplegable **Ficha libros amortización**, rellene los campos según sea necesario. Este paso asigna un libro de amortización al activo.  
4. Si necesita asignar más de un libro de amortización al activo, elija la acción **Añadir más libros amortización**. Para obtener más información, consulte [Para asignar un libro de amortización a un activo fijo](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Cuando estén rellenados todos los campos requeridos para adquirir un activo, aparecerá la notificación **Está listo para adquirir el activo. Adquirir** en la parte superior de la página.
5. Seleccione la acción **Adquirir** en la notificación.
6. Siga los pasos de la página **Adquisición activos asistida** para completar la adquisición automática del activo.

> [!NOTE]  
>   Puede registrar los costes como abonos. En ese caso, recuerde que el valor del campo **Coste con IVA** debe tener el símbolo menos que indica un abono.

Cuando elige **Finalizar**, se rellena el campo **Valor libro** de la página **Ficha activo fijo** e indica que el activo se ha adquirido según el coste especificado.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a><a name="to-set-up-a-component-list-for-a-main-asset"></a>Para configurar una lista de componentes para un activo principal

Puede agrupar sus activos en principales y sus componentes. Por ejemplo, puede tener un equipo de producción que consista en muchas partes, las cuales desea agrupar de esta manera.  

Tanto el activo principal como todos sus componentes deben configurarse como fichas individuales de activos. Después de configurar una lista de componentes, [!INCLUDE[prod_short](includes/prod_short.md)] rellena automáticamente los campos **Principal/Componente** y **Componentes de activo principal** de las fichas de activos fijos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo principal y, a continuación, elija la acción **Componentes activo ppal**.
3. En la página **Componentes activo ppal.**, seleccione el campo **A/F Nº** y, a continuación, seleccione el activo que desea agregar como componente del activo principal.
4. Cierre la página.
5. Repita los pasos 3 y 4 para cada componente que desee agregar.
6. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de activos fijos** y luego elija el enlace relacionado.
7. Seleccione la casilla de verificación **Permitir reg. en activos pples**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a><a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Para registrar una adquisición de activo manualmente con el diario general de activos fijos

El procedimiento siguiente describe cómo adquirir un activo manualmente creando y registrando líneas en la página **A/F Diario general**. También puede adquirir un activo de manera automática utilizando la página **Adquisición activos asistida**. Para obtener más información, consulte el paso 5 en [Para crear un activo y adquirirlo automáticamente](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]  
>   Puede registrar los costes como abonos. En ese caso, recuerde que el valor del campo **Importe** debe tener el símbolo menos que indica un abono.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.
2. En la página **A/F Diario general**, en el campo **A/F Tipo registro**, seleccione **Coste**.
3. Rellene los campos restantes según sea necesario.
4. Seleccione la acción **Registrar**.  

> [!TIP]  
>   Si rellena el campo **Nº seguro** del diario general de activos fijos en el momento de registrar un coste, [!INCLUDE[prod_short](includes/prod_short.md)] también registrará el coste del activo en los movimientos de seguros. Para obtener más información, vea [Asegurar activos fijos](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a><a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Para anular un coste del registro de un activo

Si se equivoca al registrar un coste, puede eliminar el movimiento mediante el proceso **Cancelar movs. A/F** y registrar seguidamente el movimiento de adquisición correcto. Los movimientos incorrectos se transfieren a la página **A/F Movs. anulados**.

Por ejemplo, si registra una adquisición con la fecha incorrecta, debe corregirla lo más pronto posible porque la fecha de registro de un activo se utiliza para realizar muchos cálculos.

> [!IMPORTANT]  
> No puede usar la función **Transacciones inversas** para los movimientos de un activo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movs. Activos**, y luego elija el enlace relacionado.  
2. En la página **Movs. Activos**, seleccione la entrada o entradas que desea cancelar.  
3. Seleccione el menú **Acciones** y, a continuación, seleccione la acción **Cancelar movs.**.
4. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Elija el botón **Aceptar** para iniciar el trabajo por lotes.
6. Cuando se hayan cancelado el movimiento o movimientos incorrectos, registre el coste correcto.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a><a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Para registrar el valor residual junto con el coste

Puede registrar el valor residual junto con el coste a partir del diario de activos.

> [!NOTE]
> Este proceso puede requerir que personalice la página A/F Diario activos agregando el campo Valor residual. El campo Para no se muestra de forma predeterminada en la página. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Diario activos** y luego elija el enlace relacionado.
2. En la página **Diarios de activos fijos**, cree la línea de adquisición. Para obtener más información, consulte [Para registrar una adquisición de un activo manualmente con el diario general de activos](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. En el campo **Valor residual** de la línea del diario, escriba el importe del valor residual como abono (prefije la cantidad con un signo menos, por ejemplo, **-** 100).
4. Seleccione la acción **Registrar**.

> [!NOTE]
> Si existe un valor residual para un activo fijo, ese valor se utilizará en el registro de amortización en lugar del valor del campo **Valor contable final** en la página **Libros amortización A/F**. Para obtener más información, consulte [Para administrar el valor contable final](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/purchase-fixed-assets/) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
