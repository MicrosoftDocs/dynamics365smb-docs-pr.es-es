---
title: Obtener clientes en la experiencia contable de Dynamics 365 | Documentos de Microsoft
description: "Información sobre cómo agregar clientes existentes al Accountant Hub de Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/23/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c7f0af8d3535f558567cd40c841909cd151ce313
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a>Agregar clientes al panel de [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Puede agregar un cliente mediante la página **Clientes** que puede abrir con la acción **Administrar clientes** de la cinta. Simplemente, elija **Nuevo** y, a continuación, rellene los campos.  

> [!div class="mx-imgBorder"]
> ![Agregar un cliente](./media/accountant-add-client/manage-client.png)

Los datos de la tarjeta para cada cliente los especifica el usuario, y puede cambiarlos según sea necesario. Sin embargo, el campo **Dirección URL del cliente** es fundamental ya que así es como puede acceder al [!INCLUDE [d365fin](includes/d365fin_md.md)] de cada cliente. Utilice la acción **Validar URL del cliente** de la cinta para comprobar que ha introducido el vínculo correcto. La URL en la que debe introducir los puntos en [!INCLUDE [d365fin](includes/d365fin_md.md)] del cliente e incluye su dirección de dominio. Por ejemplo, si han especificado un dominio como MyBusiness.com, entonces el vínculo a su [!INCLUDE [d365fin](includes/d365fin_md.md)] es *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Antes de la actualización de mayo de 2018, la URL que especificó tenía un formato diferente con el nombre de la empresa del cliente al principio. En la versión actual de [!INCLUDE [d365fin](includes/d365fin_md.md)], el formato es ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, donde ```clientdomain``` representa el dominio de su cliente.  

La URL de cliente se utiliza cuando se elige el elemento de menú **Ir a empresa** en el panel de [!INCLUDE [d365acc](includes/d365acc_md.md)].  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a>Obtener una invitación a [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] de un cliente
Una empresa que utiliza [!INCLUDE [d365fin](includes/d365fin_md.md)] puede invitarle a [!INCLUDE [d365fin](includes/d365fin_md.md)] como su contable externo. Para ser invitado, debe indicarle el correo electrónico que usa con [!INCLUDE [d365acc](includes/d365acc_md.md)], como <em>me@accountant.com</em>. El administrador de su cliente puede agregarlo a su sistema ejecutando el asistente **Invitar a contable externo**.  

Como resultado, recibirá el correo electrónico del cliente con vínculos a [!INCLUDE [d365fin](includes/d365fin_md.md)]. El primer enlace es una invitación para acceder a su empresa: ábralo y acepte los pasos que lo incorporan al [!INCLUDE [d365fin](includes/d365fin_md.md)] de su cliente. El segundo enlace es para agregar este cliente a su escritorio en [!INCLUDE [d365acc](includes/d365acc_md.md)] como se describe anteriormente.  

Cuando haya aceptado la invitación, iniciará sesión y podrá acceder a los datos financieros del cliente desde el Área de trabajo **Contable**. Para obtener más información, vea [Experiencias contables en [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Consulte también
[Introducción a [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Solución de problemas de [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  

