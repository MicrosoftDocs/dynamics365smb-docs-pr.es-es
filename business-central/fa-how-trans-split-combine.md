---
title: Reclasificar activos fijos | Documentos de Microsoft
description: Un activo fijo se reclasifica para transferirlo a otro departamento, dividirlo o combinarlo con otros activos fijos.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 76a6e005bf9d660610a307f1d6b69f902ca53e0d
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-split-or-combine-fixed-assets"></a>Permite transferir, dividir o combinar activos fijos
Puede utilizar el diario de reclasificación de activos fijos para transferir, dividir y combinar activos fijos. En el informe **A/F - Valor contable 02** puede ver o imprimir los resultados de la reclasificación de los activos fijos.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Para transferir un activo fijo a otro departamento
Puede que necesite transferir un activo dijo a un departamento diferente cuando, por ejemplo, coloca un activo en el departamento de producción mientras está en construcción y, a continuación, cuando está terminado, lo cambia al departamento de administración.  

1. Configure un activo nuevo. Especifique el nuevo departamento en el campo **Cód. departamento**.
2. Asigne un libro de amortización de activo al nuevo activo fijo. Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).
3. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **A/F Diarios reclasif.** y, a continuación, seleccione el vínculo relacionado.
4. Cree un diario de reclasificación donde el campo **A/F N. º** contenga el activo original, y el campo **A/F N. º nuevo** los nuevos activos fijos que se moverán.  
5. Seleccione la acción **Reclasificación**.

    Se han creado dos líneas en el diario de activos con la plantilla y sección que ha especificado en la ventana **Config. diario activos** para el libro de amortización especificado. Para obtener más información, consulte [Configurar amortización de activos fijos](fa-how-setup-depreciation.md).
6. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios generales A/F** y, a continuación, seleccione el vínculo relacionado.    
7. En la ventana **A/F diario general**, seleccione la acción **Registrar** para registrar la reclasificación que se ha realizado en los pasos 4 y 5.

Si registró el coste de un activo, puede utilizar el diario de reclasificación de activos fijos para dividir el coste entre varios activos.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Para dividir un activo en tres activos fijos
Puede dividir un activo en varios, por ejemplo, cuando necesita distribuir un activo entre diferentes departamentos. En este caso, puede mover, por ejemplo, el 25 % del coste y amortización del activo original al segundo activo y un 45 % al tercero. El 30 % restante permanece en el activo fijo original.

1. Configure dos activos fijos nuevos. Especifique el nuevo departamento en el campo **Cód. departamento**.
2. Asigne libros de amortización de activo a los nuevos activos fijos. Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).
3. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **A/F Diarios reclasif.** y, a continuación, seleccione el vínculo relacionado.
4. Cree dos líneas de reclasificación en el diario, una para cada activo nuevo.
5. En la primera línea, introduzca el segundo activo en el campo **A/F N. º nuevo** y 25 en el campo **% Coste reclasif**.
6. En la segunda línea, introduzca el tercer activo en el campo **A/F N. º nuevo** y 40 en el campo **% Coste reclasif**.
7. En ambas líneas, seleccione las casillas de verificación **Coste reclasif.** y **Amortización reclasif**.   
8. Seleccione la acción **Reclasificación**.

    Se han creado dos líneas en el diario de activos con la plantilla y sección que ha especificado en la ventana **Config. diario activos** para el libro de amortización especificado. Para obtener más información, consulte [Configurar amortización de activos fijos](fa-how-setup-depreciation.md).    
9. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios generales A/F** y, a continuación, seleccione el vínculo relacionado.
10. En la ventana **A/F diario general**, seleccione la acción **Registrar** para registrar la reclasificación que se ha realizado en los pasos del 4 al 8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Para combinar dos activos fijos en uno
Puede combinar varios activos en uno, por ejemplo, cuando mueve los activos fijos distribuidos a un solo departamento. Si ha registrado costes y amortización en los activos que se moverán, estos valores se combinarán con el activo fijo simple.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **A/F Diarios reclasif.** y, a continuación, seleccione el vínculo relacionado.
2. Cree un diario de reclasificación donde el campo **A/F N. º** contenga el activo que se moverá o combinará, y el campo **A/F N. º nuevo** el activo con el que se combinará..
3. Deje el campo **% Coste reclasif.** vacío para mover o combinar el coste completo.    
4. Seleccione las casillas de verificación **Coste reclasif.** y **Amortización reclasif**.
5. En la pestaña **Acciones**, elija **Reclasificar**.

    Se han creado dos líneas en el diario de activos con la plantilla y sección que ha especificado en la ventana **Config. diario activos** para el libro de amortización especificado. Para obtener más información, consulte [Configurar amortización de activos fijos](fa-how-setup-depreciation.md).   
6. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios generales A/F** y, a continuación, seleccione el vínculo relacionado.
7. En la ventana **A/F diario general**, seleccione la acción **Registrar** para registrar la reclasificación que se ha realizado en los pasos del 2 al 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Para ver los cambios en los valores del libro de amortización debido a la reclasificación del activo
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Valor contable A/F 02** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario.
3. Haga clic en el botón **Imprimir** o **Vista previa**.  

## <a name="see-also"></a>Consulte también
[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

