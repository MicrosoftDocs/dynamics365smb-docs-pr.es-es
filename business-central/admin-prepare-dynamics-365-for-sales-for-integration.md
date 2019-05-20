---
title: Integración con Dynamics 365 for Sales| Documentos de Microsoft
description: Obtenga información sobre cómo preparar Dynamics 365 Business Central para integrarse con Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 991d8432c24b1963da019e3c8b665f9ad009d077
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247285"
---
# <a name="integrating-with-dynamics-365-for-sales"></a>Integración con Dynamics 365 for Sales
El papel de vendedor se considera a menudo uno de los trabajos más orientados hacia el exterior en una empresa. Sin embargo, puede ser útil para los vendedores poder mirar hacia adentro en la empresa y ver lo que está sucediendo en la trastienda. Mediante la integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)], puede dar a sus vendedores esa visión, permitiéndoles ver la información en [!INCLUDE[d365fin](includes/d365fin_md.md)] mientras trabajan en [!INCLUDE[crm_md](includes/crm_md.md)]. Por ejemplo, al preparar una oferta de ventas podría ser útil saber si tiene suficiente inventario para cumplir el pedido. Para obtener más información, consulte [Uso de Dynamics 365 for Sales desde Business Central](marketing-integrate-dynamicscrm.md).

> [!Note]
> Estos pasos describen el proceso de integración de las versiones en línea de [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)].

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Visión general del proceso de integración
Los pasos siguientes proporcionan una visión general de los pasos de la integración de [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)]

> [!Note]  
> Estas tareas requieren el rol de seguridad **Administrador del sistema** en [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. En el centro de administración de Office 365, configure una cuenta de usuario para conectarse y sincronizar los datos con [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Configuración de la integración con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Asignar las licencias de [!INCLUDE[crm_md](includes/crm_md.md)] a los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] que utilizarán las aplicaciones integradas.

3. Configure una conexión a [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Configuración de una conexión a Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Opcional: empareje los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md).

5. Sincronice los datos entre las aplicaciones. Para obtener más información, consulte [Sincronización de Business Central y Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Acerca de la solución de integración de Business Central
La solución permite a los usuarios ver la información en [!INCLUDE[d365fin](includes/d365fin_md.md)] mientras trabajan en [!INCLUDE[crm_md](includes/crm_md.md)]. Por ejemplo, puede proporcionar información sobre las estadísticas de los clientes, permite a los usuarios emparejar y ver los registros en [!INCLUDE[d365fin](includes/d365fin_md.md)] desde [!INCLUDE[crm_md](includes/crm_md.md)], y permite a los usuarios ver si los productos están disponibles en [!INCLUDE[d365fin](includes/d365fin_md.md)].

De forma predeterminada, la guía de configuración asistida Configurar la conexión de Dynamics 365 for Sales importará la solución de integración de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para ello, la guía de configuración utiliza una cuenta de usuario de administrador. Esta cuenta también debe ser un usuario válido de [!INCLUDE[crm_md](includes/crm_md.md)] con los roles de seguridad siguientes:

* Administrador del sistema  
* Personalizador de solución  

Para obtener más información, consulte [Configuración de cuentas de usuario para la integración con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md), [Crear usuarios en Microsoft Dynamics 365 (online) y asignar roles de seguridad](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md) y [Gestionar usuarios y permisos](ui-how-users-permissions.md).  

Esta cuenta se utiliza una sola vez durante la configuración. Después que la solución se importa en [!INCLUDE[d365fin](includes/d365fin_md.md)], la cuenta ya no se necesita. La integración continuará utilizando la cuenta de usuario creada específicamente para la integración.

Además de la personalización de [!INCLUDE[crm_md](includes/crm_md.md)], la solución de integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] también crea los siguientes roles en [!INCLUDE[crm_md](includes/crm_md.md)] para la integración:

* **Administrador de integración**: permite a los usuarios administrar la conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)]. Normalmente solo se asigna a la cuenta de usuario para la sincronización.  
* **Usuario de integración**: permite a los usuarios acceder a los datos sincronizados. Normalmente se asigna a la cuenta de usuario para la sincronización y a cualquier otro usuario que necesite ver los datos sincronizados o acceder a ellos.
* **Usuario de disponibilidad de producto**: permite a los usuarios consultar la disponibilidad de los productos en [!INCLUDE[d365fin](includes/d365fin_md.md)] desde [!INCLUDE[crm_md](includes/crm_md.md)].

Al final de la guía de configuración, [!INCLUDE[d365fin](includes/d365fin_md.md)] le pedirá que empareje los vendedores con los usuarios en [!INCLUDE[crm_md](includes/crm_md.md)]. Los registros en [!INCLUDE[crm_md](includes/crm_md.md)] suelen tener asignado un propietario (usuario) y, si el emparejamiento entre el usuario en [!INCLUDE[crm_md](includes/crm_md.md)] y el vendedor en [!INCLUDE[d365fin](includes/d365fin_md.md)] no existe, la sincronización fallará. También puede hacer esto más tarde usando la acción **Emparejar vendedores** en la página de **Configuración de la conexión de Microsoft Dynamics 365**.

## <a name="see-also"></a>Consulte también  
[Configuración de cuentas de usuario para la integración con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Configuración de una conexión a Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)
[Sincronización de Business Central y Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)
