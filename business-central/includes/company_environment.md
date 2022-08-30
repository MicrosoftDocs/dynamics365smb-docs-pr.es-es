---
author: edupont04
ms.topic: include
ms.date: 04/01/2022
ms.author: edupont
ms.openlocfilehash: 74cf1897792ab15c9c74ff76e3674ca31fe599f1
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317380"
---
Los usuarios de [!INCLUDE[prod_short](prod_short.md)] a veces admiten a más de un departamento o suborganización dentro de una unidad de negocio. Por ejemplo, una empresa puede tener oficinas de ventas en distintas ciudades y múltiples países o regiones, por lo que ha creado una unidad de negocios separada para cada oficina. Las oficinas que se encuentran en el mismo país se configuran como *empresas* separadas en un *entorno* compartido. Otras oficinas se crean como empresas en entornos separados porque tienen su base geográfica en otros países.

- ¿Qué es una empresa?

  Piense en una *empresa* como un contenedor que contiene información sobre una entidad legal. Utilizando el ejemplo anterior, la empresa tiene una oficina de ventas en Seattle y otra en Nueva York, por lo que crea una compañía en [!INCLUDE[prod_short](prod_short.md)] para cada oficina, de forma que puede administrar las operaciones para cada oficina por separado.

- ¿Qué es un entorno?

  Las empresas en [!INCLUDE[prod_short](prod_short.md)] en línea existen en lo que se conoce como *entornos*. Hay dos tipos de entornos, **Producción** y **Espacio aislado**. En resumen, los entornos de producción contienen datos comerciales activos, y los entornos de espacio aislado se utilizan como un lugar seguro para probar cosas, como procesos o características comerciales nuevos. Para obtener más información, consulte [Tipos de entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (solo en inglés). Si tiene acceso a una empresa, tiene acceso al entorno en el que se encuentra. Si tiene acceso a más de una empresa y esas empresas se encuentran en entornos diferentes, cuando inicia sesión en [!INCLUDE[prod_short](prod_short.md)], debe especificar el entorno en el que desea trabajar. Los entornos son específicos de un país determinado, por lo que si su organización trabaja en varios países, necesitará entornos separados para cada país. Para obtener más información, consulte [Entornos y empresas](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (solo en inglés).
