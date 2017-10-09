---
title: Trabajar con dimensiones | Documentos de Microsoft
description: "Puede utilizar dimensiones para clasificar movimientos, por ejemplo, por departamentos o proyecto, por lo que le será muy fácil realizar un seguimiento de los datos y analizarlos."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 844668124df1897493737b28383a68a2a0a66d10
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-dimensions"></a>Trabajar con dimensiones
Para simplificar la realización de análisis en documentos, como pedidos de venta, puede utilizar dimensiones. Las dimensiones son atributos y valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de ellos. Por ejemplo, las dimensiones pueden indicar de qué proyecto o departamento procede un movimiento.  

Por ejemplo, en lugar de tener que configurar cuentas contables generales independientes para cada departamento y proyecto puede usar dimensiones. De este modo, dispone de la posibilidad de análisis, sin crear un plan de cuentas complicado. Para obtener más información, consulte [Inteligencia empresarial](bi.md).

Otro ejemplo es configurar una dimensión que se llame *Departamento* y usarla junto con esta dimensión cuando registre documentos de ventas. Así podrá usar herramientas la de inteligencia empresarial para ver qué departamento vende cada producto.
Cuantas más dimensiones use, más detallados serán los informes en los que pueda basar sus decisiones empresariales. Por ejemplo, un movimiento de ventas individual puede incluir información de múltiples dimensiones, por ejemplo:  

* La cuenta en la que se registró la venta del producto  
* Dónde se vendió el producto
* Quién lo vendió
* El tipo de cliente que lo compró  

> [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en **Suite**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Analizar por dimensiones
La funcionalidad Dimensiones desempeña una función importante en la inteligencia empresarial, por ejemplo al definir vistas de análisis. Para obtener más información, vea [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

> [!TIP]
> Como una forma rápida de analizar datos transaccionales por dimensiones, puede filtrar por dimensiones los totales del plan de cuentas y movimientos en todas las ventanas **Movimientos**. Busque la acción **Establecer filtro de dimensiones**.

## <a name="dimension-sets"></a>Grupos de dimensiones
Un grupo de dimensiones es una combinación única de valores de dimensión. Se almacena como movimientos de grupo de dimensiones en la base de datos. Cada movimiento de grupo de dimensiones representa un valor de dimensión único. El grupo de dimensiones se identifica por medio de un id común del grupo de dimensiones que está asignado a cada movimiento de grupo de dimensiones que pertenece al grupo de dimensiones.  

Cuando crea una línea de diario, cabecera de documentos o línea de documentos, puede especificar una combinación de valores de dimensión. En lugar de explícitamente guardar cada valor de dimensión en la base de datos, un Id. de grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos para especificar el grupo de dimensiones.  

## <a name="setting-up-dimensions"></a>Configurar dimensiones
Puede definir las dimensiones y los valores de dimensión para clasificar los diarios y los documentos, como pedidos de venta y pedidos de compra. Las dimensiones se configuran en la ventana **Dimensiones**, donde se crea una línea para cada dimensión, como *Proyecto*, *Departamento*, *Área* y *Vendedor*.

También se configuran los valores de dimensión. Por ejemplo, los valores pueden ser departamentos de su empresa. Los valores de dimensiones se pueden configurar en una estructura jerárquica similar al plan de cuentas, de modo que los datos se puedan desglosar en diversos niveles de granularidad y se puedan totalizar subconjuntos de valores de dimensiones. Puede definir tantas dimensiones y valores de dimensión como necesite y cualquier usuario de su empresa puede usarlos.

También puede configurar algunas dimensiones globales y abreviadas:  

* Las **dimensiones globales** se usan como filtros, por ejemplo, en informes y procesos. Solo puede utilizar dos dimensiones globales, por lo que debería elegir las dimensiones que use a menudo.
* Las **dimensiones abreviadas** están disponibles como campos en líneas de diario y documento. Puede crear un máximo de seis.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Configurar dimensiones predeterminadas para clientes, proveedores y otras cuentas
Puede asignar una dimensión predeterminada para una determinada cuenta. La dimensión se copiará en el diario o el documento cuando introduzca el número de cuenta en una línea, pero puede eliminar o cambiar el código de la línea si es necesario. También puede convertir una dimensión en obligatoria para registrar un movimiento con un tipo de cuenta específico.  

### <a name="translating-the-names-of-dimensions"></a>Traducir los nombres de dimensiones
Al crear una dimensión, y especialmente una dimensión abreviada, lo que realmente crea es un campo personalizado o un encabezado de columna. Si su empresa es internacional, puede proporcionar las traducciones del nombre de la dimensión. Los documentos que contengan la dimensión usarán el nombre traducido, si corresponde.   

### <a name="example-of-dimension-setup"></a>Ejemplo de configuración de dimensiones
Supongamos que su empresa desea realizar un seguimiento de las transacciones en función de la estructura organizativa y las ubicaciones geográficas. Para ello, puede configurar dos dimensiones en la ventana **Dimensiones**:

* **ÁREA**  
* **DEPARTAMENTO**  

| Código | Name | Título código | Título filtro |
| --- | --- | --- | --- |
| ÁREA |Área |Código de área |Filtro Área |
| DPTO |Departamento |Código de departamento |Filtro departamento |

Para **ÁREA**, agregue los siguientes valores de dimensión:

| Código | Name | Tipo valor dimensión |
| --- | --- | --- |
| 10 |América |Principio-Total |
| 2.0 |América del Norte |Estándar |
| 30 |Pacífico |Estándar |
| 40 |Sudamérica |Estándar |
| 50 |América, total |Fin-Total |
| 60 |Europa |Principio-Total |
| 70 |UE |Estándar |
| 80 |No perteneciente a la UE |Estándar |
| 90 |Europa, Total |Fin-Total |

Para las dos áreas geográficas principales, América y Europa, agregue subcategorías para las regiones aplicando sangría a los valores de dimensión. De esta manera podrá elaborar informes sobre ventas o gastos en regiones, y obtener totales de las áreas geográficas más grandes. También puede usar países o regiones como valores de dimensión, o condados o poblaciones, dependiendo de la empresa.  
> [!NOTE]  
>   Para configurar una jerarquía, los códigos deben estar en orden alfabético. Esto incluye los códigos de los valores de dimensión que se proporcionan en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Para **DEPARTAMENTO**, agregue los siguientes valores de dimensión:

| Código | Name | Tipo valor dimensión |
| --- | --- | --- |
| ADMIN |Administración |Estándar |
| PROD |Producción |Estándar |
| CCIAL |Ccial |Estándar |

Con esta configuración, agregará las dos dimensiones como las dos dimensiones globales en la ventana **Configuración de contabilidad**. Esto significa que puede usar ÁREA Y DEPARTAMENTO como filtros para los movimientos de contabilidad, así como en todos los informes y esquemas de cuentas. También están disponibles ambas dimensiones globales de forma automática para el uso en líneas de movimientos y cabeceras de documentos, como dimensiones abreviadas.  

## <a name="using-dimensions"></a>Usar dimensiones
En un documento como un pedido de ventas, puede agregar información de dimensión de una línea en particular y del mismo documento. Por ejemplo, en la ventana **Pedido de ventas**, puede introducir valores de dimensión para las dos primeras dimensiones abreviadas en las líneas de venta individuales y puede agregar más información de dimensión si elige el botón **Dimensiones**.  

Si trabaja con un diario, puede agregar información de dimensiones a un movimiento del mismo modo, si ha configurado dimensiones abreviadas como campos directamente en las líneas de diario.  

Puede configurar dimensiones predeterminadas para cuentas o tipos de cuenta, para que esas dimensiones o valores de dimensión se completen automáticamente.

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

