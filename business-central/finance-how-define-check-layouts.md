---
title: Especificar el diseño de un cheque
description: Puede diseñar e imprimir los cheques en diferentes formatos para cumplir los estándares establecidos por las autoridades locales.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 6d083e3eea85fde087a431d21bb9eae8bb4b8c5e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444642"
---
# <a name="select-a-check-layout"></a>Seleccionar una plantilla de cheques
Puede diseñar los cheques conforme a los estándares definidos por las autoridades locales. Las imágenes de los cheques se pueden imprimir en inglés, francés o español.

Los cheques se han diseñado para imprimir formatos de imágenes de cheque de Estados Unidos y Canadá en un formato cheque-matriz-cheque o en un formato matriz-matriz-cheque.

## <a name="to-select-a-check-layout"></a>Para seleccionar una plantilla de cheques
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selección informes banco** y luego elija el enlace relacionado.
2. En la página **Informe selección - Bancos**, en el campo **Uso**, seleccione **Cheque**.
3. Seleccione uno de los identificadores de informes siguientes:

| Id. informe | Nombre informe | Descripción |
| --- | --- | --- |
| 1401 |Activar |Es el informe predeterminado. |
| 10411 |Cheque (Matriz/Matriz/Cheque) |Este informe está diseñado para imprimir cheques en un formato matriz/matriz/cheque. |
| 10412 |Cheque (Matriz/Cheque/Matriz) |Este informe está diseñado para imprimir cheques en un formato matriz/cheque/matriz. |
| 10413 |Tres cheques por página |Este informe está diseñado para imprimir tres cheques por página. |

Cuando haya configurado los diseños de cheques, puede imprimir cheques desde la página **Diario de pagos**. Para obtener más información, consulte [Trabajar con cheques](payables-how-work-checks.md).

Para cambiar una de estas plantillas de cheques predeterminadas, utilice la integración de Word o RDLC. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Usando MICR y fuentes de seguridad
La versión en línea de [!INCLUDE[prod_short](includes/prod_short.md)] contiene fuentes preinstaladas en los servidores que se pueden usar al definir diseños de verificación. A continuación se describen qué fuentes están disponibles y tiene enlaces a información detallada por parte de proveedores externos de las fuentes.

> [!Important]
> MICR y verifique las fuentes de seguridad en Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] tienen licencia en un paquete de fuentes de IDAutomation.com, Inc. Estos productos solo pueden usarse como parte de y en conexión con Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].

En la actualización 15.3 y posteriores, las fuentes de reconocimiento de caracteres de tinta magnética (MICR) están instaladas y disponibles para su uso. Ambos estándares E-13B y CMC-7 son admitidos. Además de las fuentes MICR, hay fuentes de seguridad especiales disponibles para generar texto, nombres, cantidades y los símbolos de moneda Dólar, Euro, Libra y Yen, que son difíciles de manipular una vez que se ha impreso un cheque.

> [!NOTE]
> Por razones legales y de seguridad, no puede cargar fuentes personalizadas en el ambiente [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="micr-e-13b-specifications"></a>Especificaciones MICR E-13B
A continuación se resumen las especificaciones para las fuentes MICR E-13B que pueden ser útiles al calibrar fuentes para que estén en diseños de cheques con impresoras MICR específicas.

![Especificaciones MICR E-13B.](media/font_MICR_E-13B_Specifications.png "Especificaciones MICR E-13B")

### <a name="delimiter-characters"></a>Caracteres delimitadores
![Caracteres delimitadores.](media/font-micr-letters.png "Caracteres delimitadores")

La especificación completa de las fuentes MICR E-13B se puede encontrar en la documentación del proveedor aquí: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>Especificaciones MICR CMC-7
Las siguientes fuentes CMC-7 están disponibles en línea en [!INCLUDE[prod_short](includes/prod_short.md)]:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
-   IDAutomationCMC7n40

A continuación se resumen las especificaciones para las fuentes MICR CMC-7 que pueden ser útiles al calibrar fuentes para que estén en diseños de cheques con impresoras MICR específicas.

![Especificaciones MICR CMC-7.](media/font_MICR_CMC-7_Specifications.png "Especificaciones MICR CMC-7")

### <a name="delimiter-characters"></a>Caracteres delimitadores
![Caracteres delimitadores para CMC-7.](media/font-cmc7-letters.png "Caracteres delimitadores para CMC-7")

La especificación completa de las fuentes MICR CMC-7 se puede encontrar en la documentación del proveedor aquí: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Especificaciones de fuente segura
A continuación se resumen las especificaciones para las fuentes de comprobación de seguridad que pueden ser útiles al calibrar fuentes para que estén en diseños de cheques con impresoras MICR específicas.

![Verifique las especificaciones de fuentes de seguridad.](media/font_check-security-font_Specifications.png "Verifique las especificaciones de fuentes de seguridad")

La especificación completa de las fuentes de comprobación de seguridad se puede encontrar en la documentación del proveedor aquí: (https://www.idautomation.com/security-fonts/).

Las fuentes para otros fines también están disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]. Para más información, consulte [Fuentes Disponibles](ui-fonts.md)

## <a name="see-also"></a>Consulte también
[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)  
[Fuentes en Business Central](ui-fonts.md)  
[Administrar pagos](payables-manage-payables.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)   
[Completar procesos de fin de periodo](year-how-complete-period-end-processes.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]