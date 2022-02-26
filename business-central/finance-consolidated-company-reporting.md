---
title: Consolidar los datos de varias empresas
description: Este tema explica cómo puede consolidar los movimientos de contabilidad de dos o más empresas independientes (subsidiarias) en una sola empresa consolidada.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 1fd6dbc45dfbbdaa571161a8930d6b23471cac23
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2022
ms.locfileid: "7970705"
---
# <a name="consolidating-financial-data-from-multiple-companies"></a>Consolidar los datos financieros de varias empresas

Algunas organizaciones utilizan [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples empresas o entidades legales. Otros usan [!INCLUDE [prod_short](includes/prod_short.md)] en subsidiarias que deben reportar a organizaciones matrices. En ambos casos, los contables utilizan herramientas integradas para ayudar a consolidar los datos financieros.  

Puede consolidar los movimientos de contabilidad de dos o más empresas independientes (subsidiarias) en una sola empresa consolidada. Cada empresa individual implicada en una consolidación se denomina empresa. La empresa combinada se denomina empresa consolidada.  

Puede importar datos en la empresa consolidada desde otras empresas del mismo suscriptor de [!INCLUDE [prod_short](includes/prod_short.md)], desde suscriptores o desde archivos.  

Si los resultados financieros de una empresa se encuentran en una divisa diferente de los de la empresa consolidada, debe configurar tipos de cambio para la consolidación.  

Puede realizar consolidaciones:  

* A través de las empresas que tienen varios planes de cuentas.  
* Empresas que utilizan distintos ejercicios fiscales y diferentes divisas.  
* Tanto por el importe total como por un porcentaje de la información financiera de una empresa
* Utilizando distintos tipos de cambio de divisa en distintas libros mayores de contabilidad
* Empresas en otros programas de contabilidad y gestión empresarial

Configure la empresa consolidada de la misma forma que se configuran las demás empresas. El plan de cuentas es independiente del plan de cuentas de las otras empresas, y los planes de cuentas de cada una de las empresas individuales pueden diferir entre sí. Configure una lista de empresas a consolidar, compruebe los datos contables antes de consolidar, importe desde archivos o bases de datos y genere informes de consolidación. Para obtener más información, consulte [Establecer la consolidación de empresas](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> La consolidación de los datos financieros puede ser especialmente relevante en relación con los procesos entre compañías. Para obtener más información, vea [Gestión de transacciones entre empresas vinculadas](intercompany-manage.md).

## <a name="trial-balance"></a>Balance de comprobación

Si tiene más de una empresa en [!INCLUDE[prod_short](includes/prod_short.md)], el informe **Balance de comprobación consolidado** puede darle un resumen del estado financiero del todo su negocio.  

El informe combina movimientos del libro mayor de sus empresas en una empresa nueva creada por usted para contener los datos consolidados. Esta empresa valor se denomina generalmente "empresa consolidada". La empresa consolidada es sólo un contenedor para los datos consolidados, y no tiene ningún dato vivo de sus empresas. Las empresas que incluya en la empresa que se convierten en **Unidades de negocio** en el informe. Para obtener más información, consulte [Establecer la consolidación de empresas](finance-consolidated-company-reporting-setup.md).  

## <a name="consolidate-data"></a>Consolidar datos

El proceso de transferir las cifras de las unidades de negocio a la empresa consolidada es la *consolidación* real. Antes de hacer esto, es conveniente comprobar si existen diferencias entre la información básica de las empresas y de la empresa consolidada. Existen dos informes que puede utilizar para probar la base de datos y el archivo.

### <a name="to-test-the-data-before-you-consolidate"></a>Para probar los datos antes de la consolidación:

Puede probar los datos antes de transferirlos a la empresa consolidada. [!INCLUDE[prod_short](includes/prod_short.md)] busca las diferencias entre la información encontrada de las unidades de negocio y la empresa consolidada. Por ejemplo, si los números de cuenta o códigos de dimensión son diferentes. Deberá corregir los errores antes de ejecutar el informe. Puede probar la base de datos o, si va a importar datos desde un archivo XML, puede probar el archivo.  

1. Abra la empresa consolidada.  
2. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de negocio** y luego elija el enlace relacionado.  
3. Realice una de las siguientes acciones:  

    * Para probar un archivo, elija la acción **Probar archivo**, escriba el nombre del archivo y después seleccione **Imprimir**.  
    * Para probar la base de datos, elija **Probar base de datos**.  

### <a name="run-the-consolidation"></a>Ejecutar la consolidación

Después de haber probado los datos, puede transferirlos a la empresa consolidada.  

1. Inicie sesión en la empresa consolidada.  
2. En el **Centro de rol contador**, seleccione la acción **Ejecutar consolidación**.  
3. Rellene los campos requeridos.  
4. En la sección Filtro, establezca un filtro para la empresa o el nombre de la empresa relevantes.  
5. Opcionalmente, programe el informe para ejecutarlo en un momento conveniente.  

## <a name="eliminate-repeated-transactions"></a>Eliminar transacciones repetidas

Una vez que haya consolidado todas las empresas, debe encontrar transacciones que se registren más de una vez en todas las empresas y luego publicar los movimientos de eliminación para eliminarlas.

El procesamiento de las eliminaciones de consolidación es un procedimiento manual.  

Para eliminar transacciones repetidas:

1. Busque transacciones que posiblemente deban ajustarse e introduzca líneas del diario general para eliminarlas.
2. Ejecute el informe **Eliminaciones consolidación** para que le ayude a valorar el efecto de las líneas del diario antes del registro.
3. Registrar transacciones de ajuste.

En el informe **Eliminaciones consolidación** se muestra un balance de comprobación provisional en el que puede simular las consecuencias de eliminar los movimientos, comparando los movimientos de la empresa consolidada con las eliminaciones que se han escrito en el diario general.

Para poder incluir una empresa en el informe, debe estar definida en la página **Unidades de negocio** y el campo **Consolidar** debe estar seleccionado.

Cada cuenta aparece en una línea aparte, según la estructura del plan de cuentas. Una cuenta no aparecerá si todos los importes de la línea son 0. Para cada cuenta, se muestra la siguiente información:

* Número cuenta
* Nombre de cuenta.
* Si ha seleccionado uno o más códigos de empresa en el campo **Cód. unidad de negocio** de la página de solicitud, aparecerá un total de la empresa consolidada, excluyendo las empresas seleccionadas y las eliminaciones. Si no ha rellenado el campo **Cód. empresa**, aparecerá un total de la empresa consolidada, excluyendo las eliminaciones.
* Si ha seleccionado un código de empresa en el campo **Cód. empresa** de la página de solicitud, aparecerá un total de los movimientos importados desde la empresa. Si no ha rellenado el campo **Cód. empresa**, aparecerá un total de las eliminaciones registradas en la empresa consolidada.
* El total de la empresa consolidada, con todas las empresas y las eliminaciones registradas.
* Las eliminaciones a realizar en la empresa consolidada, es decir, los movimientos del diario general seleccionado en la página de solicitud.
* El texto de registro, copiado del diario general.
* El total de la empresa consolidada, después de las eliminaciones, si se registran.

## <a name="export-and-import-consolidated-data-between-databases"></a>Exportar e importar datos consolidados entre bases de datos

Si los datos de una unidad de negocio se encuentran en otra base de datos, deberá exportar los datos a un archivo antes de incluirlos en la consolidación. Cada empresa debe exportarse por separado. Para ello, usa el proceso **Exportar consolidación**.  

> [!TIP]
> Utilice el mismo proceso para exportar datos consolidados que deben enviarse a Dynamics 365 Finance, como si la empresa actual fuera una subsidiaria y la empresa matriz utilizara Dynamics 365 Finance.

Después de ejecutar el trabajo por lotes, se procesarán todos los movimientos de todas las cuentas. Para cada combinación de dimensiones seleccionadas y fecha, se obtiene el total de los campos **Importe** de los movimientos, y se exporta. Se procesa la siguiente combinación de dimensiones seleccionadas y fecha con el mismo número de cuenta, y después se procesan las combinaciones del siguiente número de cuenta, y así sucesivamente.  

Los movimientos exportados tienen los siguientes campos: **Nº cuenta**, **Fecha registro** e **Importe**. Si también se ha exportado la información sobre dimensiones, se incluirán los códigos y los valores de dimensión.  

1. Para cada línea exportada, si el total de los campos **Importe** corresponde al debe, el número de cuenta que está configurada en el campo **Cta. consol. debe** de la unidad de negocio se exporta a la línea. Si el total corresponde al haber, el número correspondiente en el campo **Cta. consol. haber** se exporta a la línea.  
2. La fecha que se usa en cada línea exportada es la fecha final del periodo o, si la transferencia se realiza cada día, la fecha exacta del cálculo.  
3. El valor de dimensión exportado para el movimiento será el valor de dimensión de la empresa consolidada del campo **Cód. consolidación** del valor de dimensión. Si no se ha introducido un valor de dimensión de empresa consolidada en el campo **Cód. consolidación** del valor de dimensión, se exportará a la línea el valor de dimensión en sí.  
4. Además, los archivos XML contienen los tipos de cambio de divisa del periodo consolidado. Estos tipos se incluyen en una sección aparte al principio del archivo.  

## <a name="see-also"></a>Consulte también

[Configuración de la consolidación de empresas](finance-consolidated-company-reporting-setup.md)  
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportar los datos de negocio a Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]