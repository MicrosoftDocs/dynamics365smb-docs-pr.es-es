---
title: "Configurar las campañas de marketing en Financials | Documentos de Microsoft"
description: "Describe cómo puede configurar y realizar campañas de marketing en Dynamics 365 for Financials"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="managing-marketing-campaigns"></a>Administrar campañas de marketing
Un buen plan de marketing puede permitirle identificar, atraer y conservar a los clientes. Un plan de marketing consta de varias campañas y otras interacciones relacionadas con sus actividades de ventas y marketing. Durante la planificación de una campaña, debe decidir a qué contactos se va a dirigir, el tipo de campaña (por ejemplo, exposición comercial o correo directo) y los vendedores que realizarán las tareas.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## <a name="defining-individual-campaigns"></a>Definir campañas individuales
Antes de crear una campaña, debe configurar *códigos de estado de campaña*. El uso de estos códigos le permitirá administrar sus campañas asignando un estado a cada una de ellas. A medida que trabaja en las distintas etapas de una campaña, podrá ver en qué etapa de la campaña se encuentra y cuál es el siguiente paso. Los códigos de estado de campaña se configuran en la ventana **Estado campaña**.

Puede crear una *ficha de campaña* para cada campaña de la que desee realizar un seguimiento. También puede acceder a estas fichas de campañas para ver información general sobre sus campañas.
Puede eliminar los movimientos de campaña, por ejemplo si registran una acción que ha sido cancelada. Sólo se pueden borrar los movimientos de campaña cancelados.

### <a name="selecting-the-target-audience"></a>Selección del público objetivo
Una vez creada una campaña, puede crear segmentos que especifiquen el público objetivo de la campaña. Para obtener más información, vea [Administrar segmentos](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Registrar porcentajes de descuento
Cuando haya configurado su campaña, decidido qué segmentos desea que cubra la campaña y establecido la fecha inicial y final, registre el porcentaje de descuento que recibirá el cliente en cada producto en las líneas de la ventana **Descuentos línea ventas**. También puede registrar precios de venta de los productos individuales en las líneas de la ventana **Precios ventas**. Puede acceder a ambas ventanas desde la ficha de campaña.

 Cuando haya configurado los precios de venta y los descuentos de líneas y los segmentos en la ficha de campaña, debe activarlos para que los precios y descuentos de campaña se reflejen en las líneas.

> [!NOTE]  
>  Para activar los precios de venta y descuentos de línea, debe especificar si todo el segmento o solo algunos contactos son los objetivos de la campaña. Si los precios de venta y descuentos de línea cubren a todos los contactos del segmento, seleccione el campo **Objetivo campaña** de la ficha desplegable **Campaña** de la ficha **Segmento**.
Si los precios de venta y descuentos de línea no se ofrecen a todos los contactos del segmento, puede desactivar el campo **Objetivo campaña** para los contactos relevantes. Si no ve este campo, puede agregarlo a la vista. Para obtener más información, vea [Personalización del usuario](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## <a name="see-also"></a>Consulte también
[Gestionar contactos](marketing-contacts.md)  
[Administrar segmentos](marketing-segments.md)  
[Administrar oportunidades de venta](marketing-manage-sales-opportunities.md)  
[Trabajar con Financials](ui-work-product.md)  

