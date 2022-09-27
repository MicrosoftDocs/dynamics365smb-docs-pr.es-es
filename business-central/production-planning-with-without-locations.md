---
title: Planificación con o sin almacenes
description: En este tema, obtenga información sobre producción y fabricación, incluida la planificación de suministros, en Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/15/2022
ms.author: edupont
ms.openlocfilehash: 4bb3f626e02259171a9a1bf41c580f34aaa19758
ms.sourcegitcommit: 2396dd27e7886918d59c5e8e13b8f7a39a97075d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524543"
---
# <a name="planning-with-or-without-locations"></a>Planificación con o sin almacenes

Antes de comenzar a utilizar el motor de planificación, le recomendamos que decida si usará o no las ubicaciones. Hay dos formas sencillas principales:

* las líneas de demanda siempre incluyen códigos de almacén y el sistema utiliza unidades de almacenamiento por completo, incluida la configuración de almacén correspondiente. Obtenga más información en [Demanda en los almacenes](#demand-at-location).  
* Las líneas de demanda nunca llevan códigos de ubicación y el sistema utiliza la ficha de producto. Consulte el escenario [Demanda en una "ubicación en blanco"](#demand-at-blank-location) a continuación.

## <a name="demand-at-location"></a>Demanda en los almacenes  

Cuando el sistema de planificación detecta demanda en un almacén (una línea con un código de almacén), actuará de distinta forma dependiendo de 2 valores de configuración críticos.  

Durante la ejecución de la planificación, el programa comprueba los dos valores de configuración por orden y genera la planificación en consecuencia:  

1. ¿Existe un SKU para el artículo en la ubicación demandada?  

    En caso afirmativo:  

    El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento.  

    Si no es así:  

2. ¿El campo **Componentes en el almacén** en la página **Configuración fabricación** contiene el código de almacén solicitado?  

    En caso afirmativo:  

    El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

    Si no es así:  

    El artículo se planifica de acuerdo con la "alternativa mínima" que cubre la demanda exacta. Los parámetros de planificación se establecen como: Política reaprov. = *Lote a lote*, Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos. (Los artículos que usan la directiva de reaprovisionamiento *Pedido* siguen usando *Pedido*, así como las demás configuraciones).

> [!TIP]
> Si suele planificar la demanda en diferentes almacenes, le recomendamos que use la capacidad Uds. de almacenan y eviten la demanda en unbicación en blanco. Obtenga más información en [Configurar unidades de almacenamiento](inventory-how-to-set-up-stockkeeping-units.md)

Consulte las variaciones en los [escenarios siguientes](#scenarios).

> [!NOTE]
> El campo **Componentes en almacén** en la página **Configuración fabricación** es muy importante para controlar cómo el sistema de planificación gestiona las líneas de demanda de producción.
>
> En lo que se refiere a la demanda de producción, [!INCLUDE [prod_short](includes/prod_short.md)] usará para los componentes y el subensamblaje el almacén indicado en la orden de producción. Con todo, si rellena este campo, puede redirigir los componentes y el subensamblaje a otro almacén.
>
> También puede definir esto para una UA específica seleccionando un código de almacén diferente en el campo **Componentes en el almacén** de la ficha UA. Tenga en cuenta que esto no tiene mucho sentido, ya que la lógica de planificación se puede distorsionar al planificar el componente de la UA.

## <a name="demand-at-blank-location"></a>Demanda en almacén en blanco

En general, cuando el sistema de planificación detecta demanda en un almacén en blanco (una línea sin código de almacén), el artículo se planifica de acuerdo con los parámetros de planificación de la ficha de producto.

El **Almacén obligatorio** en la página **Configuración de inventario** y el campo **Componentes en el almacén** en la página **Configuración fabricación** o las unidades de almacenamiento afectarán a cómo el sistema de planificación maneja las líneas de demanda con/sin códigos de almacén. Si una de las siguientes afirmaciones es true, la demanda en almacén en blanco también se considera una desviación, y el sistema de planificación reaccionará aplicando la “alternativa mínima”. El producto se planificaría así: directiva de reaprovisionamiento = *lote por lote* (el *pedido* sigue siendo *pedido*), incluir inventario = *sí*, resto de parámetros de planificación = vacío.

* El campo **Componentes en almacén** en la página **Configuración fabricación** tiene un valor.
* Una unidad de almacenamiento exite para el producto planificado.
* Se selecciona el campo **Almacén obligatorio**.

## <a name="scenarios"></a>Escenarios

Consulte las variaciones en la configuración de escenarios siguiente.

### <a name="setup-1"></a>Configuración 1

* Almacén obligatorio = *Sí*  
* La unidad de almacenamiento está configurada en *WEST*  
* Componentes en alm. = *EAST*  

#### <a name="case-11-demand-is-at-west-location"></a>Caso 1.1: La demanda está en un almacén *WEST*

El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento (incluidas posibles transferencias).

#### <a name="case-12-demand-is-at-east-location"></a>Caso 1.2: La demanda está en un almacén *EAST*

El producto se planifica en función de los parámetros de planificación de la ficha del producto.

#### <a name="case-13-demand-is-at-north-location"></a>Caso 1.3: La demanda está en un almacén *NORTH*

El producto se planifica en función de los siguientes parámetros: Política reaprov. = *Lote a lote* (*Pedido* sigue siendo *Pedido*), Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos.

#### <a name="case-14-demand-is-at-blank-location"></a>Caso 1.4: La demanda está en un almacén *EN BLANCO*

El producto se planifica en función de los siguientes parámetros: Política reaprov. = *Lote a lote* (*Pedido* sigue siendo *Pedido*), Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos.

### <a name="setup-2"></a>Configuración 2

* Almacén obligatorio = *Sí*  
* No existe unidad de almacenamiento  
* Componentes en alm. = *EAST*  

#### <a name="case-21-demand-is-at-west-location"></a>Caso 2.1: La demanda está en un almacén *WEST*

El producto se planifica en función de los siguientes parámetros: Política reaprov. = *Lote a lote* (*Pedido* sigue siendo *Pedido*), Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos.

#### <a name="case-22-demand-is-at-east-location"></a>Caso 2.2: La demanda está en un almacén *EAST*

El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

### <a name="setup-3"></a>Configuración 3

* Almacén obligatorio = *No*  
* No existe unidad de almacenamiento  
* Componentes en alm. = *EAST*  

#### <a name="case-31-demand-is-at-west-location"></a>Caso 3.1: La demanda está en un almacén *WEST*

El producto se planifica en función de los siguientes parámetros: Política reaprov. = *Lote a lote* (*Pedido* sigue siendo *Pedido*), Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos.

#### <a name="case-32-demand-is-at-east-location"></a>Caso 3.2: La demanda está en un almacén *EAST*

El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

#### <a name="case-33-demand-is-at-blank-location"></a>Caso 3.3: La demanda está en un almacén *EN BLANCO*

El producto se planifica en función de los siguientes parámetros: Política reaprov. = *Lote a lote* (*Pedido* sigue siendo *Pedido*), Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos.

### <a name="setup-4"></a>Configuración 4

* Almacén obligatorio = *No*  
* No existe unidad de almacenamiento  
* Componentes en alm. = *EN BLANCO*  

#### <a name="case-41-demand-is-at-east-location"></a>Caso 4.1: La demanda está en un almacén *EAST*

El producto se planifica en función de los siguientes parámetros: Política reaprov. = *Lote a lote* (*Pedido* sigue siendo *Pedido*), Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos.

#### <a name="case-42-demand-is-at-blank-location"></a>Caso 4.2: La demanda está en un almacén *EN BLANCO*

El producto se planifica en función de los parámetros de planificación de la ficha del producto.

Como se puede ver en el último escenario, la única manera de conseguir un resultado correcto para una línea de demanda sin código de ubicación consiste en deshabilitar todos los valores de configuración relativos a los almacenes. De forma similar, la única manera de obtener resultados de planificación estables para la demanda en los almacenes es utilizar unidades de almacenamiento.  

Por tanto, si suele planificar la demanda en diferentes almacenes, le recomendamos que use la capacidad Uds. de almacenan.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/training/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also"></a>Consulte también .

[Planificación](production-planning.md)  
[Configurar fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Inventario](inventory-manage-inventory.md)  
[Configurar unidades de almacenamiento](inventory-how-to-set-up-stockkeeping-units.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)  
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
