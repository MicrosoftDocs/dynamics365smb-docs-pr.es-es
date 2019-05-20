---
title: Descripción de la línea de registro en diario general | Documentos de Microsoft
description: Este tema introduce cambios en la codeunit 12, **Diario general-línea de registro**, que es el objeto principal de aplicación para el registro en contabilidad y es el único lugar donde insertar movimientos de contabilidad, de IVA, de clientes y de proveedores.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5fac91190e5a4cea0648f618ea2a9af0afc65fb6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246552"
---
# <a name="general-journal-post-line-overview"></a>Descripción de la línea de registro en diario general
La codeunit 12, **Diario general-lín. reg.**, es el objeto principal de aplicación para el registro en contabilidad y es el único lugar donde insertar movimientos de contabilidad, de IVA, de clientes y de proveedores. Esta codeunit se usa también para todas las operaciones de Liquidar, Desliquidar y Revertir.  
  
Mientras que la codeunit se ha mejorado en cada versión durante los diez últimos años, su arquitectura seguía permaneciendo fundamentalmente invariable. La codeunit llegó a ser muy grande, con aproximadamente 7600 líneas de código. Con esta versión de [!INCLUDE[d365fin](includes/d365fin_md.md)], se ha cambiado la arquitectura y la codeunit se ha hecho más sencillo y más fácil de mantener. Esta documentación introduce los cambios y proporciona información que necesitará para actualizar.  
  
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
En [!INCLUDE[d365fin](includes/d365fin_md.md)], la codeunit 12 incluye las mejoras siguientes:  
  
* La codeunit 12 se ha refactorizado en procedimientos más pequeños (todos con menos de 100 líneas de código).  
* Se han implementado patrones estandardizados para la búsqueda de cuentas de contabilidad mediante funciones de ayudante desde las tablas Grupo contable.  
* Se ha implementado un cuadro de motor de registro para gestionar el inicio y el fin de las transacciones y para aislar la creación en las entradas de IVA y de contabilidad, el cobro de ajustes de IVA y el cálculo de importes adicionales de divisa.  
* Se ha eliminado la duplicación del código.  
* Muchas funciones de ayuda se han transferido a las tablas correspondientes de movimientos de cliente y de proveedor.  
* El uso de variables globales se ha minimizado, de modo que cada procedimiento utiliza parámetros y encapsula su propia lógica de aplicación.  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: estructura de interfaz de registro](design-details-posting-interface-structure.md)   
[Detalles de diseño: estructura de motor de registro](design-details-posting-engine-structure.md)
