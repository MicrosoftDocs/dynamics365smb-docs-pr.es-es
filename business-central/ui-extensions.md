---
title: Instalar extensiones para personalizar Business Central | Documentos de Microsoft
description: Obtenga información sobre cómo agregar funcionalidad y personalizar Business Central mediante la instalación de extensiones.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765926"
---
# <a name="customizing-business-central-using-extensions"></a>Personalizar Business Central con extensiones

Puede cambiar [!INCLUDE[d365fin](includes/d365fin_md.md)] instalando extensiones que agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea, por ejemplo.

> [!NOTE]
> Para instalar extensiones desde AppSource o añadir extensiones por suscriptor, debe tener los permisos adecuados. Debe ser miembro del grupo de usuarios ADMIN EXTENSIÓN D365 o debe tener el conjunto de permisos de ADMIN EXTENSIÓN D365. Si es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa.<br /><br />
Para utilizar la funcionalidad que proporciona una extensión, como abrir páginas, ejecutar informes, seleccionar acciones, etc., se le deben asignar los conjuntos de permisos que se instalan como parte de la extensión.

> [!IMPORTANT]  
> No se admite la carga de extensiones por inquilino y la instalación de extensiones de AppSource a través de la página **Administración de extensiones** para instalaciones locales.

Cuando inicia [!INCLUDE[d365fin](includes/d365fin_md.md)] por primera vez, ya están instaladas algunas extensiones. Con el tiempo, tendrá disponibles más extensiones y puede elegir si desea usar la extensión o no.

Por ejemplo, Microsoft ofrece una extensión que proporciona integración con PayPal Payments Standard. Esta extensión se instala por omisión.
Pero si está disponible otra extensión que ofrece integración con otro servicio de pago, puede instalar la nueva extensión y seleccionar cuál de los dos servicios quiere usar.  

Puede administrar las extensiones en la página **Administración de extensiones**. Puede acceder a esta página desde Inicio. De forma alternativa, seleccione el icono **Buscar página o informe** ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") en la esquina superior derecha, escriba **Extensión** y, a continuación, seleccione el enlace relacionado. Para más información, ver [Instalación y desinstalación de extensiones](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Si cree que debería tener acceso a una extensión pero no encuentra la funcionalidad, consulte la página **Administración de extensiones**; si la extensión no aparece, puede instalarla tal como se describe en la sección siguiente.  

> [!NOTE]  
> Las nuevas extensiones no están disponibles en AppSource inmediatamente después anunciar una actualización. Puede estar atento a las extensiones en [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="see-also"></a>Consulte también

[Ampliación de Dynamics 365 Business Central](about-develop-extensions.md)  
[Extensiones de Business Central de otros proveedores](ui-extensions-other.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Permitir el pago de clientes mediante PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar la extensión Códigos postales de Reino Unido de GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensiones de otros proveedores](ui-extensions-other.md)  
[Introducción](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
