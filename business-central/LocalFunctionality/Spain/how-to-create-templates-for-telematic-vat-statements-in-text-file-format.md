---
title: "Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto"
description: "Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios. Puede enviar los archivos en formato de texto y en formato XML. Este procedimiento describe cómo crear plantillas para los archivos de texto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3ce5956a05805fccfd7faf246b45710fddf3b07e
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="create-templates-for-telematic-vat-statements-in-text-file-format"></a>Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto
Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios. Puede enviar los archivos en formato de texto y en formato XML. Este procedimiento describe cómo crear plantillas para los archivos de texto.  

Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).  

## <a name="to-create-a-template-for-vat-statements-in-text-file-format"></a>Para crear una plantilla para las declaraciones telemáticas de IVA en formato de archivo de texto  

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Declaración del IVA** y, a continuación, seleccione el vínculo apropiado.  
2.  Seleccione la declaración de IVA requerida y después seleccione **Diseñar archivo TXT**.  
3.  En la ventana **Formato transferencia**, rellene los campos tal como se describe en la tabla siguiente.  

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

