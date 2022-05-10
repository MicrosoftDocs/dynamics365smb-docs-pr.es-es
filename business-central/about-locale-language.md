---
title: Multilingüe y localización
description: Aprenda cómo el idioma y la configuración regional influyen en la experiencia de Business Central. Cambie el idioma de la interfaz de usuario en la página Mi configuración.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture, region, regional settings
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cdac371269e523f30712d4cb0be1087e07e70d5e
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655519"
---
# <a name="changing-language-and-region"></a>Cambiar idioma y región

[!INCLUDE[prod_short](includes/prod_short.md)] está disponible en varios mercados e idiomas en todo el mundo. En los mercados donde [!INCLUDE[prod_short](includes/prod_short.md)] está disponible, hay características regulatorias disponibles para ayudar a las empresas con los trámites regulatorios. [!INCLUDE[prod_short](includes/prod_short.md)] se puede mostrar en diferentes idiomas. Incluso puede cambiar el idioma que se utiliza para mostrar los textos. El cambio es inmediato en cuanto haya cerrado e iniciado la sesión de nuevo. Los ajustes se aplican a usted y no a todos los usuarios en la empresa.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Por ejemplo, está utilizando la versión canadiense de [!INCLUDE[prod_short](includes/prod_short.md)]. Eso significa que puede ver la interfaz de usuario en inglés, alemán, francés u otro idioma, pero sigue siendo la versión canadiense de [!INCLUDE[prod_short](includes/prod_short.md)]. No es lo mismo que [!INCLUDE[prod_short](includes/prod_short.md)] en Alemania, donde la funcionalidad se ha adaptado a los requisitos de ese mercado.  

Para cambiar el idioma de la interfaz de usuario, vaya a la página **Mi configuración**. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md#language). 

> [!NOTE]  
> La elección de idiomas se restablecerá a su configuración en su perfil de Microsoft 365 si su administrador sincroniza usuarios de Microsoft 365 a [!INCLUDE[prod_short](includes/prod_short.md)].

No puede cambiar los textos que se almacenan como datos de la aplicación. Algunos ejemplos de textos son los nombres de los productos de las existencias o los comentarios para un cliente. Es decir, estos tipos de texto no se traducen.  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] sólo admite un juego de caracteres únicos para los datos. Por lo tanto, es posible que la suscripción no admita algunos caracteres en su entorno y que surjan problemas a la hora de recuperar datos introducidos con un juego de caracteres diferente. Por ejemplo, su entorno puede utilizar solo caracteres ingleses y rusos. En este caso, si introduce datos en otro idioma, es posible que no se guarden correctamente. Póngase en contacto con el administrador del sistema para asegurarse de conocer los idiomas compatibles con su [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="changing-your-region-setting"></a>Cambiar la configuración de su región

La configuración regional es distinta del idioma y los requisitos legales en mercados local. La región determina cómo la información se muestra en términos de separador de comas y cómo el texto se alinea a la izquierda o a la derecha. La región también determinará algunos de los productos del sistema en el explorador, como la acción para crear un producto nuevo en una lista.  

Puede cambiar configuración regional de la pestaña del explorador que utiliza para trabajar [!INCLUDE[prod_short](includes/prod_short.md)]. El cambio solo se aplica a usted y no a los demás usuarios en la empresa.  La elección de región se restablecerá a su configuración en su perfil de Microsoft 365 si su administrador sincroniza usuarios de Microsoft 365 en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]  
> Cuando modifica la configuración regional, aparecerá una lista de larga idiomas de y regiones. Sin embargo, el idioma no está influenciado por la elección de la región.  

Para cambiar configuración regional, vaya a la página **Mi configuración**. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).  

## <a name="changing-the-region-setting-for-customers-contacts-and-vendors"></a>Cambiar la configuración de región para clientes, contactos y proveedores

Algunas empresas utilizan un servicio externo que valida la información de dirección en su país o región. Sin embargo, cuando necesita actualizar la información de dirección, es posible que el enfoque estructurado que utilizan estos servicios no siempre sea el adecuado para algunos escenarios. Business Central ofrece un medio más flexible para ingresar los detalles de la dirección.

En la página **Configuración de contabilidad**, si activa el botón de alternancia **Requerir el código de país o región en la dirección**, los cambios en el campo **Código de país/región** en direcciones para clientes, contactos o proveedores restablecerán los valores en otros campos de dirección.

## <a name="application-version"></a>Versión de la aplicación

En la página **Ayuda y soporte técnico** puede ver la versión de que [!INCLUDE[prod_short](includes/prod_short.md)] en la que se basa su empresa. Si desea basar una empresa en una versión diferente, su administrador puede crear un nuevo entorno de producción. Para obtener más información, vea [Crear un nuevo entorno de producción](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) en el contenido para desarrolladores y profesionales de TI.  

## <a name="languages-of-the-prod_short-help"></a>Idiomas de la Ayuda de [!INCLUDE[prod_short](includes/prod_short.md)]

El contenido de la Ayuda para la versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)] se publica en el sitio de Microsoft Docs. El contenido está disponible en diferentes idiomas. Si tiene acceso a documentos desde [!INCLUDE[prod_short](includes/prod_short.md)], el contenido se mostrará en su idioma. De forma predeterminada, si una página en particular aún no está disponible en su idioma, se mostrarán en inglés.

### <a name="how-do-i-change-the-language-of-the-microsoft-docs-site"></a>¿Cómo cambio el idioma del sitio de Microsoft Docs?

Es simple, desplácese al final de la página del explorador y elija el símbolo del mundo en la esquina inferior izquierda.

> [!NOTE]  
> La lista muestra todos los idiomas admitidos en el sitio de Documentos de Microsoft. [!INCLUDE[prod_short](includes/prod_short.md)] está disponible en un número limitado de países o regiones, y el contenido de Ayuda de [!INCLUDE [prod_short](includes/prod_short.md)] no está disponible en todos los idiomas que admite el sitio de Microsoft Docs.

## <a name="see-also"></a>Consulte también

[Recursos de ayuda y soporte técnico](product-help-and-support.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]