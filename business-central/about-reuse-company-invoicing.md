---
title: Uso de Invoicing y Business Central | Documentos de Microsoft
description: Solución para tener acceso a Microsoft Invoicing cuando se ha registrado en Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: b04da7a7fa6d831646c6af9f0606afa90dc00bd6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188857"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a>Con la misma cuenta de Office 365 en [!INCLUDE[d365fin](includes/d365fin_long_md.md)] y Microsoft Invoicing
Cuando se registra en una prueba en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede cambiar a una fase de evaluación de 30 días, puede empezar una suscripción o bien puede dejar de usar [!INCLUDE[d365fin](includes/d365fin_md.md)]. En todos los casos, si inicia sesión en el portal de Office, es posible que vea un mosaico llamado **Microsoft Invoicing** y que haga clic en él. Forma parte de la suscripción de Office 365, por lo que no todos los usuarios verán ese mosaico en el portal de Office.  

Si obtiene acceso a Microsoft Invoicing, verá un mensaje que le indica que no puede tener acceso a Microsoft Invoicing porque la cuenta se utiliza en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Se muestra un mensaje similar si instala la aplicación móvil de Invoicing.  

## <a name="workaround"></a>Solución
Invoicing y [!INCLUDE[d365fin](includes/d365fin_md.md)] tienen una plataforma compartida. Esto significa que se le reconoce como un usuario existente de [!INCLUDE[d365fin](includes/d365fin_md.md)] al hacer clic en Invoicing en el portal de Office. La razón es que Invoicing no puede utilizar la misma empresa que [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Por lo tanto, tendrá que iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] y cambiar el nombre de su empresa existente, y después crear una empresa nueva que pueda utilizarse en Invoicing. No se mueven ni sobrescriben datos durante esta solución.

### <a name="to-rename-your-company"></a>Para cambiar el nombre de su empresa
1. Inicie sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. En la esquina superior derecha, elija el icono **Configuración** ![Configuración](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") y, a continuación, elija **Mi configuración**.
3. En el campo **Empresa**, seleccione una empresa diferente.
4. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empresas** y luego elija el enlace relacionado.  
5. En la página **Empresas**, seleccione **Editar lista**.  
6. Cambiar el nombre de la entrada *Mi empresa* por otro distinto.  

    Espere unos minutos. Realizaremos varios cambios en la base de datos subyacente y este proceso suele llevar un tiempo.
7.  Cuando el sistema está preparado de nuevo, elija el botón **Crear nueva empresa**.  
8.  En el cuadro de diálogo que aparece, especifique el nombre como *Mi empresa* y elija la opción **Producción - Solo datos de configuración**.  

Esto tarda de nuevo varios minutos. Cuando se complete el proceso, podrá obtener acceso a Invoicing como parte de la experiencia de Office 365 Business Premium.  

### <a name="what-about-my-data"></a>¿Qué sucede con mis datos?
Al cambiar el nombre Mi empresa original, se cambia el nombre de las tablas de base de datos que almacenan los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] existentes, pero no se modifican los datos.  

Si utiliza Invoicing y [!INCLUDE[d365fin](includes/d365fin_md.md)], los datos se almacenan en los dos contenedores diferentes (las dos empresas). No se comparte nada, por lo que tendrá que gestionar los clientes y los productos en ambas empresas.  

## <a name="see-also"></a>Consulte también
[Preguntas más frecuentes](across-faq.md)  
[Administración](admin-setup-and-administration.md)  
