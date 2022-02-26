---
title: Configuración de códigos de operación
description: Puede añadir tantos códigos de operación como desee a la tabla. Sin embargo, los códigos C, D e I ya existe en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 540e3198c61cd0d4766f4b54a3b344ac73652b71
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437179"
---
# <a name="set-up-operation-codes"></a>Configurar códigos de operación
Puede añadir tantos códigos de operación como desee a la tabla. Sin embargo, los códigos C, D e I ya existe en [!INCLUDE[prod_short](../../includes/prod_short.md)]. Por ejemplo, los abonos siempre tienen el código de operación D. No puede configurar estos valores en la tabla porque son códigos creados por el sistema. Si intenta agregarlos, [!INCLUDE[prod_short](../../includes/prod_short.md)] devolverá un error.  

## <a name="to-set-up-operation-codes"></a>Para configurar códigos de operación  

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Códigos de operación** y luego elija el enlace relacionado.  
2.  En la página **Códigos de operación**, rellene los campos tal como se describe en la tabla siguiente  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Introduzca un código de operación. Puede introducir un letra o número.<br /><br /> Los códigos válidos son números del 1 al 8 y letras de la A a la Z.<br /><br /> Para enviar un informe bajo el régimen de CAC, debe asegurarse de que el código Z, que se requiere para este tipo de transacciones, se encuentre en la lista de códigos de operación.|  
    |**Descripción**|Escriba una descripción para el código de operación. Puede introducir un máximo de 30 caracteres alfanuméricos.|  

## <a name="to-link-operation-codes-to-general-product-posting-groups"></a>Para vincular códigos de operación a grupos de publicación de productos en general  

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos registro**, y luego elija el enlace relacionado.  
2.  Elija la acción **Grupos contables de producto general**.  
3.  En la página **Grupos de publicación de productos generales**, vincule cada código de operación a un grupo de publicación de productos general.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |Código|Introduzca un código para crear un nuevo grupo contable de producto general.|  
    |Description|Introduzca una descripción del grupo contable de producto general|  
    |Grupo reg. IVA prod. genér.|Seleccione un porcentaje de IVA para vincularlo al grupo de publicación de producto general.|  
    |Código operación|Seleccione una operación apropiada para vincularla a un grupo contable de producto general. Puede asignar el mismo código de operación a distintos grupos contables. **Nota:** Es importante vincular el código de operación al grupo de registro de IVA de producto correcto. El informe del modelo 340 usa la configuración para crear declaraciones comerciales.|  

Cuando agrega un código de operación al grupo de publicación de producto general, esa asociación se aplica a su vez a los artículos que tienen ese grupo.  

## <a name="see-also"></a>Consulte también  
 [Crear el informe 340](how-to-create-report-340.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]