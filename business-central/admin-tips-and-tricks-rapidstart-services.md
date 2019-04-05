---
title: 'Sugerencias y trucos: RapidStart Services | Documentos de Microsoft'
description: Cuando configura empresas con RapidStart Services, hay algunas sugerencias y trucos que puede aprovechar para facilitar la implementación.
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
ms.openlocfilehash: 875ab6f5875a842fb4c2ab906f39ae95607f6ba8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806695"
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
Se recomienda migrar los saldos iniciales en el orden siguiente.  

1.  Migre los saldos iniciales de contabilidad sin usar los sublibros de la cuenta de contabilidad. Use cuentas de compensación de saldos iniciales específicas, una para cada sublibro. Configure las cuentas de compensación para habilitar los registros directos.  
2.  Migre los movimientos de cliente abiertos.  
3.  Migre los movimientos de producto abiertos.  
4.  Migre los movimientos de activos abiertos.  

## <a name="see-also"></a>Consulte también  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)
