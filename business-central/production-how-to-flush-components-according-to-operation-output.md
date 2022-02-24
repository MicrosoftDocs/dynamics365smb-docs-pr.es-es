---
title: 'Procedimiento: Baje componentes según la producción de la operación | Documentos de Microsoft'
description: Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a **Terminada**. Para obtener más información, consulte Método de baja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3c1bcf36ed2ec494b54fe8fdf3b26b07aa834f7f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313401"
---
# <a name="flush-components-according-to-operation-output"></a>Bajar componentes según la salida de la operación
Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a **Terminada**.  

Si también define los códigos de vínculo de ruta, el cálculo y el registro se producen cuando termina cada operación, y se registra la cantidad realmente consumida en la operación. Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).  

Por ejemplo, si una orden de producción para producir 800 metros requiere 8 kg de un componente, cuando se registran 200 metros como salida, se registran automáticamente 2 kg de consumo.  

Esta funcionalidad se útil por los motivos siguientes:  

-   **Valoración inventario**: los movimientos de valores para la salida y el consumo se crean en paralelo según progresa la orden de producción. Sin los códigos de vínculo de ruta, el valor de inventario aumentará mientras se registra salida y después disminuirá en un momento posterior cuando el valor del consumo de componentes se registra con la orden de producción terminada.  
-   **Disponibilidad stock**: con el registro gradual del consumo, la disponibilidad de productos de componentes está más actualizado, que es importante para mantener los saldos internos entre la demanda y el suministro. Sin los códigos de vínculo de ruta, otras demandas para el componente pueden creer que está disponible mientras se encuentre pendiente un registro retrasado del consumo.  
-   **A tiempo**: con la posibilidad de personalizar los productos para las solicitudes de cliente, puede minimizar la pérdida de tiempo de asegurarse de que solo se produzcan cambios de trabajo y del sistema si es necesario.  

El siguiente procedimiento muestra cómo combinar códigos de vínculo de ruta y baja hacia atrás de modo que la cantidad que se baja para cada operación es proporcional a la salida real de la operación terminada.  

## <a name="to-flush-components-according-to-operation-output"></a>Para bajar componentes según la salida de la operación  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Editar**.  
3.  En la ficha desplegable **Reposición**, en el campo **Método de baja**, seleccione **Anticipada**.  

    > [!NOTE]  
    >  Seleccione **Pick+ Adelante** si el componente se utiliza en un almacén que está configurado para la ubicación y picking directos.  

4.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Rutas** y luego elija el enlace relacionado.  
5.  Defina los códigos de vínculo de ruta para cada operación que consume el componente. Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).  
6.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **L.M. producción** y luego elija el enlace relacionado.  
7.  Defina los códigos de vínculo de ruta desde cada instancia del componente hasta la operación donde se consume.

    > [!IMPORTANT]  
    >  El componente debe tener un vínculo de ruta hasta la última operación en la ruta.  

## <a name="see-also"></a>Consulte también  
[Crear LM de producción](production-how-to-create-production-boms.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Planificación](production-planning.md)   
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
