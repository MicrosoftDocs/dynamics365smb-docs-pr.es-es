---
title: Descripción de la línea de registro en diario general | Documentos de Microsoft
description: Este tema introduce cambios en la codeunit 12, **Diario general-línea de registro**, que es el objeto principal de aplicación para el registro en contabilidad y es el único lugar donde insertar movimientos de contabilidad, de IVA, de clientes y de proveedores.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215258"
---
# <a name="general-journal-post-line-overview"></a>Descripción de la línea de registro en diario general

La codeunit 12, **Diario general-lín. reg.**, es el objeto principal de aplicación para el registro en contabilidad y es el único lugar donde insertar movimientos de contabilidad, de IVA, de clientes y de proveedores. Esta codeunit se usa también para todas las operaciones de Liquidar, Desliquidar y Revertir.  
  
En Microsoft Dynamics NAV 2013 R2, la codeunit se rediseñó porque se había vuelto muy grande, con aproximadamente 7600 líneas de código. La arquitectura había cambiado y la codeunit hizo más sencilla y más fácil de mantener. Esta documentación describe los cambios y proporciona información que necesitará para actualizar.  
  
## <a name="old-architecture"></a>Arquitectura antigua  
La arquitectura antigua tenía las características siguientes:  
  
* Se hacía un uso extensivo de variables globales, lo que aumentaba la posibilidad de que se produjeran errores ocultos por el uso de variables con ámbito incorrecto.  
* Había muchos procedimientos largos (con más de 100 líneas de código) que también tenían una elevada complejidad ciclomática (es decir, muchas declaraciones anidadas CASE, REPEAT e IF ), que hacían el código muy complicado de leer y mantener.  
* Varios procedimientos que solo se usaban localmente y solo debían usarse localmente no estaban marcados como locales.  
* La mayoría de los procedimientos no tenían parámetros y usaban variables globales. Algunos parámetros utilizados y variables globales reemplazadas con variables locales.  
* Los patrones de código para buscar las cuentas de contabilidad y crear movimientos de contabilidad y de IVA no estaban estandardizados y variaban de un lugar a otro. Además, se producían muchas duplicaciones de código y corrupciones de simetría entre el código del cliente y el del proveedor.  
* Una gran parte del código en la codeunit 12, aproximadamente el 30 por ciento, relacionado con los cálculos de descuento de pago y tolerancia, aunque estas características no se necesitan en muchos países o regiones.  
* Las funciones de Registro, Liquidar, Desliquidar, Revertir, Descuento de pago y Tolerancia y Ajuste tipo cambio se incluían todas en la codeunit 12 con una larga lista de variables globales.  
  
### <a name="new-architecture"></a>Nueva arquitectura  
En [!INCLUDE[prod_short](includes/prod_short.md)], la codeunit 12 incluye las mejoras siguientes:  
  
* La codeunit 12 se ha refactorizado en procedimientos más pequeños (todos con menos de 100 líneas de código).  
* Se han implementado patrones estandardizados para la búsqueda de cuentas de contabilidad mediante funciones de ayudante desde las tablas Grupo contable.  
* Se ha implementado un cuadro de motor de registro para gestionar el inicio y el fin de las transacciones y para aislar la creación en las entradas de IVA y de contabilidad, el cobro de ajustes de IVA y el cálculo de importes adicionales de divisa.  
* Se ha eliminado la duplicación del código.  
* Muchas funciones de ayuda se han transferido a las tablas correspondientes de movimientos de cliente y de proveedor.  
* El uso de variables globales se ha minimizado, de modo que cada procedimiento utiliza parámetros y encapsula su propia lógica de aplicación.  
  
## <a name="see-also"></a>Consulte también

[Detalles de diseño: estructura de interfaz de registro](design-details-posting-interface-structure.md)  
[Detalles de diseño: estructura de motor de registro](design-details-posting-engine-structure.md)  
[Detalles de diseño: línea de registro en diario general (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]