---
title: Crear ubicaciones
description: 'Genere grupos de ubicaciones similares en la hoja de trabajo de creación de ubicaciones, cree ubicaciones individualmente en la ficha de ubicación o automáticamente en la Hoja de trabajo de creación de ubicación.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="create-bins"></a><a name="create-bins"></a><a name="create-bins"></a><a name="create-bins"></a>Crear ubicaciones

La forma más eficaz de crear las ubicaciones del almacén es generar grupos de ubicaciones similares en la hoja de trabajo de creación de ubicación, pero también puede crear las ubicaciones individualmente desde la ficha de almacén. También puede utilizar una función en la página **Hoja trab. creación ubicación** para crear las ubicaciones automáticamente.  

## <a name="to-create-a-bin-from-the-location-card"></a><a name="to-create-a-bin-from-the-location-card"></a><a name="to-create-a-bin-from-the-location-card"></a><a name="to-create-a-bin-from-the-location-card"></a>Para crear una ubicación desde la ficha de almacén

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y elija el enlace relacionado.  
2.  Seleccione la ubicación para la que desee crear una ubicación y elija la acción **Ubicaciones**.  
3. Seleccione la acción **Nuevo**.
4. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field"></a><a name="the-dedicated-field"></a><a name="the-dedicated-field"></a><a name="the-dedicated-field"></a>El campo dedicado

El campo **Dedicado** de la página **Ubicaciones** especifica que las cantidades de la ubicación están protegidas de picking para otras demandas. Sin embargo, las cantidades de las ubicaciones dedicadas todavía pueden reservarse. Por consiguiente, las cantidades de las ubicaciones dedicadas se incluyen en el campo **Cdad. disponible total** de la página **Reservas**.

La fabricación de una ubicación dedicada proporciona una funcionalidad similar en funciones de almacén básicas al uso de tipos de ubicaciones, que sólo está disponible en la gestión avanzada de almacén. Para obtener más información, consulte [Configurar tipos de ubicaciones](warehouse-how-to-set-up-bin-types.md).

### <a name="example"></a><a name="example"></a><a name="example"></a><a name="example"></a>Ejemplo:

Ejemplo: En un centro de trabajo se establece un código de ubicación en el campo **Cód. ubic. para producción**. Las líneas de componente del pedido de producción con ese código de almacén requieren que se coloquen allí los componentes vaciados hacia adelante. Sin embargo, hasta que los componentes se consumen en esa ubicación, se puede hacer picking de otras demandas de componentes o se los puede consumir de esa ubicación porque aún se los considera contenidos de ubicación disponibles. Para garantizar que el contenido de la ubicación está disponible solo para la demanda de componente que utiliza esa ubicación para producción, debe seleccionar el campo **Dedicado** de la línea para ese código de ubicación.

> [!Caution]
> Los productos de las ubicaciones dedicadas no se protegen cuando se les ha realizado el picking y se los consume como componentes de producción o ensamblado con la página **Picking de inventario**. Para obtener más información, consulte [Realizar picking para ensamblado o producción en una configuración básica de almacén](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a><a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a><a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a><a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Para crear las ubicaciones individualmente en la hoja de trabajo de creación de ubicación

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , especifique **Hoja trab. creación ubicación** y, a continuación, elija el vínculo relacionado.  
2.  Rellene en cada línea los campos necesarios para dar el nombre y caracterizar las ubicaciones que va a crear.  
3.  Elija la acción **Crear ubicaciones**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a><a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a><a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a><a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Para crear ubicaciones automáticamente en la hoja de trabajo de creación de ubicación

Antes de empezar a crear ubicaciones automáticamente, debe determinar el tipo de ubicaciones básicas para sus operaciones, así como también el flujo más práctico de los productos a través de la estructura física del almacén.  

> [!NOTE]  
> En cuanto utilice una ubicación, no podrá eliminarla si no está vacía. Pero si desea utilizar otro sistema de denominación de ubicaciones, puede utilizar el diario de reclasificación para mover los productos a un nuevo sistema de ubicación. No obstante, este proceso es manual y lleva cierto tiempo, por lo que es mejor configurar sus ubicaciones correctamente desde el principio.  

Para trabajar con la página **Hoja trab. creación ubicación**, debe estar configurado como empleado de almacén en el almacén donde estén las ubicaciones. Para obtener más información, vea [Configurar los empleados de almacén](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , especifique **Hoja trab. creación ubicación** y, a continuación, elija el vínculo relacionado.  
2.  Elija la acción **Calcular ubicaciones**.
3. En la página **Calcular ubicaciones**, en el campo **Cód. plantilla ubicación**, seleccione la plantilla de ubicación que desea utilizar como modelo para las ubicaciones que va a crear.
4.  Rellene una descripción para las ubicaciones que está creando.  
5.  Para crear los códigos de ubicación, rellene los campos **Desde Nº** y **Hasta Nº** en las tres categorías que se muestran en la página: **Estantería**, **Sección** y **Nivel**. El código de ubicación puede tener hasta 20 caracteres.  

    > [!NOTE]  
    >  El número de caracteres que ha introducido en las tres categorías de cada campo (por ejemplo, los caracteres que ha introducido en los tres campos **Desde Nº**) además de los separadores de campo, si existen, debe ser 20 o menos.  

     En el código puede utilizar letras como combinación de identificación, pero éstas deben ser las mismas en los campos **Desde Nº** y **Hasta Nº** . Por ejemplo, puede definir el componente Armario del código como **Desde Nº A01** y **Hasta Nº A10**. La aplicación no está configurada para generar códigos con secuencias de letras, por ejemplo, desde A01 hasta F05.  

6.  Si desea utilizar un carácter, como un guión, para separar los campos de categoría que ha definido como parte del código de ubicación, rellene el campo **Separador campo** con este carácter.  
7.  Si desea que la aplicación no cree una línea para una ubicación si ya existe, seleccione el campo **Comprueba en ubic. actual**.  
8. Cuando haya terminado de rellenar todos los campos, seleccione el botón **Aceptar**.

    La aplicación crea una línea para cada ubicación de la hoja de trabajo. Ahora puede eliminar algunas ubicaciones, por ejemplo, si tiene una estantería con un pasillo a través de los dos primeros niveles de un par de secciones.  

9. Cuando haya eliminado todas las ubicaciones innecesarias, elija la acción **Crear ubicaciones** y la aplicación creará ubicaciones para cada línea de la hoja de trabajo.  

Repita el proceso para otro grupo de ubicaciones hasta que haya creado todas las ubicaciones del almacén.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-new-bins/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
