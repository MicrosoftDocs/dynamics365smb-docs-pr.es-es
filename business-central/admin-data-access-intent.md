---
title: Administrar la intención de acceso a la base de datos en Business Central | Microsoft Docs
description: Cambie la intención de acceso a la base de datos para informes, páginas API y consultas.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 33b5a3ff604b0ddf7525b89d7a8a82bcfdd7f653
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196391"
---
# <a name="managing-database-access-intent"></a>Gestionar la intención de acceso a la base de datos 

Como superusuario o administrador, puede cambiar la intención de acceso a la base de datos en informes, páginas de tipo API y consultas para mejorar el rendimiento del servicio.

## <a name="overview"></a>Panorama

[!INCLUDE[d365fin](includes/d365fin_md.md)] se puede configurar para usar réplicas de solo lectura de la base de datos primaria (lectura-escritura). El uso de la réplica de la base de datos reduce la carga en la base de datos primaria. En algunos casos, también mejorará el rendimiento al visualizar datos en el cliente. Las réplicas son beneficiosas para los objetos, como informes, consultas y páginas API, que se usan para ver solo datos, no para modificar datos.

Cuando se ejecutan los objetos, la intención de acceso a la base de datos determina si se usa una réplica de solo lectura, si hay una disponible, o la base de datos primaria. Los informes, las páginas API y las consultas se desarrollan con una intención de acceso a la base de datos predefinida (consulte [Propiedad DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

La página **Lista de intenciones de acceso a la base de datos** permite anular la intención de acceso a la base de datos predefinida para los objetos cuando se ejecutan.

En términos de base de datos, esta característica se conoce comúnmente como *escalado de lectura*. Para obtener más información sobre el escalado de lectura y la intención de acceso a datos en [!INCLUDE[d365fin](includes/d365fin_md.md)], vea [Utilizar el escalado de lectura para un mejor rendimiento](https://review.docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview?branch=tfs337368-readscaleout) en la ayuda para desarrolladores y profesionales de TI de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-change-the-database-access-intent"></a>Para cambiar la intención de acceso a la base de datos

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Lista de intenciones de acceso a la base de datos** y luego elija el enlace relacionado.

    La página enumera todos los informes, páginas y consultas. La columna **Intento de acceso** incluye uno de los siguientes valores:

    |**Configuración**|**Descripción**|  
    |------------|-------------|  
    |**Predet.**|Indica que el objeto utiliza la intención de acceso a la base de datos predefinida.|
    |**Permitir escritura**|Establece el objeto para usar la base de datos primaria, lo que permite al usuario modificar datos.|
    |**Solo lectura**|Establece el objeto para usar la réplica de la base de datos, lo que significa que el usuario solo puede ver datos, no cambiarlos.|

2. Seleccione la acción **Editar lista**.

3. En la página **Editar - Lista de intenciones de acceso a la base de datos**, cambie el campo **Intento de acceso** para los objetos.

    > [!NOTE]
    > Si un objeto que es editable, como la Tarjeta del cliente, se establece en **Solo lectura**, se seguirá utilizando la base de datos principal, independientemente de la intención de acceso, lo que permitirá a los usuarios realizar cambios de forma normal.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también
[Funciones empresariales](across-business-functionality.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Introducción](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
