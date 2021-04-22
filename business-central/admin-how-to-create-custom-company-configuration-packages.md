---
title: Crear paquetes de configuración de empresa personalizados | Documentos de Microsoft
description: A medida que crece su empresa, probablemente confiará en un conjunto de tipos de empresa que utiliza con la mayor parte de los clientes. Puede simplificar el proceso de implementación al convertir estos tipos habituales en paquetes de configuración de empresa disponibles para volver a usarlas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e6781b01a80acfd3431fc000069dd2c8b96dffc5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779912"
---
# <a name="create-custom-company-configuration-packages"></a>Crear paquetes de configuración de empresa personalizados
A medida que crece su empresa, probablemente confiará en un conjunto de tipos de empresa que utiliza con la mayor parte de los clientes. Puede simplificar el proceso de implementación al convertir estos tipos habituales en paquetes de configuración de empresa disponibles para volver a usarlas.  

En general, debería crear un paquete de configuración por área funcional; por ejemplo, cree un paquete la funcionalidad de fabricación. Esto le permite aplicar y configurar nuevas áreas en una empresa a medida que las necesita.  

Otro método sería crear un paquete que incluya las tablas que definen la configuración, tal como las siguientes:  

-   Configuración activos fijos  
-   Configuración de contabilidad  
-   Config. existencias  
-   Configuración de fabricación  
-   Configuración de compras y pagos  
-   Configuración de marketing  
-   Configuración del servicio  
-   Configuración de ventas y cobros  
-   Configuración de almacén  
-   Configuración grupos contables  
-   Config. grupos registro IVA  
-   Config. registro inventario  

Para ver una lista completa de tablas de configuración, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración manual** y luego elija el enlace relacionado.  

> [!IMPORTANT]
> Tenga cuidado si elige tablas o campos que tienen el mismo nombre temporal pero que se diferencian por caracteres especiales, como %, &, <, >, ( y ). Por ejemplo, la tabla "XYZ" puede contener los campos "Campo 1" y "Campo 1%".
>
> El procesador XML acepta solo algunos caracteres especiales y eliminará los que no. Si al eliminar un carácter especial, como el signo % en el "Campo 1%", se obtienen dos o más tablas o campos con el mismo nombre, se producirá un error al exportar o importar un paquete de configuración.

## <a name="to-create-a-custom-company-configuration-package"></a>Crear un paquete de configuración de empresa personalizado  
1.  Cree una nueva empresa. Para obtener más información, consulte [Crear nuevas empresas en Business Central](about-new-company.md).  
3.  Configure la nueva empresa del modo que necesite. Rellene todas las tablas de configuración necesarias.  
4.  Abra la nueva empresa.
5. Abre la página **Hoja de configuración**.  
6.  Agregue a la hoja de cálculo las tablas que desee transferir a otra empresa. Asigne las líneas de la hoja de trabajo al paquete.  
7.  Cree un cuestionario para las tablas de configuración que se usan con mayor frecuencia.  
8.  Cree plantillas de configuración para facilitar la creación de datos maestros, tales como clientes o productos.  
9.  Exporte el paquete como un archivo .rapidstart.  

## <a name="see-also"></a>Consulte también  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]