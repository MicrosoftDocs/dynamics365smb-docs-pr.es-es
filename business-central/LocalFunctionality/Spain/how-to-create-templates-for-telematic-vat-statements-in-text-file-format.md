---
title: Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto
description: Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios. Puede enviar los archivos en formato de texto y en formato XML. Este procedimiento describe cómo crear plantillas para los archivos de texto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4be9719d8822db20053f60d76ace030f0800d132
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778345"
---
# <a name="create-templates-for-telematic-vat-statements-in-text-file-format"></a>Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto
Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios. Puede enviar los archivos en formato de texto y en formato XML. Este procedimiento describe cómo crear plantillas para los archivos de texto.  

Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).  

## <a name="to-create-a-template-for-vat-statements-in-text-file-format"></a>Para crear una plantilla para las declaraciones telemáticas de IVA en formato de archivo de texto  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Declaración IVA** y luego elija el vínculo correcto.  
2.  Seleccione la declaración de IVA requerida y después seleccione **Diseñar archivo TXT**.  
3.  En la página **Formato transferencia**, rellene los campos tal como se describe en la tabla siguiente.  

    > [!IMPORTANT]  
    >  Los valores de los campos están determinados por las autoridades fiscales.  
    >   
    >  Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nombre decl. IVA**|Especifique el nombre de la declaración del IVA para el que está diseñada esta plantilla.|  
    |**Nº**|Especifique el número de campo en el archivo de texto.|  
    |**Posición**|Especifique la posición de este campo en el archivo de texto.|  
    |**Longitud**|Especifique la longitud del campo.|  
    |**Escriba**|Especifique el tipo del campo. Las opciones disponibles son **Alfanumérico**, **Numérico**, **Fijo**, **Preguntar** y **Divisa**.|  
    |**Subtipo**|Especifique el subtipo del campo.<br /><br /> El subtipo especifica si la línea debe mostrar solo la parte entera de un importe, la parte decimal, o el importe total.|  
    |**Descripción**|Especifique el texto que desea que aparezca en la etiqueta.|  
    |**Valor**|Especifique el valor de la etiqueta.|  
    |**Caja**|Especifique el número de casilla desde donde recuperar los datos.|  

4.  Repita el paso anterior para las líneas adicionales en la declaración de IVA.  
5.  Elija el botón **Aceptar**.  

Esta acción crea la plantilla. Ahora puede crear un archivo que luego puede enviar a las autoridades fiscales.  

## <a name="see-also"></a>Consulte también  
 [Exportar declaraciones de IVA en formato de texto](how-to-export-vat-statements-in-text-format.md)   
 [Crear plantillas para las declaraciones telemáticas de IVA en formato XML](how-to-create-templates-for-telematic-vat-statements-in-xml-file-format.md)
