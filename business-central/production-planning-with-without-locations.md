---
title: Planificación con o sin almacenes
description: En este tema, obtenga información sobre producción y fabricación, incluida la planificación de suministros, en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/16/2021
ms.author: edupont
ms.openlocfilehash: fa1b63bb94152c130077907dbe2d4e0d08281f40
ms.sourcegitcommit: acc1871afa889cb699e65b1b318028c05f8e6444
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2021
ms.locfileid: "6635996"
---
# <a name="planning-with-or-without-locations"></a>Planificación con o sin almacenes
En cuanto a la planificación con o sin códigos de almacén en las líneas de demanda, el programa de planificación funciona directamente cuando:  

-   las líneas de demanda siempre incluyen códigos de almacén y el sistema utiliza unidades de almacenamiento por completo, incluida la configuración de almacén correspondiente.  
-   las líneas de demanda nunca incluyen códigos de almacén y el sistema no utiliza unidades de almacenamiento ni configuración de almacén (consulte el último escenario más adelante).  

Sin embargo, si las líneas de demanda a veces incluyen códigos de almacén y en otras ocasiones no, el programa de planificación seguirá determinadas reglas dependiendo de la configuración.  

> [!TIP]
> Si suele planificar la demanda en diferentes almacenes, le recomendamos que use la capacidad Uds. de almacenan.

## <a name="demand-at-location"></a>Demanda en los almacenes  

Cuando el sistema de planificación detecta demanda en un almacén (una línea con un código de almacén), actuará de distinta forma dependiendo de 3 valores de configuración críticos.  

Durante la ejecución de la planificación, el programa comprueba los tres valores de configuración por orden y genera la planificación en consecuencia:  

1. ¿Hay una marca de verificación en el campo **Almacén obligatorio** en página **Configuración de inventario**?  

    En caso afirmativo:  

2. ¿Existe unidad de almacenamiento para el producto?  

    En caso afirmativo:  

    El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento.  

    Si no es así:  

3. ¿El campo **Componentes en el almacén** en la página **Configuración fabricación** contiene el código de almacén solicitado?  

    En caso afirmativo:  

    El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

    Si no es así:  

    El producto se planifica en función de los siguientes parámetros: Política reaprov. = *Lote a lote*, Incluir existencias = *Sí*, todos los demás parámetros de planificación = vacíos. (Los artículos que usan la directiva de reaprovisionamiento *Pedido* siguen usando *Pedido*, así como las demás configuraciones).  

> [!NOTE]  
> Esta alternativa mínima solo cubre la demanda exacta. Se omite cualquier otro parámetro de planificación definido.  

Consulte las variaciones en los escenarios siguientes.  

> [!TIP]
> El **Almacén obligatorio** en la página **Configuración de inventario** y el campo **Componentes en el almacén** en la página Configuración fabricación son muy importantes para decidir cómo el sistema de planificación maneja las líneas de demanda con/sin códigos de almacén.
>
> En el caso de la demanda de producción que se compra (cuando el motor de planificación se utiliza exclusivamente para planificación de compras y no para planificación de producción), [!INCLUDE [prod_short](includes/prod_short.md)] utilizará el mismo almacén que figura en la orden de producción para los componentes. Con todo, si rellena este campo, puede redirigir los componentes a otro almacén.
>
> También puede definir esto para una UA específica seleccionando un código de almacén diferente en el campo **Componentes en el almacén** de la ficha UA. Tenga en cuenta que esto no tiene mucho sentido, ya que la lógica de planificación se puede distorsionar al planificar el componente de la UA.

Otro campo importante es el campo **Cantidad máxima de pedido** en la ficha **Producto**. Especifica una cantidad máxima permitida para una propuesta de pedido de producto y se utiliza si el producto se entrega en una unidad de transporte fija, como un contenedor, que desea que se utilice por completo, por ejemplo. Una vez detectada la necesidad de reposición y ajustado el tamaño del lote para cubrir la política de reaprovisionamiento especificada, se disminuirá la cantidad, si es necesario, para cubrir la cantidad máxima de pedido que defina para el producto. Si se mantienen las demandas adicionales, se calcularán nuevos pedidos para cubrirlas. Por lo general, este campo se usa con una política de fabricación Fab-contra-stock.  

## <a name="demand-at-blank-location"></a>Demanda en "Almacén en blanco"  
Incluso aunque el cuadro de verificación **Almacén obligatorio** esté marcado, el sistema permitirá la creación de líneas de demanda sin código de almacén, lo que también se conoce como almacén *EN BLANCO*. Ésta es una desviación del sistema porque tiene diversos valores de configuración ajustados para tratar con los almacenes (consulte más arriba) y, como resultado, el motor de planificación no creará ninguna línea de planificación para dicha línea de demanda. Si no está marcado el campo **Almacén obligatorio**, pero existe cualquiera de los valores de configuración de almacén, la situación también se considera una desviación y el sistema de planificación reaccionará generando la "alternativa mínima":   
El producto se planifica según esta lógica: Política reaprov. =  *Lote a lote* ( *Pedido* sigue siendo *Pedido)*, Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.  

Consulte las variaciones en la configuración de escenarios siguiente.  

### <a name="setup-1"></a>Configuración 1:  

-   Almacén obligatorio = *Sí*  
-   La unidad de almacenamiento está configurada en  *ROJO*  
-   Componentes en alm. =  *AZUL*  

#### <a name="case-11-demand-is-at--red-location"></a>Caso 1.1: La demanda está en un almacén  *ROJO*  

El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento (incluidas posibles transferencias).  

#### <a name="case-12-demand-is-at--blue-location"></a>Caso 1.2: La demanda está en un almacén *AZUL*  

El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

#### <a name="case-13-demand-is-at--green-location"></a>Caso 1.3: La demanda está en un almacén  *VERDE*  

El producto se planifica en función de los siguientes parámetros: Política reaprov. =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.  

#### <a name="case-14-demand-is-at--blank-location"></a>Caso 1.4: La demanda está en un almacén  *EN BLANCO*  

El producto no se planifica porque no hay definido ningún almacén en la línea de demanda.  

### <a name="setup-2"></a>Configuración 2:  

-   Almacén obligatorio = *Sí*  
-   No existe unidad de almacenamiento  
-   Componentes en alm. =  *AZUL*  

#### <a name="case-21-demand-is-at--red-location"></a>Caso 2.1: La demanda está en un almacén  *ROJO*  

El producto se planifica en función de los siguientes parámetros: Política reaprov. =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.  

#### <a name="case-22-demand-is-at--blue-location"></a>Caso 2.2: La demanda está en un almacén *AZUL*  

El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

### <a name="setup-3"></a>Configuración 3:  

-   Almacén obligatorio = *No*  
-   No existe unidad de almacenamiento  
-   Componentes en alm. =  *AZUL*  

#### <a name="case-31-demand-is-at--red-location"></a>Caso 3.1: La demanda está en un almacén  *ROJO*  

El producto se planifica en función de los siguientes parámetros: Política reaprov. =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.  

#### <a name="case-32-demand-is-at--blue-location"></a>Caso 3.2: La demanda está en un almacén *AZUL*  

El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

#### <a name="case-33-demand-is-at--blank-location"></a>Caso 3.3: La demanda está en un almacén  *EN BLANCO*  

El producto se planifica en función de los siguientes parámetros: Política reaprov. =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.  

### <a name="setup-4"></a>Configuración 4:  

-   Almacén obligatorio = *No*  
-   No existe unidad de almacenamiento  
-   Componentes en alm. =  *EN BLANCO*  

#### <a name="case-41-demand-is-at--blue-location"></a>Caso 4.1: La demanda está en un almacén  *AZUL*  

El producto se planifica en función de los siguientes parámetros: Política reaprov. =  *Lote a lote* ( *Pedido* sigue siendo  *Pedido*), Incluir existencias =  *Sí*, todos los demás parámetros de planificación = vacíos.  

#### <a name="case-42-demand-is-at--blank-location"></a>Caso 4.2: La demanda está en un almacén  *EN BLANCO*  

El producto se planifica en función de los parámetros de planificación de la ficha del producto.  

Como se puede ver en el último escenario, la única manera de conseguir un resultado correcto para una línea de demanda sin código de ubicación consiste en deshabilitar todos los valores de configuración relativos a los almacenes. De forma similar, la única manera de obtener resultados de planificación estables para la demanda en los almacenes es utilizar unidades de almacenamiento.  

Por tanto, si suele planificar la demanda en diferentes almacenes, le recomendamos que use la capacidad Uds. de almacenan.  

## <a name="see-also"></a>Consulte también

[Planificación](production-planning.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Inventario](inventory-manage-inventory.md)  
[Configurar unidades de almacenamiento](inventory-how-to-set-up-stockkeeping-units.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)  
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]