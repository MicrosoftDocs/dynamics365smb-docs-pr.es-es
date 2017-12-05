---
title: Paquetes de contenido de Dynamics 365 Business edition y Power BI | Documentos de Microsoft
description: "Obtener información, inteligencia empresarial y KPI de los datos de Dynamics 365 resulta muy sencillo con Power BI y los Dynamics 365 content packs."
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f9a85074f2bc3ed2bff6022b9c248d3568a04e93
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="enabling-your-business-data-for-power-bi"></a>Habilitar los datos de negocio para Power BI
Obtener información de los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] resulta muy sencillo con Power BI y los paquetes de contenido de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Power BI extrae los datos y, a continuación, genera un panel original e informes en función de los datos.  

Microsoft ha publicado los paquetes de contenido siguientes:

| App | Descripción |
| --- | --- |
| Microsoft Dynamics 365 for Financials | Proporciona un panel de control con datos financieros clave a lo largo del tiempo, como ingresos frente a gastos, margen de operación y ciclo de efectivo.|
| Microsoft Dynamics 365 for Financials - CRM | Proporciona un panel de control con datos clave sobre oportunidades de ventas y contactos.  |
| Microsoft Dynamics 365 for Financials - Sales | Proporciona un panel de control con datos clave sobre ventas e inventario. |

## <a name="using-the-dashboards"></a>Uso de paneles de control
Cada paquete de contenido proporciona informes que puede explorar:

* Seleccione cualquier representación visual del panel para traer uno de los informes subyacentes.  
* Filtre el informe o agregue los campos que desee supervisar.  
* Ancle esta visualización personalizada al panel para continuar con el seguimiento.  
  Puede actualizar los datos manualmente y puede configurar un calendario de actualización. Para obtener más información, vea [Configuración de actualización programada](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Los paquetes de contenido están configurados previamente para trabajar con los datos de la empresa de demostración que aparecerá al registrarse para [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cuando instala las aplicaciones en Power BI y se conecta a sus propios datos, es posible que algunos informes no funcionen porque se basan en datos que su empresa no tiene. En esos casos, simplemente puede eliminar ese informe de su panel de control.  

> [!NOTE]  
>   También puede crear sus propios informes y paneles en Power BI basándose en sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, consulte [Conectar los datos empresariales con Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Acceder a [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI
Para visualizar los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI, deberá tener lo siguiente:  

* Acceso a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, consulte [Dynamics 365 Business edition](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Acceder a Power BI. Para obtener más información, consulte [Power BI](https://powerbi.microsoft.com).

En el sitio de Power BI, podrá encontrar información adicional sobre [cómo conectar a los servicios con paquetes de contenido de Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Para acceder a los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI, en la página de la conexión, debe especificar la siguiente información:

| Campo | Descripción |
| --- | --- |
| **URL de alimentación de OData** |La URL de OData, para que Power BI pueda tener acceso a los datos de su empresa, como https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Método de autenticación** |Seleccione **Básico**. |
| **Nombre de usuario** |Su nombre tal como se muestra para la cuenta en [!INCLUDE[d365fin](includes/d365fin_md.md)], como *Juan Pérez*. |
| **Contraseña** |Esta es la clave de acceso al servicio web de su cuenta de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Esto significa que debe obtener 2 tipos de información de [!INCLUDE[d365fin](includes/d365fin_md.md)]: la *URL de OData* y la *clave de acceso al servicio web* para su cuenta de usuario.  

### <a name="getting-the-url"></a>Obtener la URL
Cuando agregue [!INCLUDE[d365fin](includes/d365fin_md.md)] a Power BI, deberá especificar una URL para que Power BI puede tener acceso a los datos de su empresa. En la página de conexión, la URL se conoce como **URL de alimentación de OData** y debe tener el formato siguiente:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
En este ejemplo, *mybusiness* es el nombre del servicio de [!INCLUDE[d365fin](includes/d365fin_md.md)] y *CRONUS US* el de la empresa de demostración con *%20* que representa el espacio del nombre.   
Para obtener la URL, en [!INCLUDE[d365fin](includes/d365fin_md.md)], busque y abra la ventana **Servicios web**. En esta ventana se muestra la lista de servicios web que están disponibles actualmente y puede copiar el enlace desde el campo **URL de OData** para uno de los servicios web de OData predeterminados.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Obtener el nombre de usuario y la clave de acceso de servicio web
Para utilizar los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI, en la ventana **Conectar a Financials**, debe especificar un nombre de usuario y una contraseña. El nombre de usuario es su nombre tal como se muestra para la cuenta en [!INCLUDE[d365fin](includes/d365fin_md.md)] de manera que Power BI pueda iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)]. La contraseña es la clave de acceso al servicio web que se ha configurado para su cuenta de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Para buscar esta información, en [!INCLUDE[d365fin](includes/d365fin_md.md)], busque la ventana **Usuarios** y, a continuación abra la ficha de la cuenta de usuario. En la ficha desplegable **General**, copie el contenido del campo **Nombre de usuario** y, en **Acceso servicio web**, copie el contenido del campo **Clave acceso servicio web**. Si el campo **Clave acceso servicio web** está en blanco, en la cinta, seleccione **Cambiar la clave de acceso al servicio web**, el campo **La clave nunca caduca** y, a continuación, seleccione el botón Aceptar. A continuación, podrá copiar la clave.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Obtener datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]
En el panel de [!INCLUDE[d365fin](includes/d365fin_md.md)] se muestran los informes más habituales que tendrá que usar para realizar el seguimiento de la empresa. Los datos se recuperan de su empresa de [!INCLUDE[d365fin](includes/d365fin_md.md)] usando los servicios web para leer los datos activos. En [!INCLUDE[d365fin](includes/d365fin_md.md)], la ventana **Servicios Web** enumera los servicios Web que se han configurado.

> [!NOTE]  
>   Si cambia el nombre de cualquiera de estos servicios web, los datos no aparecerán en Power BI.  
Si desea agregar el uso de otros datos en Power BI, deberá buscar las tablas en [!INCLUDE[d365fin](includes/d365fin_md.md)], mostrarlas como servicios web y, a continuación, agregarlas al paquete de contenido. Esto es un ejemplo avanzado y es recomendable que empiece por los datos que ya están disponibles en Power BI.  

## <a name="troubleshooting"></a>Solución de problemas
El panel de Power BI depende de los servicios web publicados que aparecen en la lista anterior y mostrará los datos de la empresa de demostración o de la suya propia si importa los datos de la solución de finanzas actual. Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.  

**"Error en la validación de parámetros, asegúrese de que todos los parámetros son válidos"**  
Si se muestra este error al introducir la URL de [!INCLUDE[d365fin](includes/d365fin_md.md)], asegúrese de que se cumplen los requisitos siguientes:  

* La URL sigue exactamente este modelo:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Elimine cualquier texto después del nombre de la empresa que aparece entre paréntesis  
* Asegúrese de que no haya ninguna barra diagonal al final del URL.  
* Asegúrese de que es una conexión segura tal como indica la URL que empieza por *https*.  

**"Error de inicio de sesión"**  
Si se produce un "error de inicio de sesión" al iniciar sesión en el panel con sus credenciales de [!INCLUDE[d365fin](includes/d365fin_md.md)], la causa puede ser una de los problemas siguientes:

* La cuenta que usa no tiene permisos para leer los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] de su cuenta.

    Verifique la cuenta de usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)] y asegúrese de haber usado la clave de acceso al servicio web correcta como contraseña y, a continuación, inténtelo de nuevo.  
* La instancia de [!INCLUDE[d365fin](includes/d365fin_md.md)] a la que está intentando conectarse no dispone de un certificado de SSL válido. En este caso, verá un mensaje de error más detallado ("incapaz de establecer una relación de SSL de confianza").

    > [!NOTE]  
>   No se admiten los certificados autofirmados.  

**"¡Vaya!"**  
Si se muestra un diálogo de error del tipo "¡Vaya!" después de pasar el diálogo de autenticación, la causa suele ser un problema de conexión con los datos del paquete de contenido.

* Verifique que la URL siga el modelo que se especificó anteriormente:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* Un error común es indicar la URL completa de un servicio web específico:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* O quizá haya olvidado indicar el nombre de la empresa:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Migrar datos de empresa de otros sistemas financieros](upload-data.md)  
[Usar [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] como origen de datos de PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] en Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

