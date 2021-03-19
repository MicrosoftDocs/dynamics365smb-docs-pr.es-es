---
title: Configurar informes 340 para las empresas pequeñas
description: Utilice el siguiente procedimiento para configurar su negocio para que informe en efectivo, es decir, Criterios de contabilidad de efectivo (CAC). Si aún no lo ha hecho, puede configurar grupos de contabilización para la contabilización del IVA en efectivo para compras y ventas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6e224e2b2f6cf8a4ea171868dc1bc2baa68922b1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384058"
---
# <a name="set-up-340-reports-for-small-businesses"></a>Configurar informes 340 para las empresas pequeñas
Utilice el siguiente procedimiento para configurar su negocio para que informe en efectivo, es decir, Criterios de contabilidad de efectivo (CAC). Si aún no lo ha hecho, puede configurar grupos de contabilización para la contabilización del IVA en efectivo para compras y ventas.  

Cuando rellena un informe 340, se supone que todas las líneas de transacción que están asociadas con el IVA no liquidado se han llevado a cabo bajo contabilidad de efectivo.  

Después de que la contabilización del IVA esté configurada para manejar el IVA no liquidado, las órdenes de venta o compra impresas, se modificarán para que la siguiente etiqueta en negrita se agregue al informe justo antes de la sección que informa las líneas del documento: **Régimen especial del criterio de caja**.  

## <a name="to-set-up-reporting-under-cac"></a>Para configurar informes según el CAC  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de contabilidad** y luego elija el enlace relacionado.  
2.  En la página **Configuración de contabilidad**, en la ficha desplegable **General**, seleccione la casilla **IVA no realizado**. Elija el botón **Aceptar**.  
3.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. grupos registro IVA** y luego elija el enlace relacionado.  
4.  En la página **Config. grupos registro IVA**, seleccione un grupo para modificar o crear un grupo de registro que tenga cuentas contables generales para tratar los importes de IVA de las diversas cuentas de IVA no realizado en la configuración de grupos registro IVA y elija la acción **Editar**.  
5.  En la ficha desplegable **General**, defina **Tipo IVA no realizado** a **Porcentaje**.  
6.  En las fichas desplegables **Ventas** y **Compras**, puede especificar cuentas contables para los diversos campos **Cuenta IVA no realizado**.  

## <a name="see-also"></a>Consulte también  
[Crear informes de IVA para las autoridades fiscales](../../finance-how-report-vat.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]