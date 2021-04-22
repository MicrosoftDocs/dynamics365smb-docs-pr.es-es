---
title: 'Procedimiento: Crear saldos iniciales del diario | Documentos de Microsoft'
description: Business Central incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada. Puede transferir fácilmente estos datos con registros en los diarios.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e1bb8e34e70d1d906850c157107b9b9701c6c50
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779862"
---
# <a name="create-journal-opening-balances"></a>Crear saldos iniciales del diario

[!INCLUDE[prod_short](includes/prod_short.md)] incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada. Puede transferir fácilmente estos datos con el diario del cliente, el diario del proveedor, el diario de productos o el diario de contabilidad.

El primer paso es crear un paquete de configuración que incluya las tablas de configuración para aquellos diarios. En el procedimiento siguiente se supone que este paso ya se completó. Para obtener más información, consulte [Establecer la configuración de una empresa](admin-set-up-company-configuration.md). Este procedimiento se describen los pasos subsiguientes, que incluyen la aplicación del paquete que proporciona un socio.  

Antes de comenzar, asegúrese de estar en la página Área de trabajo de la administración ya que proporciona el contexto correcto para su trabajo de configuración. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Procedimiento para aplicar movimientos de un diario a una nueva empresa

1. Configure una nueva empresa y aplíquele un paquete de configuración. Para obtener más información, consulte [Configurar una empresa con el asistente de RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    La nueva empresa no contiene información sobre los saldos iniciales del diario.  

2. Abra la hoja de trabajo de configuración e importe los datos existentes acerca de los clientes, los productos, los proveedores y la contabilidad. Para obtener más información, consulte [Migrar datos del cliente](admin-migrate-customer-data.md).  

    Ahora tiene los datos maestros correctos. A continuación, agregue los saldos iniciales. Los siguientes pasos describen cómo crear líneas de diario para cuentas de mayor, pero lo mismo se aplica a la creación de líneas de diario para clientes, proveedores y artículos.  
3. Elija, la acción **Crear líneas diario de cuentas general**.  
4. Rellene la ficha desplegable **Opciones** según corresponda y establezca los filtros según sea necesario. Por ejemplo, en el campo **Libro diario**, especifique un nombre.  
5. Elija el botón **Aceptar**. Los registros ahora están en el diario, pero los importes estarán vacíos.  
6. Exporte la tabla del diario a Excel y especifique manualmente la información de cuenta de registro y saldo a partir de los datos heredados.
7. Importe y aplique la información de la tabla a la nueva empresa. Las líneas del diario estarán preparadas para el registro.  
8. En la hoja de trabajo de configuración, seleccione la tabla de línea de diario y elija la acción **Datos de base de datos**.  
9. Revise la información y, a continuación, seleccione la acción **Registrar**.  
10. Repita los pasos para importar y registrar todos los saldos abiertos.  

> [!TIP]
> Puede usar los mismos trabajos por lotes para agregar saldos iniciales siempre que registre un nuevo cliente o proveedor con el que haya hecho negocios antes pero que no se haya registrado en [!INCLUDE [prod_short](includes/prod_short.md)]. Simplemente busque la tarea pertinente y luego elija el enlace correspondiente.

## <a name="see-also"></a>Consulte también

[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]