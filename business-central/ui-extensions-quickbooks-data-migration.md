---
title: "Usar la extensión de migración de QuickBooks | Documentos de Microsoft"
description: "Describe cómo utilizar la extensión para importar clientes, proveedores, productos y cuentas desde QuickBooks Desktop a Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 583f6947acd3778710f0889736439322d9179ce6
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="the-quickbooks-data-migration-extension"></a>Extensión de la migración de datos de QuickBooks
Esta extensión facilita la migración de clientes, proveedores, productos y cuentas de QuickBooks a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si la empresa usa QuickBooks actualmente, puede exportar la información correspondiente y después abrir una guía de instalación asistida para cargar los datos en [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Para obtener más información, vea [Importar datos empresariales desde otros sistemas financieros](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Exportar datos desde QuickBooks Desktop
Debe haber exportado algunos o todos los clientes, proveedores, productos de inventario y cuentas existentes a un archivo IIF (Intuit Interchange Format). La extensión de la migración de datos de QuickBooks incluye una asociación predeterminada de datos de QuickBooks para que pueda usar sus datos existentes para probar su nueva empresa [!INCLUDE[d365fin](includes/d365fin_md.md)]. La asignación predeterminada será suficiente en la gran mayoría de casos, pero puede cambiar la asignación en la guía de configuración asistida.  
En QuickBooks, el menú Archivo incluye una utilidad para exportar listas. Para las finalidades de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar las listas siguientes:

* Lista de clientes  
* Lista de proveedores  
* Lista de productos  
* Lista de cuentas  

Los datos exportados se guardan como un archivo IIF que, a continuación, puede cargar a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>Buscar la extensión de la migración de datos de QuickBooks
La extensión de la migración de datos de QuickBooks está instalada y lista como parte integrada de la guía de configuración asistida de la migración de datos. Si está preparado para empezar ahora y ha exportado sus datos de QuickBooks, elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), introduzca **Configuración asistida** y, a continuación, haga clic el vínculo relacionado. Seleccione **Migrar los datos empresariales**y, a continuación, siga los pasos en la guía.  

## <a name="see-also"></a>Consulte también
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)  

