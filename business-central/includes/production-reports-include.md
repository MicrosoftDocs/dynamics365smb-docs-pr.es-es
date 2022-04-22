---
author: edupont04
ms.topic: include
ms.date: 03/01/2022
ms.author: edupont
ms.openlocfilehash: 5a3e15669bfc590d663b7774fba84017ae842521
ms.sourcegitcommit: 865b390b5571b08084bde93b539ec9898e201933
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/02/2022
ms.locfileid: "8372026"
---
La siguiente tabla describe algunos de los informes clave en los informes de producción.

| Informe | Descripción | Id. | 
|---------|---------|---------|
| [Despliegue cantidad en L.M.](https://businesscentral.dynamics.com?report=99000753)|Muestra una lista de L.M. indentada de el o los productos que ha especificado en los filtros. La L. M. de producción se despliega completamente a todos los niveles.|99000753|
| [Puede hacer producto (tiempo)](https://businesscentral.dynamics.com?report=5871)|Muestra cómo cinco cifras de disponibilidad clave diferentes se modifican a lo largo del tiempo para un producto de la L.M. Estas cifras cambian según los eventos previstos de suministro y demanda y para el suministro que se basa en los componentes disponibles que se pueden ensamblar o fabricar.<br>Puede utilizar el informe para ver si puede completar una pedido de venta para un producto en una fecha especificada consultando su disponibilidad actual en combinación con las cantidades potenciales que sus componentes pueden suministrar si se ha iniciado un pedido de ensamblado. El informe muestra cuándo y cuántas unidades de un elemento de ensamblado y fabricación puede producir según la disponibilidad de los componentes y la disponibilidad actual del producto. Esto se muestra como la cantidad total.<br>La información se muestra en un gráfico en el que cada cifra de disponibilidad es una línea que progresa a lo largo de la escala de tiempo y se mueve hacia arriba y hacia abajo cuando las cantidades cambian. Las cifras de la cantidad provienen del mismo motor que proporciona la información para la ventana **Disponibilidad prod. por nivel L.M.**. |5871|
| [Distribución partes costes L.M.](https://businesscentral.dynamics.com?report=5872)|Muestra gráficamente cómo el coste de un elemento de ensamblado o fabricado se distribuye mediante la L.M.<br>Esta información puede resultar útil para decidir, por ejemplo, si se deben cambiar los proveedores de componentes, sustituir el uso interno de la capacidad por trabajo externo o viceversa, o cuándo revisar y modificar la lista de materiales de un producto.<br>El primer plan del informe muestra el coste unitario total de los componentes y recursos de trabajo del producto principal desglosados en un máximo de cinco partes de coste diferentes, y representadas gráficamente con diferentes colores.<br>El gráfico circular con la leyenda *Por el material o el trabajo* muestra la distribución proporcional entre el material del producto principal y los costes de mano de obra, así como sobre sus propios costes generales de fabricación. La parte de coste material incluye los costes materiales del producto. La parte de coste de mano de obra incluye la capacidad, los costes generales de capacidad y los costes subcontratados. Los costes compartidos se muestran de manera diferente dependiendo de lo que haya elegido en el campo **Mostrar solo**.<br>El gráfico circular con la leyenda *Por directo/indirecto* muestra la distribución proporcional entre los costes directos e indirectos del producto principal. La parte de coste directo incluye los costes de los materiales, la capacidad y la subcontrataciones del producto. La parte del coste indirecto incluye los costes generales de capacidad y de fabricación.<br>La tabla en la parte inferior del informe se incluye cuando se selecciona la casilla de verificación **Incluir detalles**. Muestra los valores seleccionados de la ventana Partes costes L.M. por a un nivel individual o distribuido, dependiendo de las opciones que haya elegido en el campo **Mostrar parte costes como**.|5872|
| [Cálculo detallado](https://businesscentral.dynamics.com?report=99000756)|Muestra una lista de costes por producto teniendo en cuenta los rechazos.|99000756|
| [Puntos-de-uso (nivel superior)](https://businesscentral.dynamics.com?report=99000757)|Muestra dónde y en qué cantidades se utilizan los productos en la estructura de producto.<br>El informe muestra sólo el producto como punto-de-uso, cuando el producto base se utiliza como producto de nivel superior. Por ejemplo, si el producto “A” se utiliza para producir el producto “B”, y el producto “B” para producir el “C”, el informe mostrará el producto B si ejecuta el mismo para el producto A. Si ejecuta el informe para el producto B, el producto C se mostrará como punto-de-uso.<br>También puede abrir directamente desde el producto la página **Línea puntos-de-uso**.|99000757|
| [Lista comparación LM productos](https://businesscentral.dynamics.com?report=99000758)|Este informe le brinda la posibilidad de comparar productos finales similares con respecto a los costes. Verá una lista con todos los componentes y sus costes, así como las cantidades necesarias. La fecha de cálculo normalmente se establece en la fecha de trabajo. |99000758|
| [Estadísticas orden producción](https://businesscentral.dynamics.com?report=99000791)|Especifica los diversos costes que se han acumulado para la orden de producción seleccionada.<br>El contenido del informe es muy parecido a la página **Estadísticas orden producción** .<br>Para las órdenes de producción que utilizan la directiva de fabricación de *Fab-contra-pedido*, la ventana muestra solo el coste de material y de capacidad de los productos en el nivel más alto de la L.M.|99000791|
| [Lista de tareas de capacidad](https://businesscentral.dynamics.com?report=99000780)|Muestra las órdenes de producción que esperan a ser procesadas en los centros de trabajo y en los centros de máquina. El informe se realiza para la capacidad de un centro de trabajo o un centro de máquina. El informe incluye información como hora de inicio y fin, fecha por orden de producción y cantidad de entrada.|99000780|
| [Carga centro trabajo](https://businesscentral.dynamics.com?report=99000783)|Muestra una lista de la carga de un centro de trabajo. La carga de un centro de trabajo es la suma del número requerido de veces que se ejecutan todas las órdenes actuales y planificadas en el centro de trabajo en un periodo determinado.|99000783|
| [Carga centro máquina](https://businesscentral.dynamics.com?report=99000784)|Muestra una lista de la carga de un centro de máquina. La carga de un centro de máquina es la suma del número requerido de veces que se ejecutan todas las órdenes actuales y planificadas en el centro de trabajo en un periodo determinado.|99000784|
| [Lista carencias ord. prod.](https://businesscentral.dynamics.com?report=99000788)|Este informe se puede utilizar para ver todos los componentes que no están disponibles debido a la falta de existencias. Por lo tanto, este resumen se puede utilizar para ver a tiempo, si el cronograma para una orden de producción planificada o liberada o el tiempo planificado se pueden mantener.|99000788|
|[Orden producción - Cálculo](https://businesscentral.dynamics.com?report=99000767)|Muestra una lista de las órdenes de producción y sus costes. Incluye los costes de operaciones previstos, costes de componentes previstos y costes totales.|99000767|