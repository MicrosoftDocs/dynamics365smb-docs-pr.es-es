---
title: 'Detalles de diseño: Registro de pedidos de ensamblado | Documentos de Microsoft'
description: El registro de pedidos de ensamblado se basa en los mismos principios que al registrar las actividades similares de los pedidos de venta y el consumo o la salida de producción. No obstante, los principios que se agrupan en los pedidos de ensamblado tienen su propia IU de registro, como para los pedidos de venta, mientras que el registro real de movimientos se produce en segundo plano como registro de productos directos y registro de diario de recursos, como con el de consumo, la salida y la capacidad de producción.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a26cafc11479d7065645947f63fa93d28ddb824f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246022"
---
# <a name="design-details-assembly-order-posting"></a>Detalles de diseño: Registro de pedidos de ensamblado
El registro de pedidos de ensamblado se basa en los mismos principios que al registrar las actividades similares de los pedidos de venta y el consumo o la salida de producción. No obstante, los principios que se agrupan en los pedidos de ensamblado tienen su propia IU de registro, como para los pedidos de venta, mientras que el registro real de movimientos se produce en segundo plano como registro de productos directos y registro de diario de recursos, como con el de consumo, la salida y la capacidad de producción.  

Al igual que el registro de orden de producción, se convierten los componentes consumidos y los recursos usados, y se envían como el elemento del ensamblado cuando se registra el pedido de ensamblado. Para obtener más información, consulte [Detalles de diseño: Registro de órdenes de producción](design-details-production-order-posting.md). No obstante, el flujo del coste para los pedidos de ensamblado es menos complejo, especialmente porque el registro de coste de ensamblado solo se produce una vez, y por tanto que no genera un inventario de trabajo en curso.  

Los siguientes registros de diario se producen durante el registro de pedido de ensamblado:  

-   El diario de productos registra los movimientos de producto positivos, que representan la salida del elemento del ensamblado, del encabezado de pedido de ensamblado.  
-   El diario de productos registra los movimientos de producto negativos, que representan el consumo de componentes de ensamblado, de las líneas de pedido de ensamblado.  
-   El diario de recursos registra el uso de recursos de ensamblado (unidades de tiempo) de las líneas de pedido de ensamblado.  
-   El diario de capacidad registra los movimientos de valoración relativos al uso de recursos a partir de las líneas de pedido de ensamblado.  

En el diagrama siguiente se muestran la estructura del producto y los movimientos de recursos resultantes del registro de pedido de ensamblado.  

![Movimientos de producto, recurso y capacidad resultantes del registro de pedido de ensamblado](media/design_details_assembly_posting_1.png "Movimientos de producto, recurso y capacidad resultantes del registro de pedido de ensamblado")  

> [!NOTE]  
>  Se incluyen los centros de máquina y de trabajo para ilustrar que los movimientos de capacidad se crean a partir de la producción y del ensamblado.  

En el diagrama siguiente se muestra cómo los datos del ensamblado fluyen en los movimientos durante el registro:  

![Flujo de movimiento relacionado con el ensamblado durante la publicación](media/design_details_assembly_posting_2.png "Flujo de movimiento relacionado con el ensamblado durante la publicación")  

## <a name="posting-sequence"></a>Secuencia de registro  
El registro de un pedido de ensamblado se produce en el orden siguiente:  

1.  Se registran las líneas del pedido de ensamblado.  
2.  Se registra el encabezado de pedido de ensamblado.  

En la tabla siguiente se describe la secuencia de las acciones.  

|Acción|Description|  
|------------|-----------------|  
|Inicializar registro|1. Haga las comprobaciones preliminares.<br />2. Agregue el número de registro y edite la cabecera del pedido de ensamblado.<br />3. Lance el pedido de ensamblado.|  
|Envíos postales|<ol><li>Crear la cabecera de pedido de ensamblado registrado.</li><li>Copiar líneas de comentario.</li><li>Registre las líneas del pedido de ensamblado (consumo):<br /><br /> <ol><li>Crear una página de estado para calcular el consumo de ensamblado.</li><li>Obtener la cantidad pendiente en la que se basará la línea de diario de productos.</li><li>Restablezca las cantidades consumidas y restantes.</li><li>Para líneas de pedido de ensamblado de tipo Producto:<br /><br /> <ol><li>Rellene los campos de la línea de diario de productos.</li><li>Transfiera las reservas a la línea de diario de productos.</li><li>Registre la línea del diario de productos para crear los movimientos de producto.</li><li>Crear líneas de diario de almacén y registrarlas.</li></ol></li><li>Para líneas de pedido de ensamblado de tipo Recurso:<br /><br /> <ol><li>Rellene los campos de la línea de diario de productos.</li><li>Registrar la línea del diario de productos. Esto crea movimientos de capacidad.</li><li>Crear y registrar línea de diario de recursos.</li></ol></li><li>Transfiera los valores de campo desde la línea de pedido de ensamblado a una nueva línea de pedido de ensamblado registrado creado recientemente.</li></ol></li><li>Registre el encabezado de pedido de ensamblado (salida):<br /><br /> <ol><li>Rellene los campos de la línea de diario de productos.</li><li>Transfiera las reservas a la línea de diario de productos.</li><li>Registre la línea del diario de productos para crear los movimientos de producto.</li><li>Crear líneas de diario de almacén y registrarlas.</li><li>Restablezca las cantidades de ensamblado y las cantidades restantes.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  A diferencia de la salida de producción, que se registra al coste previsto, la salida de ensamblado se registra al coste real.  

## <a name="cost-adjustment"></a>Ajuste de coste  
 Después de que se registra un pedido de ensamblado, lo que significa que los componentes (material) y los recursos se ensamblan en un nuevo producto, se debe poder determinar el coste real del elemento del ensamblado y el coste de inventario real de los componentes que intervienen. Se logra mediante el desvío de los costes de los movimientos registrados del origen (componentes y recursos) a los movimientos registrados del destino (elemento del ensamblado). El desvío de los costes se realiza mediante el cálculo y la generación de nuevos movimientos, denominados movimientos de ajuste que se asocian con los movimientos de destino.  

 Los costes de ensamblado que se desviarán se detectan con el mecanismo de detección de nivel de pedido. Para obtener información acerca de otros mecanismos de detección de ajustes, consulte [Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md).  

### <a name="detecting-the-adjustment"></a>Detección del ajuste  
La función de detección de nivel de pedido se usa en escenarios de conversión, producción y ensamblado. La función funciona de la forma siguiente:  

-   El ajuste de coste se detecta al marcar el pedido siempre que un recurso o un material se registra como consumido o utilizado.  
-   El desvío de coste se produce aplicando los costes del material o recurso a los movimientos de salida asociados al mismo pedido.  

En el gráfico siguiente se muestra la estructura del movimiento de ajuste y cómo se ajustan los costes de ensamblado.  

![Flujo de movimiento relacionado con el ensamblado durante el ajuste de coste](media/design_details_assembly_posting_3.png "Flujo de movimiento relacionado con el ensamblado durante la publicación")  

### <a name="performing-the-adjustment"></a>Realizar el ajuste  
La distribución de los ajustes detectados de la lista de materiales y los costes de recursos en los movimientos de salida de ensamblado se lleva a cabo mediante el proceso **Valorar stock - movs. producto**. Contiene la función para aplicar ajustes de multinivel, que consta de los dos elementos siguientes:  

-   Realizar el ajuste de pedido de ensamblado, que desvía el coste de la utilización de materiales y de recursos al movimiento de salida de ensamblado. Las líneas 5 y 6 del algoritmo siguiente son las responsables.  
-   Realizar los ajustes de nivel individual, que desvía los costes de los productos individuales mediante su valoración de existencias. Las líneas 9 y 10 del algoritmo siguiente son las responsables.  

![Resumen del algoritmo de ajuste de costes del registro de montaje](media/design_details_assembly_posting_4.jpg "Resumen del algoritmo de ajuste de costes del registro de montaje")  

> [!NOTE]  
>  El elemento Realizar ajustes de trabajo en curso, en las líneas 7 y 8, es responsable de enviar el material de producción y el uso de capacidad a la salida de las órdenes de producción finalizar. No se usa al ajustar los costes del pedido de ensamblado ya que el concepto de trabajo en curso no aplica al ensamblado.  

Para obtener más información acerca de cómo se registran costes de ensamblado y de producción en la contabilidad, consulte [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>Los costes de ensamblado son siempre reales  
 El concepto de trabajo en curso (WIP) no se aplica al registro de pedido de ensamblado. Los costes de ensamblado se registran solo como coste real, nunca como coste previsto. Para obtener más información, consulte [Detalles de diseño: Registro de coste previsto](design-details-expected-cost-posting.md).  

Eso se habilita mediante la estructura de datos siguiente.  

-   En el campo **Tipo** en las líneas de diario del producto, en las tablas **Movs. capacidad** y **Movimiento valor** se usa *Recurso* para identificar los movimientos del recurso de ensamblado.  
-   En el campo **Tipo mov. producto** en las líneas de diario del producto, en las tablas **Movs. capacidad** y **Movimiento valor**, se utilizan *Salida de ensamblado* y *Consumo de ensamblado* para identificar los movimientos del producto de ensamblado de salida y los movimientos de componentes de ensamblado consumidos respectivamente.  

Además, los campos del grupo contable de la cabecera de pedido de ensamblado y las líneas de pedido de ensamblado se rellenan de forma predeterminada como sigue.  

|Entidad|Escriba|IVA prod. genér.|Grupo contable producto|  
|------------|----------|-------------------|------------------------------|  
|Cabecera de pedido de ensamblado|Producto|Grupo contable existencias|Grupo contable producto|  
|Línea de pedido ensamblado|Producto|Grupo contable existencias|Grupo contable producto|  
|Línea de pedido ensamblado|Recurso||Grupo contable producto|  

Por consiguiente, en la contabilidad solo se registran los costes reales, y no se rellena ninguna cuenta provisional a partir del registro de pedidos de ensamblado. Para obtener más información, consulte [Detalles de diseño: cuentas en la contabilidad](design-details-accounts-in-the-general-ledger.md).  

## <a name="assemble-to-order"></a>Ensamblar para pedido  
El movimiento de producto obtenido como consecuencia de registrar una venta de ensamblar para pedido se liquida de forma fija en el movimiento de producto relacionado para la salida de ensamblado. Por consiguiente, el coste de una venta de ensamblar para pedido se obtiene del pedido de ensamblado con el que está vinculado.  

Los movimientos de producto del tipo Venta resultantes del registro de las cantidades de ensamblar para pedido se marcan con **Sí** en el campo **Ensamblar para pedido**.  

El registro de las líneas de pedido de venta donde una parte es cantidad de inventario y otra parte es cantidad ensamblar para pedido genera movimientos de producto independientes, uno para la cantidad de inventario y otro para la cantidad de ensamblar para pedido.  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Detalles de diseño: Registro de órdenes de producción](design-details-production-order-posting.md)   
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md)  
 [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
