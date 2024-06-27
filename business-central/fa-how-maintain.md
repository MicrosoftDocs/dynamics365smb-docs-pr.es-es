---
title: Mantener activos fijos
description: Registre las reparaciones y el servicio de un activo fijo para preservar su valor.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Mantener activos fijos

Los costes de mantenimiento son gastos operativos de las cosas que hace para preservar la condición de sus activos fijos. A diferencia de las mejoras de capital, el mantenimiento no aumenta el valor de sus activos.

Cada vez que envía un activo para recibir servicio se registran datos como la fecha de servicio, el número de proveedor, quién ha realizado el trabajo y el número de teléfono del agente de servicio. La información de mantenimiento se introduce en varias páginas:

* Ficha activo
* Pedido compra
* Factura de compra
* A/F Diario general

El ajuste de valores se utiliza para ajustar los valores a los cambios de niveles generales de precio. Utilice la acción **Ajustar valores activos** para volver a calcular los costes de mantenimiento.

## Registrar un coste de mantenimiento directamente en un activo fijo

Cada vez que se realiza mantenimiento para un activo, como un servicio de visita, puede registrarlo en la página **Registros mantenimiento**.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Activos fijos** y luego elija el enlace relacionado.  
2. Seleccione el activo en el que desea registrar el mantenimiento y, a continuación, elija la acción **Registro mantenimiento**.
3. En la página **Registro mantenimiento**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Registre los costes de mantenimiento a partir de un diario general de activos fijos

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Lista libros amortización** y luego elija el enlace relacionado.  
2. Seleccione el libro de amortización que se ha asignado al activo y, a continuación, elija la acción **Editar**.
3. En la página **Ficha libro amortización**, asegúrese de que la casilla de verificación **Mantenimiento** no esté seleccionada para no contabilizar los costes de mantenimiento en la contabilidad general.
4. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.  
5. Cree una línea inicial de diario y rellene los campos según sea necesario.
6. En el campo **A/F Tipo registro**, seleccione **Mantenimiento**.
7. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de mantenimiento.

    > [!NOTE]  
    > El paso 7 solo funciona si ha configurado lo siguiente: en la página **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cta. mantenimiento** contiene la cuenta de cargo y el campo **Cta. contrap. mantenimiento** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación. Para obtener más información, vea [Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Seleccione la acción **Registrar**.

## Registrar el coste de mantenimiento de una factura de compra

Los siguientes pasos describen cómo registrar los costes de mantenimiento de un activo fijo a partir de una factura de compra. Los pasos son parecidos para pedidos de compra.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.
2. En la ficha desplegable **General**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Seleccione **Cargo (prod.)** en el campo **Tipo** y elija **Activo fijo**.
4. En el campo **N.º**, , elija el activo y luego especifique la cantidad y el coste.
5. En el campo **A/F Tipo registro**, elija **Mantenimiento**.
6. Registre la factura de compra.

## Seguimiento de las visitas de servicio

Puede imprimir el informe **Mnto. - Próxima revisión** para ver la lista de activos programados para servicio. Puede utilizar este informe cuando desea actualizar el campo **Próxima fecha servicio** en las fichas de activos fijos.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Próxima revisión mantenimiento** y luego elija el enlace relacionado.  
2. Rellene los campos **Fecha inicial** y **Fecha final**  
3. Elija el botón **Imprimir** o **Versión preliminar**.

## Supervisar costes de mantenimiento

Puede ver estadísticas para supervisar los costes de mantenimiento.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo en el que desea ver los costes de mantenimiento y, a continuación, elija la acción **Libros amortización**.
3. En la página **Libros amortización A/F**, seleccione el libro de amortización de activos correspondiente y, a continuación, elija la acción **Estadísticas**.
4. En la página **Estadísticas activos fijos**, elija el campo **Mantenimiento**.

Utilice la página **Movs. mantenimiento** para ver los movimientos que conforman el importe en el campo **Mantenimiento**.

## Ver o imprimir los costes de mantenimiento de varios activos fijos

En el informe **Mnto. - Análisis**, puede seleccionar el examen de mantenimiento según uno, dos o tres códigos de mantenimiento para una fecha o periodo especificados. El informe puede mostrar el total de los activos seleccionados o un total para cada uno.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Análisis mantenimiento** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.
3. Elija el botón **Imprimir** o **Versión preliminar**.

## Ver movimientos de mantenimiento

Puede explorar también los costes de mantenimiento si consulta los movimientos en el libro mayor.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo en el que desea ver los movimientos de contabilidad y, a continuación, elija la acción **Libros amortización**.
3. En la página **Libros amortización A/F**, seleccione el libro de amortización de activos correspondiente y, a continuación, elija la acción **Movs. mantenimiento**.

## Ver o imprimir los movimientos de mantenimiento de varios activos fijos

En el informe **Mnto. - Detalles**, puede ver o imprimir los movimientos de mantenimiento para uno o varios activos fijos.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Detalles mantenimiento** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.
3. Elija el botón **Imprimir** o **Versión preliminar**.

## Consulte también .

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
