---
title: 'Detalles de diseño: Ajuste de coste | Documentos de Microsoft'
description: El propósito principal del ajuste de coste es desviar los cambios de coste de los orígenes de coste a los destinatarios de coste, según la valoración de existencias de un producto, para proporcionar la valoración de inventario correcta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 85f8de1a0e3aadbf55fb8c4292aeb1e216817a23
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185641"
---
# <a name="design-details-cost-adjustment"></a>Detalles de diseño: Ajuste de coste
El propósito principal del ajuste de coste es desviar los cambios de coste de los orígenes de coste a los destinatarios de coste, según la valoración de existencias de un producto, para proporcionar la valoración de inventario correcta.  

Un producto puede ser facturado por venta antes de que se haya emitido factura de compra, de forma que el valor de inventario registrado por la venta no coincida con el coste real de compra. El ajuste del coste actualiza el coste de productos vendidos (CV) para garantizar que los registros históricos de venta coincidan con los costes de las transacciones de entrada a los que se aplican. Para obtener más información, consulte [Detalles de diseño: Liquidación de productos](design-details-item-application.md).  

A continuación, se indican los propósitos, o funciones, secundarios del ajuste de coste:  

* Facture las órdenes de producción terminadas:  

    * Cambiar el estado de registros de valor de **Previsto** a **Real**.  
    * Borrar cuentas WIP. Para obtener más información, consulte [Detalles de diseño: Registro de órdenes de producción](design-details-production-order-posting.md).  
    * Registrar desviación. Para obtener más información, consulte [Detalles de diseño: Desviación](design-details-variance.md).  

* Actualice el coste unitario que aparece en la ficha del producto.  

Los costes de inventario deben ajustarse antes de que los movimientos de valores relacionados se puedan conciliar con la contabilidad. Para obtener más información, consulte [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Detección del ajuste  
La tarea de detectar si se debe producir un ajuste del coste la lleva a cabo principalmente la rutina Diario de productos - Línea de registro, mientras que la tarea de calcular y generar los movimientos de ajuste de coste la realiza el proceso **Valorar stock - movs. producto**.  

Para poder desviar costes, el mecanismo de detección determina qué orígenes han cambiado en los costes y a qué destino se deben desviar dichos costes. Las tres funciones de detección siguientes existen en [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Liq. mov. producto  
* Punto de movimiento de ajuste de coste medio  
* Nivel de pedido  

### <a name="item-application-entry"></a>Liq. mov. producto  
Esta función de detección se usa para los productos que usan las valoraciones de existencias FIFO, LIFO, Estándar y Específica, y para los escenarios de liquidaciones fijas. La función funciona de la forma siguiente:  

* El ajuste de costes se detecta al marcar los movimientos de producto de origen como *Mov. liquidado a ajustar* cada vez que se registra un movimiento de producto o de valor.  
* El coste se desvía según los encadenamientos de coste registrados en la tabla **Liq. mov. producto**.  

### <a name="average-cost-adjustment-entry-point"></a>Punto de movimiento de ajuste de coste medio  
Esta función de detección se usa para los productos que usan la valoración de existencias Media. La función funciona de la forma siguiente:  

* El ajuste de costes se detecta al marcar un registro en la tabla **Punto de entrada aj. coste promedio** cada vez que se registra un movimiento de valor.  
* El desvío de coste se produce aplicando los costes a los movimientos de valor con fecha de valoración posterior.  

### <a name="order-level"></a>Nivel de pedido  
Esta función de detección se usa en escenarios de conversión, producción y ensamblado. La función funciona de la forma siguiente:  

* El ajuste de coste se detecta al marcar el pedido siempre que un recurso o un material se registra como consumido o utilizado.  
* El desvío de coste se produce aplicando los costes del material o recurso a los movimientos de salida asociados al mismo pedido.  

La función de nivel de pedido se usa para detectar los ajustes en el registro de ensamblado. En el gráfico siguiente se muestra la estructura del movimiento de ajuste:  

![Flujo de entradas en ajuste de costes](media/design_details_assembly_posting_3.png "Flujo de entradas en ajuste de costes")  

Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Ajuste de coste manual y automático  
El ajuste del coste se puede realizar de dos formas:  

* Esto se hace manualmente ejecutando el trabajo por lotes **Valorar stock - movs. producto**. Puede ejecutar este proceso para todos los productos o solo para determinados productos o categorías de productos. Este proceso ejecuta un ajuste de coste de los productos en inventario para los que se ha realizado una transacción de entrada, como una compra. En el caso de productos que utilizan el método de coste Promedio, el trabajo por lotes también hace un ajuste si se crean transacciones de salida.  
* Automáticamente, ajustando los costes cada vez que se registra una transacción de inventario y cuando se termina una orden de producción. El ajuste de coste solo se ejecuta para el producto o productos específicos afectados por el registro. Se configura al seleccionar la casilla **Ajuste automático coste** en la página **Configuración de inventario**.  

Es buena práctica ejecutar el ajuste del coste automáticamente cuando se registra, ya que los costes unitarios se actualizan con más frecuencia y por tanto son más exactos. La desventaja es que se puede ver afectado el rendimiento de la base de datos al ejecutar el ajuste de coste con tanta frecuencia.  

Dado que es importante mantener el coste unitario de un producto actualizado, se recomienda ejecutar el trabajo por lotes **Valorar stock - movs. producto** tan a menudo como sea posible, durante horas no laborables. También puede utilizar un ajuste automático del coste. De este modo se garantiza que el coste unitario se actualiza diariamente para los productos.  

Independientemente de si ejecuta el ajuste de costes manual o automáticamente, el proceso de ajuste y sus consecuencias son los mismos. [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula el valor de la transacción de entrada y desvía ese coste a cualquier transacción de salida, como ventas o consumos, que se hayan aplicado a la transacción de entrada. El ajuste de coste crea movimientos de valoración que contienen importes de ajuste e importes que compensan el redondeo.  

Los movimientos de nuevo ajuste y de valor de redondeo tienen la fecha de registro de la factura relacionada. Las excepciones son si los movimientos de valor entran en un periodo contable o un periodo de inventario cerrado o si la fecha de registro es anterior a la del campo **Permitir registro desde** en la página **Configuración de contabilidad**. Cuando esto se produce, el trabajo por lotes asigna la fecha de registro como la primera fecha del periodo abierto siguiente.  

## <a name="adjust-cost---item-entries-batch-job"></a>Proceso Valorar stock - movs. producto  
Al ejecutar el proceso **Valorar stock - movs. producto**, tiene la opción de ejecutar el proceso para todos los productos o solo para determinados productos o categorías.  

> [!NOTE]  
>  Se recomienda ejecutar siempre el proceso para todos los productos y usar solo la opción de filtrado para reducir el tiempo de ejecución del proceso o para corregir el coste de un determinado artículo.  

### <a name="example"></a>Ejemplo  
En el ejemplo siguiente se muestra si registra un producto comprado como recibido y facturado en 01-01-20. Después, registra el producto vendido como enviado y facturado el 15-01-20. A continuación, ejecute los procesos **Valorar stock - movs. producto** y **Reg. var. inventario en contabilidad**. Se crean los siguientes registros:  

**Movimientos valor**  

|Fecha registro|Tipo mov. producto|Importe coste (Real)|Coste regis. en contab.|Cantidad facturada|Nº mov.|  
|------------------|----------------------------|----------------------------|-------------------------|-----------------------|---------------|  
|01-01-20|Compra|10.00|10.00|1|1|  
|15-01-20|Venta|-10,00|-10,00|-1|2|  

**Movimientos de relación en C/G: tabla Relación movs. productos**  

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

**Movs. contabilidad**  

|Fecha registro|Cuenta|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Cuenta de inventario]|2130|10.00|1|  
|01-01-20|[Cuenta de coste directo aplicado]|7291|-10,00|2|  
|15-01-20|[Cuenta de inventario]|2130|-10,00|3|  
|15-01-20|[Cuenta de CV]|7290|10.00|4|  

Más tarde, se registra un cargo de producto de compra de 2,00 DL facturado en 10-02-20. Ejecute el proceso **Valorar stock - movs. producto** y, a continuación, **Reg. var. inventario en contabilidad**. El proceso de ajuste del coste ajusta el coste de la venta en 2,00 DL y el proceso **Reg. var. inventario en cont.** registra los nuevos movimientos de valoración en la contabilidad. El resultado es el siguiente.  

**Valor mov.**  

|Fecha registro|Tipo mov. producto|Importe coste (Real)|Coste regis. en contab.|Cantidad facturada|Ajuste|Nº mov.|  
|------------------|----------------------------|----------------------------|-------------------------|-----------------------|----------------|---------------|  
|10-02-20|Compra|2.00|2.00|0|No|3|  
|15-01-20|Venta|-2,00|-2,00|0|Sí|4|  

**Movimientos de relación en C/G: tabla Relación movs. productos**  

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|--------------------|---------------------|-----------------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

**Movs. contabilidad**  

|Fecha registro|Cuenta|Nº cuenta (demostración En-US)||Importe|Nº mov.|  
|------------------|------------------|---------------------------------|-|------------|---------------|  
|10-02-20|[Cuenta de inventario]|2130||2.00|5|  
|10-02-20|[Cuenta de coste directo aplicado]|7291||-2,00|6|  
|15-01-20|[Cuenta de inventario]|2130||-2,00|7|  
|15-01-20|[Cuenta de CV]|7290||2.00|8|  

## <a name="automatic-cost-adjustment"></a>Ajuste automático coste  
Para configurar que el ajuste de coste se ejecute automáticamente al registrar una transacción de inventario, utilice el campo **Ajuste automático coste** en la página **Configuración de inventario**. Este campo le permite seleccionar hasta qué punto en el pasado a partir de la fecha de trabajo actual desea que se realice el ajuste de coste. Las siguientes opciones están disponibles.  

|Opción|Description|  
|----------------------------------|---------------------------------------|  
|Nunca|Los costes no se ajustan al registrarlos.|  
|DÍA|Los costes se ajustan si el registro se produce en el plazo de un día a partir de la fecha de trabajo.|  
|Semana|Los costes se ajustan si el registro se realiza dentro de una semana a partir de la fecha de trabajo.|  
|Mes|Los costes se ajustan si el registro se realiza en el plazo de un mes a partir de la fecha de trabajo.|  
|Trimestre|Los costes se ajustan si el registro se lleva a cabo en el plazo de un trimestre a partir de la fecha de trabajo.|  
|Año|Los costes se ajustan si el registro se realiza en el plazo de un año a partir de la fecha de trabajo.|  
|Siempre|Los costes siempre se ajustan al registrarlos, independientemente de la fecha de registro.|  

La selección que elija en el campo **Ajuste automático coste** es importante para el rendimiento y la exactitud de sus costes. Los periodos de tiempo más breves, como **Día** o **Semana**, afectan menos al rendimiento del sistema porque proporcionan un requisito más estricto de que solo los costes registrados en el último día o en la última semana se pueden ajustar automáticamente. Esto significa que el ajuste de coste automático no se ejecuta con tanta frecuencia y, por lo tanto, afecta menos al rendimiento del sistema. No obstante, esto significa también que los costes unitarios pueden ser menos exactos.  

### <a name="example"></a>Ejemplo  
En el ejemplo siguiente se muestra un escenario de ajuste de coste automático:  

* El 10 de enero, registra un producto comprado como recibido y facturado.  
* El 15 de enero, registra un pedido de venta del producto como enviado y facturado.
* El 5 de febrero, recibe una factura de un cargo de flete de la compra original. Registra este cargo de flete, y lo aplica a la factura de compra original, lo que aumenta el coste de la compra original.  

Si ha configurado aplicar el ajuste automático del coste en los registros que se produzcan dentro de un mes o un trimestre a partir de la fecha de trabajo actual, el ajuste automático del coste ejecutará y desviará el coste de compra a la venta.  

Si ha configurado aplicar el ajuste automático del coste en los registros que se produzcan dentro de un día o una semana a partir de la fecha de trabajo actual, el ajuste automático del coste no se ejecutará, y el coste de compra no se desviará a la venta hasta ejecutar el trabajo por lotes **Valorar stock - movs. producto**.  

## <a name="see-also"></a>Consulte también
[Modificar costes de productos](inventory-how-adjust-item-costs.md)   
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
[Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md)   
[Detalles de diseño: Registro de inventario](design-details-inventory-posting.md)   
[Detalles de diseño: Desviación](design-details-variance.md)   
[Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md)   
[Detalles de diseño: Registro de órdenes de producción](design-details-production-order-posting.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
