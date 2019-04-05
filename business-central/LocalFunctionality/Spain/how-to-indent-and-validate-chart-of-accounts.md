---
title: Test y validación del plan de cuentas
description: En la página Ficha cuenta, se puede efectuar el test y la validación del plan de cuentas. Puede escribir 20 números como máximo. Las cuentas se ordenan según la cadena.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 437ca2ac6064065a0a0cbdf46ebf2db0c60301eb
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "827135"
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

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.  
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
