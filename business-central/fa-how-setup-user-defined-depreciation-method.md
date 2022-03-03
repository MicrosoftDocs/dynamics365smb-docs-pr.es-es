---
title: Configurar método de amortización definido por el usuario
description: En Business Central, puede aplicar un método de amortización definido por el usuario para definir el método de amortización de su activo en la página Ficha activo.
author: jill-kotel-andersson
ms.reviewer: edupont
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: edupont
ms.openlocfilehash: 517c3cdb51762c3c0fadcf29ff1ad6dbf949f971
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144988"
---
# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a>Configurar activos fijos con métodos de amortización definidos por el usuario

Puede usar [!INCLUDE[prod_short](includes/prod_short.md)] para configurar métodos de amortización definidos por el usuario como se describe aquí.

Para cada método definido por el usuario, se utiliza la página **Tablas amortización**, donde debe introducir un porcentaje de amortización para cada periodo (mes, trimestre, año o periodo contable). Luego, cuando asigna un libro de amortización con un método definido por el usuario para un activo fijo, debe establecer los campos **Fecha de primera amortización definida por el usuario** y **Fecha inicio amortización** en la página **Libros amortización activos** para el activo fijo específico.  

La fórmula para calcular los importes de amortización es:  

*Importe amortización = (% Amortización x Nº días amortización x Base amortizable) / (100 x 360)*


> [!NOTE]  
> Mientras que la fecha en el campo **1ª fecha amort. def.-usuario** se utiliza para determinar los intervalos de tiempo, se utiliza **Fecha inicio amortización** para determinar el número de días de amortización. Si la **1ª fecha amort. def.-usuario** es anterior a la **Fecha inicio amortización**, el porcentaje del primer periodo de la tabla de amortización solo se usará parcialmente cuando el programa calcule la primera amortización. Es decir, el activo no estará totalmente amortizado cuando se llegue al final del último periodo.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a>Para asignar un libro de amortización a un activo fijo con un método de amortización definido por el usuario

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo fijo para el que desee configurar un libro de amortización de activos fijos.
3. Elija la acción **Relacionados** y luego elija **Activo fijo** y **Libros de amortización**. Esto abre la página **Libros amortización activos**.

   De forma predeterminada, algunos de los campos que deben completarse según las instrucciones a continuación están ocultos, por lo que debe mostrarlos. Para hacer esto, necesita personalizar la página. Para más información, vea [Para comenzar a personalizar una página a través del banner de personalización](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. En el campo **amortización**, seleccione **Definido por el usuario**.
5. En el campo **Código de tabla de amortización**, seleccione la **Tabla de amortización** que desea utilizar.
6. En el campo **Fecha inicio amortización**, seleccione la fecha de inicio para el cálculo de la amortización.
7. Cuando utiliza un método definido por el usuario, el campo **1ª fecha amort. def.-usuario** debe establecerse en una fecha que sea igual o anterior a la del campo **Fecha inicio amortización**. Si ha seleccionado un valor en el campo **Longitud del periodo** de la tabla de amortización, la fecha del campo **1ª fecha amort. def.-usuario** debe ser la fecha inicial de un periodo contable.
8. Complete el campo **Nº años amortización** o el campo **Fecha final amortización**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods"></a>Para configurar métodos de amortización definidos por usuario

En la página **Tabla amortización**, puede configurar métodos de amortización definidos por el usuario. Por ejemplo, puede configurar la amortización según el número de unidades.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tablas de amortización** y luego elija el enlace relacionado.  
2. En la página **Lista tablas amortización**, elija la acción **Nuevo**.  
3. En la página **Ficha tablas amortización**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Utilice la función **Crear suma de tabla de dígitos** para definir una tabla de depreciación basada en el método *Suma de dígitos*.

Con el mátodo *Suma de dígitos*, si un activo fijo se deprecia durante 4 años, entonces la depreciación para cada año se calcula de la siguiente manera:

Suma de dígitos = 1 + 2 + 3 + 4 = 10 de amortización:

* Año 1 = 4/10  
* Año 2 = 3/10  
* Año 3 = 2/10  
* Año 4 = 1/10  

### <a name="depreciation-based-on-number-of-units"></a>Amortización según el número de unidades

Este método definido por el usuario también se puede utilizar para amortizar según el número de unidades, por ejemplo, en el caso de máquinas de producción con una capacidad de vida establecida. En la página **Tablas amortización**, puede introducir el número de unidades que pueden producirse en cada periodo (mes, trimestre, año o periodo contable).  

### <a name="example---user-defined-depreciation"></a>Ejemplo: amortización definida por el usuario

Por motivos de impuestos puede utilizar un método amortización que le permita amortizar activos de forma acelerada.  

Por tanto, podría utilizar los siguientes tipos de amortización de un activo con una duración de tres años:  

* Año 1: 25 %  
* Año 2: 38 %  
* Año 3: 37 %  

El coste es de 100.000 DL y el periodo de amortización es de cinco años. La amortización se calcula anualmente.  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coste |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 31/12/20 |Amortización |360 |-25.000,00 |75,000.00 |
| 31/12/21 |Amortización |360 |-38.000,00 |37,000.00 |
| 31/12/22 |Amortización |360 |-37.000,00 |0 |
| 31/12/23 |Amortización |Ninguno |Ninguno |0 |
| 31/12/24 |Amortización |Ninguno |Ninguno |0 |

En el ejemplo anterior, ambos campos **Primera fecha de amortización definida por el usuario** y **Fecha de inicio de la depreciación** se establecerían en 01/01/20 en la página **Libros amortización activos** para el activo fijo específico. Si, no obstante, el campo **1ª fecha amort. def.-usuario** tuviera 01/01/20 y el campo **Fecha inicio amortización** tuviera 01/04/20, el resultado podría ser:  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coste |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 31/12/20 |Amortización |270 |-18.750,00 |81,250.00 |
| 31/12/21 |Amortización |360 |-38.000,00 |42,250.00 |
| 31/12/22 |Amortización |360 |-37.000,00 |6,250.00 |
| 31/12/23 |Amortización |90 |-6.250,00 |0 |
| 31/12/24 |Amortización |Ninguno |Ninguno |0 |


## <a name="see-also"></a>Consulte también
[Configurar activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Configurar la amortización de los activos fijos](fa-how-setup-depreciation.md)  
[Métodos de amortización de activos fijos](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
