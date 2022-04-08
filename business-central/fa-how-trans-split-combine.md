---
title: Reclasificar activos fijos
description: Un activo fijo se reclasifica para transferirlo a otro departamento, dividirlo o combinarlo con otros activos fijos.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5638, 5636, 5640, 5637
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 48f2735c39c3630611abcb785efc67cfd9473671
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511134"
---
# <a name="transfer-split-or-combine-fixed-assets"></a>Permite transferir, dividir o combinar activos fijos

Puede utilizar el diario de reclasificación de activos fijos para transferir, dividir y combinar activos fijos. En el informe **A/F - Valor contable 02** puede ver o imprimir los resultados de la reclasificación de los activos fijos.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Para transferir un activo fijo a otro departamento

Puede que necesite transferir un activo dijo a un departamento diferente cuando, por ejemplo, coloca un activo en el departamento de producción mientras está en construcción y, a continuación, cuando está terminado, lo cambia al departamento de administración.  

1. Configure un activo nuevo. Introduzca el nuevo departamento como una dimensión.  
2. Asigne un libro de amortización de activo al nuevo activo fijo. Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).
3. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de reclasificación de activos fijos** y luego elija el enlace relacionado.
4. Cree una línea de diario donde el campo **A/F N. º** contenga el activo original, y el campo **A/F N.º nuevo** los nuevos activos fijos que se moverán. Rellene el resto de los campos según corresponda.  
5. Seleccione la acción **Reclasificación**.

    Se han creado dos líneas en el diario de activos con la plantilla y sección que ha especificado en la página **Config. diario activos** para el libro de amortización especificado. Para obtener más información, consulte [Configurar amortización de activos fijos](fa-how-setup-depreciation.md).
6. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.    
7. En la página **A/F diario general**, seleccione la acción **Registrar** para registrar la reclasificación que se ha realizado en los pasos 4 y 5.

Si registró el coste de un activo, puede utilizar el diario de reclasificación de activos fijos para dividir el coste entre varios activos.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Para dividir un activo en tres activos fijos
Puede dividir un activo en varios, por ejemplo, cuando necesita distribuir un activo entre diferentes departamentos. En este caso, puede mover, por ejemplo, el 25 % del coste y amortización del activo original al segundo activo y un 45 % al tercero. El 30 % restante permanece en el activo fijo original.

1. Configure dos activos fijos nuevos. Introduzca los nuevos departamentos como dimensiones.  
2. Asigne libros de amortización de activo a los nuevos activos fijos. Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).
3. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de reclasificación de activos fijos** y luego elija el enlace relacionado.
4. Cree dos líneas de reclasificación en el diario, una para cada activo nuevo.
5. En la primera línea, introduzca el segundo activo en el campo **A/F N. º nuevo** y 25 en el campo **% Coste reclasif**.
6. En la segunda línea, introduzca el tercer activo en el campo **A/F N. º nuevo** y 40 en el campo **% Coste reclasif**.
7. En ambas líneas, seleccione las casillas de verificación **Coste reclasif.** y **Amortización reclasif**.  
8. Seleccione la acción **Reclasificación**.  

    Se han creado dos líneas en el diario de activos con la plantilla y sección que ha especificado en la página **Config. diario activos** para el libro de amortización especificado. Para obtener más información, consulte [Configurar amortización de activos fijos](fa-how-setup-depreciation.md).    
9. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.
10. En la página **A/F diario general**, seleccione la acción **Registrar** para registrar la reclasificación que se ha realizado en los pasos del 4 al 8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Para combinar dos activos fijos en uno

Puede combinar varios activos en uno, por ejemplo, cuando mueve los activos fijos distribuidos a un solo departamento. Si ha registrado costes y amortización en los activos que se moverán, estos valores se combinarán con el activo fijo simple.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de reclasificación de activos fijos** y luego elija el enlace relacionado.
2. Cree un diario de reclasificación donde el campo **A/F N. º** contenga el activo que se moverá o combinará, y el campo **A/F N. º nuevo** el activo con el que se combinará..
3. Deje el campo **% Coste reclasif.** vacío para mover o combinar el coste completo.  
4. Seleccione las casillas de verificación **Coste reclasif.** y **Amortización reclasif**.
5. Seleccione la acción **Reclasificación**.

    Se han creado dos líneas en el diario de activos con la plantilla y sección que ha especificado en la página **Config. diario activos** para el libro de amortización especificado. Para obtener más información, consulte [Configurar amortización de activos fijos](fa-how-setup-depreciation.md).   
6. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales de activos fijos** y luego elija el enlace relacionado.
7. En la página **A/F diario general**, seleccione la acción **Registrar** para registrar la reclasificación que se ha realizado en los pasos del 2 al 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Para ver los cambios en los valores del libro de amortización debido a la reclasificación del activo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Valor contable de activo fijo 02** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.
3. Haga clic en el botón **Imprimir** o **Vista previa**.  

## <a name="see-also"></a>Consulte también

[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]