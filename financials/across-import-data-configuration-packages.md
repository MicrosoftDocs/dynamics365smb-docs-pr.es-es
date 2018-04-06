---
title: Usar Excel para importar datos en Financials | Documentos de Microsoft
description: "Utilice el paquete de configuración predeterminado para agregar datos de cliente en Excel e importar los datos en Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 591d8100100ee717a932d188a87545fe4098a001
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importar datos del software de contabilidad heredado mediante un paquete de configuración
Puede importar datos maestros y algunos datos transaccionales de otros sistemas de financieros mediante el paquete de configuración predeterminado en [!INCLUDE[d365fin](includes/d365fin_md.md)]. En la ventana **Paquetes de configuración** puede trabajar con el paquete para importar y validar los datos antes de aplicar el paquete.  

> [!NOTE]  
> Los paquetes de configuración son parte de RapidStart Services para [!INCLUDE[d365fin](includes/d365fin_md.md)], un conjunto de herramientas extenso para configurar nuevas soluciones basadas en los requisitos comerciales de los clientes y los datos de configuración. RapidStart Services también ofrece la funcionalidad de importar los datos heredados. Para obtener más información, consulte [Configuración de una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

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
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

