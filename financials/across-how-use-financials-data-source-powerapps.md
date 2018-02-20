---
title: "Usar los datos para crear una aplicación | Documentos de Microsoft"
description: "Puede hacer que los datos de Financials estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con PowerApps."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 40f8d00c8ee064fdee4b676e4863279ec9e50d6d
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="connecting-to-your-financials-data-to-build-a-business-app-using-powerapps"></a>Cómo conectarse a sus datos de Financials para crear una aplicación empresarial con PowerApps
Puede convertir los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en disponibles como origen de datos en PowerApps.  

> [!NOTE]  
>   Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de PowerApps
1. En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) y, a continuación, inicie sesión.
2. En el panel de navegación izquierdo, elija **Nueva aplicación**.
3. Elija el editor, PowerApps Studio para Windows o PowerApps Studio para Web.

   PowerApps Studio para Windows es una aplicación de escritorio que se usa para crear y publicar PowerApps. PowerApps Studio para Web es la solución en línea que se usa para crear y publicar PowerApps.
4. El siguiente paso para crear una PowerApp es seleccionar los datos. Elija el icono de flecha y la opción **Nueva conexión** en la parte superior izquierda de la página.
5. En la lista de conexiones disponibles, elija **Dynamics 365 for Finance and Operations, Business edition**.
6. PowerApps mostrará una página de conexión que le solicita la información necesaria para conectarse con los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para conectarse debe especificar una dirección URL de OData, el nombre de usuario, la contraseña y el nombre de la empresa.

   Para *URL de OData*, puede copiar la dirección URL de OData V4 de cualquiera de los servicios web que se muestran en la página **Servicios Web** en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Para *Nombre empresa*, utilice el nombre que se muestra en el campo **Nombre** de la ventana **Información empresa** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene varias empresas, elija el nombre de la empresa pertinente en la lista en la ventana **Empresas**. En ambos casos, asegúrese de que el nombre que especifique en el asistente PowerApps coincide exactamente con el texto que se muestra en [!INCLUDE[d365fin](includes/d365fin_md.md)], como `My Company`.

   Para el nombre de usuario y la contraseña, utilice el nombre y la clave de acceso al servicio web que se especificó para la cuenta en la ventana **Usuarios** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, su nombre de usuario es *ADMIN* y la clave de acceso al servicio Web que actúa de contraseña es *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Elija el botón **Conexión** para continuar. PowerApps mostrará un conjunto de datos predeterminado para [!INCLUDE[d365fin](includes/d365fin_md.md)]. Elija el conjunto de datos **Genérico**.

   PowerApps mostrará una lista de tablas que están disponibles en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estas tablas, o extremos, representan todos los servicios web que haya publicado desde [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Si lo desea, puede crear una nueva dirección URL de servicio Web en [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante la acción **Crear conjunto de datos** en la página **Servicios web**, utilizando la guía de configuración asistida **Configurar informes** o eligiendo la acción **Editar en Excel** en cualquier lista.
8. Elija la tabla de que desea utilizar para su PowerApp y después seleccione el botón **Conectar**.
9. Repita los pasos anteriores agregar datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] adicionales a su modelo de datos de Power BI.

   > [!NOTE]  
>    Una vez que haya conectado correctamente con [!INCLUDE[d365fin](includes/d365fin_md.md)], no se le solicitará nuevamente la URL, el nombre de usuario o la contraseña de OData.

Ya se ha conectado correctamente con los datos de Finance and Operations, Business edition y está preparado para comenzar a crear su PowerApp. Para obtener más información, consulte la [documentación de PowerApps](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Consulte también
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  

