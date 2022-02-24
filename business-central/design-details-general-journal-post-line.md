---
title: 'Detalles de diseño: línea de registro en diario general | Documentos de Microsoft'
description: En este tema se proporciona información de los conceptos y los principios que se usan para rediseñar la función de línea de registro en el diario general en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1a8654b53dec476b175101a4d9c08f15ab3d6d6f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185377"
---
# <a name="design-details-general-journal-post-line"></a>Detalles de diseño: línea de registro en diario general
En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan para rediseñar la función de línea de registro en el diario general en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El nuevo diseño hace la codeunit 12 más sencillo y más fácil de mantener. La documentación comienza con la descripción de la información general conceptual del rediseño. A continuación, explica la arquitectura técnica para mostrar los cambios resultantes del nuevo diseño.  

## <a name="in-this-section"></a>En esta sección  
[Descripción de la línea de registro en diario general](design-details-general-journal-post-line-overview.md)  
[Detalles de diseño: estructura de interfaz de registro](design-details-posting-interface-structure.md)  
[Detalles de diseño: estructura de motor de registro](design-details-posting-engine-structure.md)  
[Cambios en codeunit 12: asociación de variables globales para línea de registro en diario general](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[Cambios en la codeunit 12: cambios en los procedimientos de registro en el diario general](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a>Consulte también  
[Trabajar con diarios generales](ui-work-general-journals.md)
