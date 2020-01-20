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
ms.date: 01/13/2020
ms.author: jswymer
ms.openlocfilehash: 9fd5c6c242932d75addcfa5c1811bdd1aff99a94
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953056"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Ver y editar en Excel desde Business Central

Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel. Para ello, tiene dos opciones. Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página. Las diferencias entre las dos acciones son las siguientes:  

## <a name="open-in-excel"></a>Abrir en Excel

- Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran. Esto significa que el libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prodshort](includes/prodshort.md)].

- Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prodshort](includes/prodshort.md)]. Solo puede guardar los cambios en el archivo de Excel en su ordenador.

- Esta acción funciona tanto en Windows como en macOS.

> [!NOTE]
> Por [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada. Sin embargo, si configura [!INCLUDE [prodshort](includes/prodshort.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.

## <a name="edit-in-excel"></a>Editar en Excel

- Con esta acción, Excel respeta la mayoría de los filtros de la página que limitan los registros que se muestran. Esto significa que el libro de Excel contendrá casi los mismos registros y columnas.

- La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prodshort](includes/prodshort.md)].

- Solo funciona en Windows; en macOS, no.

Esto se mejoró en la fase de lanzamiento 2 de 2019. Para obtener más información, vea [Mejoras en la integración de Excel](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).

> [!NOTE]
> Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel. Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Por [!INCLUDE[prodshort](includes/prodshort.md)] local, esta función solo está disponible para el cliente web.

### <a name="see-the-differences-between-the-options"></a>Consulte las diferencias entre las opciones
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Trabajar con Business Central](ui-work-product.md)  
