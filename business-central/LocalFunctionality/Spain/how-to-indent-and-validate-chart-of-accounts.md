---
title: Test y validación del plan de cuentas
description: En la página Ficha cuenta, se puede efectuar el test y la validación del plan de cuentas. Puede escribir 20 números como máximo. Las cuentas se ordenan según la cadena.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d262a354d94e540eaa59d60e66dc09a69529d105
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382053"
---
# <a name="indent-and-validate-chart-of-accounts"></a>Efectuar el test y la validación del plan de cuentas
En la página **Ficha cuenta**, se puede efectuar el test y la validación del plan de cuentas. Puede escribir 20 números como máximo. Las cuentas se ordenan según la cadena, como se muestran en el siguiente ejemplo.  

1  
10  
101  
2  
20  
2100001  
3  
31  

## <a name="to-indent-and-validate-the-chart-of-accounts"></a>Para efectuar el test y la validación del plan de cuentas  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  En la ficha desplegable **General**, en el campo **Nº** escriba el número de la cuenta de contabilidad que está configurando.  
4.  En el campo **Tipo mov.**, seleccione **Registro** o **Mayor**. **Registro** implica que se pueden registrar movimientos en la cuenta. **Mayor** implica que no se pueden registrar movimientos en la cuenta.  

    > [!NOTE]  
    >  Para Portugal, seleccione **Registro** o **Total** en el campo **Tipo mov**.  

5.  En el campo **Cta. regularización**, seleccione la cuenta a la que se enviarán los cambios después de la corrección.  
6.  Escriba información en el resto de campos relevantes.  
7.  Elija el botón **Aceptar** para cerrar la página **Ficha cuenta**.  
8.  En la página **Plan de cuentas**, seleccione una cuenta y, a continuación, elija **Test plan de cuentas**.  
9. Para validar el plan de cuentas, elija el botón **Sí** en el cuadro de diálogo. Una vez validado, se le notificará si el plan de cuentas es correcto.  
10. Elija el botón **Aceptar**.  

## <a name="to-validate-the-chart-of-accounts-in-portugal"></a>Para efectuar la validación del plan de cuentas en Portugal  

1.  En la página **Plan de cuentas**, seleccione la acción **Comprobar Plan de cuentas**.  
2.  Elija el botón **Sí**.  

## <a name="see-also"></a>Consulte también  
[Funcionalidad local para España](spain-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]