---
title: Actualizar los tipos de cambio de divisa | Documentos de Microsoft
description: "Para utilizar varias divisas en su empresa, puede configurar un código para cada divisa y usar un servicio externo para el tipo de cambio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: es-es
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a>Actualizar tipos cambio divisa
Las empresas trabajan cada vez en un mayor número de países o regiones, por lo que es muy importante que puedan comercializar y crear informes financieros en más de una divisa. Debe configurar un código por cada una de las divisas usadas en caso de que las operaciones de compra y venta se realicen en una divisa que no sea la divisa local (DL), tenga cobros y pagos en otras divisas o registre las transacciones de contabilidad en diferentes divisas.

La contabilidad se configura con la divisa local (DL), pero también se puede configurar para usarla en otra divisa a la que se asigna un tipo de cambio. Mediante la designación de una segunda divisa como la denominada divisa de informes adicional, [!INCLUDE[d365fin](includes/d365fin_md.md)] registrará automáticamente los importes tanto en la divisa local como en la divisa adicional en todos los movimientos de contabilidad y en otros movimientos, por ejemplo los del IVA. Para obtener más información, vea [Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Ajustar los tipos de cambio
Puesto que los tipos de cambio fluctúan constantemente, los equivalentes de la divisa adicional del sistema se deben ajustar regularmente. Si no se llevan a cabo estos ajustes, los importes que se hayan convertido desde divisas extranjeras (o adicionales) y registrado en contabilidad en la divisa local pueden ser erróneos. Además, los movimientos diarios registrados antes de que se introduzca el tipo de cambio del día en el programa se tienen que actualizar una vez que se haya introducido esta información. El proceso Ajustar tipos de cambio se usa para ajustar los tipos de cambio de los movimientos de clientes, proveedores y bancos. También sirve para actualizar los importes en la divisa adicional de los movimientos de contabilidad.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Para configurar un servicio de tipo de cambio de divisa
Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa como FloatRates.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Servicios de tipo de cambio de divisas** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Seleccione la casilla de verificación **Activado** para activar el servicio.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Para actualizar los tipos de cambio de divisa mediante un servicio
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Divisas** y luego elija el enlace relacionado.
2. Seleccione la acción **Actualizar tipos de cambio**.

El valor del campo **Tipo cambio** en la página **Divisas** se actualiza con el último tipo de cambio de divisa.

## <a name="see-also"></a>Consulte también
[Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

