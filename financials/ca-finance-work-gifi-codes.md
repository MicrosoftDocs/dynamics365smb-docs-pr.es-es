---
title: "Códigos GIFI en Canadá | Documentos de Microsoft"
Description: "En Canadá, puede configurar códigos GIFI (índice general de información financiera) y asignarlos a cuentas contables"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Procedimiento: Trabajar con los códigos GIFI en Canadá
La información fiscal puede incluir cuentas contables, informes, balances de ingresos, hojas de balance y extractos de remanentes. La información se fiscal clasifica mediante códigos. El uso de los códigos ayuda al director a procesar la información, a prepararse para el registro electrónico y a validar la información de impuestos electrónicamente. El uso de los códigos ayuda también a las organizaciones estadísticas a trabajar más eficazmente puesto que la información financiera es más fácilmente accesible. Para obtener más información, vea [la página web de la Agencia de Ingresos de Canadá](http://www.cra-arc.gc.ca/)

La Agencia de Ingresos de Canadá usa el código del Índice General de Información Financiera (GIFI) para recopilar, validar y procesar la información financiera y de impuestos electrónicamente. Se recomienda asignar códigos del GIFI únicamente a las cuentas auxiliares, de forma que todo se realice mediante el software de preparación de impuestos.

Cuando una cuenta está asociada a un código GIFI se informa a la agencia de ingresos que está bajo ese código. Varias cuentas pueden tener el mismo código GIFI pero cada cuenta solo puede tener un código.

Puede exportar la información del saldo con el código GIFI y guardar el archivo exportado en un Excel que será útil para transferir la información en el software de preparación de impuestos.

## <a name="to-set-up-gifi-codes"></a>Para configurar códigos GIFI
En Dynamics NAV deberá configurar los códigos GIFI para las cuentas contables, los informes, los balances de ingresos, las hojas de balance y los extractos de remanentes.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Códigos GIFI** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Códigos GIFI**, seleccione la acción **Nuevo**.
3. Configurar los códigos GIFI rellenando los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>Para asignar códigos GIFI a cuentas
Para realizar un informe sobre la información financiera por código GIFI, cada uno de éstos debe estar asociado con la cuenta apropiada en el plan de cuentas.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione una cuenta contable relevante y, a continuación, seleccione la acción **Editar**.
3. En la ficha desplegable **Contabilidad de costes**, en el campo **Código GIFI**, seleccione un código GIFI apropiado.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Para ver los saldos de la cuenta usando el informe del código GIFI
Puede revisar los saldos de su cuenta con el código GIFI usando el informe **Saldos de cuenta con código GIFI**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Saldos de cuenta con código GIFI** y, a continuación, seleccione el vínculo relacionado.
2. Especifique qué se debe incluir en el informe rellenando los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="to-export-balance-information-using-gifi-codes"></a>Para exportar información del saldo usando los códigos GIFI
Puede exportar la información del saldo usando los códigos GIFI y guardar el archivo exportado en Excel. Puede modificar, guardar o eliminar el archivo. Puede usar el archivo para transferir información sobre el software de preparación de impuestos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Exportar info. GIFI a Excel** y, a continuación, seleccione el vínculo relacionado.
2. Especifique que desea exportar a Excel rellenando los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Elija el botón **Aceptar**.

> [!NOTE]  
>   El archivo de Excel tiene las características siguientes:

* El saldo se redondea al porcentaje más próximo, pero el valor de celda mantiene el mismo como hace en la contabilidad general.
* Los números negativos se representan como número positivo entre corchetes. Por consiguiente, -123 se representa como (123).

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)   
[Configurar las finanzas](finance-setup-finance.md)

