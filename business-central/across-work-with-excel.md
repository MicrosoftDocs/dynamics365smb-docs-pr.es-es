---
title: Ver y editar en Excel desde Business Central
description: Obtenga más información sobre cómo puede abrir las páginas en Microsoft Excel desde Business Central para un mejor análisis de datos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443486"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Ver y editar en Excel desde Business Central

Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, también puede ver los registros mediante Microsoft Excel. Dependiendo de la página, tiene dos opciones para ver en Excel. Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página. Este artículo explica las diferencias entre las dos acciones.

## <a name="open-in-excel"></a>Abrir en Excel

Con la acción **Abrir en Excel** puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prod_short](includes/prod_short.md)]. Solo puede guardar los cambios en el archivo de Excel en su ordenador.

- Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran. El libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prod_short](includes/prod_short.md)].

- Esta acción funciona tanto en Windows como en macOS.

- A partir de la actualización 18.3, también puede ver listas que se muestran en partes de la página, como las líneas en un pedido de venta. Por ahora, esta capacidad es una función opcional, que requiere que habilite **Exportar cualquier parte de la lista a Excel** en **Administración de características**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> Por [!INCLUDE[prod_short](includes/prod_short.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada. Sin embargo, si configura [!INCLUDE[prod_short](includes/prod_short.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Editar en Excel

Con la acción **Editar en Excel** puede realizar cambios en registros en Excel y luego volver a publicarlos en [!INCLUDE[prod_short](includes/prod_short.md)].

- Con esta acción, Excel respeta la mayoría de los filtros en la página que limitan los registros mostrados, por lo que el libro de Excel contendrá casi los mismos registros y columnas.

- Solo funciona en Windows; en macOS, no.

- Puede cambiar la compañía con la que está trabajando. Para cambiar de empresa, seleccione el icono **Opciones** ![Opciones del complemento de Excel.](media/cogwheel.png "Opciones del complemento de Excel") En el panel Complemento de Excel, seleccione la empresa del campo **Empresa**.  

    > [!IMPORTANT]
    > Al cambiar de compañía, asegúrese de que el campo **Entorno** no está vacío. Si es así, configúrelo en una de las opciones disponibles; de lo contrario, el complemento no funcionará correctamente.  

Si realiza cambios en el complemento, debe volver a cargarlo para actualizar la conexión. Para recargar, use el menú del ![complemento de Excel](media/excel-addin-menu.png "Menú del complemento de Excel") en la esquina superior derecha del complemento. Si no puede cargar el complemento, hable con su administrador. Si es el administrador, consulte [Configurar el complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Para [!INCLUDE[prod_short](includes/prod_short.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel y solo está disponible para el cliente web. Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Consulte las diferencias entre las opciones
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Mejoras en la integración de Excel en el segundo lanzamiento de versiones 2 de 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]