---
title: Realizar un seguimiento de los segmentos y las interacciones relacionadas | Documentos de Microsoft
description: Obtenga información sobre cómo crear segmentos para definir grupos de contactos y especificar interacciones para los segmentos.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 5f11d7c5607f54061166eebd11fb7e7cc58d5fbc
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "921683"
---
# <a name="managing-interactions-for-segments"></a>Administrar interacciones para segmentos
La página **Segmento** es un tipo de hoja de cálculo con la que puede:

* Crear segmentos.
* Guardar los criterios de segmentación usados para seleccionar los contactos.
* Grabar el segmento y registrar interacciones relacionadas con los contactos del segmento.

## <a name="segmenting"></a>Segmentar
Hay varias formas de crear segmentos:

* Puede introducir manualmente en las líneas del segmento los contactos que desee incluir en el mismo.
* Puede seleccionar contactos.
* Puede volver a utilizar un segmento grabado como base para crear uno nuevo.
* Puede volver a utilizar los criterios de segmentación guardados.

## <a name="interactions"></a>Interacciones
En la página **Segmento**, puede crear a la vez interacciones para varios contactos. Por ejemplo, puede combinar un segmento con un documento de Microsoft Word, para poder enviar una carta a todos los contactos del segmento.

Puede especificar información acerca de la interacción del segmento en la cabecera de **Segmento**. Por ejemplo, puede elegir la plantilla de interacción que se usará con todos los contactos, especificar una descripción, un tipo de correspondencia, etc. Sin embargo, puede modificar esta información en la línea de segmento para cada contacto en particular, por ejemplo, si especifica otra descripción de un contacto. Si combina un segmento con un documento de Microsoft Word, puede personalizar el documento para que se envíe a uno o más contactos del segmento, por ejemplo, agregando comentarios personalizados al documento.

## <a name="logging"></a>Registro
En la página **Segmento**, si elige **Registrar**, la aplicación registra las interacciones en la página **Mov. log de interacción** y registra el segmento. Después de grabar el segmento, sólo podrá encontrarlo en la página **Segmentos archivados**.

En la página **Segmentos archivados**, puede decidir crear un segmento de seguimiento que contenga los mismos contactos que el segmento que ha archivado.

## <a name="see-also"></a>Consulte también
[Crear segmentos](marketing-how-create-segment.md)  
[Crear interacciones de segmentos](marketing-how-create-interactions.md)  
[Administrar segmentos](marketing-segments.md)  
[Registrar interacciones con contactos](marketing-interactions.md)  
[Administrar oportunidades de venta](marketing-manage-sales-opportunities.md)  
[Creación y administración de contactos](marketing-contacts.md)  
[Trabajar con Business Central](ui-work-product.md)
