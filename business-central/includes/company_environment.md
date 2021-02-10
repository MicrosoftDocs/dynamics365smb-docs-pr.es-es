---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dcfc54d36b212b296747d28945324ac46c38cada
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753622"
---
Las personas a veces admiten a más de una empresa y necesitan pasar fácilmente de trabajar en una empresa a otra en [!INCLUDE [prod_short](prod_short.md)]. Por ejemplo, una empresa puede tener oficinas de ventas en ciudades y múltiples países, por lo que ha creado una unidad de negocios separada para cada oficina. Las oficinas que se encuentran en el mismo país se configuran como empresas separadas en un entorno compartido. Otras oficinas se crean como empresas en entornos separados porque tienen su base geográfica en otros países.<br><br>  

¿Qué es un entorno? Las empresas en [!INCLUDE[prod_short](prod_short.md)] existen en lo que se conoce como *entornos*. Hay dos tipos de entornos, **Producción** y **Espacio aislado**. En resumen, los entornos de producción contienen datos comerciales activos, y los entornos de espacio aislado se utilizan como un lugar seguro para probar cosas, como procesos o características comerciales nuevos. Para obtener más información, consulte [Tipos de entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments). Si tiene acceso a una empresa, tiene acceso al entorno en el que se encuentra. Si tiene acceso a más de una empresa y esas empresas se encuentran en entornos diferentes, cuando inicia sesión en [!INCLUDE[prod_short](prod_short.md)], debe especificar el entorno en el que desea trabajar. Los entornos son específicos de un país determinado, por lo que si su organización trabaja en varios países, necesitará entornos separados para cada país.<br><br>  

¿Qué es una empresa? Piense en una *empresa* como un contenedor que contiene información sobre una entidad legal. Utilizando el ejemplo anterior, la empresa tiene una oficina de ventas en Seattle y otra en Nueva York, por lo que crea una compañía en [!INCLUDE[prod_short](prod_short.md)] para cada oficina, de forma que puede administrar las operaciones para cada oficina por separado.  
