---
title: 'Detalles de diseño: Liquidación de producto | Documentos de Microsoft'
description: En este tema se describe cómo se produce la liquidación de producto cuando se registra una transacción del inventario.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, item ledger, costing
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ddb2cd65abc96e27486782a1e9c9937858920f7c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "916425"
---
# <a name="design-details-item-application"></a>Detalles de diseño: Liquidación de productos
Cuando se registra una transacción de inventario, el registro de cantidad se guarda en los movimientos de producto y el registro de valor en los movimientos de valoración. Para obtener más información, consulte [Detalles de diseño: Registro de inventario](design-details-inventory-posting.md).  
  
Además, se hace una solicitud de producto para conectar al destinatario del coste con el origen del coste y hacer así un desvío de coste al método de coste. Para obtener más información, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] hace dos tipos de liquidación de productos.  
  
|Tipo de aplicación|Description|  
|----------------------|---------------------------------------|  
|Liquidación de cantidad|Creado para todas las transacciones de inventario|  
|Coste liquidación|Creado para registros de entrada junto con una liquidación de cantidad como resultado de la interacción del usuario en procesos especiales.|  
  
Las liquidaciones de producto se pueden crear de las siguientes formas.  
  
|Método|Description|Tipo de aplicación|  
|------------|---------------------------------------|----------------------|  
|Automática|Se produce como un desvío de coste general según la valoración de existencias|Liquidación de cantidad|  
|Fijo|Realizado por el usuario cuando:<br /><br /> -   Procesar devoluciones<br />-   Registrar correcciones<br />-   Procedimiento para deshacer registros de cantidades<br />-   Creación de los envíos directos **Nota**: La liquidación fija se puede realizar manualmente si especifica un número de movimiento en el campo **Liquid. de mov. pdto** o con una función, como **Revertir líneas documentos registrados**.|Liquidación de cantidad<br /><br /> Coste liquidación **Nota:** La liquidación del coste solo se produce en transacciones de entrada cuando el campo **Liquid. de mov. pdto** se rellena para crear una liquidación fija. Vea la tabla siguiente.|  
  
El hecho que de que se hagan liquidaciones de cantidad o de coste depende de la dirección de la transacción de inventario y de si la liquidación de producto se realiza de modo automático o fijo, en conexión con procesos especiales.  
  
En la tabla siguiente se muestra, según los campos de la aplicación central en las líneas de transacción de inventario, cómo fluyen los costes según la dirección de la transacción. También indica cuándo y por qué la liquidación del producto es de tipo cantidad o coste.  
  
||Campo Liq. por nº orden producto|Campo Liquid.-de mov. pdto|  
|-|--------------------------------|----------------------------------|  
|Aplicación de movimiento de salida|El movimiento de salida obtiene el coste del movimiento de entrada abierto.<br /><br /> **Liquidación de cantidad**|No compatible|  
|Aplicación de movimiento de entrada|El movimiento de entrada envía el coste al movimiento de salida abierto.<br /><br /> El movimiento de entrada es el origen de coste.<br /><br /> **Liquidación de cantidad**|El movimiento de entrada obtiene el coste del movimiento de salida. **Nota:** Al realizar esta liquidación fija, la transacción de entrada se trata como una devolución de venta. Por lo tanto, el movimiento de salida liquidado permanecerá abierto. <br /><br /> El movimiento de entrada NO es el origen de coste.<br /><br /> **Coste liquidación**|  
  
> [!IMPORTANT]  
>  Una devolución de venta NO se considera un origen de coste cuando se liquida de forma fija.  
>   
>  El movimiento de venta permanece abierto hasta que se registra el origen real.  
  
Un movimiento de liquidación de producto registra la siguiente información.  
  
|Campo|Description|  
|---------------------------------|---------------------------------------|  
|**Nº mov. producto**|el número del movimiento del producto para la cual se ha creado este movimiento de liquidación.|  
|**Nº mov. prod. entrada**|El número de movimiento de producto correspondiente a la entrada de existencias con el que debería vincularse la transacción (si es aplicable).|  
|**Nº mov. prod. salida**|El número de movimiento de producto correspondiente a la salida de existencias con el que debería vincularse la transacción (si es aplicable).|  
|**Cantidad**|la cantidad que desea aplicarse.|  
|**Fecha registro**|la fecha de la transacción.|  
  
## <a name="inventory-increase"></a>Entrada de existencias  
Cuando registra una entrada de existencias, se registra un único movimiento de liquidación de producto sin que exista una liquidación con un movimiento externo.  
  
### <a name="example"></a>Ejemplo  
En la tabla siguiente se muestra el movimiento de liquidación de producto que se crea al registrar un albarán de compra de 10 unidades.  
  
|Fecha reg.|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|Nº mov. producto|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
  
## <a name="inventory-decrease"></a>Salida de existencias  
Cuando registra una salida de existencias, se crea un movimiento de liquidación de producto que enlaza la salida de existencias con una entrada de existencias. Este vínculo se crea mediante la guía de la valoración de existencias del producto. En el caso de productos que usen métodos de coste FIFO, Estándar y Promedio, la vinculación se basa en el principio de "primero en entrar, primero en salir". La salida de existencias se aplica a la entrada de existencias con la fecha de registro más temprana. En el caso de productos que usen métodos de coste LIFO, la vinculación se basa en el principio de "último en entrar, primero en salir". La salida de existencias se aplica a la entrada de existencias con la fecha de registro más reciente.  
  
En la tabla **Mov. producto**, el campo **Cantidad pendiente** muestra la cantidad que todavía no se ha procesado. Si la cantidad pendiente es mayor que 0, se selecciona la casilla **Abrir**.  
  
### <a name="example"></a>Ejemplo  
El ejemplo a continuación muestra el movimiento de liquidación de producto creado cuando se registra un albarán de ventas de 5 de los productos que se recibieron en el ejemplo anterior. El primer movimiento de liquidación de producto es el albarán de compra. El segundo movimiento de liquidación es el albarán de venta.  
  
En la tabla siguiente se muestran los dos movimientos de liquidación de producto que son el resultado de la entrada de existencias y de la salida de existencias, respectivamente.  
  
|Fecha reg.|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|Nº mov. producto|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|03-01-20|1|2|-5|2|  
  
## <a name="fixed-application"></a>Liquidación fija  
Se realiza una liquidación fija cuando especifica que el coste de una entrada de existencias debería aplicarse a una salida de existencias específico o viceversa. La liquidación fija afecta a las cantidades restantes de los movimientos, pero también revierte el coste exacto del movimiento original que está liquidando.  
  
Para llevar a cabo una liquidación fija, deberá utilizar los campos **Liq. por nº orden producto** o **Liquid. de mov. pdto** situados en las líneas del documento para especificar el movimiento de producto al que desea aplicar la línea de transacción. Por ejemplo, podría realizar una liquidación fija cuando desee crear una liquidación de coste que especifique que debería aplicarse una devolución de ventas a un albarán de ventas concreto con el fin de invertir el coste de dicho albarán de ventas. En este caso, [!INCLUDE[d365fin](includes/d365fin_md.md)] ignorará el método de coste y aplicará la salida de existencias (o la entrada, en caso de tratarse de una devolución de ventas) al movimiento de producto que especifique. La ventaja de llevar a cabo una liquidación fija, es que el coste de la transacción original se pasa a la nueva transacción.  
  
### <a name="example--fixed-application-in-purchase-return"></a>Ejemplo: Liquidación fija en devolución de compra  
El ejemplo siguiente, en el que se ilustra el efecto de la liquidación fija de una devolución de compra de un producto mediante la valoración de existencias FIFO, se basa en el escenario siguiente:  
  
1. En el número de movimiento 1, el usuario registra una compra en un coste de 10,00 DL.  
2. En el número de movimiento 2, el usuario registra una compra en un coste de 20,00 DL.  
3. En el número de movimiento 3, el usuario registra una devolución de compra. El usuario realiza una liquidación fija en la segunda compra al introducir el número de movimiento de producto en el campo **Liq. por nº orden producto** en la línea de pedido de devolución de compra.  
  
En la tabla siguiente se muestran los movimientos de producto como consecuencia del escenario.  
  
|**Fecha reg.**|**Tipo mov. producto**|**Cantidad**|**Importe coste (real)**|**Nº mov. producto**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|04-01-20|Compra|10|10.00|1|  
|05-01-20|Compra|10|20.00|2|  
|06-01-20|Compras (devolución)|-10|-20,00|3|  
  
Ya que la liquidación fija se realiza desde la devolución de compra al registro de la segunda compra, los productos se devuelven con el coste correcto. Si el usuario no hubiera realizado la liquidación fija, el producto devuelto se habría valorado incorrectamente en DL 10,00, ya que la devolución habría sido aplicada al primer registro de compra según el método FIFO.  
  
En la tabla siguiente se muestra el movimiento de liquidación de producto que es el resultado de la liquidación fija.  
  
|Fecha reg.|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|Nº mov. producto|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|06-01-20|1|3|10|3|  
  
A continuación, el coste de la segunda compra, DL 20,00, se pasará correctamente a la devolución de la compra.  
  
### <a name="example--fixed-application-with-average-cost"></a>Ejemplo: Liquidación fija con coste medio  
El ejemplo siguiente, en el que se ilustra el efecto de la liquidación fija, se basa en el escenario siguiente de un producto que usa la valoración de existencias Media:  
  
1. En los números de movimiento 1 y 2, el usuario registra dos facturas de compra. La segunda factura tiene el coste unitario directo incorrecto de 1000,00 DL.  
2. En el número de movimiento 3, el usuario registra un abono de compra con una liquidación fija aplicada al movimiento de compra con el coste unitario directo incorrecto. La suma para el campo **Importe coste (real)** para los dos movimientos de valoración de liquidación fija se convierte en 0,00  
3. En el número de movimiento 4, el usuario registra otra factura de compra con el coste unitario directo correcto de DL 100,00  
4. En el número de movimiento 5, el usuario registra una factura de venta.  
5. La cantidad de inventario es 0 y el valor de inventario también es 0,00  
  
En la tabla siguiente se muestra el resultado del escenario en los movimientos de valoración del producto.  
  
|Fecha reg.|Tipo mov. producto|Cdad. valorada|Importe coste (real)|Liq. por nº orden producto|Valorado a coste medio|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compra|1|200.00||N.º|1|1|  
|01-01-20|Compra|1|1000.00||No|2|2|  
|01-01-20|Compra|-1|-1000|2|No|3|3|  
|01-01-20|Compra|1|100.00||No|4|4|  
|01-01-20|Venta|-2|-300,00||Sí|5|5|  
  
Si el usuario no hubiera realizado la liquidación fija entre el abono de compra y la compra con el precio de compra incorrecto (paso 2 en el caso anterior), el coste se habría ajustado de forma distinta.  
  
En la tabla siguiente se muestra el resultado en los movimientos de valoración del producto si el paso 2 del escenario anterior se lleva a cabo mediante una liquidación fija.  
  
|Fecha reg.|Tipo mov. producto|Cdad. valorada|Importe coste (real)|Liq. por nº orden producto|Valorado a coste medio|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compra|1|200.00||N.º|1|1|  
|01-01-20|Compra|1|1000.00||No|2|2|  
|01-01-20|Compra|-1|433,33||Sí|3|3|  
|01-01-20|Compra|1|100.00||No|4|4|  
|01-01-20|Venta|-2|866,67||Sí|5|5|  
  
En la entrada número 3, el valor del campo **Importe coste (real)** se valora por promedio, y por tanto incluye el registro erróneo de 1000,00. Así pues, se convierte en -433,33, que es un coste excesivo. El cálculo es 1300 / 3 = .-433,33.  
  
En el número de movimiento 5, el valor del campo **Importe coste (real)** para esta entrada es también incorrecto por la misma razón.  
  
> [!NOTE]  
>  Si crea una liquidación fija para una salida de existencias para un producto que utiliza el método de coste Promedio, esta salida no recibirá el coste medio para el producto de la forma habitual, si no que recibirá el coste de la entrada de existencias que haya especificado. Dicha salida ya no formará parte del cálculo del coste medio.  
  
### <a name="example--fixed-application-in-sales-return"></a>Ejemplo: Liquidación fija en devolución de venta  
Las liquidaciones fijas también son un método muy válido para revertir el coste con exactitud, por ejemplo con devoluciones de ventas.  
  
El ejemplo siguiente, en el que se ilustra cómo una liquidación fija garantiza una reversión de coste exacta, se basa en el escenario siguiente:  
  
1. El usuario registra una factura de compra.  
2. El usuario registra una factura de venta.  
3. El usuario registra un abono de venta para el producto devuelto, que se aplica al movimiento de venta, para revertir el coste correctamente.  
4. Llega un coste de flete relacionado con el pedido de compra registrado anteriormente. El usuario lo registra como un cargo de producto.  
  
En la tabla siguiente se muestra el resultado de los pasos 1 a 3 del escenario en los movimientos de valoración del producto.  
  
|Fecha reg.|Tipo mov. producto|Cdad. valorada|Importe coste (real)|Liquid.-de mov. pdto|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compra|1|1000.00||1|1|  
|01-02-20|Venta|-1|1000.00||2|2|  
|01-03-20|Venta (abono)|1|1000|2|3|3|  
  
En la tabla siguiente se muestra el movimiento de valoración que es el resultado del paso 4 del escenario, registro del cargo de producto.  
  
|Fecha reg.|Tipo mov. producto|Cdad. valorada|Importe coste (real)|Liquid.-de mov. pdto|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-04-20|(Cargo de producto)|1|100.00||1|4|  
  
En la tabla siguiente se muestra el efecto de la reversión de coste exacta en los movimientos de valoración del producto.  
  
|Fecha reg.|Tipo mov. producto|Cdad. valorada|Importe coste (real)|Liquid.-de mov. pdto|Nº mov. producto|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Compra|1|1000.00||1|1|  
|01-02-20|Venta|-1|1100.00||2|2|  
|01-03-20|Venta (abono)|1|1100.00|2|3|3|  
|01-04-20|(Cargo de producto)|1|100.00||1|4|  
  
Al ejecutar el proceso **Valorar stock - movs. producto**, el aumento de coste del movimiento de compra, debido al cargo de producto, se desvía al movimiento de venta (número de movimiento 2). A continuación, el movimiento de venta desvía este aumento de coste al movimiento de abono de venta (movimiento número 3). El resultado final es que el coste se revierte correctamente.  
  
> [!NOTE]  
>  Si está trabajando con reembolsos o abonos y ha configurado el campo **Coste exacto devolución obligatorio** en la página **Configuración compras y pagos** o en la página **Configuración ventas y cobros**, según corresponda en su caso, [!INCLUDE[d365fin](includes/d365fin_md.md)] rellenará automáticamente los distintos campos de registro al usar la función **Copiar documento**. Si utiliza la función **Revertir líneas documentos registrados**, el programa siempre rellenará esos campos automáticamente.  
  
> [!NOTE]  
>  Si registra una transacción con una liquidación fija y el movimiento de producto al que lo está aplicando está cerrado (lo que significa que la cantidad restante es cero), el programa deshará automáticamente la liquidación anterior y volverá a aplicar el movimiento del producto utilizando la liquidación fija que ha especificado.  
  
## <a name="transfer-application"></a>Solicitud de transferencia  
Cuando un producto se transfiere de una ubicación a otra, dentro del inventario de la empresa, se crea una liquidación entre los dos movimientos de transferencia. La valoración de un movimiento de transferencia depende de la valoración de existencias. En el caso de productos con método de coste Promedio, la valoración se lleva a cabo mediante el coste promedio en el periodo de coste medio en el que tiene lugar la fecha de valoración de la transferencia. En el caso de productos con otros métodos de coste, la valoración se lleva a cabo realizando un seguimiento retroactivo hasta el coste de la entrada de existencias original.  
  
### <a name="example--average-costing-method"></a>Ejemplo: Método de coste promedio  
El ejemplo siguiente, en el que se ilustra cómo se liquidan los movimientos de transferencia, se basa en el escenario siguiente de un producto que usa la valoración de existencias Media y un periodo de coste medio de un día.  
  
1. El usuario compra el producto con un coste de 10,00 DL.  
2. El usuario vuelve a comprar el producto con un coste de 20,00 DL.  
3. El usuario transfiere el producto de la ubicación AZUL a la ROJA.  
  
En la tabla siguiente se muestra el efecto de la transferencia en los movimientos de valoración del producto.  
  
|Fecha reg.|Tipo mov. producto|Cód. almacén|Cdad. valorada|Importe coste (real)|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Compra|AZUL|1|10.00|1|  
|01-01-20|Compra|AZUL|1|20.00|2|  
|01-02-20|Transferencia|AZUL|-1|15.00|3|  
|01-02-20|Transferencia|ROJO|1|15.00|4|  
  
### <a name="example--standard-costing-method"></a>Ejemplo: Método de coste Estándar  
El ejemplo siguiente, en el que se ilustra cómo se liquidan los movimientos de transferencia, se basa en el escenario siguiente de un producto que usa la valoración de existencias Estándar y un periodo de coste medio de un día.  
  
1. El usuario compra el producto con un coste estándar de 10,00 DL.  
2. El usuario transfiere el producto de la ubicación AZUL a la ROJA con un coste estándar de 12,00 DL.  
  
En la tabla siguiente se muestra el efecto de la transferencia en los movimientos de valoración del producto.  
  
|Fecha reg.|Tipo mov. producto|Cód. almacén|Cdad. valorada|Importe coste (real)|N.º de movimiento|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Compra|AZUL|1|10.00|1|  
|01-02-20|Transferencia|AZUL|-1|10.00|2|  
|01-02-20|Transferencia|ROJO|1|10.00|3|  
  
Como el valor de la entrada de existencias original es 10,00 DL, la transferencia se valora en ese coste, no en 12,00 DL.  
  
## <a name="reapplication"></a>Nueva liquidación  
Debido a la forma en la que se calcula el coste unitario de un producto, una liquidación de producto que sea incorrecta podría resultar en un coste medio sesgado y en un coste unitario también sesgado. Los escenarios siguientes pueden provocar liquidaciones de producto incorrectas, lo que requiere deshacerlas y volver a liquidar los movimientos de producto:  
  
* Ha olvidado realizar una liquidación fija.  
* Ha realizado una liquidación fija incorrecta.  
* Desea invalidar la liquidación creada automáticamente al efectuar el registro, según la valoración de existencias del producto.  
* Tiene que devolver un producto al que ya se le ha aplicado una ventana, sin usar la función **Revertir líneas documentos registrados** y, por lo tanto, debe deshacer la liquidación.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] ofrece una característica para analizar y corregir las liquidaciones de productos. Este trabajo se realiza en la página **Hoja liquidación**.  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Métodos de coste](design-details-costing-methods.md)  
[Detalles de diseño: Coste medio](design-details-average-cost.md)  
[Detalles de diseño: Ajuste de coste](design-details-cost-adjustment.md)  
