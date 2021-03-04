---
title: 'Sugerencias y trucos: RapidStart Services | Documentos de Microsoft'
description: Cuando configura empresas con RapidStart Services, hay algunas sugerencias y trucos que puede aprovechar para facilitar la implementación.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e9506697eacfb4bd411266078e4245e59a11353
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922422"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Sugerencias y trucos: RapidStart Services

Cuando configura empresas con RapidStart Services, hay algunas sugerencias y trucos que puede aprovechar para facilitar la implementación.  

## <a name="take-advantage-of-configuration-templates"></a>Aprovechar las plantillas de configuración

Las plantillas de configuración pueden ayudarle a simplificar el proceso de implementación. Al usarlas, puede incluir clientes similares en los segmentos y, a continuación, desarrollar un protocolo de implementación que trate a todos los clientes de un segmento de forma similar. De ese modo, puede aplicar un nivel de preconfiguración en cada segmento y continuar con una implementación rápida.  

## <a name="configuration-questionnaires"></a>Cuestionarios de configuración

Para ayudar al proceso de rellenar un cuestionario de configuración, considere la posibilidad de definir las respuestas predeterminadas para indicar los procedimientos recomendados.  

## <a name="batch-creation-of-journal-lines"></a>Creación por lotes de líneas de diario

Se recomienda usar las herramientas de migración de datos que se ofrecen para migrar los movimientos del diario. De lo contrario, si usa un trabajo por lotes para crear líneas de diario, eso tiene un ámbito limitado y genera solo los campos predeterminados en un diario. El resto del diario debe completarse manualmente.  

## <a name="migrating-transactions"></a>Migración de transacciones

Se recomienda migrar los saldos iniciales en el orden siguiente. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Migre los saldos iniciales de contabilidad sin usar los sublibros de la cuenta de contabilidad. Use cuentas de compensación de saldos iniciales específicas, una para cada sublibro. Configure las cuentas de compensación para habilitar los registros directos.  
2. Migre los movimientos de cliente abiertos.  <!--work on these-->
3. Migre los movimientos de producto abiertos.  
4. Migre los movimientos de activos abiertos.  

## <a name="make-each-package-manageable"></a>Haga que cada paquete sea manejable

Cuando utilice paquetes de configuración para migrar datos, separe los datos en paquetes separados para facilitar la portabilidad. Por ejemplo, si desea migrar 20 años de entradas del libro mayor, la importación puede tardar muchas horas y días. En su lugar, divida los datos para que cada paquete sea más manejable. Actualmente, no existen reglas firmes sobre lo que hace que un paquete funcione, pero si ve problemas al importar o exportar un paquete, intente hacerlo más pequeño y vea si eso ayuda.  

## <a name="see-also"></a>Consulte también

[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]