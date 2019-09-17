---
title: Configurar el registro de correo electrónico | Documentos de Microsoft
description: Aprenda a convertir las interacciones de correo electrónico entre vendedores y clientes en oportunidades de venta reales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 08/26/2019
ms.author: bholtorf
ms.openlocfilehash: e42618be17ff4f9bfe0d54a88e70d5a1841568c1
ms.sourcegitcommit: 8d9f08304b2f3b5504332bc626383797564ac5e3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920471"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Realizar un seguimiento de los intercambios de mensajes de correo electrónico entre vendedores y contactos
Aproveche al máximo las comunicaciones entre los vendedores y sus clientes actuales o potenciales mediante el seguimiento de los intercambios de correos electrónicos y, a continuación, conviértalos en oportunidades procesables. [!INCLUDE[d365fin](includes/d365fin_md.md)] puede funcionar con Exchange Online para mantener un registro de los mensajes entrantes y salientes. Puede ver y analizar el contenido de cada mensaje en la página **Movimientos del log de interacción**.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a>Configuración de [!INCLUDE[d365fin](includes/d365fin_md.md)] para registrar los mensajes de correo electrónico
Comience con el registro de correo electrónico en dos sencillos pasos:

1. Conecte [!INCLUDE[d365fin](includes/d365fin_md.md)] con Exchange Online para su suscripción de Office 365. Exchange Online gestiona sus mensajes de correo electrónico. Hemos facilitado este paso al proporcionar una guía de configuración asistida. Solo necesita sus credenciales de administrador para su cuenta de administrador en Office 365. Para comenzar la guía, vaya a **Configuración asistida** y, a continuación, elija **Configurar registro de correo electrónico**. 
2. Asegúrese de que se han introducido direcciones de correo electrónico válidas en [!INCLUDE[d365fin](includes/d365fin_md.md)] para sus vendedores y contactos, dependiendo de si son clientes potenciales o existentes. Para ello, para cada cliente o vendedor, abra la ficha **Contacto** o **Vendedor/Comprador** y consulte el campo **Correo electrónico**.

> [!Tip]
> Después de completar los pasos de la guía, puede comprobar si la conexión se ha realizado correctamente. Busque **Configuración de marketing**, seleccione **Proceso**, **Funciones** y, a continuación, **Validar configuración de registro de correo electrónico**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Visualización de los intercambios de mensajes de correo electrónico en el registro de interacciones
[!INCLUDE[d365fin](includes/d365fin_md.md)] crea una entrada en la página **Log de interacción** cada vez que un vendedor y un contacto intercambian un mensaje de correo electrónico. Para ver el log de interacción, abra la ficha **Contacto** o **Vendedor/Comprador** correspondiente a la persona y, a continuación, elija **Navegar**, **Historial** y **Movimientos del log de interacción**. Hay algunas cosas que podemos hacer con cada entrada del registro, por ejemplo:

* Ver el contenido del mensaje de correo electrónico que se ha intercambiado haciendo clic en la acción **Mostrar datos adjuntos**.
* Convertir un intercambio de correos electrónicos en una oportunidad de ventas. Si una entrada parece prometedora, puede convertirla en una oportunidad y luego administrar su progreso hasta una venta. Para hacerlo, seleccione la entrada y, a continuación, seleccione la acción **Crear oportunidad**. Para obtener más información, consulte [Administrar oportunidades de venta](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Consulte también
[Gestionar las relaciones](marketing-relationship-management.md)

