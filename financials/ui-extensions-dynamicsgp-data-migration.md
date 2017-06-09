---
title: "Migración de datos de Microsoft Dynamics GP | Documentos de Microsoft"
description: "Proporciona información sobre la extensión de migración de datos de Dynamics GP"
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
ms.openlocfilehash: a94afbd0ee689f6bd9157d0b441959f252230f08
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials"></a>Extensión de la migración de datos de Dynamics GP para Dynamics 365 for Financials
Esta extensión facilita la migración de clientes, proveedores, productos de inventario y cuentas de Dynamics GP a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si la empresa usa Dynamics GP actualmente, puede exportar los registros maestros correspondientes y después abrir una guía de instalación asistida para agregar los datos a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Migrar datos empresariales desde otros sistemas financieros](upload-data.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportar datos desde Dynamics GP
Deberá haber exportado todos los clientes, proveedores, productos de inventario y cuentas existentes, o parte de ellos, mediante la funcionalidad de exportación de datos de Dynamics GP. Para las finalidades de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar los tipos de datos siguientes:

* Cuenta  
* Cliente  
* Elemento  
* Proveedor  

La extensión de la migración de datos de Dynamics GP asigna automáticamente los datos exportados para que estén a su disposición rápidamente en la nueva empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Durante el proceso, se crea información de configuración auxiliar, por ejemplo grupos contables. Los productos de inventario se incorporarán al sistema con el método de valoración de coste FIFO. Las cuentas se configurarán como el segmento de cuenta principal desde Dynamics GP con dimensiones, porque [!INCLUDE[d365fin](includes/d365fin_long_md.md)] no tiene segmentos de cuentas.

## <a name="see-also"></a>Consulte también
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizando extensiones](ui-extensions.md)  

