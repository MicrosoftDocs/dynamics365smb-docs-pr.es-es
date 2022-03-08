---
title: Multilingüe y localización | Documentos de Microsoft
description: Aprende cómo el idioma y la configuración regional influyen en la experiencia de Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2d98f433acbe5905d9807bf7e7ded8708ed22d3b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189026"
---
# <a name="changing-language-and-locale"></a>Cambiar idioma y región

[!INCLUDE[d365fin](includes/d365fin_md.md)] se admite varios en mercados y está disponible en los idiomas compatibles con aquellos mercados. Este es el resultado de asistencia para varios idiomas en el tiempo de ejecución en combinación con el soporte para los requisitos legales de los mercados admitidos. Esto significa que [!INCLUDE[d365fin](includes/d365fin_md.md)] puede presentarse en varios idiomas. Puede cambiar el idioma que se utiliza para mostrar textos, y el cambio es inmediato, una vez que haya cerrado sesión automáticamente e iniciado de nuevo. Los ajustes se aplican a usted y no a todos los usuarios en la empresa.  

Por ejemplo, si utiliza la versión canadiense de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede ver la interfaz de usuario en inglés y en francés, pero sigue siendo la versión canadiense de [!INCLUDE[d365fin](includes/d365fin_md.md)] en todos los demás aspectos. No es lo mismo que, por ejemplo, [!INCLUDE[d365fin](includes/d365fin_md.md)] en el Reino Unido.  

Para cambiar el idioma de la interfaz de usuario, vaya a la página **Mi configuración**. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md#language).  

Cambiar los textos que se almacenan como datos de la aplicación no forma parte de la capacidad multi-idioma. Es una cuestión de diseño de la aplicación. Algunos ejemplos de textos son los nombres de los productos de las existencias o los comentarios para un cliente. Es decir, estos tipos de texto no se traducen.  

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] sólo admite un juego de caracteres únicos para los datos. Por lo tanto, es posible que la suscripción no admita algunos caracteres y que surjan problemas a la hora de recuperar datos introducidos con un juego de caracteres diferente. Por ejemplo, es posible que su suscriptor sólo admita los caracteres de inglés y ruso y si introduce datos en un idioma diferente, es posible que éstos no se almacenen correctamente. Póngase en contacto con el administrador del sistema para asegurarse de conocer los idiomas compatibles con su [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="changing-the-locale"></a>Cambiar configuración regional
La configuración regional es distinta del idioma y los requisitos legales en mercados local. La región determina cómo la información se muestra en términos de separador de comas, alineación a la izquierda o a la derecha, y algunos otros valores. La región también determinará algunos de los productos del sistema en el explorador, como la acción para crear un producto nuevo en una lista, por ejemplo.  

Puede cambiar configuración regional de la pestaña del explorador que utiliza para trabajar [!INCLUDE[d365fin](includes/d365fin_md.md)]. el cambio sólo se aplica a usted y no a los demás usuarios en la empresa.  

> [!IMPORTANT]  
>  Cuando modifica la configuración regional, aparecerá una lista de larga idiomas de y regiones. Sin embargo, sólo la configuración regional se utiliza en la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Para cambiar configuración regional, vaya a la página **Mi configuración**. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).  

## <a name="application-version"></a>Versión de la aplicación

En la página **Ayuda y soporte técnico** puede ver la versión de que [!INCLUDE [prodshort](includes/prodshort.md)] en la que se basa su empresa. Si desea basar una empresa en una versión diferente, su administrador puede crear un nuevo entorno de producción. Para obtener más información, vea [Crear un nuevo entorno de producción](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) en el contenido para desarrolladores y profesionales de TI.  

## <a name="languages-of-the-d365fin-help"></a>Idiomas de la Ayuda de [!INCLUDE[d365fin](includes/d365fin_md.md)]
El contenido de la Ayuda de la funcionalidad principal de [!INCLUDE[d365fin](includes/d365fin_md.md)] se publica en el sitio de Documentos de Microsoft y está disponible en varios idiomas. Si tiene acceso a documentos desde [!INCLUDE[d365fin](includes/d365fin_md.md)], el contenido se mostrará en su idioma. Si una página en particular aún no está disponible en su idioma, se mostrarán en inglés.

### <a name="how-do-i-change-the-language"></a>¿Cómo cambio el idioma?
Es simple, desplácese al final de la página del explorador y elija el símbolo del mundo en la esquina inferior izquierda.

> [!NOTE]  
> La lista muestra todos los idiomas admitidos en el sitio de Documentos de Microsoft. [!INCLUDE[d365fin](includes/d365fin_md.md)] está disponible en un número limitado de países/regiones, pero el contenido de Ayuda está disponible en varios idiomas. Sin embargo, el contenido de Ayuda no está disponible en todos los idiomas que el sitio de Documentos de Microsoft admite.

## <a name="see-also"></a>Consulte también

[Recursos de ayuda y soporte técnico](product-help-and-support.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Introducción](product-get-started.md)  
