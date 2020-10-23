---
title: Como crear una L.M. de producción | Documentos de Microsoft
description: Una L.M. de producción contiene datos maestros que describen los componentes y los productos semiterminados utilizados en la fabricación de un producto principal. Una vez creada la orden de producción para el producto principal, la L.M. de producción controlará el cálculo de las necesidades de material tal como se representan en la página **Componentes orden producción**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1d053c65b94efdb3b033c617f1b6b2db316c1ec2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919293"
---
# <a name="create-production-boms"></a>Crear LM de producción
Una lista de materiales (L.M.) de producción contiene datos maestros que describen los componentes y los subconjuntos utilizados en la fabricación de un producto principal. Una vez creada la orden de producción para el producto principal, la L.M. de producción controlará el cálculo de las necesidades de material tal como se representan en la página **Componentes orden producción**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] también admite L.M. de ensamblado. Utilice los pedidos de ensamblado para crear productos finales de los componentes en un proceso sencillo que se pueda realizar por uno o varios recursos básicos, que no sean máquinas o centros de trabajo, o sin ningún recurso. Por ejemplo, un proceso de ensamblado podría ser el picking de dos botellas de vino y un saco de café y, después, empaquetarlo todo como artículo de regalo. Para obtener más información, consulte [L.M. de ensamblado o L.M. de producción](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

Para poder configurar una ruta, lo siguiente debe existir:  

- Se deben crear fichas de producto para los productos principales que forman parte de la fabricación. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).
- Se han configurado recursos de producción. Para obtener más información, consulte [Configurar centros de trabajo y centros de máquina](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a>Crear una L.M. de producción.  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **L.M. de producción** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Para editar la L.M., establezca el campo **Estado** en **Nueva** o **En desarrollo**. Para activarla, establezca el campo **Estado** en **Certificada**.  

    Proceda a rellenar las líneas de la L.M. de producción.
5. En el campo **Tipo**, seleccione si el producto de esta línea de L.M. es un producto normal o una L.M. de producción. Si es una L.M. de producción, debe ser una L.M. de producción certificada.  
6.  En el campo **N.º**, busque y seleccione el producto o la L.M. de producción en cuestión, o especifíquelo en el campo.  
7.  En el campo **Cantidad por**, especifique cuántas unidades componen el producto principal, por ejemplo, cuatro ruedas para un automóvil.  
8.  En el campo **% Rechazo**, puede especificar el porcentaje fijo de componentes que se rechazan durante la producción. Cuando los componentes estén preparados para su consumo en una orden de producción lanzada, este porcentaje se sumará a la cantidad esperada en el campo **Consumo (cantidad)** de un diario de producción. Para obtener más información, vea [Registrar el consumo y la salida](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Este porcentaje de rechazo representa los componentes que se rechazan durante la producción, cuando se seleccionan de las existencias, mientras que el porcentaje de rechazo en las líneas de ruta representa la salida rechazada, antes de preparar las existencias.  

9.  En el campo **Código de conexión de ruta**, introduzca un código para conectar el componente con una operación específica. Para obtener más información, consulte [Para crear conexiones de ruta](production-how-to-create-routings.md#to-create-routing-links).
10. Para copiar líneas de una L.M. de producción existente, seleccione la acción **Copiar L.M.** para seleccionar las líneas existentes.  
11.  Certifique la L.M. de producción.  
12.  Ahora puede asociar la L.M. de producción nueva a la ficha del producto principal en cuestión. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Para volver a calcular el coste estándar del producto desde la ficha del producto, seleccione la acción **Fabricación** y, a continuación, seleccione la ación **Calcular coste estándar**.  

## <a name="to-create-a-new-versions-of-a-production-bom"></a>Para crear una versión nueva de una L.M. de producción
Se utilizan las nuevas versiones de la L.M. de producción cuando, por ejemplo, un producto se sustituye por otro, o cuando un cliente solicita una versión especial de un producto. El principio de versión permite administrar varias versiones de una L.M. de producción. La estructura de la versión de la L.M. de producción se corresponde con la de la L.M. de producción. La diferencia básica es la validez en el tiempo de las versiones. La validez se define mediante la fecha inicial.  

La fecha inicial indica el comienzo del periodo en el que la versión es válida. Para lo demás, la fecha inicial es un criterio de filtro para cálculos y evaluaciones. La versión de L.M. es válida hasta que la siguiente versión se convierta en la válida debido a su fecha inicial.  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **L.M. de producción** y luego elija el enlace relacionado.  
2.  Seleccione la L.M. de producción a copiar y después seleccione la acción **Versiones**.  
3.  Seleccione la acción **Nuevo**.  
4. Rellene los campos según sea necesario.
5. En el campo **Código de versión**, introduzca la identificación única de la versión. Se permite cualquier combinación de letras y números.  

    A la versión que se acaba de crear se le asigna automáticamente el estado **Nueva.**
6. Cuando la versión de la L.M. está completa, establece el campo **Estado** como **Certificada**.  

El periodo de validez de la versión se especifica mediante el campo **Fecha inicial**.  

> [!NOTE]  
>  Seleccione la opción **Producto** en el campo **Tipo** para utilizar un producto de los datos maestros del producto en la L.M. de producción. Si el producto tiene también una L.M. de producción, por lo que en la ficha de producto está relleno el campo **Nº L.M. producción**, también se tiene en cuenta esta L.M.  
>   
>  Seleccione la opción de **L.M. producción** si desea utilizar una L.M. de producción ficticia en la línea.  
>   
>  Las L.M. de producción ficticias sirven para estructurar productos. Este tipo de L.M. de producción nunca lleva a un producto terminado, sino que se utiliza exclusivamente para determinar la demanda dependiente. Las L.M. de producción ficticias no poseen sus propios datos maestros del producto.

## <a name="quantity-calculation-formula-on-production-boms"></a>Fórmula de cálculo de la cantidad en la L.M. de producción  
La cantidad se calcula teniendo en cuenta las distintas dimensiones, que se especificaron en las líneas de la L.M. de producción. Las dimensiones se refieren a la unidad de orden del producto correspondiente. Se pueden especificar los valores de largo, ancho, alto y peso como dimensiones.  

Las columnas Fórmula cálculo, Largo, Ancho, Alto y Peso no se muestran ya que sólo se utilizan por usuarios cualificados. Si desea utilizar el cálculo de la cantidad, debe mostrar primero estas columnas.  

La relación entre los componentes individuales se define en la fórmula de cálculo. Existen las posibilidades siguientes como fórmula de cálculo:  

-  **Vacía**: No se tienen en cuenta las dimensiones. (Cantidad = Cantidad por.)  
-  **Largo**: Cantidad = Cantidad por *Largo  
-  **Largo x Ancho**: Cantidad = cantidad por * Largo x Ancho  
-  **Largo x Ancho x Profundidad**: Cantidad = Cantidad por Largo x Ancho x Profundidad  
-  **Peso**: Cantidad = Cantidad por x Peso  

### <a name="example"></a>Ejemplo  
En una L.M. de producción, se necesitan setenta componentes de metal con las dimensiones: largo = 0,20 m. y ancho: 0,15 m. Los valores se introducen de la manera siguiente: Fórmula de cálculo = Largo x Ancho, Largo = 20, Ancho = 15, Cantidad por = 70. La cantidad se obtiene de Cantidad por x Largo * Ancho, es decir, Cantidad = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a>Consulte también  
[Creación de rutas](production-how-to-create-routings.md)   
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Planificación](production-planning.md)   
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
