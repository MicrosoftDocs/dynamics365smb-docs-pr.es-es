---
title: Configurar Mapas en línea
description: Aprenda a configurar Business Central para ofrecer indicaciones e información de ubicación con un servicio de mapas en línea.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.form: '800, 804'
ms.date: 07/15/2022
ms.author: bholtorf
---
# <a name="set-up-online-maps"></a>Configurar Mapas en línea

Si planea realizar una visita a una dirección guardada en una tarjeta, por ejemplo a un cliente, puede conseguir un mapa en un servicio en línea con indicaciones de rutas descritas en el idioma que seleccione. Para que este servicio de mapas en línea pueda buscar las indicaciones y el mapa correctos, debe configurarlo en [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-online-map-feature"></a>Configurar la característica de mapas en línea

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración Online Map** y luego elija el enlace relacionado.
2. En la página **Configuración Online Map**, rellene los campos. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Active el botón de alternancia **Habilitado**.

### <a name="customize-the-online-map-provider-features"></a>Personalizar las funciones del proveedor de mapas en línea

Para personalizar la función de mapas en línea más allá de las opciones enumeradas en la página **Configuración Online Map** o para usar un proveedor de mapas diferente, siga estos pasos:

1. En la página **Configuración Online Map**, elija la acción **Configuración parámetros**.
2. En la página **Config. parámetros Online Map**, elija la acción **Nueva**.
3. Rellene los campos para personalizar cómo [!INCLUDE[prod_short](includes/prod_short.md)] generará las URL para los servicios disponibles. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
   * Consulte la lista **Parámetro de sustitución de Online Map** en el panel **Cuadro informativo** de los datos disponibles para generar URL.

## <a name="see-also"></a>Consulte también .

[Usar Mapas en línea para encontrar ubicaciones e indicaciones](across-online-maps.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
