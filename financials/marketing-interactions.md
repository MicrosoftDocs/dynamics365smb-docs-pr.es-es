---
title: Interacciones | Documentos de Microsoft
description: "Describe cómo usar interacciones con los contactos en Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a423f5581f6803b60a0351d0b91f2c08ebafeba7
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="managing-interactions-with-contacts"></a>Gestión de las interacciones con los contactos
En [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], las interacciones son todos los tipos de comunicaciones entre su empresa y sus contactos. Por ejemplo, pueden ser por carta, fax, correo electrónico, teléfono, reuniones, etc.

El área de Gestión de relaciones permite registrar todas las interacciones que tenga con sus contactos para poder hacer un seguimiento de las ventas y los esfuerzos comerciales dirigidos a éstos y mejorar las interacciones de negocio futuras. La configuración de su aplicación para registrar interacciones consta de tres pasos:

* Configurar plantillas de interacción  
* Crear interacciones en contactos o segmentos  
* Ver y gestionar las interacciones registradas  

##  <a name="set-up-interaction-templates"></a>Configurar plantillas de interacción
Antes de poder crear y registrar interacciones, debe configurar las plantillas de interacción. Al crear interacciones, debe especificar las plantillas en las que se basa. Una plantilla de interacción es un modelo que define las características básicas de una interacción.
Puede configurar una plantilla de interacción en la ventana **Plantillas de interacción**.  

## <a name="create-interactions"></a>Crear interacciones
Hay dos maneras de registrar interacciones:

* puede crear de forma manual las interacciones relacionadas con un único contacto o un segmento. Para obtener más información, vea [Procedimiento: Crear interacciones en contactos y segmentos](marketing-how-create-interactions.md)  
* Puede registrar automáticamente interacciones cuando realiza acciones en la aplicación, por ejemplo, cuando imprime una factura o un presupuesto. Para obtener más información, vea [Registro automático de interacciones con contactos](marketing-auto-record-interactions.md)

## <a name="view-and-manage-recorded-interactions"></a>Ver y administrar las interacciones registradas
Puede ver todas las interacciones archivadas que no han sido borrados en la ventana **Movs. log. interacción**. Puede abrir esta ventana por:

* Mediante el icono **Buscar por página o informe** para buscar en **Movs. log. interacción**.
* Seleccionar la acción **Movs. log. interacción** en un contacto o segmento.
  La ventana **Movs. log. interacción** contiene las interacciones que ha creado manualmente y las interacciones que la aplicación ha registrado automáticamente.

En esta ventana puede:

* Ver el estado de las interacciones.
* Marcar las interacciones como canceladas.

Puede eliminar los movimientos de registro de interacción que han sido cancelados. Para eliminar os movimientos de registro de interacción, en la esquina superior derecha, seleccione el icono **Buscar por página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Eliminar mov. cancel. reg. inter.** y, a continuación, seleccione el vínculo relacionado y rellene la información.

## <a name="see-also"></a>Consulte también
[Gestionar contactos](marketing-contacts.md)  
[Administrar oportunidades de venta](marketing-manage-sales-opportunities.md)  
[Trabajar con Financials](ui-work-product.md)  

