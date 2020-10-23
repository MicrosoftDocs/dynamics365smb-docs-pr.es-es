---
title: Solución de problemas del hub de empresas
description: Obtenga información sobre cómo solucionar problemas en el hub de empresas de Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f348de3e8116efd789f85f1b011ecc7013bf2b1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927728"
---
# <a name="troubleshooting-your-company-hub"></a>Solución de problemas del hub de empresas

Agregar empresas al panel del hub de empresas es bastante sencillo, pero este artículo le ayudará a solucionar los problemas que puedan surgirle.  

## <a name="check-errors"></a>Comprobar errores

Utilice la acción **Comprobar errores** para ver una lista de errores recientes. Puede ver detalles adicionales de cada error y puede limpiar el registro eliminando las entradas más antiguas.  

## <a name="connection-failed"></a>Error de conexión

Puede haber un par de razones por las que no puede conectarse a una empresa, incluidas las siguientes:

- La dirección URL del campo **Vínculo de entorno** no es válida  

  Vaya a la página **Vínculos de entorno**, abra el entorno al que no puede conectarse y luego elija la acción **Probar la conexión**.  
- La empresa del cliente está actualmente fuera de línea, por ejemplo, si se está actualizando

  En el escritorio, seleccione el elemento de menú **Herramientas** y, a continuación, elija **Comprobar errores**. De esta manera se abrirá una lista con detalles técnicos, por lo que es posible que desee ponerse en contacto con su administrador si encuentra errores. Por ejemplo, el mensaje de error "*El servidor ha rechazado las credenciales del cliente*" sugiere que no tiene acceso.  
- No tiene acceso a todas las empresas del entorno a las que intenta conectarse

  En [!INCLUDE [prodshort](includes/prodshort.md)], una organización puede tener varias unidades denominadas empresas y es posible que no tenga acceso a todas las empresas. Trabaje con su administrador o cliente para asegurarse de que tiene acceso a las empresas en las que quiere trabajar.  

## <a name="data-does-not-refresh"></a>Los datos no se actualizan

Cuando agrega una empresa o solicita una actualización de los datos, [!INCLUDE [prodshort](includes/prodshort.md)] busca los datos. Pero debe actualizar la página por sí mismo, como mediante la acción **Recargar todas las empresas**, actualice la página del navegador, salga del panel de control y luego vuelva allí, o alguna acción similar.  

Si ha agregado una empresa, pero no se muestra en la lista, también puede usar la acción **Recargar todas las empresas** para actualizar la lista.

## <a name="see-also"></a>Consulte también .

[Administrar el trabajo de varias empresas en el hub de empresas](company-hub.md)  
[Agregar empresas al hub de empresas](company-hub-add-company.md)  
[Experiencias contables en Business Central](finance-accounting.md)  
