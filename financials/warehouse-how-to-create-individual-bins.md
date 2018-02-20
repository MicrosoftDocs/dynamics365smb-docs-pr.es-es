---
title: Crear ubicaciones | Documentos de Microsoft
description: "La forma más eficaz de crear las ubicaciones del almacén es generar grupos de ubicaciones similares en la hoja de trabajo de creación de ubicación, pero también puede crear las ubicaciones individualmente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f8cd19f97c530397dd6b499157e13340331aa3ba
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="create-bins"></a>Crear ubicaciones
La forma más eficaz de crear las ubicaciones del almacén es generar grupos de ubicaciones similares en la hoja de trabajo de creación de ubicación, pero también puede crear las ubicaciones individualmente desde la ficha de almacén. También puede utilizar una función en la ventana **Hoja trab. creación ubicación** para crear las ubicaciones automáticamente.  

## <a name="to-create-a-bin-from-the-location-card"></a>Para crear una ubicación desde la ficha de almacén  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y seleccione el vínculo relacionado.  
2.  Seleccione la ubicación para la que desee crear una ubicación y elija la acción **Ubicaciones**.  
3. Seleccione la acción **Nuevo**.
4. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Para crear las ubicaciones individualmente en la hoja de trabajo de creación de ubicación  
1.  Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja trab. creación ubicación** y, a continuación, seleccione el vínculo relacionado.  
2.  Rellene en cada línea los campos necesarios para dar el nombre y caracterizar las ubicaciones que va a crear.  
3.  Elija la acción **Crear ubicaciones**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Para crear ubicaciones automáticamente en la hoja de trabajo de creación de ubicación  
Antes de empezar a crear ubicaciones automáticamente, debe determinar el tipo de ubicaciones básicas para sus operaciones, así como también el flujo más práctico de los productos a través de la estructura física del almacén.  

> [!NOTE]  
>  En cuanto utilice una ubicación, no podrá eliminarla si no está vacía. Pero si desea utilizar otro sistema de denominación de ubicaciones, puede utilizar el diario de reclasificación para mover los productos a un nuevo sistema de ubicación. No obstante, este proceso es manual y lleva cierto tiempo, por lo que es mejor configurar sus ubicaciones correctamente desde el principio.  

Para trabajar con la ventana **Hoja trab. creación ubicación**, debe estar configurado como empleado de almacén en el almacén donde estén las ubicaciones. Para obtener más información, vea [Configurar los empleados de almacén](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja trab. creación ubicación** y, a continuación, seleccione el vínculo relacionado.  
2.  Elija la acción **Calcular ubicaciones**.
3. En la ventana **Calcular ubicaciones**, en el campo **Cód. plantilla ubicación**, seleccione la plantilla de ubicación que desea utilizar como modelo para las ubicaciones que va a crear.
4.  Rellene una descripción para las ubicaciones que está creando.  
5.  Para crear los códigos de ubicación, rellene los campos **Desde Nº** y **Hasta Nº** en las tres categorías que se muestran en la ventana: **Estantería**, **Sección** y **Nivel**. El código de ubicación puede tener hasta 20 caracteres.  

    > [!NOTE]  
    >  El número de caracteres que ha introducido en las tres categorías de cada campo (por ejemplo, los caracteres que ha introducido en los tres campos **Desde Nº**) además de los separadores de campo, si existen, debe ser 20 o menos.  

     En el código puede utilizar letras como combinación de identificación, pero éstas deben ser las mismas en los campos **Desde Nº** y **Hasta Nº** . Por ejemplo, puede definir el componente Armario del código como **Desde Nº A01** y **Hasta Nº A10**. El programa no está configurado para generar códigos con secuencias de letras, por ejemplo, desde A01 hasta F05.  

6.  Si desea utilizar un carácter, como un guión, para separar los campos de categoría que ha definido como parte del código de ubicación, rellene el campo **Separador campo** con este carácter.  
7.  Si desea que el sistema no cree una línea para una ubicación si ya existe, seleccione el campo **Comprueba en ubic. actual**.  
8. Cuando haya terminado de rellenar todos los campos, seleccione el botón **Aceptar**.

    El programa crea una línea para cada ubicación de la hoja de trabajo. Ahora puede eliminar algunas ubicaciones, por ejemplo, si tiene una estantería con un pasillo a través de los dos primeros niveles de un par de secciones.  

9. Cuando haya eliminado todas las ubicaciones innecesarias, elija la acción **Crear ubicaciones** y el sistema creará ubicaciones para cada línea de la hoja de trabajo.  

Repita el proceso para otro grupo de ubicaciones hasta que haya creado todas las ubicaciones del almacén.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

