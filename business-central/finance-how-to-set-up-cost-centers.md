---
title: Cómo configurar centros de coste | Documentos de Microsoft
description: Los centros de coste son departamentos que son responsables de los costes y de los ingresos. El plan de centros de coste es similar a la información de dimensión de contabilidad.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: bc2349e75724dbfaf0028cf015bfbe311f75bb81
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301942"
---
# <a name="set-up-cost-centers"></a>Configurar centros de costes
Los centros de coste son departamentos que son responsables de los costes y de los ingresos. El plan de centros de coste es similar a la información de dimensión de contabilidad. Puede configurar el plan de centros de coste de la siguiente forma:  

-   Transfiera los valores de dimensión en la contabilidad al plan de centros de coste. Puede hacer los ajustes necesarios después de la transferencia.  
-   Cree un nuevo plan de centro de coste que es independiente de la contabilidad o agregue un nuevo centro de coste a un plan existente de centro de coste. Debe crear cada centro de coste por separado.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Para transferir los valores de dimensión en la contabilidad al plan de centros de coste  
1.  Configure una dimensión para que sea la dimensión del centro de coste en la página **Actualizar dimensiones contabilidad costes**. Sólo los valores de esta dimensión se transfieren.  
2.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan centros coste** y luego elija el enlace relacionado.  
3.  En la pestaña **Acciones**, en el grupo **Funciones**, seleccione **Traer centros de coste de dimensión** para transferir los valores de dimensión al plan de centros de coste. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión centro coste** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de centros de coste. No puede definir una sincronización del plan de centros de coste a los valores de dimensión de la contabilidad.  

El plan de centros de coste contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Crear nuevos centros de coste en la página Plan centros coste  
Puede configurar y mantener centros de coste en la ficha **Ficha centro de coste** o bien en la página **Plan centros coste**. En este procedimiento, va a configurar centros de coste en la página **Plan de centros de coste**.  

1. Abra la página **Plan centros coste** en el modo de edición.  
2. En el campo **Código**, introduzca el código del centro de coste. Todos los centros de coste deben disponer de un código.  
3. En el campo **Nombre**, introduzca el nombre del centro de coste.  
4. Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del centro de coste.  

    - Para los centros de coste de la línea **Total** debe rellenar el campo **Totales**. Utilice el operador **or**, que es una línea vertical (**&#124;**) para establecer rangos de centros de coste.  
    - Para centros de coste del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Aplicar sangría.  
5.  Rellene los campos **Orden clasificación** y **Subtipo de coste** .  
6.  Seleccione la siguiente línea vacía para crear un centro de coste nuevo y, a continuación, repita del paso 2 al 5.  
7.  Cuando haya configurado todos los centros de coste, elija la acción **Aplicar sangría a centros coste**. Elija el botón **Sí**.  

> [!IMPORTANT]  
>  Si ha introducido definiciones en los campos **Totales** para los centros de coste de **Total-final** antes de ejecutar la función Aplicar sangría, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)  
[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)   
[Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)   
[Acerca de la contabilidad de costes](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
