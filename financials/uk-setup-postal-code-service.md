---
title: "Configurar la extensión Códigos postales de Reino Unido de GetAddress.io | Documentos de Microsoft"
description: "Describe cómo instalar y configurar el servicio de códigos postales para importar direcciones del Reino Unido"
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 29b3b551e3ea8e8dfd52a3846332eec47f9346ce
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="set-up-the-getaddressio-uk-postcodes-extension"></a>Configurar la extensión Códigos postales de Reino Unido de GetAddress.io
Esta extensión facilita la introducción de direcciones del Reino Unido de entidades como clientes, contactos, empleados, proveedores, bancos, etc. 

La extensión Códigos postales de Reino Unido de GetAddress.io utiliza la API de getAddress para buscar direcciones en códigos postales en el Reino Unido. Para usar la extensión, deberá obtener un plan y una clave para la API de getAddress. Es fácil y le ayudamos a hacerlo cuando configure la extensión Códigos postales de Reino Unido de GetAddress.io. Los planes se basan en el uso, o lo que a veces se denominan llamadas. Una llamada, en este caso, se produce cuando [!INCLUDE[d365fin](includes/d365fin_md.md)] muestra una lista de direcciones de un código postal. Dependiendo de la frecuencia con que agregue direcciones, seleccione el plan que le resulte más adecuado. Si solo elige **Obtener clave de API** en la página, utilizará el plan **Gratuitos**, que permite añadir 20 direcciones al día y es válido durante 30 días. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Para configurar la extensión Códigos postales de Reino Unido de GetAddress.io 
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Conexiones de servicio** y elija el vínculo relacionado.  
2. En la ventana **Conexiones de servicio**, elija **Servicio de códigos postales de Reino Unido**.
3. En la página **Configuración de proveedor de códigos postales**, elija **Desactivado**.
4. En la ventana **Selección de servicio de código postal**, elija **GetAddress.io**.
5. En la ventana **Configuración de GetAddress.io**, elija **Obtener clave de API** para abrir la página **Planes** en el sitio web de la API de getAddress.  

    **Nota**: Puede que sea necesario permitir las ventanas emergentes en el explorador.
6. Compre un plan, o elija **Obtener clave de API** y proporcione la dirección de correo electrónico.
7. Abra el correo electrónico de getAddress.io y copie la clave de API. La clave se encuentra en el encabezado **Su clave de API**.
8. En la ventana **Configuración de GetAddress.io**, pegue la clave de API en el campo **Clave de API** y, a continuación, elija **Aceptar**.
9. En la página **Conexiones de servicio**, compruebe que el campo **Proveedor de direcciones** muestra **GetAddress.io**. Si es así, el servicio está habilitado.

## <a name="see-also"></a>Consulte también
[Códigos postales de Reino Unido de GetAddress.io](ui-extensions-getaddressio.md) [Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante extensiones](ui-extensions.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)
