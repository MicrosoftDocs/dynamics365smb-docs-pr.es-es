---
title: Administrar la intención de acceso a la base de datos en Business Central
description: Cambie la intención de acceso a la base de datos para informes, páginas API y consultas.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9880
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 15300f780cbe92a1f5e288979a1c84f34f63cb1a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532436"
---
# <a name="managing-database-access-intent"></a>Gestionar la intención de acceso a la base de datos

Como superusuario o administrador, puede cambiar la intención de acceso a la base de datos en informes, páginas de tipo API y consultas para mejorar el rendimiento del servicio.

## <a name="overview"></a>Panorama

[!INCLUDE[prod_short](includes/prod_short.md)] se puede configurar para usar réplicas de solo lectura de la base de datos primaria (lectura-escritura). El uso de la réplica de la base de datos reduce la carga en la base de datos primaria. En algunos casos, también mejorará el rendimiento al visualizar datos en el cliente. Las réplicas son beneficiosas para los objetos, como informes, consultas y páginas API, que se usan para ver solo datos, no para modificar datos.

Cuando se ejecutan los objetos, la intención de acceso a la base de datos determina si se usa una réplica de solo lectura, si hay una disponible, o la base de datos primaria. Los informes, las páginas API y las consultas se desarrollan con una intención de acceso a la base de datos predefinida (consulte [Propiedad DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

La página **Lista de intenciones de acceso a la base de datos** permite anular la intención de acceso a la base de datos predefinida para los objetos cuando se ejecutan.

En términos de base de datos, esta característica se conoce comúnmente como *escalado de lectura*. Para obtener más información sobre el escalado de lectura y la intención de acceso a datos en [!INCLUDE[prod_short](includes/prod_short.md)], vea [Utilizar el escalado de lectura para un mejor rendimiento](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) en la ayuda para desarrolladores y administración de [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-change-the-database-access-intent"></a>Para cambiar la intención de acceso a la base de datos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Lista de intenciones de acceso a la base de datos** y luego elija el enlace relacionado.

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

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/deploy-configure-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también
[Funciones empresariales](across-business-functionality.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
