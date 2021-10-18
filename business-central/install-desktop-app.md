---
title: Obtener Business Central en el escritorio
description: Este artículo describe cómo obtener la aplicación Business Central en un escritorio de Windows o MACiOS.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: phone, tablet
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: babf20be3c22a3d4b7dd710e2486c59bc11351fe
ms.sourcegitcommit: 795f0298e32b4c0174aeeb9a7da64f1e5c8457d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2021
ms.locfileid: "7596652"
---
# <a name="get-business-central-desktop-app"></a>Obtener la aplicación de escritorio Business Central

Si tiene un ordenador con Windows (PC) o macOS, puede instalar una aplicación Business Central en su escritorio. 
> [!NOTE]
> Si está utilizando el lanzamiento de versiones 1 de Business Central de 2021 o anterior, obtenga la aplicación de la [Tienda de Windows](https://go.microsoft.com/fwlink/?LinkId=734848).

## <a name="why-use-the-app"></a>¿Por qué usar la aplicación?

La aplicación Business Central se parece al cliente web, pero ofrece algunos beneficios como:

- La aplicación está disponible en el menú **Inicio**, puede anclarla fácilmente a la barra de tareas o hacer que se inicie de forma predeterminada cuando inicie su ordenador.
- En general, la aplicación también es más rápida y fluida de renderizar en pantalla, sin diferencias de rendimiento en comparación con la ejecución [!INCLUDE[prod_short](includes/prod_short.md)] en el navegador.
- La aplicación se abre en su propia ventana, independientemente de las ventanas del navegador. Esta función hace que sea más fácil de encontrar cuando se ejecuta una gran cantidad de aplicaciones o pestañas del navegador.
- Si tiene más de un entorno de Business Central (solo en línea), puede instalar la aplicación por separado para cada entorno.

     Cuando abre la aplicación para un entorno específico, el nombre del entorno se incluye en el título de la ventana. Cuando se trabaja en varios entornos [!INCLUDE[prod_short](includes/prod_short.md)], cada ventana de la aplicación se muestra por separado. El nombre le facilita ver qué ventana está asociada con cada entorno.

## <a name="install-the-app"></a>Instalar la aplicación

1. Abra el cliente web [!INCLUDE[prod_short](includes/prod_short.md)] en Microsoft Edge o Google Chrome.

2. Si aparece la página para seleccionar el entorno, puede hacer una de estas dos cosas:

   - Seleccione el entorno y vaya al siguiente paso para instalar la aplicación. En este caso, la aplicación instalada abrirá el entorno que seleccione.
   - No seleccione el entorno y vaya al siguiente paso para instalar la aplicación. En este caso, la aplicación instalada abrirá la página de selección del entorno, en lugar de un entorno específico.

3. Para instalar la aplicación, dependiendo de su navegador, seleccione ![Icono para instalar una aplicación en Edge.](media/ui-edge-install-app-icon.png) **Aplicación disponible. Instalar Business Central** o ![Icono para instalar una aplicación en Chrome.](media/ui-chrome-install-app-icon.png) **Instalar Business Central** y, después, **Instalar**.

   | Microsoft Edge | Google Chrome |
   |--|--|
   | :::image type="content" source="media/ui-edge-install-app-v2.png" alt-text="Ilustración de un botón para instalar una aplicación en Edge."::: | :::image type="content" source="media/ui-chrome-install-app-v2.png" alt-text="Ilustración de un botón para instalar una aplicación en Chrome."::: |

  > [!TIP]
  > Con Edge, también puede instalar la aplicación si va al menú **Configuración y más** en el navegador y, después, seleccione **Aplicaciones** > **Instalar este sitio como una aplicación** > **Instalar**.

Una vez instalada, la aplicación aparece en el menú **Inicio**. Si ha seleccionado un entorno específico para la aplicación, el nombre del entorno se agrega al nombre de la aplicación en el menú **Inicio**.

### <a name="for-business-central-on-premises"></a>Para Business Central local

La instalación de la aplicación cuando utiliza Business Central local es básicamente la misma que se describe anteriormente. Si solo tiene un inquilino, simplemente abra Business Central en su navegador y, después, seleccione ![Icono para instalar una aplicación en Edge.](media/ui-edge-install-app-icon.png) **Aplicación disponible. Instalar Business Central** o ![Icono para instalar una aplicación en Chrome.](media/ui-chrome-install-app-icon.png) **Instalar Business Central** como se muestra arriba. 

La diferencia es cuando tiene varios inquilinos. A diferencia de [!INCLUDE[prod_short](includes/prod_short.md)] en línea, donde puede instalar la aplicación por separado para diferentes entornos, en el formato local solo puede instalar la aplicación para un inquilino. Por lo tanto, antes de instalar la aplicación cuando tenga varios inquilinos, asegúrese de cambiar al inquilino correcto. Una vez instalada, cuando abra la aplicación, abrirá directamente el inquilino.

<!-- for FAQ or troubleshooting
> [!NOTE]
> To install the app, [!INCLUDE[prod_short](includes/prod_short.md)] must be configured for HTTPS. If it isn't, you won't see ![Icon for installing an app in Edge.](media/ui-edge-install-app-icon.png) **App available. Install Business Central** or ![Icon for installing an app in Chrome.](media/ui-chrome-install-app-icon.png) **Install Business Central** in the browser. If you're having problems, contact your administrator or see [Configuring SSL to Secure the Business Central Web Client Connection](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection) about how to configure HTTPS.
-->

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[P+F sobre aplicaciones móviles](ui-mobile-faq.yml)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]