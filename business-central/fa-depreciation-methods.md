---
title: Métodos de amortización de activos fijos
description: Conozca los diferentes métodos integrados para depreciar o amortizar activos fijos en la versión predeterminada de Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9e531a4f304829b0549fbe21e8d671708373ab22
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774160"
---
# <a name="depreciation-methods-for-fixed-assets"></a>Métodos de amortización de activos fijos

Hay ocho métodos de amortiación disponibles en la versión predeterminada de [!INCLUDE [prod_short](includes/prod_short.md)]:  

* Lineal  
* Regresivo 1  
* Regresivo 2  
* Rs1/L  
* Rs2/L  
* Definido por el usuario  

  > [!NOTE]  
  > Especifique su propio método de amortización definiendo tablas de amortización.
* Manual  

  > [!NOTE]  
  > Utilice este método para activos no sujetos a amortización, por ejemplo, los terrenos. Debe introducir la amortización en el diario general de activos fijos. El proceso **Calcular amortización** ignora los activos fijos que utilizan este método de amortización.  
* Convenio de medio año  

  > [!NOTE]  
  > Al utilizar este método, se amortiza la misma cantidad de un activo fijo cada año.  

## <a name="straight-line-depreciation"></a>Amortización lineal

Al utilizar el método lineal, debe especificar una de las siguientes opciones en el libro de amortización de activos fijos:  

* El periodo de amortización (años o meses) o una fecha final amortización  
* Un porcentaje fijo anual  
* Un importe fijo anual  
* Periodo de amortización  

### <a name="depreciation-period"></a>Periodo de amortización

Si introduce el periodo de amortización (número de años de amortización, número de meses o fecha de finalización), la siguiente fórmula calcula el importe de amortización:  

*Importe amortización = ((Valor neto – Valor residual) x N. º días amortización) / Días restantes amortización*  

Los días restantes de amortización se calculan como el número de días de amortización, menos el número de días entre la fecha inicial de amortización y la última fecha de movimiento del activo.  

El valor neto puede reducirse con apreciaciones, depreciaciones, importes personalizado 1 o 2, según se desactive el campo **tipo reg. IVAIncluye en cálc. amortización** y si se activa el campo **Compone valor contable** en la página **A/F Config. tipo registro**. Este cálculo garantiza que el activo se amortiza por completo al llegar la fecha final de amortización.  

### <a name="fixed-yearly-percentage"></a>Porcentaje fijo anual

Si introduce un porcentaje fijo anual, la aplicación utiliza la fórmula siguiente para calcular el importe de amortización:  

*Importe amortización = (% Lineal x Base amortizable x Nº días amortización) / (100 x 360)*  

### <a name="fixed-yearly-amount"></a>Importe fijo anual

Si introduce un importe fijo anual, la aplicación utiliza esta fórmula para calcular el importe de amortización:  

*Importe amortización = (Importe fijo amortización x Número días amortización) / 360*  

### <a name="example---straight-line-depreciation"></a>Ejemplo: amortización lineal

Un activo tiene un coste de 100.000 DL. Su vida estimada es de ocho años. El proceso **Calcular amortización** se realiza cada dos años.  

Para este ejemplo, el movimiento de activo fijo es el siguiente:  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coste |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 30/06/20 |Amortización |180 |-6.250,00 |93,750.00 |
| 31/12/20 |Amortización |180 |-6.250,00 |87,500.00 |
| 30/06/21 |Amortización |180 |-6.250,00 |81,250.00 |
| 31/12/21 |Amortización |180 |-6.250,00 |75,000.00 |
| 30/06/27 |Amortización |180 |-6.250,00 |6,250.00 |
| 31/12/27 |Amortización |180 |-6.250,00 |0 |

## <a name="declining-balance-1-depreciation"></a>Amortización con regresivo 1

Este método de amortización acelerado asigna la mayor parte del coste de un activo en los primeros años de su vida útil. Si utiliza este método, deberá introducir un porcentaje fijo anual.  

La fórmula siguiente calcula los importes de amortización:  

*Importe amortización = (% Regresivo x Nº días amortización x Base amortizable) / (100 x 360)*  

La base amortizable se calcula como el valor neto menos la amortización desde la fecha inicial del año fiscal actual.  

El importe de amortización registrado puede contener ciertos movimientos con diferentes tipos de registros (depreciación, personalizado1 y personalizado2) registrados desde el inicio del año fiscal actual. Estos tipos de registro se incluyen en el importe de amortización registrado, si los campos **Tipo amortización** y **Compone valor neto** están activados en la página **Config. tipo registro A/F**.  

### <a name="example---declining-balance-1-depreciation"></a>Ejemplo: amortización con regresivo 1

Un activo tiene un coste de 100.000 DL. El valor del campo **% Regresivo** es 25. El proceso **Calcular amortización** se realiza cada dos años.  

La siguiente tabla muestra el aspecto de los movimientos de activo fijo.  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Costes |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 30/06/20 |Amortización |180 |-12.500,00 |87,500.00 |
| 31/12/20 |Amortización |180 |-12.500,00 |75,000.00 |
| 30/06/21 |Amortización |180 |-9.375,00 |65,625.00 |
| 31/12/21 |Amortización |180 |-9.375,00 |56,250.00 |
| 30/06/22 |Amortización |180 |-7.031,25 |49,218.75 |
| 31/12/22 |Amortización |180 |-7.031,25 |42,187.50 |
| 30/06/23 |Amortización |180 |-5.273,44 |36,914.06 |
| 31/12/23 |Amortización |180 |-5.273,44 |31,640.62 |
| 30/06/24 |Amortización |180 |-3.955,08 |27,685.54 |
| 31/12/24 |Amortización |180 |-3.955,08 |23,730.46 |

Método de cálculo:  

* Año 1: *25 % de 100 000 = 25 000 = 12 500 + 12 500*

* Año 2: *25 % de 75 000 = 18 750 = 9375 + 9375*

* Año 3: *25 % de 56 250 = 14 062,50 = 7031,25 + 7031,25*

El cálculo continúa hasta que el valor neto iguala al importe de redondeo final o al valor residual que ha introducido.  

## <a name="declining-balance-2-depreciation"></a>Amortización con regresivo 2

Los métodos Regresivo 1 y Regresivo 2 calculan el mismo importe total de amortización para cada año. Sin embargo, si ejecuta el proceso **Calcular amortización** más de una vez al año, el método Regresivo 1 dará como resultado importes de amortización iguales para cada periodo de amortización. Por otra parte, el método Regresivo 2 dará como resultado importes de amortización cada vez más reducidos en cada periodo.  

### <a name="example---declining-balance-2-depreciation"></a>Ejemplo: amortización con regresivo 2

Un activo tiene un coste de 100.000 DL. El valor del campo **% Regresivo** es 25. El proceso **Calcular amortización** se realiza cada dos años. Los movimientos de activos son los siguientes:  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Costes |(Fecha inicio amortización)|100,000.00 |100,000.00 |
| 30/06/20 |Amortización |180 |-13.397,46 |86,602.54 |
| 31/12/20 |Amortización |180 |-11.602,54 |75,000.00 |
| 30/06/21 |Amortización |180 |-10.048,09 |64,951.91 |
| 31/12/21 |Amortización |180 |-8.701,91 |56,250.00 |

Método de cálculo:  

* *BV* = Valor neto  
* *ND* = Número días de amortización  
* *DBP* = porcentaje de balance de deterioro  
* *P* = *DBP*/100  
* *D* = *ND*/360  

La fórmula para calcular los importes de amortización es:  

*IA* = *VN* x (1 – (1 – P)<sup>D</sup>)

Los valores de amortización son:  

| Fecha | Cálculo |
| --- | --- |
| 30/06/20 |IA = 100 000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 13 397,46 |
| 31/12/20 |IA = 86 602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11 602,54 |
| 30/06/21 |IA = 75 000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10 048,09 |
| 31/12/21 |IA = 64 951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8701,91 |

## <a name="db1sl-depreciation"></a>Amortización Rs1/L

Rs1/L es una combinación abreviada de Regresivo 1 y Lineal. El cálculo continúa hasta que el valor neto iguala al importe de redondeo final o al valor residual que ha introducido.  

El proceso **Calcular amortización** calcula un importe lineal y otro regresivo, pero sólo se transfiere al diario el mayor de los dos importes.  

Puede usar varios porcentajes para el cálculo regresivo.  

Si utiliza este método, deberá introducir la vida útil estimada y el porcentaje regresivo en la página **A/F Libros amortización**.  

### <a name="example---db1-sl-depreciation"></a>Ejemplo: amortización Rs1/L

Un activo tiene un coste de 100.000 DL. En la página **A/F Crear libros amortización**, el campo **% Regresivo** contiene 25 y el campo **Nº años amortización** contiene 8. El proceso **Calcular amortización** se realiza cada dos años.  

Los movimientos contables de activos fijos son los siguientes:  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Costes |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 30/06/20 |Amortización |180 |-12.500,00 |87,500.00 |
| 31/12/20 |Amortización |180 |-12.500,00 |75,000.00 |
| 30/06/21 |Amortización |180 |-9.375,00 |65,625.00 |
| 31/12/21 |Amortización |180 |-9.375,00 |56,250.00 |
| 30/06/22 |Amortización |180 |-7.031,25 |49,218.75 |
| 31/12/22 |Amortización |180 |-7.031,25 |42,187.50 |
| 30/06/23 |Amortización |180 |-5.273,44 |36,914.06 |
| 31/12/23 |Amortización |180 |-5.273,44 |31,640.62 |
| 30/06/24 |Amortización |180 |-3.955,08 |27,685.54 |
| 31/12/24 |Amortización |180 |-3.955,08 |23,730.46 |
| 30/06/25 |Amortización |180 |-3.955,08 |19.775,38 L |
| 31/12/25 |Amortización |180 |-3.955,08 |15.820,30 L |
| 30/06/26 |Amortización |180 |-3.955,08 |11.865,22 L |
| 31/12/26 |Amortización |180 |-3.955,07 |7.910,15 L |
| 30/06/27 |Amortización |180 |-3.955,08 |3.955,07 L |
| 31/12/27 |Amortización |180 |-3.955,07 |0,00 L |

`SL` después del valor neto significa que se utilizó el método lineal.  

Método de cálculo:  

* Año 1 (2020):  

    *Importe regresivo: 25% de 100.000 = 25.000=12.500+12.500*  

    *Importe lineal = 100.000/8=12.500=6.250+6.250*  

    Se utiliza el importe regresivo, ya que es el importe mayor.  

* Año 5 (2025):  

    *Importe regresivo: 25% de 23,730.46 = 4,943.85=2,471.92+2,471.92*  

    *Importe lineal = 23.730,46/3 = 7.910,15=3.995,07+3.995,08*  

    Se utiliza el importe lineal, ya que es el importe mayor.  

## <a name="user-defined-depreciation"></a>Amortización definida por el usuario

La aplicación dispone de una utilidad que permite configurar los métodos de amortización definidos por el usuario.  

Con un método definido por el usuario, se utiliza la página **Tablas amortización**, donde debe introducir un porcentaje de amortización para cada periodo (mes, trimestre, año o periodo contable). Luego, cuando asigna un libro de amortización con un método definido por el usuario para un activo fijo, debe establecer los campos **Fecha de primera amortización definida por el usuario** y **Fecha inicio amortización** en la página **Libros amortización activos** para el activo fijo específico.  

La fórmula para calcular los importes de amortización es:  

*Importe amortización = (% Amortización x Nº días amortización x Base amortizable) / (100 x 360)*  

### <a name="depreciation-based-on-number-of-units"></a>Amortización según el número de unidades

Este método definido por el usuario también se puede utilizar para amortizar según el número de unidades, por ejemplo, en el caso de máquinas de producción con una capacidad de vida establecida. En la página **Tablas amortización**, puede introducir el número de unidades que pueden producirse en cada periodo (mes, trimestre, año o periodo contable).  

### <a name="to-set-up-user-defined-depreciation-methods"></a>Para configurar métodos de amortización definidos por usuario

En la página **Tabla amortización**, puede configurar métodos de amortización definidos por el usuario. Por ejemplo, puede configurar la amortización según el número de unidades.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Tablas de amortización** y luego elija el enlace relacionado.  
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

Si utiliza un método definido por el usuario, los campos **Primera fecha de amortización definida por el usuario** y **Fecha de inicio de amortización** deben rellenarse en la página **Libros amortización activos** para el activo fijo especificado. El campo **1ª fecha amort. def.-usuario** y el contenido del campo **Longitud periodo** en la página **Tablas amortización** se utilizan para determinar los intervalos de tiempo a utilizar en los cálculos de amortización. Así se garantiza que la aplicación comenzará a utilizar el porcentaje especificado para todos los activos en el mismo día. El campo **Fecha inicio amortización** se utiliza para calcular el número de días de amortización.  

En el ejemplo anterior, ambos campos **Primera fecha de amortización definida por el usuario** y **Fecha de inicio de la depreciación** se establecerían en 01/01/20 en la página **Libros amortización activos** para el activo fijo específico. Si, no obstante, el campo **1ª fecha amort. def.-usuario** tuviera 01/01/20 y el campo **Fecha inicio amortización** tuviera 01/04/20, el resultado podría ser:  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coste |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 31/12/20 |Amortización |270 |-18.750,00 |81,250.00 |
| 31/12/21 |Amortización |360 |-38.000,00 |42,250.00 |
| 31/12/22 |Amortización |360 |-37.000,00 |6,250.00 |
| 31/12/23 |Amortización |90 |-6.250,00 |0 |
| 31/12/24 |Amortización |Ninguno |Ninguno |0 |

## <a name="half-year-convention-depreciation"></a>Amortización de convenio de medio año

El método Convenio medio año solo se aplicará si activó el campo **Usar convenio medio año** en la página fija **A/F Libro amortización**.  

Este método de amortización puede utilizarse junto con los siguientes métodos de amortización en la aplicación:  

* Lineal  
* Regresivo 1  
* Rs1/L  

Al aplicar el Convenio medio año, un activo fijo tiene seis meses de amortización en el primer año fiscal, independientemente del contenido del campo **Fecha primera amortización**.  

> [!NOTE]  
> La vida estimada del activo que resta después del año fiscal siempre será de medio año con el método Convenio medio año. De esta manera, para poder aplicar correctamente el método Convenio medio año, el campo **Fecha final amortización** de la página **Libro de amortización activos** siempre debe contener una fecha exactamente seis meses antes de la fecha final del año fiscal en el que se amortizó totalmente el activo fijo.  

### <a name="example---half-year-convention-depreciation"></a>Ejemplo - Amortización de convenio de medio año

Un activo tiene un coste de 100.000 DL. La **Fecha inicio amortización** es 01/03/20. La vida estimada es de cinco años, por lo que la **Fecha final amortización** debe ser el 30/06/25. El proceso **Calcular amortización** se realiza cada año. Este ejemplo sigue el calendario fiscal anual.  

Los movimientos contables de activos fijos son los siguientes:  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/03/20 |Coste |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 31/12/20 |Amortización |270 |-10.000,00 |90,000.00 |
| 31/12/21 |Amortización |360 |-20.000,00 |70,000.00 |
| 31/12/22 |Amortización |360 |-20.000,00 |50,000.00 |
| 31/12/23 |Amortización |360 |-20.000,00 |30,000.00 |
| 31/12/24 |Amortización |360 |-20.000,00 |10,000.00 |
| 31/12/25 |Amortización |180 |-10.000,00 |0.00 |

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Ejemplo - Amortización Rs1/L utilizando el convenio de medio año

Un activo fijo tiene un coste de 100 000 DL. La **Fecha inicio amortización** es 01/11/20. La vida estimada es de cinco años, por lo que la **Fecha final amortización** debe ser el 30/06/25. En la página **A/F Libros amortización**, el campo **% Regresivo** contiene 40. El proceso **Calcular amortización** se realiza cada año. Este ejemplo sigue el calendario fiscal anual.  

Los movimientos contables de activos fijos son los siguientes:  

| Fecha | A/F Tipo registro | Días | Importe | Valor contable |
| --- | --- | --- | --- | --- |
| 01/11/20 |Coste |(Fecha inicio amortización) |100,000.00 |100,000.00 |
| 31/12/20 |Amortización |60 |-20.000,00 |80,000.00 |
| 31/12/21 |Amortización |360 |-32.000,00 |48,000.00 |
| 31/12/22 |Amortización |360 |-19.200,00 |28,800.00 |
| 31/12/23 |Amortización |360 |-11.520,00 |17,280.00 |
| 31/12/24 |Amortización |360 |-11.520,00 |5.760,00 L |
| 31/12/25 |Amortización |180 |-5.760,00 |0,00 L |

`SL` después del valor neto significa que se utilizó el método lineal.  

Método de cálculo:  

* Año 1:  

    *Importe del saldo de pérdida de valor = Importe de todo el año = 40 % de 100 000 = 40 000.* Por lo tanto, por medio año, 40 000/2 = 20 000  

    *Importe lineal = Importe de todo el año = 100 000/5 = 20 000.* Por lo tanto, por medio año, = 20 000/2 = 10 000  

    Se utiliza el importe del saldo de pérdida de valor, ya que es el importe mayor.  

* Año 5 (2024):  

    *Importe regresivo: 40% de 17.280,00 = 6.912,00*  

    *Importe lineal = 28.800 / 1,5 = 11.520,00*  

    Se utiliza el importe lineal, ya que es el importe mayor.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Duplicación de movimientos en más libros de amortización

Si tiene tres libros de amortización, B1, B2 y B3, y desea duplicar los movimientos del B1 al B2 y B3, puede activar el campo **Compone lista duplicados** en las fichas del libro de amortización para B2 y B3. Esto puede resultar de utilidad si el libro de amortización B1 está integrado en la contabilidad y utiliza el diario general de activos fijos, y los libros de amortización B2 y B3 no están integrados con la contabilidad y utiliza el diario de activos.  

Cuando introduzca un movimiento en B1 del diario general de activos fijos y active el campo **Utiliza lista duplicados**, la aplicación duplicará el movimiento en los libros B2 y B3 del diario de activos en el momento de registrar el movimiento.  

> [!NOTE]  
> No puede duplicar en el mismo diario y proceso de diario desde el que está duplicando. Si registra movimientos en el diario general de activos fijos, podrá duplicarlos en el diario de activos o en el diario general de activos fijos mediante otro proceso.  

> [!NOTE]  
> No puede utilizar la misma serie de numeración en los diarios generales de activos fijos y en los diarios de activos fijos. Al registrar movimientos en los diarios generales de activos fijos, debe dejar en blanco el campo **Nº documento**. Si introduce un número en el campo, el número se duplica en el diario de activos fijos. También tendrá que modificar manualmente el número de documento para poder registrar el diario.  

## <a name="see-also"></a>Consulte también

[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]