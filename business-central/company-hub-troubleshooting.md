---
title: Solución de problemas del hub de empresas
description: Aprenda a solucionar cualquier problema cuando la empresa se concentre en Dynamics 365 Business Central para gestionar el trabajo en varias empresas.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accountant, accounting, troubleshoot'
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: edupont
---
# Solución de problemas del hub de empresas

Agregar empresas al panel del hub de empresas es bastante sencillo, pero este artículo le ayudará a solucionar los problemas que puedan surgirle.  

## Comprobar errores

Utilice la acción **Comprobar errores** para ver una lista de errores recientes. Puede ver detalles adicionales de cada error y puede limpiar el registro eliminando las entradas más antiguas.  

## Error de conexión

Puede haber un par de razones por las que no puede conectarse a una empresa, incluidas las siguientes:

- La dirección URL del campo **Vínculo de entorno** no es válida  

  Vaya a la página **Vínculos de entorno**, abra el entorno al que no puede conectarse y luego elija la acción **Probar la conexión**.  
- La empresa del cliente está actualmente fuera de línea, por ejemplo, si se está actualizando

  En el escritorio, seleccione el elemento de menú **Herramientas** y, a continuación, elija **Comprobar errores**. De esta manera se abrirá una lista con detalles técnicos, por lo que es posible que desee ponerse en contacto con su administrador si encuentra errores. Por ejemplo, el mensaje de error "*El servidor ha rechazado las credenciales del cliente*" sugiere que no tiene acceso.  
- No tiene acceso a todas las empresas del entorno a las que intenta conectarse

  En [!INCLUDE [prod_short](includes/prod_short.md)], una organización puede tener varias unidades denominadas empresas y es posible que no tenga acceso a todas las empresas. Trabaje con su administrador o cliente para asegurarse de que tiene acceso a las empresas en las que quiere trabajar.  

## Los datos no se actualizan

Cuando agrega una empresa o solicita una actualización de los datos, [!INCLUDE [prod_short](includes/prod_short.md)] busca los datos. Pero debe actualizar la página por sí mismo, como mediante la acción **Recargar todas las empresas**, actualice la página del navegador, salga del panel de control y luego vuelva allí, o alguna acción similar.  

Si ha agregado una empresa, pero no se muestra en la lista, también puede usar la acción **Recargar todas las empresas** para actualizar la lista.

## Consulte también .

[Administrar el trabajo de varias empresas en el hub de empresas](company-hub.md)  
[Agregar empresas al hub de empresas](company-hub-add-company.md)  
[Experiencias contables en Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]