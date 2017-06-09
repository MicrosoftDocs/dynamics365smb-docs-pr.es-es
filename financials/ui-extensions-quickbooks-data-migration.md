---
title: "Migración de datos de QuickBooks | Documentos de Microsoft"
description: "Proporciona información sobre la extensión de migración de datos de QuickBooks"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 860ee6b26071e8264deb68bec3b039f384c7be0f
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>Extensión de la migración de datos de QuickBooks para Dynamics 365 for Financials
Esta extensión facilita la migración de clientes, proveedores, productos y cuentas de QuickBooks a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si la empresa usa QuickBooks actualmente, puede exportar la información correspondiente y después abrir una guía de instalación asistida para cargar los datos en [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Para obtener más información, vea [Importar datos empresariales desde otros sistemas financieros](upload-data.md).

## <a name="exporting-data-from-quickbooks"></a>Exportar datos desde QuickBooks
Debe haber exportado algunos o todos los clientes, proveedores, productos de inventario y cuentas existentes a un archivo IIF (Intuit Interchange Format). La extensión de la migración de datos de QuickBooks incluye una asociación predeterminada de datos de QuickBooks para que pueda usar sus datos existentes para probar su nueva empresa [!INCLUDE[d365fin](includes/d365fin_md.md)]. La asignación predeterminada será suficiente en la gran mayoría de casos, pero puede cambiar la asignación en la guía de configuración asistida.  
En QuickBooks, el menú Archivo incluye una utilidad para exportar listas. Para las finalidades de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar las listas siguientes:

* Lista de clientes  
* Lista de proveedores  
* Lista de productos  
* Lista de cuentas  

Los datos exportados se guardan como un archivo IIF que, a continuación, puede cargar a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Consulte también
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizando extensiones](ui-extensions.md)  

