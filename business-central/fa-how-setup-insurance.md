---
title: Configure el seguro de los activos fijos
description: Configure una ficha de seguridad y la información de póliza de seguro general para administrar la cobertura del seguro de los activos fijos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'policy, coverage'
ms.search.form: '5607, 5648, 5644, 5651'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Configure el seguro de los activos fijos

Para gestionar la cobertura del seguro de los activos fijos, debe configurar la información general de los seguros y una ficha de seguro por cada póliza.

## Para configurar la información general de seguros

Para poder utilizar las características de seguro en [!INCLUDE[prod_short](includes/prod_short.md)], debe configurar antes alguna información general de seguro.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuraciones A/F** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Para configurar tipos de seguros

Puede agrupar las pólizas de seguros en categorías, como seguro contra robo o contra incendios. Los tipos de seguros se utilizan en la ficha de seguro.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tipos seguros** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## Para configurar fichas de seguros

Puede acumular información acerca de cada póliza de seguros en la ficha de seguro.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguro** y luego elija el enlace relacionado.  
2. En la página **Seguro**, seleccione la acción **Nuevo** para crear una ficha de seguro nueva.  
3. Rellene los campos según sea necesario.

## Para configurar libros diarios de seguros

[!INCLUDE[prod_short](includes/prod_short.md)] crea automáticamente un libro de diario de seguros la primera vez que abra la página **Diario seguros**, pero puede configurar libros de diario adicionales. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros diario seguros**, y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## Para configurar secciones del diario de seguros

En un libro del diario de seguros puede configurar secciones. Los valores de la sección del diario se utilizan como valores predeterminados si no se rellenan los campos de las líneas de diario. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md)  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros diario seguros**, y luego elija el enlace relacionado.  
2. Seleccione una plantilla de diario de seguros y, a continuación, selecciona la acción **Secciones**.
3. En la página **Secciones diario seguros**, rellene los campos según sea necesario.

> [!NOTE]  
>   Los números tienen una función especial en los nombres de diario. Si un nombre de libro diario o un nombre de sección del diario contiene un número, el número aumenta automáticamente en uno cada vez que se registra el diario. Por ejemplo, si se escribe HH1 en el campo **Nombre**, el nombre del diario cambiará a HH2 después de registrar el diario llamado HH1.

## Consulte también .

[Configuración de activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
