---
title: Obtener Business Central en el escritorio
description: Este artículo describe cómo obtener la aplicación Business Central en un escritorio de Windows o MACiOS.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'phone, tablet'
ms.date: 01/11/2022
ms.author: jswymer
---
# <a name="get-business-central-desktop-app"></a><a name="get-business-central-desktop-app"></a>Obtener la aplicación de escritorio Business Central

Si tiene un ordenador con Windows (PC) o macOS, puede instalar una aplicación Business Central en su escritorio. La aplicación funciona con Business Central Online y localmente.

## <a name="why-use-the-app"></a><a name="why-use-the-app"></a>¿Por qué usar la aplicación?

La aplicación Business Central se parece al cliente web, pero ofrece algunos beneficios como:

- La aplicación está disponible en el menú **Inicio**, puede anclarla fácilmente a la barra de tareas o hacer que se inicie de forma predeterminada cuando inicie su ordenador.
- En general, la aplicación también es más rápida y fluida de renderizar en pantalla, sin diferencias de rendimiento en comparación con la ejecución [!INCLUDE[prod_short](includes/prod_short.md)] en el navegador.
- La aplicación se abre en su propia ventana, independientemente de las ventanas del navegador. Esta función hace que sea más fácil de encontrar cuando se ejecuta una gran cantidad de aplicaciones o pestañas del navegador.
- Si existe más de un entorno de Business Central (solo en línea), puede instalar la aplicación por separado para cada entorno.

     Cuando abre la aplicación para un entorno específico, el nombre del entorno se incluye en el título de la ventana. Cuando se trabaja en varios entornos [!INCLUDE[prod_short](includes/prod_short.md)], cada ventana de la aplicación se muestra por separado. El nombre le facilita ver qué ventana está asociada con cada entorno.

## <a name="install-the-app-for-business-central-online"></a><a name="install-the-app-for-business-central-online"></a>Instalar la aplicación para Business Central Online

Hay dos formas de instalar la aplicación para Business Central Online. Puedes instalarla directamente desde el navegador o desde Microsoft Store. Cualquiera que sea el enfoque que utilice, es la misma aplicación. La diferencia es que la instalación desde el navegador le permite instalar la aplicación para cada entorno cuando hay más de uno.

### <a name="from-microsoft-store"></a><a name="from-microsoft-store"></a>Desde Microsoft Store

1. Vaya a [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=2182870).
2. Escoja **Obtener** > **Instalar**. 
3. Cuando la aplicación se haya instalado, seleccione **Abrir** y luego inicie sesión en Business Central.

La próxima vez que quiera abrir la aplicación, búsquela en el menú **Inicio**.

### <a name="from-the-browser"></a><a name="from-the-browser"></a>Desde el navegador

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

## <a name="install-the-app-for-business-central-on-premises"></a><a name="install-the-app-for-business-central-on-premises"></a>Instalar la aplicación para Business Central de forma local

La instalación de la aplicación de escritorio cuando utiliza Business Central local se realiza directamente desde el navegador según se [describió anteriormente](#from-the-browser). Si solo tiene un inquilino, simplemente abra Business Central en su navegador y, después, seleccione ![Icono para instalar una aplicación en Edge.](media/ui-edge-install-app-icon.png) **Aplicación disponible. Instalar Business Central** o ![Icono para instalar una aplicación en Chrome.](media/ui-chrome-install-app-icon.png) **Instalar Business Central** como se muestra arriba.

La diferencia es cuando tiene varios inquilinos. A diferencia de [!INCLUDE[prod_short](includes/prod_short.md)] en línea, donde puede instalar la aplicación por separado para diferentes entornos, solo puede instalar la aplicación para un inquilino. Por lo tanto, antes de instalar la aplicación cuando tenga varios suscriptores, asegúrese de cambiar al suscriptor correcto. Una vez instalada, cuando abra la aplicación, abrirá directamente el inquilino.

> [!IMPORTANT]
> Si está utilizando el primer lanzamiento de versiones de Business Central 2021 (versión 18) o anterior, no puede instalar la aplicación como se describe en este artículo. En su lugar, instale la aplicación desde [Microsoft Store](https://go.microsoft.com/fwlink/?LinkId=734848). Para obtener más información y ayuda sobre la instalación de esta aplicación heredada, consulte [Preparación e instalación de la aplicación Business Central](/dynamics365/business-central/dev-itpro/deployment/install-business-central-app).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/alternative-interfaces-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[P+F sobre aplicaciones móviles](ui-mobile-faq.yml)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
