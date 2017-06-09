---
title: "Configurar la amortización de los activos fijos | Documentos de Microsoft"
description: "Describe cómo configurar el sistema para la amortización de los activos fijos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d14eb7cc55abd8d7aaddf2f3a8edcf20354fdec
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-depreciation"></a>Procedimiento: Configurar la amortización de los activos fijos
 Puede utilizar varios métodos de amortización para preparar extractos financieros y devoluciones de impuestos. Muchas grandes empresas utilizan amortizaciones en línea en sus extractos financieros porque les suele permitir obtener ganancias mayores. Sin embargo, en casos de devolución de impuestos, muchas empresas utilizan un método de amortización acelerado. Para obtener más información, consulte [Métodos de amortización](fa-depreciation-methods.md).

 Cuando cree los libros de amortización pertinentes, debe asignar uno o más a cada activo. Un libro de amortización que se asigna a un activo se le conoce como un libro de amortización de activo. Por consiguiente, la ventana de los libros asignados de amortización se denomina **Libros amortización A/F**.

## <a name="to-create-a-depreciation-book"></a>Para crear un libro de amortización
En un libro de amortización de activos puede especificar la forma en que se amortizarán los activos. Para aplicar distintos métodos de amortización, puede configurar varios libros de amortización.  

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Libros amortización** y elija el vínculo relacionado.
2. En la ventana **Lista libros amortización**, elija la acción **Nuevo**.
3. En la ventana **Ficha libros amortización**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    **Nota:** Puede registrar transacciones de activos en las ventanas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna. Vaya al siguiente paso para indicar qué tipo de diario se utiliza para las distintas actividades de activo de forma predeterminada.
4. En la ficha desplegable **Integración**, seleccione la casilla de las transacciones de cada actividad de activo que desee registrar en la ventana **A/F Diario general**.
5. Repita los pasos del 2 al 4 para cada método de amortización o de registro que desee asignar a los activos fijos en un libro de amortización.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Para asignar un libro de amortización a un activo fijo
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Activos fijos** y elija el vínculo relacionado.
2. Seleccione el activo fijo para el que desee configurar un libro de amortización de activos fijos.
3. En la ficha desplegable **Ficha libros amortización**, rellene los campos según sea necesario.
4. Si necesita asignar más de un libro de amortización al activo, elija la acción **Añadir más libros amortización**.
5. Opcionalmente, elija la acción **Libros amortización** para especificar uno o más libros de amortización de activos.

    **Nota:** Cuando utilice el método de amortización manual, debe introducir la amortización de forma manual en el diario general de activos. La función **Calcular amortización** ignora los activos que utilizan el método de amortización manual. Puede utilizar este método para activos no sujetos a amortización como, por ejemplo, los terrenos.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Para asignar un libro de amortización a varios activos con un solo proceso
Si desea asignar un libro de amortización a varios activos fijos, puede utilizar el proceso **A/F Crear libros amortización** para crear los libros necesarios de activos fijos.  

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Activos fijos** y elija el vínculo relacionado.
2. Seleccione el activo al que desea asignarle un libro de amortización y, a continuación, elija la acción **Editar**.
3. En la ventana **Ficha libro amortización**, elija la acción **A/F Crear libros amortización**.
4. En la ventana **A/F Crear libros amortización**, rellene el campo **Libro amortización**.
5. Elija el campo **A/F Copiar desde n. º** y, a continuación, seleccione el número de activo que desea utilizar como base para la creación de los nuevos libros de amortización de activos.

    Si rellena este campo, los campos de amortización de los nuevos libros de amortización de activos fijos contendrán la misma información que los campos correspondientes del libro desde el que va a copiarlos. Deje este campo en blanco si desea crear libros de amortización de activos fijos con los campos de amortización vacíos.  
6. En la ficha desplegable **Activo**, puede establecer un filtro para seleccionar los activos para los que desee crear los libros de amortización de activos.
7. Elija el botón **Aceptar**.

## <a name="to-set-up-depreciation-posting-types"></a>Para configurar los tipos de registro de amortización
Para cada libro de amortización, debe configurar el modo en que desea que [!INCLUDE[d365fin](includes/d365fin_md.md)] administre los distintos tipos de registro. Por ejemplo, si el registro debe ser débito o abono, y si el tipo de registro se debe incluir en la base de amortización.  

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Libros amortización** y elija el vínculo relacionado.  
2. Seleccione el libro de amortización que desea configurar y, a continuación, elija la acción **A/F Config. tipo registro**.
3. En la ventana **A/F Config. tipo registro**, rellene los campos según sea necesario.

    **Nota:** En la ventana **Config. tipos registro A/F** no puede insertar ni borrar líneas. Sólo puede modificar las líneas existentes.

    Se recomienda que no cambie la configuración de los libros de amortización de los movimientos que ya se han registrado. Los cambios no afectarán a los movimientos ya registrados, lo que provocaría estadísticas del libro de amortización erróneas.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Para configurar las plantillas y los procesos predeterminados para la amortización de activos
Puede definir para cada libro de amortización una configuración predeterminada para libros y secciones. Estos valores predeterminados se usan para duplicar líneas de un diario a otro, crear líneas de diario con los procesos **Calcular amortización** o **Ajustar valores activos fijos** o duplicar los costes de adquisición en el diario de seguros.  

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Libros amortización** y elija el vínculo relacionado.  
2. Seleccione el libro de amortización en el que desea definir los diarios predeterminados y, a continuación, elija la acción **Configuración del diario A/F**.  
3. Si desea tener una configuración predeterminada para cada usuario, elija el campo **Id. usuario** y selecciónela desde la ventana **Usuarios**.  
4. En el resto de campos, seleccione la sección o plantilla del diario que debe usarse de forma predeterminada.  

## <a name="see-also"></a>Consulte también
[Configurar activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

