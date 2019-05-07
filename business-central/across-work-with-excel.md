---
title: Ver y editar en Excel desde Business Central | Documentos de Microsoft
description: Obtenga más información sobre cómo puede abrir las páginas en Microsoft Excel desde Business Central para un mejor análisis de datos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 68139f258595bcca2658e394a4251e30dfbe6510
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "925045"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Ver y editar en Excel desde Business Central 

Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel. Para ello, tiene dos opciones. Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página. Las diferencias entre las dos acciones son las siguientes:  

## <a name="open-in-excel"></a>Abrir en Excel

-    Con esta acción, Excel respeta los filtros de la página y limita los registros que se muestran. Esto significa que el libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prodshort](includes/prodshort.md)].

-    Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prodshort](includes/prodshort.md)]. Solo puede guardar los cambios en el archivo de Excel en su ordenador. 

-    Esta acción funciona tanto en Windows como en macOS. 

>[!NOTE]
>Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Abrir en Excel** no está disponible si se está usando la acción **Editar en Excel**.

## <a name="edit-in-excel"></a>Editar en Excel

-    Con esta acción, el libro de Excel no respeta los filtros de la página y no limita los registros que se muestran. Esto significa que el libro de Excel contiene todos los registros y columnas disponibles, independientemente de lo que se muestra en la página. 

-    La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prodshort](includes/prodshort.md)].

-    Solo funciona en Windows; en macOS, no.

>[!NOTE]
>Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha instalado el complemento de Excel. Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Consulte las diferencias entre las opciones 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Consulte también
[Trabajar con Business Central](ui-work-product.md)  
