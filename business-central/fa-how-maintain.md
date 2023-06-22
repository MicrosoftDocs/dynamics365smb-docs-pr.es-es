---
title: Mantener activos fijos
description: Usted mantiene un registro de mantenimiento de cualquier reparación y servicio en un activo fijo para preservar el valor de ese activo fijo.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="maintain-fixed-assets" />Mantener activos fijos

Los gastos de mantenimiento son costes periódicos habituales necesarios para mantener el valor de los activos fijos. A diferencia de los incrementos de capital, estos no aumentan de valor.

Puede registrar y mantener un archivo actualizado del mantenimiento y servicio de sus activos fijos para tener registros de mantenimiento completos en un activo fácilmente accesible. Cada vez que se envía un activo a recibir servicio se registran todos los datos importantes, como la fecha de servicio, el número de proveedor y el número de teléfono del agente de servicio. El registro de mantenimiento se realiza para cada activo desde la ficha de activos fijos pertinente.

El ajuste de valores se utiliza para ajustar los valores a los cambios de niveles generales de precio. El proceso **Ajustar valores activos** puede utilizarse para volver a calcular los costes de mantenimiento.

## <a name="to-record-maintenance-work-on-a-fixed-asset" />Para registrar el trabajo de mantenimiento en un activo

Cada vez que se realiza mantenimiento, como un servicio de visita, puede registrarlo en el activo correspondiente en la página **Registros mantenimiento**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.  
2. Seleccione el activo en el que desea registrar el mantenimiento y, a continuación, elija la acción **Registro mantenimiento**.
3. En la página **Registro mantenimiento**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal" />Para registrar los costes de mantenimiento a partir de un diario general de activos fijos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Lista libros amortización** y luego elija el enlace relacionado.  
2. Seleccione el libro de amortización que se ha asignado al activo y, a continuación, elija la acción **Editar**.
3. En la página **Ficha libro amortización**, asegúrese de que la casilla **Mantenimiento** no está seleccionada. Esto asegura que los costes de mantenimiento no se registren en el libro mayor.
4. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.  
5. Cree una línea inicial de diario y rellene los campos según sea necesario.
6. En el campo **A/F Tipo registro**, seleccione **Mantenimiento**.
7. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de mantenimiento.

    > [!NOTE]  
    >   El paso 7 solo funciona si ha configurado lo siguiente: en la página **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cta. mantenimiento** contiene la cuenta de cargo y el campo **Cta. contrap. mantenimiento** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación. Para obtener más información, vea [Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Seleccione la acción **Registrar**.

## <a name="to-follow-up-on-fixed-assets-service-visits" />Para realizar un seguimiento de visitas servicio en activos fijos

Puede imprimir el informe **Mnto. - Próxima revisión** para ver los activos programados con una visita. Puede utilizar este informe en el momento de actualizar el campo **Próxima fecha servicio** en las fiches de activos fijos.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Próxima revisión mantenimiento** y luego elija el enlace relacionado.  
2. Rellene los campos **Fecha inicial** y **Fecha final**  
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="to-monitor-maintenance-costs" />Para supervisar costes de mantenimiento

Puede ver los costes de mantenimiento si consulta las estadísticas de un activo.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo en el que desea ver los costes de mantenimiento y, a continuación, elija la acción **Libros amortización**.
3. En la página **Libros amortización A/F**, seleccione el libro de amortización de activos correspondiente y, a continuación, elija la acción **Estadísticas**.
4. En la página **Estadísticas activos fijos**, elija el campo **Mantenimiento**.

La página **Movs. mantenimiento** se abre y muestra los movimientos que conforman el importe en el campo **Mantenimiento**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets" />Para ver o imprimir los costes de mantenimiento de varios activos fijos

En el informe **Mnto. - Análisis**, puede seleccionar la vista de mantenimiento según uno, dos o tres códigos de mantenimiento para una fecha o periodo especificados. Puede ver el total de los activos seleccionados o un total para cada uno.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Análisis mantenimiento** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="to-view-maintenance-ledger-entries" />Para ver movimientos de mantenimiento

Puede estudiar también los costes de mantenimiento si consulta los movimientos en el libro mayor.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo en el que desea ver los movimientos de contabilidad y, a continuación, elija la acción **Libros amortización**.
3. En la página **Libros amortización A/F**, seleccione el libro de amortización de activos correspondiente y, a continuación, elija la acción **Movs. mantenimiento**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets" />Para ver o imprimir los movimientos de mantenimiento de varios activos fijos

En el informe **Mnto. - Detalles**, puede ver o imprimir los movimientos de mantenimiento para uno o varios activos fijos.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Detalles mantenimiento** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.
3. Elija el botón **Imprimir** o **Versión preliminar**.

## <a name="see-related-microsoft-trainingtrainingpathsmanage-fixed-assets-maintenance-insurances" />Consultar la [formación de Microsoft](/training/paths/manage-fixed-assets-maintenance-insurances/) relacionada

## <a name="see-also" />Consulte también .

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
