---
title: Actualizar costes estándar
description: Debe actualizar periódicamente los costes estándar de los componentes y distribuir los nuevos costes al producto principal.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="update-standard-costs"></a>Actualizar costes estándar
Debe actualizar periódicamente los costes estándar de los componentes y distribuir los nuevos costes al producto principal. El proceso normalmente consiste en los cuatro pasos siguientes:  

1.  Actualizar los costes en los niveles de componente y de capacidad. Para obtener más información, consulte el proceso **Sugerir coste estándar prod.**.  
2.  Consolide y distribuya los costes de componentes y de capacidad para calcular el coste total de fabricación o ensamblado de los productos.  
3.  Implementar los costes estándar que se introducen al ejecutar los trabajos por lotes anteriores. Los costes estándar no tienen efecto hasta que se implementan. Use el trabajo por lotos **Implementar cambios de coste estándar** que actualiza los cambios en el coste estándar en los artículos con los de la tabla de la Hoja de trabajo de coste estándar.  
4.  Implementar los cambios para actualizar el campo **Coste unitario** en la ficha del producto y realizar una revalorización de inventario. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).  

Para obtener más información, consulte [Acerca de Calcular el coste estándar](finance-about-calculating-standard-cost.md).
  
## <a name="to-update-standard-costs"></a>Para actualizar los costes estándar

1.  Ejecute el proceso **Valorar stock - movs. producto**. Para iniciar el trabajo por lotes, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ajustar coste: movimientos de producto**, y luego elija el enlace relacionado. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Revise los resultados y realice los cambios que considere necesarios.  
2.  Ejecute el proceso **Regis. variación existencias**. Para iniciar el trabajo por lotes, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Regis. variación existencias**, y luego elija el enlace relacionado. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Revise los resultados y realice los cambios que considere necesarios.  
3.  Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") introduzca **Hoja trab. coste estándar** y luego use una o más de las acciones siguientes:

    1.  Ejecute el proceso **Sugerir coste estándar prod.**  
    2.  Revise los resultados y realice los cambios que considere necesarios.  
    3.  Ejecute el proceso **Sugerir coste estándar capacidad**.  
    4.  Revise los resultados y realice los cambios que considere necesarios.
    5. Ejecute el proceso **Distribuir coste estándar**.
    6.  Revise los resultados y realice los cambios que considere necesarios.
    7.  Ejecute el proceso **Implementar cambios de coste estándar**.  
4.  Revise y registre la página **Diario revalorizac.** , el cual se ha rellenado con entradas provenientes de los pasos anteriores del proceso.  

## <a name="see-also"></a>Consulte también

 [Acerca del cálculo de coste estándar](finance-about-calculating-standard-cost.md)   
 [Gestión de costes de inventario](finance-manage-inventory-costs.md)   
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md)   
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
