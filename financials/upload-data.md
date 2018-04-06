---
title: Importar los datos empresariales heredados a Finance and Operations, Business edition | Documentos de Microsoft
description: Puede migrar datos para clientes, proveedores e inventario, por ejemplo, desde Excel, QuickBooks o Dynamics GP, a Finance and Operations, Business edition.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QuickBooks, transfer, import, migrate, initialize, implement
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fe1f89ee875924370a206359a3f7238f0224ab80
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Importar datos de empresa de otros sistemas financieros
Cuando se registra en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede elegir crear una empresa vacía, de este modo podrá cargar sus datos y probar su nueva empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)]. En función de la solución de finanzas que use su empresa actualmente, puede transferir información sobre clientes, proveedores, inventario y cuentas bancarias.  

Desde el área de trabajo, puede iniciar una guía de configuración asistida que le ayudará a transferir los datos de la empresa de un archivo Excel o de otros formatos. El tipo de archivos que puede cargar depende de las extensiones disponibles. Por ejemplo, puede migrar los datos de QuickBooks, ya que [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye una extensión que gestiona la conversión desde QuickBooks. Si desea migrar los datos de otras soluciones de finanzas, debe comprobar si hay una extensión disponible para esa solución o importarlos desde Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] incluye plantillas de cuentas, clientes, proveedores y productos de inventario que puede elegir para que se apliquen al importar sus datos.

> [!NOTE]  
> Para un trabajo de implementación más amplio, puede utilizar RapidStart Services para [!INCLUDE[d365fin](includes/d365fin_md.md)], que es un conjunto de herramientas extenso para configurar nuevas soluciones basadas en los requisitos comerciales de los clientes y los datos de configuración. RapidStart Services también ofrece la funcionalidad de importar los datos empresariales. Para obtener más información, consulte [Configuración de una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).  

## <a name="importing-data-from-quickbooks-desktop-quickbooks-online-or-dynamics-gp"></a>Importar datos de QuickBooks Desktop, QuickBooks Online o Dynamics GP
Si su empresa actualmente usa QuickBooks o Dynamics GP, puede exportar la información pertinente a un archivo. Puede iniciar la guía de configuración asistida para transferir los datos.
Por ejemplo, si su archivo incluye clientes y proveedores, puede elegir transferir solo los datos de cliente. Podrá transferir el resto de la información más adelante.  

La configuración asistida incluye una opción para cambiar la configuración predeterminada de la transferencia, pero le recomendamos que solo introduzca la configuración avanzada si está familiarizado con tablas de bases de datos. En gran la mayoría de las empresas, la asignación predeterminada de QuickBooks o Dynamics GP a [!INCLUDE[d365fin](includes/d365fin_md.md)] transferirá la información que desee.  

Para obtener más información, vea [Migración de datos de QuickBooks Desktop](ui-extensions-quickbooks-data-migration.md), [Migración de datos de QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md) o [Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="importing-data-from-configuration-packages"></a>Importar datos desde los paquetes de configuración
[!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un paquete de configuración que puede exportar a Excel y configurar los datos en esa aplicación. A continuación, puede volver a importar los datos desde Excel. El paquete consta de 27 tablas, incluidos datos maestros, como clientes, proveedores, productos y cuentas, otras tablas básicas de configuración, como métodos de envío, y tablas de transacciones, como encabezado y líneas de venta.  

> [!NOTE]  
>   El trabajo con paquetes de configuración es una función avanzada y le recomendamos que se ponga en contacto con el administrador. Para obtener más información, vea [Importar datos del software de contabilidad heredado mediante un paquete de configuración](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Importar datos del software de contabilidad heredado mediante un paquete de configuración](across-import-data-configuration-packages.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Migración de datos de QuickBooks Desktop](ui-extensions-quickbooks-data-migration.md)  
[Migración de datos de QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md)  
[Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)   
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

