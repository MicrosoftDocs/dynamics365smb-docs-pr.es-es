---
title: 'Procedimiento: Crear saldos iniciales del diario | Documentos de Microsoft'
description: Business Central incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada. Puede transferir fácilmente estos datos con registros en los diarios.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 612eb9cfa5c6cd45bf154f4813efa3b349f44841
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806807"
---
# <a name="create-journal-opening-balances"></a>Crear saldos iniciales del diario
[!INCLUDE[d365fin](includes/d365fin_md.md)] incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada. Puede transferir fácilmente estos datos con el diario del cliente, el diario del proveedor, el diario de productos o el diario de contabilidad.

El primer paso es crear un paquete de configuración que incluya las tablas de configuración para aquellos diarios. En el procedimiento siguiente se supone que este paso ya se completó. Para obtener más información, consulte [Establecer la configuración de una empresa](admin-set-up-company-configuration.md). Este procedimiento se describen los pasos subsiguientes, que incluyen la aplicación del paquete que proporciona un socio.  

Antes de comenzar, asegúrese de estar en la página Área de trabajo del implementador de RapidStart Services ya que proporciona el contexto correcto para su trabajo de configuración. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Procedimiento para aplicar movimientos de un diario a una nueva empresa  
1. Configure una nueva empresa y aplíquele un paquete de configuración. Para obtener más información, consulte [Configurar una empresa con el asistente de RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    La nueva empresa no contiene información sobre los saldos iniciales del diario.  

2. Abra la hoja de trabajo de configuración e importe los datos existentes acerca de los clientes, los productos, los proveedores y la contabilidad. Para obtener más información, consulte [Migrar datos del cliente](admin-migrate-customer-data.md).  
3. Elija, por ejemplo, la acción **Crear líneas diario general**.  
4. Rellene la ficha desplegable **Opciones** según corresponda y establezca los filtros según sea necesario. Por ejemplo, en el campo **Libro diario**, especifique un nombre.  
5. Elija el botón **Aceptar**. Los registros ahora están en el diario, pero los importes estarán vacíos.  
6. Exporte la tabla del diario a Excel y especifique manualmente la información de cuenta de registro y saldo a partir de los datos heredados.
7. Importe y aplique la información de la tabla a la nueva empresa. Las líneas del diario estarán preparadas para el registro.  
8. En la hoja de trabajo de configuración, seleccione la tabla de línea de diario y elija la acción **Datos de base de datos**.  
9. Revise la información y, a continuación, seleccione la acción **Registrar**.  
10. Repita los pasos para importar y registrar todos los saldos abiertos.  

## <a name="see-also"></a>Consulte también  
[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)
