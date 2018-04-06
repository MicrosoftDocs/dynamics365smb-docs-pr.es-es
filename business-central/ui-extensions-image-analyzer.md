---
title: "Uso de la extensión del analizador de imágenes | Documentos de Microsoft"
description: "Estas extensiones le permiten analizar imágenes de personas de contacto y elementos para encontrar atributos, para que pueda asignarlos rápidamente en Business Central."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e075aedde1bd52a6b852fd92e419aca11367b742
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---

# <a name="the-image-analyzer-extension-for-microsoft-business-central"></a>Extensión del analizador de imágenes de Microsoft Business Central
La extensión del analizador de imagen utiliza análisis de imagen muy potentes proporcionados por la API de Computer Vision de Microsoft Cognitive Services para detectar los atributos de las imágenes que se importan para los elementos y las personas de contacto, de modo que pueda revisarlos y asignarlos fácilmente. Para los elementos, los atributos podrían ser si el elemento es una tabla o un automóvil, y si es rojo o azul. Para las personas de contacto, los atributos podrían ser el género o edad.

El analizador sugiere atributos basados en etiquetas que encuentra la API de Computer Vision y un nivel de confianza. De forma predeterminada, sugiere atributos solo si está seguro en al menos un 80 % que el atributo es correcto. Si es necesario, puede establecer otro nivel de confianza. Para obtener más información acerca de cómo se determinan las etiquetas y el nivel de confianza, consulte el [API de Computer Vision](https://go.microsoft.com/fwlink/?linkid=851476).  

El analizador está disponible en [!INCLUDE[d365fin](includes/d365fin_md.md)], pero hay un límite en el número de elementos que puede analizar durante un cierto período de tiempo. De forma predeterminada, puede analizar 100 imágenes por mes.

Después de habilitar la extensión, el analizador se ejecuta cada vez que importa una imagen a un elemento o persona de contacto. Verá los atributos, el nivel de confianza y los detalles de inmediato y podrá decidir qué hacer con cada atributo. Si ha importado imágenes antes de activar la extensión del analizador de imágenes, debe ir al elemento o a las tarjetas de contacto y seleccionar la acción **Analizar imagen**.  

>   [!NOTE]  
>   Al habilitar esta extensión, acepta que Microsoft pueda almacenar sus datos y utilizarlos para mejorar sus servicios, como por ejemplo, mejorar la API de Computer Vision. Para ayudar a proteger la privacidad, tomamos medidas para mantener el anonimato de los datos y mantenerlos seguros. No publicaremos sus datos dejamos ni permitiremos que otras personas los usen. Puede eliminar la imagen del elemento en [!INCLUDE[d365fin](includes/d365fin_md.md)], sin embargo, la API de Computer Vision aún tendrá la imagen de forma identificada. Para obtener más información, consulte [Centro de confianza de Microsoft](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Requisitos
Hay algunos requisitos para las imágenes:

* Formatos de imagen: JPEG, PNG, GIF, BMP  
* Tamaño del archivo máximo: menos de 4 MB  
* Dimensiones de la imagen: mayor de 50 x 50 píxeles  

## <a name="blacklisting-suggested-attributes"></a>Listas negras de atributos sugeridos
Si el análisis sugiere un atributo que no desea ver, puede añadirlo a una lista negra. Sin embargo, preste atención. Los atributos de la lista negra ya no aparecerán más para otros artículos ni personas de contacto. Si desea eliminar un atributo de la lista negra, puede elegir **Atributos de la lista negra** y, a continuación, eliminarlo.

## <a name="to-enable-image-analyzer"></a>Activar el analizador de imágenes
La extensión del analizador de imágenes viene incorporada en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Solo necesita activarla.

> [!NOTE]  
> Para activar la extensión del analizador de imágenes, debe ser administrador. Asegúrese de que se le ha asignado el conjunto de permisos de usuario **SUPER**.

1. Para activar la extensión del analizador de imágenes, elija una de estas acciones:

* Abrir un elemento o tarjeta de contacto. En la barra de notificación, elija **Analizar imágenes**y, a continuación, siga los pasos de la guía de configuración asistida.  
* Seleccione el ícono ![Buscar página o informe](media/ui-search/search_small.png "Buscar página o informe"), introduzca **Conexiones servicio** y, a continuación, seleccione **Configuración de análisis de imagen**. Seleccione la casilla **Activar analizador de imágenes**y, a continuación, complete los pasos de la guía de configuración asistida.  

>   [!TIP]  
>   La página **Configuración del análisis de imágenes** también permite cambiar el grado de confianza de las sugerencias de atributos. Por ejemplo, si desea exigir un mayor grado de confianza, puede introducir un porcentaje más alto.

## <a name="to-analyze-an-image-of-an-item"></a>Analizar una imagen de un producto
Los siguientes pasos describen cómo analizar una imagen que se importó antes de activar la extensión del analizador.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el producto y, a continuación, elija la acción **Analizar imagen**.  
3. La página **Atributos del analizador de imágenes** muestra los atributos detectados, el nivel de confianza y otros detalles sobre el atributo. Utilice las opciones **Acción para realizar** para especificar qué debe hacer con el atributo.  

>   [!TIP]  
>   Puede agregar el nombre del atributo a la descripción del artículo mediante **Añadir a la descripción del artículo**. Por ejemplo, esto puede ser útil para agregar rápidamente detalles.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Analizar una imagen de una persona de contacto
Los siguientes pasos describen cómo analizar una imagen que se importó antes de activar la extensión del analizador.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contactos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la persona de contacto y, a continuación, elija la acción **Analizar imagen**.  
3. En la ficha desplegable **Cuestionario perfil**, revise las sugerencias y realice correcciones si es necesario.  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Usar su propia cuenta para la API de Computer Vision
También puede utilizar su propia cuenta para la API de Computer Vision, por ejemplo, si desea analizar más imágenes de las que permitimos.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración analizador de imágenes** y, a continuación, seleccione el vínculo relacionado.  
2. Ingrese el **API de URI** y la **Clave de API** que recibió para la API de Computer Vision.  

>   [!NOTE]  
>   Si no está escrito, debe agregar **/analyze** al final de la API de URI. Por ejemplo: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Ver cuántos análisis ha dejado en el período actual
Puede ver el número de análisis que ha realizado y cuántos pueden hacerse en el período actual.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración analizador de imágenes** y, a continuación, seleccione el vínculo relacionado.  
2. El **Tipo límite**, el **Valor límite** y los **Análisis realizados** proporcionan la información de uso.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Detener el uso de la extensión del analizador de imágenes
1. Seleccione el ícono ![Buscar página o informe](media/ui-search/search_small.png "Buscar página o informe"), introduzca **Conexiones servicio** y, a continuación, seleccione **Configuración del analizador de imágenes**.  
2. Desactive la casilla **Activar analizador de imágenes**.  

## <a name="see-also"></a>Consulte también
[Trabajar con atributos de producto](inventory-how-work-item-attributes.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

