---
title: Exportar declaraciones de IVA en formato de texto
description: Puede exportar una declaración de IVA en formato de texto y después enviarla electrónicamente a las autoridades fiscales.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="export-vat-statements-in-text-format"></a><a name="export-vat-statements-in-text-format"></a><a name="export-vat-statements-in-text-format"></a>Exportar declaraciones de IVA en formato de texto
Puede exportar una declaración de IVA en formato de texto y después enviarla electrónicamente a las autoridades fiscales.  

Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).  

## <a name="to-export-a-vat-statement-in-text-format"></a><a name="to-export-a-vat-statement-in-text-format"></a><a name="to-export-a-vat-statement-in-text-format"></a>Para exportar declaraciones de IVA en formato de texto

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Declaraciones de IVA** y luego elija el enlace relacionado.  
2.  Seleccione la declaración de IVA requerida y después seleccione **Generar archivo TXT**.  

    > [!IMPORTANT]  
    >  El nombre de la declaración de IVA debe ser de tipo de plantilla **Informe 1 columna**.  
    >   
    >  En la versión estándar de [!INCLUDE[prod_short](../../includes/prod_short.md)], el nombre de la declaración del IVA para la declaración telemática 320 es del tipo **Informe 1 columna**.  

4.  En la ficha desplegable **Opciones** de la página **Declaración telemática IVA**, rellene los campos tal y como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Movs. IVA incluidos**|Especifique si la declaración de IVA debe incluir los movimientos pendientes, los cerrados, o ambos.|  
    |**Movs. IVA incluidos**|Especifique si la declaración de IVA debe incluir únicamente los movimientos del periodo que se especifica en el campo **Filtro fecha** o también movimientos de periodos anteriores.|  
    |**Divisa adicional**|Seleccione que se muestren los importes del informe en una divisa adicional de informe.|  

5.  En la ficha desplegable **Lín. declaración IVA**, especifique un valor del campo **Filtro fecha**.  

    Opcionalmente, seleccione los filtros adicionales.  
6.  Elija el botón **Aceptar**.  
7.  En la página **Formato de transferencia**, verifique que la declaración de IVA se configura correctamente y después seleccione el botón **Aceptar**.  
8.  Seleccione el botón **Abrir** o **Guardar**.  

Ahora puede enviar la declaración del IVA a las autoridades fiscales.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
 [Informes IVA](vat-reports.md)   
 [Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto](how-to-create-templates-for-telematic-vat-statements-in-text-file-format.md)   
 [Exportar declaraciones de IVA en formato XML](how-to-export-vat-statements-in-xml-format.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
