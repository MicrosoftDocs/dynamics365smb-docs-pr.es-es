---
title: Asegurar activos fijos
description: Puede asignar uno o varios activos fijos a una póliza de seguros con el registro de los movimientos de cobertura del seguro desde la página **Diario seguros**.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="insure-fixed-assets"></a>Asegurar activos fijos

Utilice la página **Tarjeta de seguro** para configurar una póliza de seguro que cubra uno o más activos fijos. Puede asignar un activo fijo a una póliza de seguro o varios activos fijos a una póliza de seguro.

Asigne un activo fijo a una póliza de seguros con el registro de los movimientos de cobertura del seguro desde la página **Diario seguros**.

Además, puede asignar un activo fijo a una póliza de seguro y crear movimientos de cobertura cuando registra el coste. Se registra un costo de adquisición del diario de activos fijos con el campo  **Nº de seguro** completado. Debe activar la opción **Contabilización automática de seguros** en la página **Configuración de activos fijos** . Para obtener más información, consulte [Adquirir un activo fijo mediante un diario del L/M de activos fijos](fa-how-acquire.md#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

Si la opción **Contabilización automática de seguros** en la página **Configuración de activos fijos** no está activada, la publicación de adquisiciones desde el El diario de activos fijos crea líneas en la página  **Diario de seguros** . Debes publicar esas líneas manualmente.

> [!WARNING]  
> Si no activa la opción **Contabilización automática de seguros** en la página **Configuración de activos fijos**, su diario de seguros debe basarse en una plantilla de diario sin una serie numérica. Esto se debe a que los números de documentos insertados de la línea de diario de activo fijo permanecerán en conflicto con las series numéricas del diario de seguros. Para obtener más información acerca de las plantillas de diarios y secciones, consulte [Configurar la información general de los activos fijos](fa-how-setup-general.md).

Después de asignar un activo fijo a una póliza de seguro, el campo **Asegurado** en la tarjeta de activo fijo contiene **Sí**. Cuando vende el activo fijo, la alternancia se desactiva automáticamente.

## <a name="to-create-or-modify-an-insurance-card"></a>Para crear o modificar una ficha de seguros

Cuando reciba información de cambios en el importe de cobertura, debe especificar la nueva información de la página **Ficha seguro** para poder asegurarse un análisis correcto de la póliza de seguros.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguro** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** para crear una ficha de póliza seguro nueva. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. De forma alternativa, seleccione la póliza de seguro que desea cambiar y, a continuación, elija la acción **Editar**.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>Asigne un activo fijo a una póliza de seguros realizando el registro desde un diario de seguro.

Asigne un activo fijo a una póliza de seguros realizando el registro desde un movimiento de cobertura seguro.  

El procedimiento siguiente explica cómo crear una línea en un diario de seguros manualmente. Si la opción **Contabilización automática de seguros** está activada en la página **Configuración de activos fijos**, las líneas del diario de seguros se crean automáticamente cuando usted contabiliza los costos de adquisición. En ese caso, todo lo que tiene que hacer es registrar el diario.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de seguros**, y luego elija el enlace relacionado.  
2. Abra el diario correspondiente y rellene las líneas de diario según sea necesario.  
3. Para asignar varios activos fijos a una póliza seguros, cree las líneas del diario con el mismo valor en el campo **N.º seguro** pero con valores diferentes en el **A/F n.º**.  
4. Seleccione la acción **Registrar**.  

    > [!NOTE]  
    > Los movimientos de un diario seguros solo se registran en los movimientos de seguros.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>Para actualizar el valor del seguro de un activo fijo

Puede utilizar el proceso **Ajustar valores seguros** para actualizar el valor de los activos cubiertos.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ajustar valores seguros** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.

    > [!NOTE]  
    >   En el campo **Valor ajuste**, introduzca una disminución del 5 %, por ejemplo 95, mientras que introduce un aumento del 2 %, como 102.  
3. Elija el botón **Aceptar**.  

   El proceso calcula el importe nuevo como porcentaje del valor total asegurado, como se indica en la página **Estadísticas seguro** y, a continuación, crea una línea en el diario de seguros.  
4. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de seguros**, y luego elija el enlace relacionado.  
5. Abra el diario de seguros pertinente, revise los valores creados y, a continuación, regístrelos en los movimientos de seguros.  

## <a name="to-monitor-insurance-coverage"></a>Para controlar la cobertura de seguros

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona informes dedicados y páginas de estadísticas para usarlos en el análisis de las pólizas de seguro y saber si sus activos fijos tienen un exceso o una falta de seguro.  

### <a name="overview-of-insurance-policies"></a>Resumen de pólizas de seguro

Para obtener una visión general de las pólizas de seguros, obtenga una vista previa del informe **Seguro - Lista** o imprímalo. El informe muestra todas las pólizas y los campos más importantes de las fichas de seguro.  

### <a name="insurance-coverage"></a>Cobertura del seguro

Para ver qué pólizas cubren cada activo y por cuánto, puede previsualizar o imprimir el informe **Seguro - Total asegurado**.  

#### <a name="overunder-coverage"></a>Cobertura excesiva o insuficiente

Puede comprobar si los activos fijos están sobreasegurados o insuficientemente asegurados de las siguientes maneras:  

* En la página **Estadísticas seguro**. Con un importe positivo en el campo **Sobre/Infra asegurado** que significa que el activo está sobreasegurado. Un importe negativo significa que el activo está infraasegurado.  
* En la página **Estadísticas activo**. Elija el campo **Valor total asegurado** para ver la página **Movs. seguro**.  
* El informe **Sobre/Infra asegurado**.  
* El informe **Análisis seguros**.  

### <a name="uninsured-fixed-assets"></a>Activos fijos no asegurados

Para verificar si olvidó asignar un activo fijo a una póliza de seguro, puede imprimir o obtener una vista previa del informe **Seguros - FA sin seguro** . Este informe muestra los activos fijos cuyos montos no se registran en el libro mayor de cobertura de seguro.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>Para ver los movimientos cobertura de seguro

Puede ver las entradas que realizó en el libro mayor de cobertura del seguro.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguro** y luego elija el enlace relacionado.  
2. Seleccione la póliza relevante y, a continuación, seleccione la acción **Movimientos seguro**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>Para ver el total del valor del seguro de los activos

Una página de matriz muestra los valores de seguro que se registran para cada póliza de seguro para cada activo fijo que resultan de los importes relacionados con el seguro registrados.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguro** y luego elija el enlace relacionado.  
2. Seleccione la póliza relevante y, a continuación, seleccione la acción **Valor asegurado total por A/F**.  
3. Rellene los campos según sea necesario.  
4. Elija la acción **Mostrar matriz**.  
5. Para ver los movimientos de seguros subyacentes, elija un valor en la matriz.  

## <a name="to-correct-insurance-coverage-entries"></a>Para corregir movimientos de seguros

Si se asignó un activo fijo a una póliza de seguro incorrecta, puede corregirlo creando dos asientos de reclasificación desde el diario de seguros.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de seguros**, y luego elija el enlace relacionado.  
2. Cree una línea de diario del activo fijo y la póliza de seguro correcta en la que el valor del campo **Importe** es positivo.  
3. Cree otra línea de diario del activo fijo y la póliza de seguro incorrecta en la que el valor del campo **Importe** es negativo.  
4. Seleccione la acción **Registrar**.  

El activo fijo se elimina de la póliza de seguro incorrecta en la segunda línea. El activo se asigna a la póliza de seguro correcta en la primera línea del diario.  

## <a name="see-also"></a>Consulte también

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
