---
title: Ver y editar en Excel desde Business Central (contiene vídeo)
description: Obtenga más información sobre cómo puede abrir las páginas en Microsoft Excel desde Business Central para un mejor análisis de datos.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 82d08e1c072f74434ad50943a97baf77712cb171
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529412"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Ver y editar en Excel desde Business Central

Con las páginas que muestran una lista de registros en filas y columnas, como una lista de clientes, órdenes de venta o facturas, puede exportar la lista a Microsoft Excel y verla ahí. Dependiendo de la página, tiene dos opciones para ver en Excel. Ambas opciones están disponibles en el icono **Compartir** ![Compartir una página en otra aplicación.](media/share-icon.png) en la parte superior de una página. Puede seleccionar la acción **Abrir en Excel** o la acción **Editar en Excel** en la página. Este artículo explica las diferencias entre las dos acciones.

## <a name="open-in-excel"></a>Abrir en Excel

Con la acción **Abrir en Excel** puede realizar cambios en los registros en Excel, pero no puede volver a publicar los cambios en [!INCLUDE[prod_short](includes/prod_short.md)]. Solo puede guardar los cambios en el archivo de Excel, sin afectar los datos en [!INCLUDE[prod_short](includes/prod_short.md)].

- Con esta acción, Excel respeta los filtros de la página que limita los registros que se muestran. El libro de Excel contendrá las mismas filas y columnas que aparecen en la página de [!INCLUDE[prod_short](includes/prod_short.md)].

- Esta acción funciona tanto en Windows como en macOS.

- A partir de la actualización 18.3, también puede ver listas que se muestran en partes de la página, como las líneas en un pedido de venta. 

> [!NOTE]
> Por [!INCLUDE[prod_short](includes/prod_short.md)] local, la acción **Abrir en Excel** está disponible de forma predeterminada. Sin embargo, si configura [!INCLUDE[prod_short](includes/prod_short.md)] local para editar datos en Excel, la acción **Abrir en Excel** se reemplaza por la acción **Editar en Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Editar en Excel

La acción **Editar en Excel** está disponible en la mayoría de las listas, pero no en todas. Con la acción **Editar en Excel** puede realizar cambios en registros en Excel y luego volver a publicarlos en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando se abre Excel, verá el panel **Complemento de Excel** a la derecha.

- Con esta acción, Excel respeta la mayoría de los filtros en la página que limitan los registros mostrados, por lo que el libro de Excel contendrá casi los mismos registros y columnas.

- Para obtener los datos más recientes de [!INCLUDE[prod_short](includes/prod_short.md)], elija **Actualizar** en el panel Complemento de Excel.

- Puede cambiar la compañía con la que está trabajando. Para cambiar de empresa, seleccione el icono **Opciones** ![Opciones del complemento de Excel.](media/cogwheel.png "Opciones del complemento de Excel") En el panel Complemento de Excel, seleccione la empresa del campo **Empresa**.  

    > [!IMPORTANT]
    > Al cambiar de compañía, asegúrese de que el campo **Entorno** no está vacío. Si es así, configúrelo en una de las opciones disponibles; de lo contrario, el complemento no funcionará correctamente.  

Si realiza cambios en el complemento, debe volver a cargarlo para actualizar la conexión. Para recargar, use el menú del ![complemento de Excel](media/excel-addin-menu.png "Menú del complemento de Excel") en la esquina superior derecha del complemento. Si no puede cargar el complemento, hable con su administrador. Si es el administrador, consulte [Obtener el complemento de Business Central para Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> El complemento funciona con Excel para la web (en línea) desde cualquier dispositivo siempre que utilice un navegador compatible. También funciona con la aplicación Excel para Windows (PC); pero no para macOS.
>
> Para [!INCLUDE[prod_short](includes/prod_short.md)] local, la acción **Editar en Excel** solo está disponible si el administrador ha configurado el complemento de Excel y solo está disponible para el cliente web. Para los administradores: si desea aprender cómo instalar el complemento de Excel, consulte [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Primer inicio de sesión

La acción **Editar en Excel** requiere que el complemento Business Central esté instalado en Excel. En algunos casos es posible que su administrador haya configurado el complemento para instalarse automáticamente. En este caso, solo debe iniciar sesión en Business Central en el panel **Complemento de Excel** con su nombre de usuario y contraseña. De lo contrario, se abrirá el panel **Nuevo complemento de Office**. Para instalar el complemento, elija **Confía en este complemento**, que instalará el complemento directamente desde la Tienda Office.

Si por alguna razón el complemento no se instala, comuníquese con su administrador o intente instalarlo manualmente. Para más información, consulte [Instalar el complemento manualmente para su propio uso](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Consulte las diferencias entre las opciones
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a>Consulte también

[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Mejoras en la integración de Excel en el segundo lanzamiento de versiones de 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
