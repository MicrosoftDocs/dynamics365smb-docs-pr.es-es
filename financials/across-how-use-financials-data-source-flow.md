---
title: Conectar los datos con Flow | Documentos de Microsoft
description: "Puede hacer que los datos de Financials estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado
Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.  

> [!NOTE]  
>   Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Flow
1. En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com/en-us/) y, a continuación, inicie sesión.
2. Seleccione **Mis flujos** en la cinta en la parte superior de la página.
3. En la ventana **Mis flujos**, elija la opción **Crear desde cero**.
4. En la lista de desencadenadores disponibles, seleccione uno de los dos desencadenadores de [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles: *Cuando se cree un registro* o *Cuando se modifique un registro*.
5. Flow mostrará una página de conexión que le solicita la información necesaria para conectarse con los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para conectarse debe especificar un nombre para la conexión, una dirección URL de OData, el nombre de usuario, la contraseña y el nombre de la empresa.

   Para *URL de OData*, puede copiar la dirección URL de OData V4 de cualquiera de los servicios web que se muestran en la página **Servicios Web** en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Para *Nombre empresa*, utilice el nombre que se muestra en el campo **Nombre** de la ventana **Información empresa** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene varias empresas, elija el nombre de la empresa pertinente en la lista en la ventana **Empresas**. En ambos casos, asegúrese de que el nombre que especifique en el asistente PowerApps coincide exactamente con el texto que se muestra en [!INCLUDE[d365fin](includes/d365fin_md.md)], como `My Company`.

   Para el nombre de usuario y la contraseña, utilice el nombre y la clave de acceso al servicio web que se especificó para la cuenta en la ventana **Usuarios** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, su nombre de usuario es *ADMIN* y la clave de acceso al servicio Web que actúa de contraseña es *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Para obtener más información, vea [Administrar usuarios y permisos](ui-how-users-permissions.md).
6. Elija el botón **Crear** al final de la página para continuar.

   Flow mostrará una lista de tablas que están disponibles en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estas tablas, o extremos, representan todos los servicios web que haya publicado desde [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Si lo desea, puede crear una nueva dirección URL de servicio Web en [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante la acción **Crear conjunto de datos** en la página **Servicios web**, utilizando la guía de configuración asistida **Configurar informes** o eligiendo la acción **Editar en Excel** en cualquier lista.
7. Elija los datos que desee utilizar en Flow.

Ya se ha conectado correctamente con los datos de Dynamics 365 y está preparado para comenzar a crear su flujo. Para obtener más información, consulte la [documentación de Flow](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Consulte también
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Administrar usuarios y permisos](ui-how-users-permissions.md)    
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  

