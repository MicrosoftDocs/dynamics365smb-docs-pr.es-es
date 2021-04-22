---
title: 'Detalles de diseño: Estructura de tabla | Documentos de Microsoft'
description: Para conocer cómo se ha rediseñado el almacenamiento y el registro de movimientos de dimensión, es importante entender la estructura de tabla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e118b27d1bafc4de1ffc8d2db4597317942b6f65
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777703"
---
# <a name="design-details-table-structure"></a>Detalles de diseño: Estructura de tablas
Para entender cómo se almacenan y registran los movimientos de dimensión, es importante comprender la estructura de tabla.  

## <a name="table-480-dimension-set-entry"></a>Tabla 480, Mov. grupo dimensiones  
Esta tabla no se puede modificar. Tras escribir los datos en la tabla, no se podrá eliminar o modificar.

|N.º de campo|Nombre de campo|Tipo de datos|Comentario|  
|---------------|----------------|---------------|-------------|  
|1|**Id.**|Entero|>0,0 está reservado para el grupo de dimensiones vacío. Hace referencia al campo 3 de la tabla 481.|  
|2|**Cód. dimensión**|Código 20|Relación de tabla con la tabla 348.|  
|3|**Cód. valor dimensión**|Código 20|Relación de tabla con la tabla 349.|  
|4|**Id. valor de dimensión**|Entero|Hace referencia al campo 12 de la tabla 349. Es la clave secundaria que se usa para recorrer la tabla 481.|  
|5|**Nombre dimensión**|Texto 30|CalcField. Búsqueda en la tabla 348.|  
|6|**Nombre valor dimensión**|Texto 30|CalcField. Búsqueda en la tabla 349.|  

## <a name="table-481-dimension-set-tree-node"></a>Tabla 481, Nodo árbol grupo dimensiones  
Esta tabla no se puede modificar. Se usa para buscar un grupo de dimensiones. Si no se encuentra el grupo de dimensiones, se crea un nuevo grupo.  

|Nº campo|Nombre de campo|Tipo de datos|Comentario|  
|---------------|----------------|---------------|-------------|  
|1|**Id. grupo dimensiones principal**|Entero|0 para el nodo de nivel superior.|  
|2|**Id. valor de dimensión**|Entero|Relación de tabla con el campo 12 de la tabla 349.|  
|3|**Id. grupo dimensiones**|Entero|AutoIncrement. Se usa en el campo 1 de la tabla 480.|  
|4|**Utilizándose**|Booleano|Falso si no se usa.|  

## <a name="table-482-reclas-dimension-set-buffer"></a>Tabla 482 Almacenaje grupo de dimensiones reclas.  
Esta tabla se usa cuando se modifica un código de valor de dimensión, por ejemplo, en un movimiento de producto mediante la página **Diario reclasificación producto**.  

|N.º de campo|Nombre de campo|Tipo de datos|Comentario|  
|---------------|----------------|---------------|-------------|  
|1|**Cód. dimensión**|Código 20|Relación de tabla con la tabla 348.|  
|2|**Cód. valor dimensión**|Código 20|Relación de tabla con la tabla 349.|  
|3|**Id. valor de dimensión**|Entero|Hace referencia al campo 12 de la tabla 349.|  
|4|**Nuevo cód. valor dim.**|Código 20|Relación de tabla con la tabla 349.|  
|5|**Nuevo Id. valor de dimensión**|Entero|Hace referencia al campo 12 de la tabla 349.|  
|6|**Nombre dimensión**|Texto 30|CalcField. Búsqueda en la tabla 348.|  
|7|**Nombre valor dimensión**|Texto 30|CalcField. Búsqueda en la tabla 349.|  
|8|**Nuevo nombre valor dimensión**|Texto 30|CalcField. Búsqueda en la tabla 349.|  

## <a name="transaction-and-budget-tables"></a>Tablas de transacción y de presupuesto  
Además de otros campos de dimensión en la tabla, este campo es importante:  

|N.º de campo|Nombre de campo|Tipo de datos|Comentario|  
|---------------|----------------|---------------|-------------|  
|480|**Id. grupo dimensiones**|Entero|Hace referencia al campo 1 de la tabla 480.|  

### <a name="table-83-item-journal-line"></a>Tabla 83, Lín. diario producto  
Además de otros campos de dimensión en la tabla, estos campos son importantes.  

|N.º de campo|Nombre de campo|Tipo de datos|Comentario|  
|---------------|----------------|---------------|-------------|  
|480|**Id. grupo dimensiones**|Entero|Hace referencia al campo 1 de la tabla 480.|  
|481|**Id. grupo dimensiones nuevo**|Entero|Hace referencia al campo 1 de la tabla 480.|  

### <a name="table-349-dimension-value"></a>Tabla 349, Valor de dimensión  
Además de otros campos de dimensión en la tabla, estos campos son importantes.  

|N.º de campo|Nombre de campo|Tipo de datos|Comentario|  
|---------------|----------------|---------------|-------------|  
|12|**Id. valor de dimensión**|Entero|AutoIncrement. Se usa para las referencias de las tablas 480 y 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field"></a>Tablas que contienen el campo Id. grupo dimensiones
 El campo **Id. grupo dimensiones** (480) existe en las siguientes tablas. En el caso de tablas que almacenan datos registrados, el campo solo muestra dimensiones no modificables marcadas como Explorar en profundidad. En el caso de tablas que almacenan documentos de trabajo, el campo se puede modificar. Las tablas de búfer que se usan internamente no necesitan capacidades que se puedan modificar o no se puedan modificar.  

 El campo 480 no se puede modificar en las tablas siguientes.  

|Nº tabla|Nombre tabla|  
|---------------|----------------|  
|17|**Mov. contabilidad**|  
|21|**Mov. cliente**|  
|25|**Mov. proveedor**|  
|32|**Mov. producto**|  
|110|**Histórico cab. albarán venta**|  
|111|**Histórico lín. albarán venta**|  
|112|**Histórico cab. factura venta**|  
|113|**Histórico lín. factura venta**|  
|114|**Histórico cab. abono venta**|  
|115|**Histórico lín. abono venta**|  
|120|**Histórico cab. albarán compra**|  
|121|**Histórico lín. albarán compra**|  
|122|**Histórico cab. factura compra**|  
|123|**Histórico lín. factura compra**|  
|124|**Histórico cab. abono compra**|  
|125|**Histórico lín. abono compra**|  
|169|**Mov. proyecto**|  
|203|**Mov. recurso**|  
|271|**Mov. banco**|  
|281|**Mov. inventario físico**|  
|297|**Cab. recordatorio emitido**|  
|304|**Cab. doc. interés emitido**|  
|5107|**Archivo cab. venta**|  
|5108|**Archivo lín. venta**|  
|5109|**Archivo cab. compra**|  
|5110|**Archivo lín. compra**|  
|5601|**A/F Movimiento**|  
|5625|**Mov. mantenimiento**|  
|5629|**Mov. seguro**|  
|5744|**Cab. transferencia envío**|  
|5745|**Línea transfer. envío**|  
|5746|**Cab. transfer. recep.**|  
|5747|**Lín. transfer. recep.**|  
|5802|**Movimiento valor**|  
|5832|**Movs. capacidad**|  
|5907|**Movimiento servicio**|  
|5908|**Cab. servicio**|  
|5933|**Buffer regis. ped. serv.**|  
|5970|**Cab. contrato servicio archiv.**|  
|5990|**Cabecera envío servicio**|  
|5991|**Línea envío servicio**|  
|5992|**Cabecera factura servicio**|  
|5993|**Lín. factura servicio**|  
|5994|**Cabecera abono servicio**|  
|5995|**Línea abono servicio**|  
|6650|**Cabecera envío devolución**|  
|6651|**Lín. envío devolución**|  
|6660|**Cab. recep. devolución**|  
|6661|**Lín. recep. devol.**|  

El campo 480 se puede modificar en las tablas siguientes.  

|Nº tabla|Nombre tabla|  
|---------------|----------------|  
|36|**Cab. venta**|  
|37|**Lín. venta**|  
|38|**Cab. compra**|  
|39|**Lín. compra**|  
|81|**Lín. diario general**|  
|83|**Lín. diario producto**|  
|89|**Línea de diario L.M.**|  
|96|**Mov. presupuesto**|  
|207|**Lín. diario recurso**|  
|210|**Lín. diario proyecto**|  
|221|**Diario gen. distribución**|  
|246|**Lín. hoja demanda**|  
|295|**Cab. recordatorio**|  
|302|**Cab. doc. interés**|  
|5405|**Orden producción**|  
|5406|**Lín. orden prod.**|  
|5407|**Componente orden producción**|  
|5615|**A/F Distribución**|  
|5621|**A/F Lín. diario**|  
|5635|**Lín. diario seguro**|  
|5740|**Cab. transferencia**|  
|5741|**Lín. transferencia**|  
|5900|**Cab. servicio**|  
|5901|**Lín. prod. servicio**|  
|5902|**Línea servicio**|  
|5965|**Cabecera contrato servicio**|  
|5997|**Línea servicio estándar**|  
|7134|**Movimiento del presupuesto de productos**|  
|99000829|**Planif. componente**|  

El campo 480 existe en las siguientes tablas de búfer.  

|Nº tabla|Nombre tabla|  
|---------------|----------------|  
|49|**Mem. inter. factura**|  
|212|**Mem. inter. proyecto**|  
|372|**Mem. inter. pago**|  
|382|**Mem. inter. mov. CV**|  
|461|**Mem. int. lín. fact. prepago**|  
|5637|**A/F Mem. int. reg. C/G**|  
|7136|**Búfer del presupuesto de productos**|  

## <a name="see-also"></a>Consulte también

[Información general de los movimientos del grupo dimensiones](design-details-dimension-set-entries-overview.md)  
[Detalles de diseño: Búsqueda de combinaciones de dimensiones](design-details-searching-for-dimension-combinations.md)   
