---
title: Usar Excel para importar datos en Financials | Documentos de Microsoft
description: "Utilice el paquete de configuración predeterminado para agregar datos de cliente en Excel e importar los datos en Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: 8cf36afea60b089afac8f1c27d126cd19b88ce94
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importar datos del software de contabilidad heredado mediante un paquete de configuración
Puede importar datos maestros y algunos datos transaccionales de otros sistemas de financieros mediante el paquete de configuración predeterminado en [!INCLUDE[d365fin](includes/d365fin_md.md)]. En la ventana **Paquetes de configuración** puede trabajar con el paquete para importar y validar los datos antes de aplicar el paquete.  

Si está familiarizado con los servicios de RapidStart para Microsoft Dynamics, también estará familiarizado con los paquetes de configuración. El paquete de configuración predeterminado admite la mayoría de tipos de datos habituales que desea importar de un sistema heredado. En Excel, puede agregar los datos del sistema heredado y configurarlos según la lógica empresarial de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>   Opcionalmente, utilice asistentes de migración para importar datos de QuickBooks GP o Dynamics GP. Para obtener más información, consulte [Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md) o [Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="working-with-data-in-excel"></a>Trabajar con datos en Excel
Al exportar el paquete de configuración predeterminado a Excel, el libro generado contiene una hoja de trabajo para cada tabla del paquete. Para simplificar sus tareas, puede aprovechar las herramientas de manipulación de XML que se integran en Excel. También puede utilizar las funciones integradas de Excel para ayudar con el formato de datos y para colocar los datos en la celda correcta. Por ejemplo, agregue una hoja de cálculo en blanco y copie los datos heredados en ella. A continuación, cree una fórmula de Excel para asignar datos en la hoja de cálculo de transformación entre los campos en la hoja de cálculo exportada y los datos heredados del cliente. Después de asignar todos los datos, copie el intervalo de datos en la hoja de cálculo de la tabla.  

> [!IMPORTANT]  
>  No cambie las columnas en las hojas de cálculo. Si se mueven, modifican o eliminan, la hoja de cálculo no podrá importarse a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="tables-in-the-default-configuration-package"></a>Tablas del paquete de configuración predeterminado
El paquete de configuración predeterminado admite las tablas siguientes:

-   Condiciones de pago
-   Grupo precio cliente
-   Condiciones de envío
-   Vendedor/Comprador
-   Lugar
-   Cuenta
-   Cliente
-   Proveedor
-   Elemento
-   Cab. venta
-   Lín. venta
-   Cab. compra
-   Lín. compra
-   Lín. diario general
-   Lín. diario producto
-   Grupo contable cliente
-   Grupo contable proveedor
-   Grupo contable inventario
-   Unidad de medida
-   Gr. contable negocio
-   Gr. contable producto
-   Configuración grupos contables
-   Territorio
-   Categoría producto
-   Precio venta
-   Precio compra

## <a name="importing-customer-data"></a>Importar datos de cliente
Después de que los datos del cliente se hayan introducido en Excel, importe los datos a [!INCLUDE[d365fin](includes/d365fin_md.md)]. En la ventana **Paquetes de configuración**, se importan los datos del archivo de Excel y puede validar que los datos sean coherentes con [!INCLUDE[d365fin](includes/d365fin_md.md)] antes de aplicar el paquete.

## <a name="see-also"></a>Consulte también
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

