---
title: Cómo configurar objetos de coste | Documentos de Microsoft
description: Aprender cómo configurar los objetos de coste, que son parecidos a las dimensiones de contabilidad.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 616fcbe937e556c17e8beb79f68bc961ea8bbe18
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806639"
---
# <a name="set-up-cost-objects"></a>Configurar objetos de costes
Los objetos de coste son proyectos, productos o servicios de una empresa. El plan de objetos de coste es similar a la información de dimensión de contabilidad. Puede configurar el plan de objetos de coste de la siguiente forma:  

* Transfiera los valores de dimensión en la contabilidad al plan de objetos de coste. Puede hacer los ajustes necesarios después de la transferencia.  
* Cree un plan del objeto de coste que es independiente de la contabilidad o agregue un objeto de coste nuevo a un plan existente de objetos de coste. Debe crear cada objeto de coste por separado.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Para transferir valores de dimensión de la contabilidad al plan de objetos de coste  
1.  Configurar una dimensión para que sea la dimensión del objeto de coste en la página **Actualizar dimensiones CA**. Sólo los valores de esta dimensión se transfieren.  
2.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan objetos coste** y luego elija el enlace relacionado.  
3.  Elija la acción **Traer objetos coste de dimensión** para transferir los valores de dimensión al plan de objetos de coste. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión objeto coste** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de objetos de coste. No puede definir una sincronización del plan de objetos de coste a los valores de dimensión de la contabilidad.  

El plan de objetos de coste contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Crear nuevos objetos de coste en la página Plan objetos coste  
Puede configurar y mantener objetos de coste en la ficha **Plan objeto de coste** o bien en la página **Plan objetos coste**. En este procedimiento, va a configurar objetos de coste en la página **Plan de objetos de coste**.  

1.  Abra la página **Plan objetos coste** en el modo de edición.  
2.  En el campo **Código**, introduzca el código del objeto de coste. Todos los objetos de coste deben disponer de un código.  
3.  En el campo **Nombre**, introduzca el nombre del objeto de coste.  
4.  Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del objeto de coste.  

    * Para los objetos de coste de la línea **Total** debe rellenar el campo **Total desde/a**. Utilice el operador **or**, que es una línea vertical (**&#124;**), para establecer rangos de objetos de coste.  
    * Para objetos de coste del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Aplicar sangría.  
5.  Rellene el campo **Orden clasificación**.  
6.  Seleccione la siguiente línea vacía para crear un objeto de coste nuevo y, a continuación, repita del paso 2 al 5.  
7.  Cuando haya configurado todos los objetos de coste, elija la acción **Aplicar sangría a objetos coste**. Elija el botón **Sí**.  

> [!IMPORTANT]  
>  Si ha introducido definiciones en los campos **Total desde/a** para los objetos de coste de **Total final** antes de ejecutar la función Aplicar sangría, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)  
[Definición de centros de coste y de objetos de coste para el plan de cuentas](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldos entre el tipo de coste, centro de coste y objeto de coste](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)   
[Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)   
[Acerca de la contabilidad de costes](finance-about-cost-accounting.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
