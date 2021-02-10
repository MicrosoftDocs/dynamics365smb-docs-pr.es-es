---
title: Ver y editar la configuración básica | Documentos de Microsoft
description: Obtenga información sobre cómo cambiar algunos de los valores básicos, por ejemplo, el área de trabajo, la empresa o la fecha de trabajo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df3807f3d5d2baa7f50df4091a0d1f2622d09ff8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757647"
---
# <a name="change-basic-settings"></a>Cambiar la configuración básica

En la página **Mi configuración**, puede ver y cambiar la configuración básica de [!INCLUDE[prod_short](includes/prod_short.md)]. Los cambios que realice sólo afectan a su área de trabajo; no a las áreas de trabajo de otros usuarios.  

## <a name="role-center"></a><a name="role-center"></a> Área de trabajo
El área de trabajo representa la página Inicio, una pantalla de inicio que está designada para las necesidades específicas del trabajo en una empresa. Dependiendo de su función, el Área de trabajo le brinda una descripción general del negocio, su departamento o sus tareas personales. También le ayuda a navegar por sus tareas diarias y encontrar el trabajo que le asignaron.

-   En la parte superior, la navegación le permite cambiar entre clientes, proveedores, artículos y otras listas importantes de información. Del mismo modo, las acciones le permiten iniciar tareas, como crear una nueva factura de venta, directamente desde el Área de trabajo.

-   En el centro, busque el área **Actividades**, que muestra los datos actuales y se puede hacer clic o tocar para ver información más detallada. Los indicadores de rendimiento clave (KPI) pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de efectivo o ingresos y gastos. También puede crear una lista de clientes favoritos en el área de trabajo para las cuentas empresariales con las que hace negocios a menudo o a las que necesita prestar especial atención.

### <a name="to-change-the-role"></a>Para cambiar el rol
El rol pedido es **Administrador de negocio**, pero puede seleccionar otro rol para usar un área de trabajo que se adapte mejor a sus necesidades.
1. En la esquina superior derecha, elija el icono **Configuración** ![Configuración](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") y, a continuación, elija la acción **Mi configuración**.
2. En la página **Mi configuración**, en el campo **Rol**, seleccione el rol que desea usar de forma predeterminada. Por ejemplo, seleccione **Contable**.
3. Elija el botón **Aceptar**.

## <a name="company"></a><a name="company"></a>Compañía
Una empresa funciona como un contenedor de datos en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede haber múltiples empresas en una base de datos, pero solo se puede seleccionar una a la vez.

La empresa predeterminada se llama CRONUS y solo contiene datos de demostración. Puede crear una nueva empresa con datos personalizados. Para obtener más información, consulte [Crear nuevas empresas](about-new-company.md).

## <a name="to-change-the-company-name"></a>Para cambiar el nombre de la empresa
El nombre de la empresa siempre se muestra en la esquina superior izquierda y funciona como una acción que puede elegir para volver al área de trabajo. Puede cambiar este nombre en la página **Información de empresa**.

1. Elija el icono ![Icono de rueda dentada para abrir el menú Configuración](media/ui-experience/settings_icon_small.png) y luego elija la acción **Información de empresa**.
2. En el campo **Nombre**, introduzca el nuevo nombre de empresa.
3. Salga de la página. El sistema se reinicia y muestra la nueva empresa en la esquina superior izquierda.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a>Para mostrar un distintivo de empresa para acceder rápidamente a la información de la empresa  
Puede agregar un distintivo personalizado en la esquina superior derecha, que puede elegir para ver rápidamente el nombre de la empresa y la información de suscriptor en un cuadro emergente.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.
2. En la ficha desplegable **Distintivo de la empresa**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Si se define un distintivo de la empresa, no puede cambiar el nombre de la empresa como se describe en [Para cambiar el nombre de la empresa](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Fecha de trabajo
La fecha de trabajo más utilizada es la fecha actual. Es posible que tenga que cambiar temporalmente la fecha de trabajo para realizar tareas como la finalización de las transacciones de una fecha que no sea la fecha de hoy.

> [!TIP]  
> En todos los campos de fecha, escriba **h** para introducir rápidamente la fecha de hoy y escriba **t** para introducir rápidamente la fecha de trabajo, que es el valor en el campo **Fecha de trabajo** en la página **Mi configuración**.

> [!IMPORTANT]  
>  Después de modificar la fecha de trabajo, si cierra la sesión o cambia a otra empresa, los datos de trabajo vuelven a la fecha de trabajo predeterminada. Por lo tanto, la próxima vez que inicie sesión o vuelva a cambiar a la empresa original, es posible que tenga que volver a establecer la fecha de trabajo.

### <a name="work-date-indication"></a>Indicación de la fecha de trabajo
Siempre que la fecha de trabajo no esté establecida en la fecha de hoy, aparecerán dos tipos de indicadores en las páginas que se pueden editar y donde la fecha de trabajo es fundamental:

* Aparece un recordatorio en la parte superior de la página que le indica cuál es la fecha de trabajo establecida. El recordatorio proporciona un vínculo directo a la configuración de la fecha de trabajo en la página **Mi configuración** para que pueda cambiar la fecha si lo desea. Desde el recordatorio, también puede elegir descartarlo para el resto de la sesión. A menos que cambie la fecha de trabajo a "hoy", el recordatorio aparecerá la próxima vez que inicie sesión.

* Si descarta el recordatorio, la fecha de trabajo aparecerá en el título de la página.  

Si la fecha de trabajo no está establecida en el día actual (hoy), la fecha de trabajo actual se muestra en la esquina superior izquierda de todas las páginas donde puede editar datos.

## <a name="region"></a><a name="region"></a> Región

El valor **Región** determina cómo se muestran o se forman las fechas, los tiempos, los números, y divisas.

## <a name="language"></a><a name="language"></a> Idioma
Cambia el idioma de la pantalla. Este campo aparece sólo cuando hay más de un idioma a elegir.

El idioma inicial lo determina el administrador o la configuración de su navegador cuando inicia sesión en [!INCLUDE[prod_short](includes/prod_short.md)]. El idioma que establezca se usará en todos los dispositivos desde los que inicie sesión, como un teléfono o una tableta.

Los idiomas adicionales para [!INCLUDE[prod_short](includes/prod_short.md)] se pueden instalar desde AppSource. Si bien todos los idiomas de visualización compatibles se muestran en la lista, el administrador debe instalar la aplicación de idioma pertinente para el suscriptor antes de que los usuarios puedan cambiar al nuevo idioma en [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="changing-when-i-receive-notifications"></a>Cambio al recibir notificaciones
Seleccione este vínculo para ver o cambiar las notificaciones que recibe sobre determinados eventos o cambios de estado, cuando va a facturar a un cliente que tiene un saldo vencido o cuando el inventario disponible es inferior a la cantidad que va a vender, por ejemplo. Para obtener más información, consulte [Administrar notificaciones](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Crear nuevas en empresas](about-new-company.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
