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
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: b25413c8f0479aaccfc67ae96f2870690f993dfa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927277"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Ver y editar en Excel desde Business Central

Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel. Para ello, tiene dos opciones. Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página. Las diferencias entre las dos acciones son las siguientes:  

## <a name="open-in-excel"></a>Abrir en Excel

- Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran. Esto significa que el libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prodshort](includes/prodshort.md)].

- Puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prodshort](includes/prodshort.md)]. Solo puede guardar los cambios en el archivo de Excel en su ordenador.

- Esta acción funciona tanto en Windows como en macOS.

> [!NOTE]
> Por [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada. Sin embargo, si configura [!INCLUDE[prodshort](includes/prodshort.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.

## <a name="edit-in-excel"></a>Editar en Excel

- Con esta acción, Excel respeta la mayoría de los filtros de la página que limitan los registros que se muestran. Esto significa que el libro de Excel contendrá casi los mismos registros y columnas.

- La ventaja de la acción **Editar en Excel** es que le permite realizar cambios en los registros en Excel y luego publicarlos de nuevo en [!INCLUDE[prodshort](includes/prodshort.md)].

- Solo funciona en Windows; en macOS, no.

- Puede cambiar la compañía con la que está trabajando. Para hacerlo, seleccione el icono **Opciones** ![Opciones de complemento de Excel](media/cogwheel.png "Opciones del complemento de Excel") en el panel Complemento de Excel y luego seleccione la compañía en el campo **Empresa**.  

    > [!IMPORTANT]
    > Al cambiar de compañía, asegúrese de que el campo **Entorno** no está vacío. Si es así, configúrelo en una de las opciones disponibles; de lo contrario, el complemento no funcionará correctamente.  

Si realiza cambios en el complemento, debe volver a cargarlo para actualizar la conexión. Para recargar, use el menú del ![complemento de Excel](media/excel-addin-menu.png "Menú del complemento de Excel") en la esquina superior derecha del complemento.

> [!NOTE]
> Para [!INCLUDE[prodshort](includes/prodshort.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel y solo está disponible para el cliente web. Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Consulte las diferencias entre las opciones
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Mejoras en la integración de Excel en el segundo lanzamiento de versiones 2 de 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
