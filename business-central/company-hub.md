---
title: Administrar el trabajo de varias empresas en el hub de empresas
description: Más información sobre el hub de empresas de Dynamics 365 Business Central que puede utilizar para gestionar su trabajo en varias empresas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/29/2020
ms.author: edupont
ms.openlocfilehash: e8a1e6de5cc8889f144e08db8ed77e4543cb9b4c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752060"
---
# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Administrar el trabajo de varias empresas en el hub de empresas

Algunas personas trabajan en varias empresas en [!INCLUDE [prod_short](includes/prod_short.md)], y algunos también trabajan en más de una organización, como contables externos o empleados y gerentes de corporaciones con múltiples subsidiarias. Para estos usuarios y muchos otros, el hub de empresas sirve como página de aterrizaje para administrar el trabajo en los diversos entornos en los que trabajan, en empresas, entornos y regiones.  

Puede acceder al centro cambiando al rol **Hub de empresas** Mi Configuración, o abriendo directamente la página **Hub de empresas**. Puede hacer el mismo trabajo en ambos lugares, pero las acciones se colocan de forma ligeramente diferente en los menús.  

> [!NOTE]
> Puede conectar el hub de la empresa a tantas empresas como necesite. Sin embargo, solo puede conectar el hub de la empresa a empresas alojadas en [!INCLUDE [prod_short](includes/prod_short.md)] en línea.

## <a name="company-hub-home-page"></a>Página de inicio del hub de empresas

Si usa el rol **Hub de empresas**, su página de inicio muestra una lista de empresas a las que tiene acceso, incluida información sobre datos de puntos de interés clave (KPI) y vínculos para abrir cada empresa. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Elija la acción **Hub de empresas** para abrir el hub de empresas, donde puede trabajar más de cerca con cada empresa.  

> [!TIP]
> Para acceder a una empresa específica en [!INCLUDE [prod_short](includes/prod_short.md)], elija el nombre de la empresa o elija el producto de menú **Ir a empresa**, con lo que iniciará sesión automáticamente en una nueva pestaña del navegador.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Acciones para una empresa que figura en el centro empressarial":::

Puede agregar nuevas empresas, como cuando obtiene un nuevo cliente o cuando su corporación agrega una nueva subsidiaria. Para más información, consulte [Agregar empresas al hub de empresas](company-hub-add-company.md).  

> [!TIP]
> Para actualizar los datos en el hub de empresas, debe tener acceso a los datos de las empresas de las que provienen los datos.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## <a name="assigned-tasks"></a>Tareas asignadas

En [!INCLUDE [prod_short](includes/prod_short.md)], puede asignarse tareas y asignarlas a otros, y viceversa. El hub de empresas le ofrece un resumen de las tareas asignadas por cada empresa y también puede tener acceso a una lista de todas las tareas asignadas mediante **Mis tareas de usuario** en la página **Inicio**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a>Mis tareas de usuario

La lista **Mis tareas de usuario** le ayuda a priorizar su día al mostrar más información sobre sus tareas asignadas en todas sus empresas.  

Puede ordenarlas por fecha de vencimiento, por ejemplo, o por otro tipo de datos que lo ayuden a priorizar su día. De forma predeterminada, la lista muestra todas las tareas que tiene asignadas, pero puede configurar filtros para que solo se muestren las tareas marcadas como de alta prioridad, por ejemplo.  

Para elegir una tarea, simplemente selecciónela de la lista de tareas pendientes del usuario. En la cinta de opciones, el vínculo **Ir al elemento de la tarea** abrirá la página en la que puede realizar el trabajo.  

Cuando haya terminado una tarea, simplemente márquela como completada.  

Para obtener más información sobre empresas y entornos, consulte [Vínculos de entorno](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a>Acceder al hub de empresas

Para acceder al hub de empresas, debe tener acceso a través del grupo de usuarios *CENTRO EMPRESARIAL D365* o a través del conjunto de permisos *CENTRO EMPRESARIAL D365*. También debe tener acceso a las empresas que figuran en el hub de empresas, lo que significa que debe ser un usuario de esas empresas. Para obtener más información, vea [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).  

> [!IMPORTANT]
> El hub de empresas es una lista de todas la empresas, por lo que cualquier usuario al que se le conceda acceso al centro empressarial podrá ver todas las empresas en su propio suscriptor [!INCLUDE [prod_short](includes/prod_short.md)] y todos los KPI de las empresas a las que tienen acceso.

Si no puede encontrar el hub de empresas y sabe que se le ha concedido acceso a él, consulte con su administrador si el hub de empresas aparece en la página **Administración de extensiones**. Para obtener más información, consulte [Personalizar Business Central con extensiones](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a>Establecer el hub de empresas

Para comenzar a utilizar el hub de empresas, debe agregar una o más empresas a su panel. Para más información, consulte [Agregar empresas al hub de empresas](company-hub-add-company.md).  

Pero, para agregar una empresa, debe haber tenido acceso a una o más instancias de [!INCLUDE [prod_short](includes/prod_short.md)] además de la empresa para la que utiliza el hub de empresas.  

Por ejemplo, si es contable, sus clientes pueden invitarle a sus [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Invitar a un contable externo a Business Central](finance-accounting.md#inviteaccountant).  

Los administradores pueden usar la misma guía de configuración asistida para agregarle a su [!INCLUDE [prod_short](includes/prod_short.md)] o pueden agregarle a la cuenta de Azure AD relevante del Centro de administración de Microsoft 365. Para obtener más información, consulte [Administrar usuarios y grupos](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a>Consulte también .

[Agregar empresas al hub de empresas](company-hub-add-company.md)  
[Experiencias contables en Business Central](finance-accounting.md)  
[Hub de empresas para extensión de Business Central](ui-extensions-company-hub.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]