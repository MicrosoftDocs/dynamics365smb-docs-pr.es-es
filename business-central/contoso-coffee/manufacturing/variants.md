---
title: Variantes
description: Tutorial para aprender a actualizar la previsión de la demanda para cada variante de un producto en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-variants"></a><a name="walkthrough-variants"></a>Tutorial: variantes

En este artículo, le guiaremos a través de los pasos para usar los datos de demostración de Contoso Coffee para obtener más información sobre variantes.

## <a name="scenario"></a><a name="scenario"></a>Caso

Usted es el planificador de producción de Contoso Coffee. Debe actualizar la previsión de la demanda para cada variante del artículo SP-SCM1006, AutoDripLite. Como tienen colores diferentes, debe asegurarse de que se utiliza la lista de materiales (BOM) correcta para cada variante. Ejecute la hoja de trabajo de planificación para calcular el suministro.  

## <a name="steps"></a><a name="steps"></a>Pasos

1. Configure las unidades de mantenimiento de existencias para el artículo SP-SCM1006, AutoDripLite. Asigne una BOM para SKU con las variantes RED y WHITE.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba *productos*, y luego elija el enlace relacionado.  

    2. Abra el producto **SP-SCM1006, AutoDripLite**.

    3. Seleccione la acción **Crear unidad de almacenamiento**.  

    4. Establezca el campo **Crear por** en *Almacén y variante*.

    5. Establezca un filtro para el almacén en *Norte* y, a continuación, elija el botón **Aceptar**.

    6. Elija la acción **Unidades de almacenamiento**.  

    7. Actualice las listas de materiales de producción para las siguientes unidades de almacenamiento:

        1. RED en NORTH, establezca SP-SCM1006-RED  

        2. WHITE en NORTH, establezca SP-SCM1006-WHITE  

        3. Mantenga el número de lista de materiales de producción vacío para BLACK en NORTH  

2. Actualice la configuración de fabricación y respete la previsión de demanda en ubicaciones y variantes.  

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba *configuración de fabricación* y luego elija el vínculo relacionado.  

    2. Active el campo **Usar previsión en almacenes**.

    3. Active el campo **Usar previsión en variante**.

    4. Cierre la ventana **Configuración fabricación**.

3. Crear un nuevo pronóstico de demanda mensual, *AUTODRIP*. Fíltrelo por el producto SP-SCM1006 y el almacén NORTH. Establezca la demanda de mayo para cada variante. 

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba *previsión de demanda*, y luego seleccione el vínculo relacionado.

    2. Cree una nueva previsión de demanda con el nombre *AUTODRIP*.

    3. Elija la acción **Editar previsión de la demanda**.

    4. En el campo **Ver por**, seleccione *Mes*.

    5. En el campo **Filtro producto** seleccione *SP-SCM1006*

    6. Active el campo **Usar previsión en almacenes**.

    7. En el campo **Filtro almacén**, seleccione *NORTH*.

    8. Active el campo **Usar previsión en variante**.

    9. Para cada línea se actualizan los valores en la columna de mayo

        1. RED en NORTH, establezca 100

        2. WHITE en NORTH, establezca 200

        3. BLACK en NORTH, establezca 300

    10. Cerrar ventanas de pronóstico de demanda

4. Ejecute el plan MPS en mayo para las previsiones de demanda creadas. Revise los componentes para ver que la pintura del artículo se correlaciona con la variante.

    1. Elija el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba *hoja planificación* y luego elija el vínculo relacionado.

    2. Seleccione la acción **Calcular planificación regenerativa**.

    3. Active el campo **MPS**.

    4. Desactive el campo **MPS**.

    5. En el campo **Fecha inicial**, seleccione *1 de mayo*

    6. En el campo **Fecha final**, seleccione *31 de mayo*

    7. En el campo **Usar previsión**, seleccione *AUTODRIP*

    8. Seleccione la acción **Aceptar**.

    9. Para cada línea creada, elija la acción **Componentes** y revise qué pintura se usa.  

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Introducción a datos de demostración de Contoso Coffee](../contoso-coffee-intro.md)  
