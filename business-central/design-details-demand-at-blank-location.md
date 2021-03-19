---
title: 'Detalles de diseño: Aprovisionamiento y demanda | Documentos de Microsoft'
description: Este tema introduce el concepto de demanda, que es el término común usado para todo tipo de demanda bruta, como un pedido de venta o una necesidad de componente de una orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cbafba8d012244b10c142912b357188a1f7eece4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386954"
---
# <a name="design-details-demand-at-blank-location"></a>Detalles de diseño: Demanda en almacén vacío
Cuando un usuario crea un evento de demanda, como una línea de pedido de venta, unas veces el programa permite que especifique un código de almacén y otras no, es decir, usa un almacén en blanco.

En el caso de demanda con o sin códigos de almacén, el programa de planificación funciona directamente cuando:

- las líneas de demanda siempre incluyen códigos de almacén y el sistema utiliza unidades de almacenamiento por completo, incluida la configuración de almacén correspondiente.
- Las líneas de demanda nunca incluyen códigos de almacén y el sistema no utiliza unidades de almacenamiento ni configuración de almacén (consulte el último caso en la sección siguiente).

Sin embargo, si los eventos de demanda a veces incluyen códigos de almacén y en otras ocasiones no, el programa de planificación seguirá determinadas reglas dependiendo de la configuración.

## <a name="demand-at-location"></a>Demanda en los almacenes
Cuando el sistema de planificación detecta demanda en un almacén (una línea con un código de almacén), actuará de distinta forma dependiendo de tres valores de configuración críticos. Durante la ejecución de la planificación, el programa comprueba los tres valores de configuración por orden y genera la planificación en consecuencia:

1. ¿Tiene una marca de verificación el campo **Almacén obligatorio**?

    En caso afirmativo:

2. ¿Existe unidad de almacenamiento para el producto?

    En caso afirmativo:

    El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento.

    Si no es así:

3. ¿Contiene el campo Componentes en alm. el código de almacén que tiene la demanda?

  En caso afirmativo:

  El producto se planifica en función de los parámetros de planificación de la ficha del producto.

  Si no es así:

  El producto se planifica según estos parámetros: Política reaprov. = Lote por lote, Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos, productos que utilizan la política de reaprovisionamiento = El pedido continúa utilizando el pedido, así como los demás ajustes.

> [!NOTE]
> La configuración de planificación excepcional que se envía como la última reacción en el paso 3 anterior se denomina en adelante "alternativa mínima". Esta configuración de planificación solo cubre la demanda exacta y se omite todos los demás parámetros de planificación.

Para obtener información acerca de las variaciones de esta lógica de planificación, consulte la sección de casos a continuación.

## <a name="demand-at-blank-location"></a>Demanda en almacén en blanco
Incluso aunque el campo **Almacén obligatorio** esté marcado, el programa permitirá la creación de líneas de demanda sin código de almacén, lo que también se conoce como "almacén en blanco”. Ésta es una desviación del sistema porque tiene diversos valores de configuración ajustados para tratar con los almacenes (consulte más arriba) y, como resultado, el motor de planificación no creará ninguna línea de planificación para dicha línea de demanda.

Si el campo **Almacén obligatorio** no está seleccionado pero existe algún valor de configuración de almacén, también se considera una desviación, y el sistema de planificación reaccionará aplicando la “alternativa mínima”. El producto se planificaría así: directiva de reaprovisionamiento = lote por lote (el pedido sigue siendo pedido), incluir inventario = sí, resto de parámetros de planificación = vacío.

## <a name="scenarios"></a>Escenarios
En los escenarios siguientes se describen las variaciones de la demanda en el almacén en blanco y cómo resuelve el sistema de planificación la "alternativa mínima".

### <a name="setup-1"></a>Configuración 1:
Almacén obligatorio = Sí

La unidad de almacenamiento está configurada para ROJO

Componentes en almacén = AZUL

#### <a name="case-11-demand-is-at-red-location"></a>Caso 1.1: La demanda está en el almacén ROJO
El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento.

#### <a name="case-12-demand-is-at-blue-location"></a>Caso 1.2: La demanda está en el almacén AZUL
El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.

#### <a name="case-13-demand-is-at-green-location"></a>Caso 1.3: La demanda está en el almacén VERDE
El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.

#### <a name="case-14-demand-is-at-blank-location"></a>Caso 1.4: La demanda está en el almacén EN BLANCO
El producto no se planifica porque no hay definido ningún almacén en la línea de demanda.

### <a name="setup-2"></a>Configuración 2:
Almacén obligatorio = Sí

No existe unidad de almacenamiento

Componentes en almacén = AZUL

#### <a name="case-21-demand-is-at-red-location"></a>Caso 2.1: La demanda está en el almacén ROJO
El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.

#### <a name="case-22-demand-is-at-blue-location"></a>Caso 2.2: La demanda está en el almacén AZUL
El producto se planifica en función de los parámetros de planificación de la ficha del producto.

### <a name="setup-3"></a>Configuración 3:
Almacén obligatorio = No

No existe unidad de almacenamiento

Componentes en almacén = AZUL

#### <a name="case-31-demand-is-at-red-location"></a>Caso 3.1: La demanda está en el almacén ROJO
El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.

#### <a name="case-32-demand-is-at-blue-location"></a>Caso 3.2: La demanda está en el almacén AZUL
El producto se planifica en función de los parámetros de planificación de la ficha del producto.

#### <a name="case-33-demand-is-at-blank-location"></a>Caso 3.3: La demanda está en el almacén EN BLANCO
El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.

### <a name="setup-4"></a>Configuración 4:
Almacén obligatorio = No

No existe unidad de almacenamiento

Componentes en almacén = EN BLANCO

#### <a name="case-41-demand-is-at-blue-location"></a>Caso 4.1: La demanda está en el almacén AZUL
El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.

#### <a name="case-42-demand-is-at-blank-location"></a>Caso 4.2: La demanda está en el almacén EN BLANCO
El producto se planifica en función de los parámetros de planificación de la ficha del producto.

Como se ilustra en el último caso, la única manera de conseguir un resultado correcto para una línea de demanda sin código de ubicación consiste en deshabilitar todos los valores de configuración relativos a los almacenes. De forma similar, la única manera de obtener resultados de planificación estables para la demanda en los almacenes es utilizar unidades de almacenamiento (UA). Por consiguiente, si las empresas normalmente planifican la demanda en los almacenes, es muy recomendable utilizar el módulo Unidades de almacenamiento.

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]