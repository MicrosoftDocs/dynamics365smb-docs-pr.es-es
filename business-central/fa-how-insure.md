---
title: Aseguramiento de activos fijos
description: Puede asignar uno o varios activos fijos a una póliza de seguros con el registro de los movimientos de cobertura del seguro desde la página **Diario seguros**.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 06/29/2021
ms.author: bholtorf
---
# Aseguramiento de activos fijos
Una póliza de seguro para un activo fijo se representa con una ficha de seguro. Puede asignar uno o varios activos fijos a una póliza de seguro.

Asigne un activo fijo a una póliza de seguros con el registro de los movimientos de cobertura del seguro desde la página **Diario seguros**.

Además, puede asignar un activo fijo a una póliza de seguro y crear movimientos de cobertura cuando registra el coste. Puede realizar esta acción si registra un coste desde el diario de activos fijos con el campo **N. º seguro** rellenado. La casilla de verificación **Registro auto. seguro** de la página **Configuración activos fijos** debe estar seleccionada. Para obtener más información, consulte [Para registrar una adquisición de un activo manualmente con el diario general de activos](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

Si la casilla de verificación **Registro auto. seguro** de la página **Configuración activos fijos** no está seleccionada, las adquisiciones registradas del diario de activos fijos crearán líneas en la página **Diario de seguros** y deberá registrarlas manualmente.

> [!WARNING]  
>   Si no selecciona la casilla de verificación **Registro auto. seguro** de la página **Configuración activos fijos**, el diario de seguros deberá basarse en una plantilla de diario sin una serie numérica. Esto se debe a que los números de documentos insertados de la línea de diario de activo fijo permanecerán en conflicto con las series numéricas del diario de seguros. Para obtener más información acerca de las plantillas de diarios y secciones, consulte [Configurar la información general de los activos fijos](fa-how-setup-general.md).

Después de asignar un activo fijo a una póliza de seguros, se seleccionará la casilla de verificación **Asegurado** en la ficha del activo. Cuando vende el activo fijo, la casilla se deselecciona automáticamente.

## Para crear o modificar una ficha de seguros
Una póliza de seguro para un activo fijo debe representarse con una ficha de seguro.

Cuando reciba información de cambios en el importe de cobertura, debe especificar la nueva información de la página **Ficha seguro** para poder asegurarse un análisis correcto de la póliza de seguros.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguro** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** para crear una ficha de póliza seguro nueva. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. De forma alternativa, seleccione la póliza de seguro que desea cambiar y, a continuación, elija la acción **Editar**.

## Asigne un activo fijo a una póliza de seguros realizando el registro desde un diario de seguro.
Asigne un activo fijo a una póliza de seguros realizando el registro desde un movimiento de cobertura seguro.  

El procedimiento siguiente explica cómo crear una línea en un diario de seguros manualmente. Si la casilla de verificación **Registro auto. seguro** está seleccionada en la página **Configuración A/F**, las líneas del diario de seguros se crearán automáticamente al registrar los costes. En ese caso, todo lo que tiene que hacer es registrar el diario.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de seguros**, y luego elija el enlace relacionado.  
2. Abra el diario correspondiente y rellene las líneas de diario según sea necesario.  
3. Para asignar varios activos fijos a una póliza seguros, cree las líneas del diario con el mismo valor en el campo **N.º seguro** pero con valores diferentes en el **A/F n.º**.  
4. Seleccione la acción **Registrar**.  

    > [!NOTE]  
    >   Los movimientos de un diario seguros solo se registran en los movimientos de seguros.  

## Para actualizar el valor del seguro de un activo fijo
Puede utilizar el proceso **Ajustar valores seguros** para actualizar el valor de los activos cubiertos.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ajustar valores seguros** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.

    > [!NOTE]  
    >   En el campo **Valor ajuste**, introduzca una disminución del 5 %, por ejemplo 95, mientras que introduce un aumento del 2 %, como 102.  
3. Elija el botón **Aceptar**.  

   El proceso calcula el importe nuevo como porcentaje del valor total asegurado, como se indica en la página **Estadísticas seguro** y, a continuación, crea una línea en el diario de seguros.  
4. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de seguros**, y luego elija el enlace relacionado.  
5. Abra el diario de seguros pertinente, revise los valores creados y, a continuación, regístrelos en los movimientos de seguros.  

## Para controlar la cobertura de seguros
[!INCLUDE[prod_short](includes/prod_short.md)] proporciona informes dedicados y páginas de estadísticas para usarlos en el análisis de las pólizas de seguro y saber si sus activos fijos tienen un exceso o una falta de seguro.  

### Resumen de pólizas de seguro
Para obtener una visión general de las pólizas de seguros, obtenga una vista previa del informe **Seguro - Lista** o imprímalo. El informe muestra todas las pólizas y los campos más importantes de las fichas de seguro.  

### Cobertura seguro
Para ver qué pólizas cubren cada activo y por cuánto, puede previsualizar o imprimir el informe **Seguro - Total asegurado**.  

### Sobre/infraseguro
Puede comprobar si los activos tienen un exceso o una falta de seguro de la siguiente forma:  

* En la página **Estadísticas seguro**. Con un importe positivo en el campo **Sobre/Infra asegurado** que significa que el activo está sobreasegurado. Un importe negativo indica que está infrasegurado.  
* En la página **Estadísticas activo**. Elija el campo **Valor total asegurado** para ver la página **Movs. seguro**.  
* El informe **Sobre/Infra asegurado**.  
* El informe **Análisis seguros**.  

### Activos fijos sin seguro
Para comprobar si ha olvidado asignar un activo fijo a una póliza seguros, puede imprimir o previsualizar el informe **A/Fs asegurados – no asegurados**. Este informe muestra los activos fijos para los que no ha habido ningún importe registrado en los movimientos de cobertura del seguro.  

## Para ver los movimientos cobertura de seguro
Puede ver los movimientos realizados en los movimientos de seguros.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguro** y luego elija el enlace relacionado.  
2. Seleccione la póliza relevante y, a continuación, seleccione la acción **Movimientos seguro**.  

## Para ver el total del valor del seguro de los activos
Una página de matriz dedicada muestra los valores de seguros registrados para cada póliza de seguro de cada activo fijo como resultado de los importes relacionados con los seguros que ha registrado.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguro** y luego elija el enlace relacionado.  
2. Seleccione la póliza relevante y, a continuación, seleccione la acción **Valor asegurado total por A/F**.  
3. Rellene los campos según sea necesario.  
4. Elija la acción **Mostrar matriz**.  
5. Para ver los movimientos de seguros subyacentes, elija un valor en la matriz.  

## Para corregir movimientos de seguros
Si se adjuntó un activo fijo a la póliza de seguros incorrecta, puede corregir este movimiento con la creación de dos movimientos de reclasificación del diario de seguro.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de seguros**, y luego elija el enlace relacionado.  
2. Cree una línea de diario del activo fijo y la póliza de seguro correcta en la que el valor del campo **Importe** es positivo.  
3. Cree otra línea de diario del activo fijo y la póliza de seguro incorrecta en la que el valor del campo **Importe** es negativo.  
4. Seleccione la acción **Registrar**.  

El activo se desvinculará de la póliza de seguros incorrecta, en la segunda línea, y se adjuntará a la correcta en la primera línea.  

## Consulte también
[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]