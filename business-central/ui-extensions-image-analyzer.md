---
title: Extensión del analizador de imágenes
description: Estas extensiones le permiten analizar imágenes de personas de contacto y elementos para encontrar atributos, para que pueda asignarlos rápidamente en Business Central.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: bbeffd4175751e08043d79f596027a79c88503bc
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074617"
---
# <a name="the-image-analyzer-extension"></a>Extensión del analizador de imágenes

La extensión del analizador de imagen utiliza análisis de imagen muy potentes proporcionados por la API de Computer Vision de Azure Cognitive Services para detectar los atributos de las imágenes que se importan para los elementos y las personas de contacto, de modo que pueda revisarlos y asignarlos fácilmente. Para los elementos, los atributos podrían ser si el elemento es una tabla o un automóvil, y si es rojo o azul. Para las personas de contacto, los atributos podrían ser el género o edad.

El analizador sugiere atributos basados en etiquetas que encuentra la API de Computer Vision y un nivel de confianza. De forma predeterminada, sugiere atributos solo si está seguro en al menos un 80 % que el atributo es correcto. Si es necesario, puede establecer otro nivel de confianza. Para obtener más información acerca de cómo se determinan las etiquetas y el nivel de confianza, consulte el [API de Computer Vision](https://go.microsoft.com/fwlink/?linkid=851476).  

El analizador está disponible en [!INCLUDE[prod_short](includes/prod_short.md)], pero hay un límite en el número de elementos que puede analizar durante un cierto período de tiempo. De forma predeterminada, puede analizar 100 imágenes por mes.

Después de habilitar la extensión, el analizador se ejecuta cada vez que importa una imagen a un elemento o persona de contacto. Verá los atributos, el nivel de confianza y los detalles de inmediato y podrá decidir qué hacer con cada atributo. Si ha importado imágenes antes de activar la extensión del analizador de imágenes, debe ir al elemento o a las tarjetas de contacto y seleccionar la acción **Analizar imagen**.  

## <a name="privacy-notice"></a>Aviso de privacidad

Esta extensión utiliza la API de Computer Vision de Azure Cognitive Services, que puede tener diferentes niveles de compromisos de cumplimiento que [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando habilita la extensión del analizador de imágenes, los datos del cliente, como una imagen de contacto o una imagen de un producto, se enviarán a la API de Computer Vision. Al instalar esta extensión, acepta que este conjunto limitado de datos se envíe a la API de Computer Vision. Tenga en cuenta que puede desactivar, así como desinstalar, la extensión del analizador de imágenes en cualquier momento para interrumpir el uso de esta funcionalidad. Para obtener más información, consulte [Centro de confianza de Microsoft](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Requisitos

Hay algunos requisitos para las imágenes:

* Formatos de imagen: JPEG, PNG, GIF, BMP  
* Tamaño del archivo máximo: menos de 4 MB  
* Dimensiones de la imagen: mayor de 50 x 50 píxeles  

## <a name="to-enable-image-analyzer"></a>Activar el analizador de imágenes

La extensión del analizador de imágenes viene incorporada en [!INCLUDE[prod_short](includes/prod_short.md)]. Solo necesita activarla.

> [!NOTE]  
> Para activar la extensión del analizador de imágenes, debe ser administrador. Asegúrese de que se le ha asignado el conjunto de permisos de usuario **SUPER**. Para obtener más información, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

Para activar la extensión del analizador de imágenes, lleve a cabo una de estas acciones:

* Abrir un elemento o tarjeta de contacto. En la barra de notificación, elija **Analizar imágenes** y, a continuación, siga los pasos de la guía de configuración asistida.  
* Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conexiones de servicio** y luego elija **Configuración del análisis de imagen**. Seleccione la casilla **Activar analizador de imágenes** y, a continuación, complete los pasos de la guía de configuración asistida.  

    > [!TIP]  
    > La página **Configuración del análisis de imágenes** también permite cambiar el grado de confianza de las sugerencias de atributos. Por ejemplo, si desea exigir un mayor grado de confianza, puede introducir un porcentaje más alto.

## <a name="to-analyze-an-image-of-an-item"></a>Analizar una imagen de un producto

Los siguientes pasos describen cómo analizar una imagen que se importó antes de activar la extensión del analizador.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2. Seleccione el producto y, a continuación, elija la acción **Analizar imagen**.  
3. La página **Atributos del analizador de imágenes** muestra los atributos detectados, el nivel de confianza y otros detalles sobre el atributo. Utilice las opciones **Acción para realizar** para especificar qué hacer con el atributo o elija **Agregar a la descripción del producto** para agregar el nombre del atributo a la descripción del producto. Por ejemplo, esto puede ser útil para agregar rápidamente detalles. 

La acción **Acción para realizar** tiene las siguientes opciones:

  * *Ignorar*

    No se realizarán acciones
  * *Usar como atributo*

    El valor se agrega a los atributos del producto. Para obtener más información sobre cómo trabajar con el formulario, consulte [Trabajar con atributos de producto](inventory-how-work-item-attributes.md)
  * *Usar como categoría*

    El valor seleccionado se agrega como una categoría. Para obtener más información, consulte [Clasificar productos](inventory-how-categorize-items.md)
  * *Agregar a la lista negra*

    Si el análisis sugiere un atributo que no desea ver, puede bloquearlo. Sin embargo, preste atención. Los atributos bloqueados ya no aparecerán más para otros productos. Si desea desbloquear un atributo, elija **Ver atributos de la lista negra** y, a continuación, eliminarlo de la lista.
  
    > [!NOTE]  
    > De forma predeterminada **Atributos del producto** muestra atributos donde la **Puntuación de confianza** está por encima del **% de umbral de puntuación de confianza** definido en el **Configuración de análisis de imagen**. Para ver todos los atributos detectados, elija la acción **Ver todos los atributos**.

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Analizar una imagen de una persona de contacto

Los siguientes pasos describen cómo analizar una imagen que se importó antes de activar la extensión del analizador.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.  
2. Seleccione la persona de contacto y, a continuación, elija la acción **Analizar imagen**.  
3. En la ficha desplegable **Cuestionario perfil**, revise las sugerencias y realice correcciones si es necesario. Para obtener más información, consulte [Utilizar cuestionarios de perfil para clasificar contactos comerciales](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    > 
    > La API de Computer Vision devuelve los siguientes atributos:
    > * *edad*
    >
    >     Una "edad visual" estimada en años. Es la edad de una persona en comparación con la edad biológica real.
    > * *sexo*
    >
    >    Mujer o varón.
    > 
    > La API de Computer Vision no devuelve el nivel de confianza para los atributos de edad y género.
  
## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Usar su propia cuenta para la API de Computer Vision

También puede utilizar su propia cuenta para la API de Computer Vision, por ejemplo, si desea analizar más imágenes de las que permitimos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de análisis de imagen** y luego elija el enlace relacionado.  
2. Ingrese el **API de URI** y la **Clave de API** que recibió para la API de Computer Vision.  

    > [!NOTE]  
    > Si no está escrito, debe agregar **/analyze** al final de la API de URI. Por ejemplo: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Ver cuántos análisis ha dejado en el período actual

Puede ver el número de análisis que ha realizado y cuántos pueden hacerse en el período actual.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de análisis de imagen** y luego elija el enlace relacionado.  
2. El **Tipo límite**, el **Valor límite** y los **Análisis realizados** proporcionan la información de uso.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Detener el uso de la extensión del analizador de imágenes

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conexiones de servicio** y luego elija **Configuración del analizador de imágenes**.  
2. Desactive la casilla **Activar analizador de imágenes**.  

Opcionalmente, desinstale la extensión por completo. Siempre puede volver a recuperarla en AppSource. Para obtener más información, consulte [Instalación y desinstalación de extensiones en Business Central](ui-extensions-install-uninstall.md#uninstalling-an-extension).  

## <a name="see-also"></a>Consulte también

[Trabajar con atributos de producto](inventory-how-work-item-attributes.md)  
[Clasificar productos](inventory-how-categorize-items.md)  
[Use cuestionarios de perfil para clasificar contactos comerciales](marketing-create-contact-profile-questionnaire.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
